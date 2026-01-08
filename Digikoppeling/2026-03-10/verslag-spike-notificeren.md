# Verslag spike notificeren

Auteurs: Tim van der Lippe (Logius) & Stas Mironov (Logius)
Datum: 2026-01-06
Status: werkversie
Opdrachtgever: FDS

## Omschrijving

Onderzoek de functionele & technische eisen en implicaties om een toekomstbestendige notificatiefunctie in Digikoppeling te realiseren op basis van CloudEvents (NL GOV-profiel) als moderne vervanger van ebMS.
Breng tegelijk in kaart welke impact de standaardisatie van notificaties—CloudEvents plus een abonnementsstandaard—heeft op het huidige digitale landschap en op de inrichting van een interoperabele notificatievoorziening binnen het Federatief Datastelsel (FDS), en bepaal haalbare implementatieopties.

Hiervoor hebben we de volgende primaire doelstellingen uitgewerkt:

- Breng de functionele en non-functionele eisen in kaart voor een notificatiefunctie in DigiKoppeling op basis van het CloudEvents-profiel.
- Geef aan hoe CloudEvents icm Digikoppeling REST-API als moderne vervanger van ebMS optreden.
- Onderzoek daarbij hoe Notificaties volgens zowel PUSH als PULL mechanismen kunnen worden verwerkt;

En de volgende secundaire doelstellingen komen deels aan bod:

- Analyseer de implementatie­mogelijkheden en implicaties voor DigiKoppeling — denk aan interoperabiliteit, naleving van standaarden en implementatieopties
- Analyseren van de impact die de standaardisatie van CloudEvents en abonnements­standaarden heeft op het huidige digitale landschap.
- Adviseren over de meest kansrijke oplossingsrichtingen, zodat vervolgbeslissingen goed onderbouwd zijn onder vast te lopen op een vooringenomen oplossing.

## Aanpak

Om deze doelstellingen te behalen hebben we de volgende aanpak gebruikt:

- Inventariseren huidige gebruikers van ebMS oplossingen
- Inhoudelijke interviews van huidige gebruikers voor inventariseren van (non-)functionele eisen
- Deelname aan inhoudelijke besprekingen binnen [Kennisplatform API's](https://developer.overheid.nl/communities/kennisplatform-apis/) over notificeren op basis van API's.

## Achtergrond

Op dit moment bevat [Digikoppeling](https://www.logius.nl/onze-dienstverlening/gegevensuitwisseling/digikoppeling) meerdere koppelvlakken: [ebMS](https://gitdocumentatie.logius.nl/publicatie/dk/ebms/), [REST API](https://gitdocumentatie.logius.nl/publicatie/dk/restapi/) en [WUS](https://gitdocumentatie.logius.nl/publicatie/dk/wus/).
Binnen het [Federatief Datastelsel](https://realisatieibds.nl/groups/view/0056c9ef-5c2e-44f9-a998-e735f1e9ccaa/federatief-datastelsel/wiki/view/89eea995-7c1c-412e-93c1-0319d9ee5baa/afsprakenstelsel-fds) (FDS) wordt er voornamelijk gewerkt met REST API's en komen de andere koppelvlakken op dit moment niet voor.
Binnen het FDS zijn er verschillende [standaarden als leidend geselecteerd](https://federatief.datastelsel.nl/kennisbank/standaarden/):

- [REST API Design Rules](https://gitdocumentatie.logius.nl/publicatie/api/adr/) (ADR) verplicht voor alle REST API's en vastgesteld binnen het FDS als de gekozen transportwijze van gegevensuitwisseling
- [NL Gov CloudEvents](https://gitdocumentatie.logius.nl/publicatie/notificatieservices/cloudevents-nl/) als inhoudelijk formaat voor het uitwisselen van notificaties (berichten tussen applicaties over plaatsgevonden gebeurtenissen)

Deze standaarden worden toegepast in een nationale context, waarbij het NL Gov profiel op CloudEvents is gebaseerd op de [internationale CloudEvents standaard](https://github.com/cloudevents/spec/blob/v1.0.2/cloudevents/spec.md) ontwikkeld door de [Cloud Native Computing Foundation](https://www.cncf.io/).

### Functies van standaarden

De standaarden binnen het FDS zijn complementair en leveren elk hun eigen puzzelstukje voor de gehele opgave die het FDS beoogt op te lossen.
Hierbij definiëren CloudEvents de inhoud van berichten en REST API's de transportwijze hoe berichten worden afgeleverd.
Beide aspecten zijn nodig om tot een solide notificatiefunctie te komen.

Als we dit leggen naast ebMS, dan is ebMS een standaard die de transportwijze standaardiseert.
Dit betekent dat REST API's en ebMS hetzelfde puzzelstukje kunnen oplossen.
**CloudEvents is dus geen puzzelstukje dat ebMS vervangt**, omdat de eerste over berichtinhoud gaat en de tweede over het transport.
Het is ook mogelijk om notificaties in het CloudEvents formaat te versturen via ebMS.

Om de doelstellingen uit te werken moeten we daarom altijd CloudEvents in combinatie met REST API's analyseren.
De vergelijkingen zullen dus meer focussen op de verschillen en overeenkomsten van REST API's en ebMS, omdat beiden over transport gaan.

## Functionele eisen van transport

Deze sectie bevat de functionele eisen die overheidsorganisaties stellen aan notificatiefuncties, op basis van huidig gebruik van ebMS2.
Hierbij focussen we op eisen die de standaard op technisch niveau uitwerkt.

### Afleverzekerheid

De huidige ebMS toepassingen worden gebruikt om serviceberichtpatronen toe te passen.
Hierbij wordt er een bericht over het transport verstuurd en wordt er een ontvangstbericht teruggestuurd.
Sommige organisaties spreken af dat dit ontvangstbericht nogmaals rondgaat, zodat de verzender ook dit ontvangstbericht kan accorderen.
Hierbij word voor elk servicebericht dus 4 berichten over het transport verstuurd: het initiele bericht van de verzender, het initiele ontvangsbericht van de ontvanger, een accordeerbericht van de verzender en een finaal ontvangstbericht over het accordeerbericht van de ontvanger.

Deze vorm van verzenden en accorderen is niet feilloos ([Two General's Problem](https://en.wikipedia.org/wiki/Two_Generals%27_Problem)), maar geeft in de praktijk voldoende waarborging dat het bericht is aangekomen.
Het gevolg is dat er, op basis van de configuratie van hoe vaak ontvangstberichten heen en weer worden gestuurd, een grote mate van zekerheid is dat het bericht is aangekomen.
Berichtenstromen die als cruciaal worden gezien (dus dat er geen enkel bericht mag ontbreken bijvoorbeeld vanwege wetgeving over het informeren naar de burger) vereisen een hoge mate van afleverzekerheid.
Andere berichtenstromen waar dit minder van belang is (bijvoorbeeld bij monitoring, waar het over trends gaat in plaats van de performance op een specifiek tijdstip) hoeven minder ontvangstberichten te versturen.

### Onweerlegbaarheid

In het verlengde van afleverzekerheid volgt ook onweerlegbaarheid: "de waarborg dat ontvangst en/of verzending van een contract of een bericht niet kan worden ontkend door de beide betrokken partijen" ([Wikipedia](https://nl.wikipedia.org/wiki/Onweerlegbaarheid)).
Uit onze interviews kwam naar voren dat deze eis vooral van belang is in de justitionele keten en bij de Belastingdienst, waar de verantwoordelijkheid voor een rechtspersoon voortvloeit uit het sturen van een servicebericht tussen organisaties.
Als organisatie A verantwoordelijk is voor een rechtspersoon en een bericht stuurt naar organisatie B om aan te geven dat zij nu verantwoordelijk is, dan kan organisatie B hier een ondertekend ontvangstbericht over sturen.
Omdat dit ontvangstbericht ondertekend is, maakt het dat onweerlegbaar is dat organisatie B deze verantwoordelijkheid accepteert.
Als er in de toekomst onduidelijkheid is, dan kan organisatie A terugvallen op het ontvangstbericht om aan te tonen dat organisatie B deze heeft geaccepteerd.

Het is dus nodig om het ontvangstbericht te ontvangen, omdat daaruit de onweerlegbaarheid voortvloeit.
Dit kan extra afspraken vereisen over bijvoorbeeld op welk tijdstip dit plaatsvond.
Het vereist dus ook dat de ontvangstberichten worden opgeslagen voor een van tevoren afgesproken termijn.
Deze afspraken worden vastgelegd bij het opzetten van de berichtenstroom in een contract (CPA) waarin ook de publieke certificaten van beide organisaties zijn opgenomen.

### Foutafhandeling (retries)

De bovenstaande eisen gaan over de gevallen waarin de berichten succesvol zijn aangekomen.
Echter is er ook een reële kans dat de berichten niet aankomen.
Hierover worden afspraken gemaakt op welke termijn en hoe vaak er nieuwe pogingen worden ondernomen.
Bijvoorbeeld: "elke 24 uur is er een nieuwe poging, met een maximum van 5 pogingen".
Het opnieuw proberen van afleveren heet "retrying" en wordt dus in eenzelfde contract vastgelegd als bovengenoemde afspraken.

Uit onze interviews blijkt dat organisaties hier in hun operationele onderhoud ook actief gebruik van maken.
Berichtenstromen kunnen er tijdelijk uitliggen vanwege onderhoud of als er een grote hoeveelheid berichten in korte tijd binnenstromen.
In het eerste geval hebben organisaties de vrijheid om onderhoud te plegen in periodes die korter zijn dan de afgesproken termijnen.
In het bovenstaande voorbeeld zal er op 5 aaneengesloten dagen een poging worden ondernomen, waardoor het mogelijk is om in het weekend onderhoud te plegen, zonder dat er berichten verloren gaan.
In het tweede geval zetten organisaties dit in om "throttling" toe te passen, waarbij systemen artificieel worden gelimiteerd op de hoeveelheid berichten die worden geaccepteerd.
Dit kan worden gebruikt om onderliggende systemen te ontzorgen, als die de ontvangen berichten niet met hetzelfde tempo kunnen verwerken.

## Non-functionele eisen

Deze sectie bevat de non-functionele eisen die overheidsorganisaties stellen aan notificatiefuncties, op basis van de huidige implementatie binnen overheidsorganisaties.
Deze eisen zijn transport-onafhankelijk, echter zijn deze vaak gevolg van de technische limitaties van de gekozen transportwijze.

### Interne werkwijze afstemmen op technische oplossing

De huidige berichtenstromen zijn gekenmerkt door cycli van ontvangen en later verwerken van berichten.
Hier geven geïnterviewden aan dat berichten worden samengevoegd voor betere performance.
Dit houdt in dat in plaats van 1000 losse berichten de lijn over gaan, in plaats daarvan er 1 groot bestand met als inhoud 1000 berichten wordt verstuurd.
Dit levert betere performance op, omdat de overhead voor berichten verminderd wordt.
Het is ook beter te managen, omdat er bij fouten maar enkele grote batches betrokken zijn in plaats van een grote berg kleine berichten.

Deze werkwijze heeft tot gevolg dat er grote hoeveelheden berichten in 1 keer aankomen en dus verwerkt moeten worden.
Het kost tijd om dit te verwerken, waardoor er pieken van belasting op systemen komen.
Organisaties "smeren" daarom de berichten op achterliggende systemen uit over een langere periode, om zo de werklast voor de achterliggende systemen te beheersen.
Systemen zijn op deze werkwijze ingericht en in de interviews komt naar voren dat de interne organisatiearchitectuur hier ook een reflectie op is.
Als de technische werkwijze van berichtenverkeer wordt aangepast, dan heeft dat impact op de organisatiearchitectuur.

Om tot een houdbare manier van werken te komen moeten organisaties dus afspraken maken en een organisatiestructuur opzetten die past bij de manier van transporteren.
Als er gekozen wordt voor kleinere hoeveelheden berichten, dan zal dat er anders uit zien dan als er grotere hoeveelheden gebundeld worden.

### Koppelafspraken tussen organisaties

Naast de berichtenstroom moeten er koppelafspraken worden gemaakt tussen organisaties.
Bij ebMS2 wordt er gebruik gemaakt van CPA's, waarin afspraken over de functionele eisen staan alsmede identificatie van de betreffende verzendende en ontvangende organisaties.
Deze afspraken worden centraal beheerd in het CPA-register.
Deze formele vastlegging van afspraken geeft organisaties houvast en controle over de uitgaande en binnenkomende berichtenstromen.
Omdat de configuratie vastgelegd is in een gestandaardiseerd formaat kan deze worden ingeladen in een ebMS2 adapter.
Dit zorgt er voor dat beide organisaties dezelfde configuratie gebruiken, wat foutgevoeligheid bij manueel handelen vermijd.

Voor REST API's zijn er contracten beschikbaar voor het opzetten van connecties met FSC.
Deze contracten bevatten deels de informatie die CPA's ook bevatten, maar er zal extra informatie moeten worden vastgelegd om een volwaardig alternatief te bieden.
Daarnaast moeten API gateways en marktoplossingen deze contracten kunnen inlezen, om ook het automatisch configureren mogelijk te maken.

### Vertrouwen

Enkele belangrijke berichtenstromen maken op dit moment gebruik van ebMS2.
Hier is jarenlange ervaring mee opgedaan en heeft zich op cruciale piekmomenten bewezen.
Het opbouwen van vertrouwen in deze werkwijze zorgt ervoor dat organisaties zich comfortabel voelen bij het operationeel beheer van deze berichtenstromen.
Dit vertrouwen vloeit voort uit monitoring van performance, de manier van communicatie tussen verzender en ontvanger, en de leeftijd van de technologie.
Een alternatieve oplossing zal dus op deze vlakken een adequate en bewezen oplossing moeten bieden om tot eenzelfde niveau van vertrouwen te komen.

Bij elke migratie zal er tijd overheen gaan om dit vertrouwen op te bouwen.
Daarom is het cruciaal dat er op kleine schaal ervaring wordt op gedaan.
Dit is in het geval van de huidige ebMS2 toepassingen lastiger, omdat de huidige berichtenstromen groot zijn en daarom niet geschikt voor dit soort experimenten.

### Internationaal gebruik

Oplossingen die op internationaal niveau worden gebruikt hebben de voorkeur boven oplossingen die enkel nationaal worden toegepast.
Dit vereist wel dat er een internationale oplossing aanwezig moeten zijn.
In het geval van berichtenstromen is op Europees niveau gekozen voor [eDelivery met ebMS3 plus AS4](https://ec.europa.eu/digital-building-blocks/sites/spaces/DIGITAL/pages/467110114/eDelivery).
Geïnterviewden geven aan dat ze met deze nieuwe versie ervaring hebben op basis van andere trajecten en dat ze het als een adequate oplossing zien.
Om de verscheidenheid van oplossingen te verkleinen gebruiken organisaties het liefst een eenduidige aanpak.
RINIS beheert het landelijk knooppunt voor [OOTS](https://sdg.pleio.nl/) voor het uitwisselen van digitale bewijsstukken over landsgrenzen heen, gebaseerd op ebMS3.
Belastingdienst geeft tevens aan dat ze voor Europese samenwerkingen financiële data delen met financiële diensten van andere landen op basis van ebMS3.

Hierbij geeft de Belastingdienst aan dat ze het principe **Reuse > Buy > Build** toepassen.
De voorkeur gaat uit naar het hergebruiken van bestaande koppelingen, wat in context van de internationale gemeenschap ebMS3 is.
Een alternatieve oplossing zal aansluiting moeten maken met Europa om ook daar integraties te bewerkstelligen.
In het kader van API's houdt dat bijvoorbeeld in dat er hernieuwde energie zou moeten worden gestoken in het [eDelivery REST API profiel](https://ec.europa.eu/digital-building-blocks/sites/spaces/EDELCOMMUNITY/pages/254313406/Project+API4IPS+in+ISA%C2%B2+action+Innovative+Public+Services).

## Implementatie met REST API's voor notificeren

Om aan deze eisen te voldoen zijn additionele afspraken  nodig over de transportwijze, waarbij de focus minder ligt op de berichtinhoud (lees: CloudEvents).
Dit vereist afspraken bovenop de huidige afspraken voor REST API's binnen het FDS.
Op dit moment zijn er nog geen vastgestelde standaardoplossingen binnen zowel de ADR (nationaal niveau) als REST API's in het algemeen (internationaal) die voldoen aan deze eisen.
Op internationaal niveau wordt er wel gewerkt aan standaardisatie op asynchrone API interactiepatronen met AsyncAPI, maar dit standaardiseert enkel de manier van beschrijven van API's en geeft geen invulling aan de functionele eisen zoals boven beschreven.

Binnen het Kennisplatform API's gaat de werkgroep Notificeren aan de slag om een oplossing te vinden die voldoen aan deze eisen.
De aanpak is tweeledig: enerzijds een architectuur voor notificeren beschrijven ([beschikbaar op NORA](https://www.noraonline.nl/wiki/Architectuur_Notificeren_in_het_Federatief_Datastelsel)) en anderzijds de technologie in de praktijk beproeven.

In de praktijkbeproeving wordt ook meegenomen wat de consequenties van PUSH en PULL mechanismen zijn.
Sommige overheidsorganisaties hebben hier al ervaring mee, zoals RvIG met de [BRP API gebeurtenissen](https://github.com/BRP-API/brp-api-gebeurtenissen) (in ontwikkeling).
Deze API maakt gebruik van een PULL mechanisme waar op bepaalde intervallen events kunnen worden opgehaald op een locatie.
Hierbij worden de events (in CloudEvents formaat) dus niet gelijk verstuurd naar de afnemer, maar moet de afnemer zelf bepalen wanneer die checkt of er nieuwe events zijn.
De data gerelateerd aan waar het event over gaat wordt niet meegenomen in het event (dus informatie-arm) en vereist een bevraging aan de BRP API.

Dit staat in contrast met een PUSH mechanisme waar er direct een bericht aankomt bij de afnemer.
In een PUSH mechanisme kan zowel informatie-arm als -rijk worden genotificeerd.
Het verschil tussen PUSH en PULL is dus wie actie moet ondernemen om de notificatie te ontvangen.
Bij PUSH ligt de actie bij de aanbieder, bij PULL bij de afnemer.

