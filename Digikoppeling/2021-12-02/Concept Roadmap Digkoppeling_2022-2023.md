  

Concept Roadmap Digikoppeling 2022-2023
===============

*  Toevoegen RESTful API profiel aan Digikoppeling
*  Signing & Encryptie toevoegen aan RESTful API profiel
*  Aanvulling Digikoppeling governance
*  Verbeteren Informatievoorziening / Nieuwe wijze van Publiceren
*  Best Practice Identificatie van Organisaties, Organisatieonderdelen en voorzieningen
*  Analyse knelpunten Routering en Intermediairs in gegevensverkeer
*  Verkennen mogelijk gebruik ebMS3/AS4
*  Interoperabiliteit platformen WUS bij gebruik MTOM in combinatie met WS-Security (signing)
*  Doorontwikkeling RESPEC/Digikoppeling template voor publicatie van specificaties
*  Update Beheermodel / aansluiting op Logius Standaarden BOMOS generiek beheer model & governance
*  Lange termijn visie : Hoe om te gaan met uitfasering/vervanging van profielen
*  Periodiek actualiseren architectuur

Achtergrond
-----------

Digikoppeling bevordert interoperabiliteit door digitale berichtuitwisseling te standaardiseren. Hierbij maakt Digikoppeling gebruik van internationale open standaarden. Daarmee is Digikoppeling een belangrijke pijler voor de Generieke Digitale Infrastructuur (GDI) die publieke dienstverlening en uitvoering mogelijk maakt.

Digikoppeling bestaat uit een set standaarden die het mogelijk maakt om berichten tussen overheidsinstellingen en organisaties die met of binnen de overheid digitaal informatie willen uitwisselen, op gestandaardiseerde wijze veilig uit te wisselen. Gebruik van deze standaarden wordt ondersteund door de Digikoppeling voorzieningen; de Centrale OIN Raadpleegvoorziening, de Compliance voorzieningen en het CPA Register. Dit ten behoeve van ontwikkeling en implementatie van systemen die Digikoppeling toepassen. Daarmee is Digikoppeling de invulling van de servicegerichte architectuur die de Nederlandse Overheid Referentie Architectuur (NORA) voorschrijft.

Door middel van deze roadmap wil de productgroep Digikoppeling richting geven aan het product voor de komende jaren en duidelijkheid geven over de toekomst van Digikoppeling.

### Doel roadmap

Dit document is gericht op het voorbereiden van de tactische keuzes voor doorontwikkeling van de Digikoppeling standaard én voorzieningen in de komende jaren. Hierbij is rekening gehouden met de vele ontwikkelingen die spelen rond Digikoppeling zoals

* het toenemende gebruik van op REST gebaseerde webservices
* het vernieuwde OIN beleid
* de behoefte met betrekking tot het anders aanbieden van de informatie over Digikoppeling.

De Roadmap Digikoppeling heeft als doel te beschrijven hoe de Digikoppeling standaard en de voorzieningen in de periode van 2022 t/m 2023 meegroeien met de behoeften van haar gebruikers. Daarnaast wordt er in dit document een terugblik gegeven op de vorige roadmap die liep van 2020 t/m2021.

### Totstandkoming Roadmap

De samenstelling van deze Roadmap is opgesteld door de productgroep Digikoppeling van Logius. Hierbij is gekeken naar de (toekomstige) ontwikkelingen rond de Digikoppeling standaard, vragen van het Technisch Overleg Digikoppeling en lopende vragen en wensen vanuit de markt over de voorzieningen. Vervolgens is een aantal onderwerpen benoemd die als project opgepakt zullen worden en is er gerangschikt op prioriteit.

De onderwerpen voor het standaardendeel van de roadmap zijn in **DATUM** besproken door het Technisch Overleg (TO) en de concept roadmap is in **DATUM** ter vaststelling ingediend. De leden van het TO konden hier zowel mondeling als schriftelijk op reageren en deze reacties zijn meegenomen in voorliggende **[concept/definitieve]** versie.

### Positionering Digikoppeling

De scope van Digikoppeling zal niet veranderen:  
Digikoppeling maakt het mogelijk dat organisaties die, met of binnen de overheid, digitaal informatie willen uitwisselen dit op een gestandaardiseerde wijze veilig kunnen doen. Het is in beginsel geen infrastructuur maar een set aan afspraken over het gebruik van internationale open standaarden. Digikoppeling kent wel ondersteunende voorzieningen maar deze zijn gericht op ondersteuning van het ontwikkelproces bij implementatie van Digikoppeling en niet op directe ondersteuning van productie-situaties zelf.

Interoperabiliteit is gewaarborgd omdat Digikoppeling bestaat uit standaarden die breed in de markt worden ondersteund en omdat voor Digikoppeling specifieke opties zijn gekozen.  
Digikoppeling is daarmee een essentiële bouwsteen van de elektronische overheid en vult de door NORA voorgeschreven servicegerichte architectuur in.

De Digikoppeling Standaard is op dit moment afgebakend op basis van berichtenuitwisseling, op basis van ebMS of WUS. Binnen de Nederlandse Overheid vinden steeds meer ontwikkelingen plaats op het gebied van informatie-uitwisseling op basis van RESTful Api’s. Dit roept mogelijk vragen op wanneer welk protocol gebruikt moet of mag worden. In de roadmap 2022-2023 is aandacht voor de wijze waarop Digikoppeling omgaat met deze ontwikkeling.

Onderwerpen Digikoppeling Standaarden
-------------------------------------

In eerdere edities van de Digikoppeling roadmap liepen de onderwerpen met betrekking tot de Digikoppeling standaarden en aanverwante voorzieningen door elkaar heen. In deze editie heeft de productgroep Digikoppeling ervoor gekozen deze onderdelen afzonderlijk weer te geven. De onderwerpen van de roadmap Digikoppeling voorzieningen staan [hier](https://logius.nl/diensten/digikoppeling/documentatie/digikoppeling-roadmap-2020-2021#onderwerpen-digikoppeling-voorzieningen) .

### \> Toevoegen RESTful API profiel aan Digikoppeling

_Wat is het issue of de wens?_

Digikoppeling maakt gebruik van EBMS, WUs en GB om informatie uit te wisselen tussen overheden. Al enige jaren is het echter gangbaar om informatie uit te wisselen door bronnen direct te raadplegen/wijzigen door gebruik te maken van een alternatief architectuurpatroon REST (REpresentational State Transfer). REST maakt opgang binnen de Nederlandse overheid.  
Wanneer het best welk architectuurpatroon kan worden toegepast en hoe dat zich verhoudt tot de ‘pas toe of leg uit’ –verplichting om Digikoppeling toe te passen, is voor veel partijen nog onduidelijk. Logius ziet het als haar taak om de situatie rondom het gebruik van Digikoppeling en REST voor iedereen inzichtelijk te maken.

_Wat gaat er gebeuren?_

Digikoppeling heeft in 2020 een Digikoppeling REST API profiel opgesteld dat is gebaseerd op de ‘Pas toe of leg uit ‘-standaard: API design Rules. Deze laatste komt van het Kennisplatform API’s en is sinds september 2020 bij Logius in beheer genomen. De uitbreiding van Digikoppeling met een REST API profiel is voorgelegd aan het forum Standaardisatie voor opname op de pas-toe-of-leg-uit lijst. Bij een positief doorlopen procedure (en na goedkeuring door OBDO) zal Digikoppeling begin 2022 het REST API profiel bevatten.  
De Digikoppeling achitectuurdocumentatie wordt dan ook aangepast zodat inzichtelijk wordt wanneer het best welk koppelvlak kan worden toegepast.

_Wat is het resultaat?_

Een Digikoppeling standaard waar, naast ebMS, WUS en GB, ook een profiel voor Digikoppeling RESTFul API’s is opgenomen.

_Wanneer gaat dit gebeuren?_

Q1 2022

### \> Signing & Encryptie toevoegen aan RESTful API profiel

_Wat is het issue of de wens?_

Digikoppeling EBMS & WUS kennen specifieke profielen voor signing & encryptie, het huidige Digikoppeling RESTful API profiel kent dit nog niet

_Wat gaat er gebeuren?_

Wanneer het REST API profiel door het OBDO wordt goedgekeurd voor opname op de pas-toe-of-leg-uit lijst van het Forum Standaardisatie zal het onderdeel signing en encryptie worden ingevuld, hierbij zal worden aangesloten op de ontwikkelingen binnen het kennisplatform API's.

_Wat is het resultaat?_

Een Digikoppeling standaard waarin voor het Digikoppeling REST API profiel ondersteuning is voor signing & encryptie.

_Wanneer gaat dit gebeuren?_

Q2 2022-Q4 2022

### \> Aanvulling Digikoppeling governance

_Wat is het issue of de wens?_

Traditioneel bestond de governance van Digikoppeling uit drie lagen: Operationeel (het Technisch Overleg), tactisch en strategisch. Door een reorganisatie bij Logius en het verdwijnen van de Digicommissaris zijn die laatste twee lagen weggevallen. Om effectief beheer te kunnen voeren is een complete governancestructuur noodzakelijk.

_Wat gaat er gebeuren?_

Digikoppeling zal een nieuwe tactische en strategische laag inrichten om de huidige governance aan te vullen. Het kan dat deze taken belegd worden bij reeds bestaande gremia, maar als dit geen optie is, kan Digikoppeling ook zelf nieuwe gremia optuigen en faciliteren. Voor invulling van de tactische en strategische governance lagen zal gekeken worden of deze gebruik kan maken van de MIDO governance voor het GDI. Het heeft de voorkeur om nieuwe gremia binnen bestaande structuren te zoeken.

_Wat is het resultaat?_

Een optimale governancestructuur die weer bestaat uit drie lagen.

_Wanneer gaat dit gebeuren?_

Q1 2022 – Q4 2022

### \> Verbeteren Informatievoorziening / Nieuwe wijze van Publiceren

_Wat is het issue of de wens?_

De digikoppeling documentatie moet eenvoudig toegankelijk zijn. Gebruikers moeten gemakkelijk de voor hen relevante onderdelen kunnen vinden en benaderen. Informatie staat nu verspreid over een aantal verschillende websites waarbij onderliggende relaties niet altijd gelegd worden;

_Wat gaat er gebeuren?_

Digikoppeling onderhoudt de beheerdocumentatie en standaardspecificaties op Github; Algemene informatie en vergaderstukken wordt via logius.nl en digistandaarden.pleio.nl verstrekt. OIN specficatie en interface worden via portaal.digikoppeling.nl gepubliceerd. Tevens publiceert Logius nu een source en documentatie voor een aantal producten via gitlab, waaronder ook aan digikoppeling gerelateerde diensten.  Onderzocht zal worden hoe de informatie meer geordend en meer geïntegreerd kan worden aangeboden en hoe de community beleving kan worden verbeterd.

_Wat is het resultaat?_

Een omgeving waar alle documentatie m.b.t. de Digikoppeling standaard online (in HTML) beschikbaar is. Ook diensten en aanvullende informatie worden waar mogelijk via één website gepubliceerd. Wanneer verschillende sites gebruikt worden wordt de onderlinge samenhang duidelijk gemaakt zodat gebruikers alle informatie rondom de Digikoppeling standaard kunnen vinden.

_Wanneer gaat dit gebeuren?_

Q1 2022 – Q2 2022

### \> Best Practice Identificatie van Organisaties, Organisatieonderdelen en voorzieningen

_Wat is het issue of de wens?_

Het OIN-beleid is sinds 2016 op het punt van het gebruik van SubOIns voor organisatieonderdelen en –voorzieningen verduidelijkt en uitgebreid. Het lijkt erop dat het steeds belangrijker wordt om entiteiten in een uitwisselketen te kunnen identificeren. Er bestaat tussen organisaties verschil in inzicht in de toepassing van identificatie.

Er is behoefte aan inzicht in hoe nu wordt en moet worden omgaan met identificatie in uitwisselketens tussen en met overheden.

_Wat gaat er gebeuren?_

Inventarisatie hoe organisaties omgaan met identificatie van onderdelen in de uitwisselketen. Bepalen welke practices kunnen worden aangeduid als best practices voor het omgaan met identificatie.

_Wat is het resultaat?_

Best practice beschrijving van Identificatie van Organisaties, Organisatieonderdelen en voorzieningen.

_Wanneer gaat dit gebeuren?_

Q1-Q2 2022

### \> Analyse knelpunten Routering en Intermediairs in gegevensverkeer

_Wat is het issue of de wens?_

Het is binnen overheidsketens steeds gebruikelijker om gebruik te maken van dienstverlening vanuit de Cloud, en diensten af te nemen van SAAS leveranciers. Dit heeft impact op vragen als wat is het endpoint in een keten, wie is de oorspronkelijker aanbieder of uiteindelijke ontvanger, hoe herken ik die en hoe weet ik dit zeker. Digikoppeling biedt met signing en encryptie tools aan, sommige sectoren hebben voorzieningen ontwikkeld, die bovenstaande vragen deels beantwoorden, andere partijen zijn zoekende hoe om te gaan met de nieuwe situatie.

_Wat gaat er gebeuren?_

In kaart brengen wat de knelpunten zijn bij uitwisselketens met transparante en niet-transparante intermediairs. Inventariseren welke oplossingen in de praktijk toegepast worden. Onderzoeken welke oplossingen uitgewerkt dienen te worden en vervolgens kunnen worden toegepast in Digikoppeling.

_Wat is het resultaat?_

Een analyse van de knelpunten en oplossingsrichtingen, met de impact ervan op Digikoppeling.

_Wanneer gaat dit gebeuren?_

Q1-Q2 2022

### \> Verkennen mogelijk gebruik ebMS3/AS4

_Wat is het issue of de wens?_

De ebMS2 standaard wordt niet verder doorontwikkeld. Het ligt daarom voor de hand om te kijken of ebMS2 vervangen kan worden ebMS3. En dan met name het AS4 profiel hierop. Dit is ook onderdeel van de EU eDelivery standaard voor gegevensuitwisseling over landsgrenzen heen.

In 2018 heeft Digikoppeling laten onderzoeken of en wanneer het zinnig is om ebMS2 vervangen door de nieuwe versie. Naar aanleiding van dat onderzoek besloot het TO dat er voorlopig geen directe aanleiding is om ebMS2 actief te vervangen.

Begin 2020 is in het TO besloten om ebMS2 weliswaar nog niet actief te vervangen, maar dat het wel zinnig is om als Digikoppeling bij te houden hoe de ondersteuning van ebMS2, vanuit leveranciers, zich ontwikkeld en als eens te verkennen welk ebMS3 profiel eventueel bruikbaar zal zijn binnen de Digikoppeling standaard.

_Wat gaat er gebeuren?_

Digikoppeling gaat verkennen of het eDelivery ebMS3 AS4 profiel geschikt is voor gebruik binnen Digikoppeling en wat daar nog eventueel aan toegevoegd dient te worden.

Daarnaast zal Digikoppeling partijen, die ervaring hebben met het opstellen van een eigen ebMS3 profiel, uitnodigen om in het TO te komen vertellen hoe dit proces is verlopen.

_Wat is het resultaat?_

Met bovengenoemde acties heeft Digikoppeling in de 2e helft van 2022 een goed beeld van moeilijkheden en mogelijkheden van het gebruik van de ebMS3 standaard zodat eind 2022 met het TO opnieuw besproken kan worden of en op welke termijn het zinnig is om over te gaan op de nieuwe versie.

_Wanneer gaat dit gebeuren?_

Q2-Q4 2022

### \> Interoperabiliteit platformen WUS bij gebruik MTOM in combinatie met WS-Security (signing)

_Wat is het issue of de wens?_

Bij gebruik van MTOM in combinatie met signing en encryptie zijn er verschillen in hoe de verschillende platformen hiermee omgaan in de default instellingen en in de mogelijkheden om certificaat informatie wel of niet als reference te kunnen specificeren/verwerken;

_Wat gaat er gebeuren?_

Er zal onderzocht worden of aanvullende afspraken in de standaard kunnen helpen om de interoperabiliteit op dit punt te vergroten;

_Wat is het resultaat?_

_Resultaat is een analyse met indien mogelijk een voorstel voor aanvullende afspraken_

_Wanneer gaat dit gebeuren?_

_Q1-Q2 2022_

### \> Doorontwikkeling RESPEC/Digikoppeling template voor publicatie van specificaties

_Wat is het issue of de wens?_

Digikoppeling documentatie wordt d.m.v. RESPEC gepubliceerd. RESPEC is een hulpmiddel ontwikkeld door W3C voor technische specificaties (respec.org).  
RESPEC wordt doorontwikkeld en de Digikoppeling documentatie tooling zal meelopen in deze ontwikkeling om ook nieuwe functionaiteiten te ondersteunen;

_Wat gaat er gebeuren?_

Het Digikoppeling RESPEC template zal de ontwikkelingen bij RESPEC volgen.

_Wat is het resultaat?_

Het resultaat is een Digikoppeling RESPEC template dat up to date is met de algemene/centrale RESPEC ontwikkeling en dat voldoet aan de Digitoegankelijkheidseisen.

(Voordeel hiervan is ook dat technisch onderhoud uiteindelijk bij de W3C Respec community komt te liggen)

_Wanneer gaat dit gebeuren?_

_Q1-Q2 2022_

### \> Update Beheermodel / aansluiting op Logius Standaarden BOMOS generiek beheer model & governance

_Wat is het issue of de wens?_

Momenteel wordt een nieuw generiek beheermodel gebaseerd op BOMOS ontwikkeld binnen de afdeling Standaarden;  
Het Digikoppeling beheermodel zal in lijn moeten blijven met het generieke model.

_Wat gaat er gebeuren?_

Het Digikoppeling beheermodel zal in lijn worden gebracht met het generieke model.

_Wat is het resultaat?_

Een Digikoppeling beheermodel in lijn met het generieke beheermodel volgens BOMOS van de afdeling Standaarden.

_Wanneer gaat dit gebeuren?_

_Q1-Q2 2022_

### \> Lange termijn visie : Hoe om te gaan met uitfasering/vervanging van profielen

_Wat is het issue of de wens?_

Als nieuwe profielen worden geïntroduceerd , is de vraag hoe moet worden omgegaan met het al dan niet toestaan van meerdere vergelijkbare profielen binnen Digikoppeling;

_Wat gaat er gebeuren?_

In het TO zal dit onderwerp besproken worden

_Wat is het resultaat?_

Een visie op uitfasering/vervanging van profielen

_Wanneer gaat dit gebeuren?_

_Q1-Q2 2022_

### _\> Periodiek actualiseren architectuur_

_Wat is het issue of de wens?_

De Digikoppeling architectuur dient periodiek te worden bijgewerkt om goed aan te blijven aansluiten bij ontwikkelingen in de NORA, Gemma, KP-API's en andere overheidsbrede architectuur ontwikkelingen;

_Wat gaat er gebeuren?_

_Bijwerken van het huidige architectuurdocument_

_Wat is het resultaat?_

Een nieuwe versie van het architectuur document

_Wanneer gaat dit gebeuren?_

_Q3 2022 & Q3 2023_

### Tijdlijn Roadmap Digikoppeling Standaarden

| Activiteit | Q1 2022 | Q2 2022 | Q3 2022 | Q4 2022 | Q1 2023 | Q2 2023 | Q3 2023 | Q4 2023 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |  
| \> Toevoegen RESTful API profiel aan Digikoppeling | X   | X   |     |     |     |     |     |     |
| \> Signing & Encryptie toevoegen aan RESTful API profiel | X   | X   | X   | X   |     |     |     |     |
| \> Aanvulling Digikoppeling governance | X   | X   | X   | X   |     |     |     |     |
| \> Verbeteren Informatievoorziening / Nieuwe wijze van Publiceren | X   | X   | X   | X   | X   | X   |     |     |
| \> Best Practice Identificatie van Organisaties, Organisatieonderdelen en voorzieningen | X   | X   |     |     |     |     |     |     |
| \> Analyse knelpunten Routering en Intermediairs in gegevensverkeer | X   | X   |     |     |     |     |     |     |
| \> Verkennen mogelijk gebruik ebMS3/AS4 |     |     | X   | X   | X   | X   |     |     |
| \> Interoperabiliteit platformen WUS bij gebruik MTOM in combinatie met WS-Security (signing) | X   | X   |     |     |     |     |     |     |
| \> Doorontwikkeling RESPEC/Digikoppeling template voor publicatie van specificaties | X   | X   | X   | X   | X   | X   | X   | X   |
| \> Update Beheermodel / aansluiting op Logius Standaarden BOMOS generiek beheer model & governance |     |     | X   | X   | X   |     |     |     |
| \> Lange termijn visie : Hoe om te gaan met uitfasering/vervanging van profielen |     |     | X   | X   | X   |     |     |     |
| \> Periodiek actualiseren architectuur |     |     | X   |     |     |     | X   |     |

  

---
