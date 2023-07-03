# Technisch Overleg Digikoppeling

22 juni 2023

## Aanwezigen

| Naam | Organisatie |
| --- | --- |
| Bijen, Antoon | Justid |
| Coemans, Maarten | SNG |
| De Boer, Karl | Enable-U |
| Fieten, Sander | Casquis |
| Green, Alexander | Logius |
| Haasnoot, Peter | Logius |
| IJzermans, Jochem | UWV |
| Koster, Ronald | VNG |
| Nicolaij, Heymen | PinkRoccade |
| Pauw, Elzo | UWV |
| Reinhoud, Erwin | Kennisnet |
| Sinnige, Hans | RINIS |
| Van der Plas, Martin | Logius |
| Van Gelderen, Edward | VNG |
| Van Kester, Jos | VNG |
| Welmer, Han | TNO |
| Wisse, Edwin | Logius |

## Verslag vorig TO

[Verslag TO Digikoppeling 2023-03-09](https://github.com/Logius-standaarden/Overleg/blob/main/Digikoppeling/2023-03-09/Verslag.md)

Geen opmerkingen

## Vernieuwing FSC / NLX

### Presentatie

**Peter Haasnoot:** Korte introductie op de FSC-standaard. Het is een vervolg op de eerdere NLX-software ontwikkelprojecten. We hebben al vaker contact gehad over de ontwikkelingen in NLX, echter was dit louter in de context van ontwikkeling van Open Source software en software modules. Wij hebben ook eerder gekeken naar de relatie tussen de Digikoppeling en NLX; Hier zagen wij dat NLX zaken invult die niet in Digikoppeling zitten en andersom; je zou kunnen zeggen dat zij elkaar aankunnen vullen. Wellicht interessant om een mogelijke aansluiting met elkaar te bekijken.

De presentatie van Edward van Gelderen is [hier](https://github.com/Logius-standaarden/Overleg/raw/main/Digikoppeling/2023-06-22/FSC-delegation-animatie.pptx) [.pptx, 109 KB] te vinden. Vragen of opmerkingen zijn welkom op het adres op de eerste slide.

### Vergelijking met bestaande implementatie

**Maarten Coemans:** Wij [SNG] implementeren dezelfde logica al in transacties. Wij hebben zelf ook gewoon een administratie die los contracten tussen bijvoorbeeld in Centric en een gemeente administreert. Maar Centric meldt zich bij ons aan met certificaat van Centric en niet met certificaat van een gemeente om dezelfde redenen als jullie, dus het idee begrijpen wij.

**Edward van Gelderen:** Dan zitten we op hetzelfde spoor en ben je het snel op veel punten met elkaar eens. Wij bekijken het vooral vanuit de gemeenten, maar ik denk dat die behoefte veel breder is. Men heeft vooral de behoefte om op dezelfde manier samen te werken, derhalve moet je het verheffen tot een standaard. In dit geval is die standaard er uiteraard al, namelijk het Digikoppeling Koppelvlakstandaard REST API. Alleen hebben wij het idee dat dat dat daar veel meer keuzes vastgelegd zouden kunnen worden, zodat we daadwerkelijk met zijn allen op dezelfde manier met die koppelingen omgaan en alleen dan kunnen we echt technisch interoperabel gaan worden. Iedere variant bedraagt een unieke situatie en je wilt dat eigenlijk proberen te vermijden.

### Client Credentials Flow

**Maarten Coemans:** Wat is de impact op een bestaande uitwisseling? Stel dat je dit er tussen wil zetten.

**Edward van Gelderen:** Voor een normale API call is het slechts een kwestie van dit ertussen zetten. Administratief dient wel een dergelijk contract aangemaakt te worden. Verder is het verloop hetzelfde, daar de gateway transparant is voor de client en de client dus niet weet of het direct naar de API gaat of door welke gateway en of er een token bij hoort. Dat verleg je allemaal naar die gateway en de FSC manager functionaliteit. Utrecht heeft bijvoorbeeld voor de interne organisatie NLX, oude stijl, geïmplementeerd. De ideeën zijn redelijk vergelijkbaar. De impact was niet heel groot, alhoewel dit moeilijk te kwantificeren is, maar wel positief doordat dun interne organisatie ineens heel makkelijk te managen is. Het is geen _rocket science_; het enige wat het is is keuzes maken. Als we dit nou met zijn allen doen zijn we een stuk verder, want dat doen we allemaal hetzelfde. Het is in principe gewoon een OAuth-flow en die hebben wij niet bedacht. Het is common sense, die is goed, dus die hebben we gebruikt.

**Antoon Bijen:** Dus gebaseerd op OAuth?

**Edward van Gelderen:** De Client Credentials Flow.

**Antoon Bijen:** Het is dus een standaard dat door de grote API gateways ondersteund wordt?

**Edward van Gelderen:** Dit is de grootste verandering ten opzichte van NLX, omdat het daar eigen software was. Bestaande gateways verstaan reeds OAuth, waardoor de drempel laag wordt en de impact op deze manier eigenlijk lager is dan hoe het in NLX was.

**Antoon Bijen:** Heeft een bestaande gateway een extra component nodig?

**Edward van Gelderen:** De FSC manager is nodig. Deze hebben wij als losse component beschikbaar, maar is ook vanuit de papieren standaard zelf te implementeren. De FSC manager bevat alle logica rondom contracten zodat de gateway dat niet hoeft te doen. Wij denken dat het logischer is dat je het buiten de gateway neerzet. Zolang het maar compliant is aan hetgeen wat we met elkaar afgesproken hebben.

### Complexiteit in communicatie i.p.v. implementatie

**Sander Fieten:** Zijn er twee communicatielijnen, eerst tussen de FSC managers en daarna tussen de gateways? Als iemand al gerechtigd is met het contract waarom kan je niet op basis van een recent bericht het pad tussen de gateways opstellen zonder eerst nog een token op te halen?

**Edward van Gelderen:** Dat is eigenlijk hoe NLX-oude-stijl werkte. Echter bleek uit diverse organisaties een behoefte te zijn de bekende Client Credentials Flow van OAuth te dupliceren.

**Ronald Koster:** Inderdaad wist de gateway reeds van de contracten af, dus er was helemaal geen token nodig. In de praktijk bleek echter dat bestaande gateways moeite hebben _out of the box_ de contractdata binnen te krijgen. Er is een juridisch component en veel gateways praten dat niet, dan zou je direct naar de database moeten gaan waar de contracten in staan. Daar hadden veel bestaande gateways moeite mee, maar gateways begrijpen wel JWT's. Daarom besloten wij het contractbeheer uit de gateways te laten zodat de gateways enkel het token controleren en niets van de koppeling met contracten hoeft te weten.

**Sander Fieten:** Nog steeds dient ergens de identiteit van iemand vastgesteld te worden, ook om dat token uit te geven waardoor je alsnog weer met die certificaten te maken hebt. Dit lijkt louter complexiteit toe te voegen. Mensen hadden veel problemen met certificaatmanagement, maar uiteindelijk verschuif je dat gewoon naar een stap eerder in het proces, dus ik vraag me af of dat probleem hiermee wel opgelost wordt.

**Edward van Gelderen:** Wij hebben gekozen om complexiteit van implementatie te verminderen door de drempel voor de gateway zo laag mogelijk te houden en hebben daarom die tokens geïmplementeerd.

**Karl de Boer:** Het doel van deze oplossing is dan ook niet het PKIoverheidcertificaatbeheer makkelijker te maken, maar om delegatie transparanter en veiliger te maken.

### Service discovery

**Jos van Kester:** Is er een centraal of decentraal service register nodig of lokaal. Indien het centraal is, wie beheert dat dan?

**Edward van Gelderen:** Met betrekking tot service tot service discovery heeft een groep samenwerkende organisaties een telefoonboek ("directory"). Daar melden die organisaties ("peers") zich bij aan. De directory zorgt ervoor dat het inzichtelijk is welk services er zijn en waar ze staan.

**Jos van Kester:** Wie beheert dat telefoonboek en hoe kunnen wijzigingen aangebracht worden?

**Edward van Gelderen:** Tot op heden beheerde VNG Realisatie dat. Tijdelijk is de hosting en exploitatie door RINIS opgepakt. De subsidie loopt tot 2024.

**Jos van Kester:** Ik zit in de inburgeringswet en vanuit die hoek hebben we uitgebreid gekeken naar NLX. FSC zal morgen nog geen standaard zijn die Logius ie uitgevaardigd en gepubliceerd, maar wij volgen het zeker met grote interesse.

**Edward van Gelderen:** Dit zijn de eerste stappen op landelijk niveau, maar op gemeentelijk niveau je soortgelijke discussie en wat lastig blijkt is dat veel logische use cases liever even wachten totdat het een standaard is. Het vervelende daarvan is dat het lang duurt voordat het een standaard is, omdat je namelijk die use cases moet hebben om te kunnen bewijzen. Vanuit gemeentelijk perspectief is het me nog niet gelukt dat te doorbreken.

Han Welmer wijst de Directory aan als een Single Point of Failure. Edward van Gelderen wil in gesprek gaan naar de behoeftes en oplossingen.

Voor verdere vragen of opmerkingen wordt verzocht buiten dit overleg contact op te nemen met Edward van Gelderen.

Peter Haasnoot meldt dat Edward van Gelderen dit onderwerp onlangs bij de Werkgroep Beveiliging van het Kennisplatform API's heeft aangedragen om informatie te verschaffen en feedback te vergaren. Edward van Gelderen deelt de URL naar de FSC-standaard: [commonground.gitlab.io/standards/fsc/](https://commonground.gitlab.io/standards/fsc/)

## Discussiestukken OIN

### Veld doel t.b.v. (wettelijke) taak

Peter Haasnoot presenteert het discussiestuk om de sub-OIN registratie uit te breiden met het veld "doel", zie [hier](https://github.com/Logius-standaarden/Overleg/blob/main/Digikoppeling/2023-06-22/OIN_Stelsel_veld_reden_doel.md).

Arnoud Quanjer heeft schriftelijk de volgende reactie gegeven.
<details>
<summary>e-mail</summary>

> Het op sub-OIN vastleggen van doelbinding lijkt de VNG niet de juiste oplossing voor het geschetste probleem. Conceptueel is het OIN vergelijkbaar met een BSN nummer dat je uit DigiD krijgt voor personen: het identificeert een organisatie uniek en levert de authenticatie er bij. Je weet dus zeker dat een identiteit klopt. Net zoals je niet een apart BSN nummer hebt voor elke overheidsdienst waar je als persoon contact mee hebt, is het ook niet wenselijk dat organisaties een apart OIN nummer hebben per wettelijke taak / grondslag. De identiteit zou iedere keer hetzelfde moeten zijn voor de gehele organisatie. Het is mogelijk om meerdere van elkaar te onderscheiden certificaten aan te vragen die allemaal hetzelfde OIN hebben. Dus je kan de ene applicatie / afdeling een ander certificaat en zelfs beheerproces geven dan een andere organisatie, en toch hetzelfde OIN gebruiken.
>
> Door de VNG wordt in samenwerking met Logius en het Kennisplatform API’s gewerkt aan de Federated Services Connectivity (FSC) standaard met als doel deze onderdeel te van het Digikoppeling REST profiel. In de FSC-standaard wordt onder meer de problematiek van het kunnen instellen van de  bevoegdheden tussen bronnen, afnemers en intermediars opgelost. De standaard stelt voor dat:
> 
> -	een Organisatie (Peer) wordt geïdentificeerd door OIN
> -	Een organisatie talloze verschillende certificaten kan hebben, allemaal met zelfde OIN, maar wel uniek identificeerbaar (met thumbprint)
> -	Contracten worden ingeregeld op het niveau van de thumbprint
>
> Het koppelen van grondslagen aan organisaties kan hiermee dus op het niveau van de thumbprint worden geregeld. In aanvulling op de FSC methode om contracten op certificaat vast te leggen ipv op OIN, zou het COR register de mogelijkheid moeten bieden om specifieke certificaten per OIN te registreren. Organisaties zouden dan de gelegenheid moeten hebben om aan ieder certificaat uitleg toe te voegen over het gebruik / het doel / contactinfo van het certificaat.
>
> Het lijkt ons verstandig om voordat over het voorliggende voorstel wordt besloten de ontwikkelingen rondom de FSC-standaard en het Digikoppeling REST-profiel mee te nemen in de discussie om te voorkomen dat we elkaar in de wielen rijden.
</details>

**Elzo Pauw:** Probeer je hiermee te voorkomen dat iemand een onzin sub-OIN gebruikt? Ik zie geen use case waarin het veld reden relevant is voor ons.

**Antoon Bijen:** Binnen justitie hebben we te maken met samenwerkingsverbanden waarbij meerdere partijen samenwerken voor een specifieke taak.

**Peter Haasnoot:** Het zou zich dus kunnen lenen zodat je ook een samenwerkingsverband kan identificeren en adresseren. Het veld reden toevoegen kan helpen bepaalde soorten misbruik te voorkomen, bijvoorbeeld het gebruik van onzin sub-OIN's- en sub-OIN's gebruiken voor een ander taak dan waar het eigenlijk voor was bedoeld.

**Antoon Bijen:** Zit dat niet in je aanvraagproces, want ik neem toch aan dat dat je niet zomaar sub-OIN krijgt?

**Elzo Pauw:** Het toevoegen van het veld reden klinkt als een redenering van meer is beter, maar waar houdt het op? Ik weet ook niet of dit uiteindelijk in het certificaat zelf zou komen of puur in het register.

**Peter Haasnoot:** Het idee was dat het in het register zou komen te staan als metadata.

**Antoon Bijen:** Ik zie wel degelijk toegevoegde waarde voor dat voor het veld, met name voor partijen die kijken welke organisaties horen bij een specifieke organisatie. Ik zie daarentegen maar weinig nadelen extra optioneel veld. Bij het aanvraagproces wordt het veld gecontroleerd door Logius, zodat er inderdaad niet zomaar van alles ingezet kan worden.

**Elzo Pauw:** Wij houden zelf de koppelingen bij, dus ik zie niet wat we met die extra informatie zouden doen. Wat voor type informatie is het en waar zouden we op zoeken in dat veld?

**Antoon Bijen:** Wellicht kan het de naam van de toepassing bevatten waar je op kan letter bij een nieuwe koppeling met een partij die je op dat moment nog niet kent. Je kunt te maken krijgen met een grote organisatie met meerdere afdelingen. Die zou je zelfstandig kunnen registeren, maar het kan handig zijn om het juiste OIN op te zoeken op basis van een taakomschrijving. Goed dat we dit onderling overleggen. Het is geen noodzaak dit op te nemen, maar het kan dienen als additionele toelichting.

**Pauw Elzo:** Als meer beter is, waar houdt het dan op? Dan zouden we nog heel veel dingen toe kunnen voegen.

**Peter Haasnoot:** De informatie kloppend te houden brengt ook beheerlast mee. Antoon heeft de use case duidelijk verwoord; Zijn er anderen die dit veld als concrete noodzaak zien?

**Maarten Coemans:** Als je meerdere sub-OIN's gaat vastleggen moet het altijd duidelijk zijn. Bij het OM krijgen wij echter het OIN door van de meewerkende organisatie, dus ik zie het niet als een concrete noodzaak. In ons proces moet de ketenpartner in het contract aangeven welk OIN zij gebruiken. Waar wordt het OIN-register wel voor gebruikt? Heel beperkt in ons geval.

**Karl de Boer:** Wij gebruiken de API om de juiste KVK-nummers op te halen van OIN's. De ene werkt met OIN's, de ander met KVK-nummers en de andere weer met andere nummers. We gebruiken het register dus altijd om te verifiëren wanneer we een weer een nieuwe tennant inrichten. Dat doen we vooral via de user interface, maar de API wordt ook gebruikt.

### Scope

Erwin Reinhoud meldt dat het COR niet alle HRN's ontsluit, waarmee het volgende discussiestuk aangebroken wordt: [OIN Register en Scope](https://github.com/Logius-standaarden/Overleg/blob/main/Digikoppeling/2023-06-22/OIN_Stelsel_Scope.md).

**Erwin Reinhoud:** Je hebt OIN's die op basis van een HRN zijn gemaakt en binnen het onderwijs willen we voor dat soort OIN's een verificatie kunnen doen. Wij dachten dit bij de COR te kunnen doen, maar niet elke private partij (bijv. leverancier) met een PKIoverheid-certificaat staat erin. We kunnen dus niet meer dan enkel bilateraal de uitwisseling van OIN doen, wat een valide manier is, maar als je toch een centraal register hebt lijkt het ons daar gebruik van te maken.

**Peter Haasnoot:** Welke organisaties wil men in het COR tegenkomen? Zijn er nog anderen die daar een bepaalde mening of behoefte over hebben gezien hun domein?

**Maarten Coemans:** Wij als SNG zijn geen SAAS-leverancier, maar een informatieknooppunt, of "hub". Wij verifiëren de authenticiteit van de achterliggende organisaties, maar ik weet niet of je dit daar helemaal mee gaat oplossen.

## Stand van zaken Roadmap

Peter Haasnoot presenteert de tweejaarlijkse [roadmap](https://github.com/Logius-standaarden/Digikoppeling-Algemeen/blob/-/Digikoppeling_Roadmap_2022_2023.md) die dit jaar ten einde komt en stelt voor in de volgende sessie (september 2023) de onderwerpen voor de toekomst te gaan bepalen.

## Grote en kleine wijzigingen, issues en pull requests

### Digikoppeling baseren op ebMS3

Edwin Wisse meldt dat de ebMS-transitie bij de programmeringstafel is besproken en dat ons gevraagd is een impact analyse uit te voeren bij de stakeholders en wijst naar een schriftelijke toelichting in [bijlage](https://github.com/Logius-standaarden/Overleg/blob/main/Digikoppeling/2023-06-22/impact_ebMS.md).

Geen vragen of opmerkingen van de aanwezigen.

### Best practices

Peter Haasnoot meldt dat de informatieve best practice documenten van tekstuele correcties en verduidelijkingen. De aanwezigen hebben geen bezwaar tegen het publiceren van deze wijzigingen.

### RSIN of KVK-nummer leidend voor OIN

De vraag staat als issue op GitHub samen met een wijzigingsvoorstel. Edwin Wisse meldt dat er een evaluatie loopt omtrent omgang met het OIN-stelsel waardoor dit punt even _on hold_ is gezet.

### Signing & Encryptie toevoegen aan RESTful API profiel

De Werkgroep Beveiliging (sub-werkgroep Signing) heeft een vergelijking tussen JAdES en httpbis-message-signatures opgesteld onder [Vergelijking REST API Signing Standaarden](https://geonovum.github.io/KP-APIs/publicaties/REST_API_Signing_Standaarden/). Peter Haasnoot licht toe dat de JAdES standaard vanuit de EU wordt ontwikkeld maar nog de draft status heeft. Daarentegen is httpbis-message-signatures een generieke internationale standaard die binnen de IETF ontwikkeld wordt waar de laatste stemrondes lopen om het definitief te maken. Het tijdspad is echter nog niet duidelijk.

Daar steeds meer partijen de wens hebben om Rest API te kunnen invullen nadert de noodzaak hier afspraken over te maken. De verwachting is in Q3 een conceptmodule op te hebben gesteld voor Signing. Politie heeft ervaring opgedaan met httpbis-message-signatures voor intern gebruik. Vraag aan de leden voor meer voorbeelden van use-cases of pilotprojecten. Functioneel kunnen ze allebei worden ingezet, maar de mate van ondersteuning in bestaande tooling van leveranciers kan de doorslag geven één tot vaste standaard te verheffen.
