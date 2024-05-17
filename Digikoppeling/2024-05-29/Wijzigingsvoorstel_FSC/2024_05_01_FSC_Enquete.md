(Concept)

# Enquete FSC Wijzigingsvoorstel

Standpunten zijn opgevraagd tbv bespreking in komend Technisch Overleg Digikoppeling;
NB Dit zijn nog geen definitieve keuzes, we streven ernaar om in het komend TO d.d. 29 mei te komen tot een definitief besluit)

# Resultaten Enquete

_Wat is het standpunt van jullie organisatie ten aanzien van het wijzigingsvoorstel FSC_

| Nr	| Naam	| Standpunt |
|-------|-------|-----------|
|1	|RDW	|Neutraal |
|2	|Pink Roccade	| Neutraal |
|3	|DUO	|(Nog) Niet akkoord |
|4	|J&V / JUSTID	|Niet akkoord |
|5	|Kadaster	|Neutraal |
|6	|UWV	|Akkoord |
|7	|SNG	|Niet akkoord |
|8	|Geonovum	|Akkoord |

# Toelichtingen per organisatie

## Organisatie RDW

### Wat is het standpunt van jullie organisatie ten aanzien van het wijzigingsvoorstel FSC  (na de (impact)analyse)
* [ ]  Akkoord met goedkeuring 
* [ ]  Niet akkoord met goedkeuring
* [X]  Neutraal

### Toelichting bij standpunt  
De RDW ondersteunt momenteel vrijwel alle digikoppeling patronen voor berichtuitwisseling met andere overheidspartijen. Dit zorgt voor een, nu al, complex landschap van koppelingen waar veel tijd in gaat zitten qua ontwikkeling en beheer. De FSC standaard zorgt aan de kant van de RDW voor een toename aan complexiteit, aangezien er een nieuwe standaard moet worden geïmplementeerd en onderhouden.

Wat ons betreft zou er ook moeten worden gewerkt aan het uitfaseren van standaarden, om het landschap overzichtelijk te houden. Het NCSC (nationaal cybersecurity centrum) classificeert bijvoorbeeld TLS versies als “goed”, “voldoende” of “uit te faseren”. Hetzelfde zou kunnen worden gedaan voor digikoppeling standaarden, waarbij de WUS standaard bijvoorbeeld nu de status “voldoende” zou kunnen krijgen. Over een aantal jaar zou deze standaard de status “uit te faseren” kunnen krijgen. Op deze manier wordt een groei van het aantal standaarden voorkomen, en werken we als TO aan een eenduidige manier van koppelen.

We zien in de FSC standaard veel goede dingen, met name het standaardiseren van het werken met tussenpartijen is een goede toevoeging. Tegelijk zou ook moeten worden gedacht aan het opruimen van standaarden om het aantal daarvan te beperken.

### Welke termijn verwachten jullie nodig te hebben om aan het nieuwe Digikoppeling REST API profiel (met daarin opgenomen FSC ) te kunnen voldoen (d.w.z. wanneer het wijzigingsvoorstel wordt aangenomen).
Hier kunnen we geen uitspraak over doen, nadat de standaard wordt goedgekeurd zal bijvoorbeeld eerst de centrale directory uit de FSC standaard moeten worden geïmplementeerd voordat de RDW de standaard over kan nemen.

## Organisatie: PinkRoccade Local Government

### Wat is het standpunt van jullie organisatie ten aanzien van het wijzigingsvoorstel FSC  (na de (impact)analyse)
* [ ]  Akkoord met goedkeuring 
* [ ]  Niet akkoord met goedkeuring
* [x]  Neutraal

### Toelichting bij standpunt 
Algemeen beeld over FSC is positief. Vooral de ‘delegatie’-oplossing zal op termijn positieve invloed hebben op efficiëntie en beheerlast; hiermee na de transitie ook kostenbesparend zijn.
Daartegenover staat dat alle in de keten samenwerkende organisaties moeten meebewegen om de vruchten hiervan te plukken. Naast het vaststellen van de standaard zijn ook sturing en incentives nodig om de ingebruikname gedurende langere periode te stimuleren.
Voor nu dus een neutrale houding, omdat de adoptie-maatregelen en consequenties onvoldoende scherp zijn, dit mede in relatie tot al dan niet aanwezige klantbehoefte. 
Daarbij zijn we van mening dat het vervallen van whitelisting van inkomende verbindingen onvoldoende is toegelicht en vinden dat hiervoor in de standaard wel een voorziening nodig is, temeer omdat het opnemen van outways in het DNS niet verplicht is.

### Welke termijn verwachten jullie nodig te hebben om aan het nieuwe Digikoppeling REST API profiel (met daarin opgenomen FSC ) te kunnen voldoen (d.w.z. wanneer het wijzigingsvoorstel wordt aangenomen).*
We verwachten 12 maanden nodig te hebben voor implementatie van het geheel vanaf de goedkeuringsdatum met daarbij een concrete klantcasus als randvoorwaarde.

## Organisatie Dienst Uitvoering Onderwijs.

### Wat is het standpunt van jullie organisatie ten aanzien van het wijzigingsvoorstel FSC  (na de (impact)analyse)
* [ ]  Akkoord met goedkeuring 
* [ ]  Niet akkoord met goedkeuring
* [x]  Nog niet akkoord met goedkeuring
* [ ]  Neutraal

### Toelichting bij standpunt  
Edustandaard zit wat betreft het toepassen van OAUTH op de wip. Het is onvermijdelijk dat DUO dit gaat toepassen in verband met  de zogenaamd nationale groeifondsen.  Wij hopen natuurlijk dat dit een nationale oplossing is en dat onderwijs daar netjes binnenvalt. Maar FSC nu opnemen in Digikoppeling gaat ons net iets te snel. Dit zijn onze overwegingen:

1.	Wij ondersteunen het expliciet valideren van de relatie tussen een gegevensverantwoordelijke en een (cloud-)leverancier die een dienst aanroept volgens Digikoppeling. Zoiets hebben we binnen Edustandaard al afgesproken. Een elders nog voorkomende werkwijze waarbij de gegevensverantwoordelijke zijn PKI-certificaat moet afgeven aan zijn verwerker keuren we af. 
2.	De FSC - oplossing komt er op neer dat drie partijen (gemeente, leverancier, dienst) met hun eigen PKI-certificaat een ‘contract’  tekenen. Dit contract wordt door de FSC-manager gedistribueerd. De dienst kan daardoor de aanvraag van een (cloud)leverancier valideren tegen het contract en concluderen of  de aanvraag (nog) geldig is. Wij verwachten dat deze werkwijze wordt uitgewerkt in het nieuwe profiel voor NL-GOV waarin de zogenaamde client credentials variant voor direct access clients wordt uitgewerkt.  Maar dat is work-in-progress.  DUO vindt het onverantwoord om FSC op te nemen in Digikoppeling zolang NL-GOV dat niet heeft uitgewerkt en het  goedkeuringsproces heeft doorlopen.
3.	Het onderwijs heeft een bestaande oplossing voor dergelijks op advies van de Digikoppeling-gemeenschap. De aanvraag wordt gedaan door de LAS-leverancier met zijn eigen PKI-certificaat.  In de dienstaanvraag geeft de LAS-leverancier in een query-parameter het OIN-nummer door van de school namens wie ze werken en de dienst valideert dit aan de hand van een geregistreerde bewerkersovereenkomst (centraal of bij de dienst zelf). Er is één groot verschil met FSC, de school heeft geen PKI-certificaat. Ze tekenen wel, maar dat is ofwel een ‘natte’ handtekening ofwel omdat een medewerker van de school is ingelogd op een website.  Diverse partijen in het onderwijs wijzen een oplossing af waarbij scholen (alles bij elkaar zo’n 8000) met PKI-certificaten moeten werken.  Wij verwachten dat de Edustandaard variant ook wordt opgenomen in Digikoppeling. 

### Welke termijn verwachten jullie nodig te hebben om aan het nieuwe Digikoppeling REST API profiel (met daarin opgenomen FSC ) te kunnen voldoen (d.w.z. wanneer het wijzigingsvoorstel wordt aangenomen).*
DUO is betrokken bij één concreet project (groeifonds Npulse onderdeel Onderwijs Koppeling Examinering (OKE) ) dat per omgaande uitsluitsel nodig heeft. Vervanging van oudere (WUS-)profielen is een kwestie van LCM en zal enkele jaren duren. 

## Organisatie Justitiële Informatiedienst en DI&I namens geheel JenV

### Wat is het standpunt van jullie organisatie ten aanzien van het wijzigingsvoorstel FSC  (na de (impact)analyse)

* [ ]  Akkoord met goedkeuring 
* [x]  Niet akkoord met goedkeuring
* [ ]  Neutraal

### Toelichting bij standpunt 
Hoewel FSC zeker van meerwaarde kan zijn in het gestructureerd koppelen en autoriseren op API’s is onduidelijk welke meerwaarde tegen welke kosten wordt bereikt en van welke impact sprake is. Ook zouden wij ervoor willen waken om een standaard enkel vanuit verplichting draagvlak te geven. Dit draagvlak zou in de eerste plaats moeten komen uit het feit dat het een aanvulling is en een duidelijke meerwaarde biedt voor de partijen die hier gebruik van maken. Deze meerwaarde wordt tot nu toe nog niet voldoende duidelijk uit bijvoorbeeld het aantal organisaties die hierin het voortouw nemen en early adopter zijn. Tevens zou een verplichting tot verminderde flexibiliteit en wendbaarheid kunnen leiden.  Hier is nog niet voldoende over bekend, ook is nog niet voldoende ervaring opgedaan om al in deze fase FSC als verplichting op te nemen. Ook is nog onduidelijk welke effecten ontstaan door de FSC benadering versus de algemene markt-/internet brede benadering, ofwel door de speciale overheid- versus algemene niet-overheid benadering. Ons voorstel en dringend advies zou dan ook zijn om eerst een periode de standaard als (aanbevolen) optie in Digikoppeling op te nemen. Mocht adoptie hiermee tot stand komen, en er geen onoverkomelijke nadelen blijken te zijn, dan kan het uiteindelijk alsnog verplicht worden, maar blijft adoptie uit dan moet geconcludeerd worden dat afnemers onvoldoende meerwaarde zien, dan wel ook andere methoden/mogelijkheden nodig hebben. Dit zou een goede werkwijze zijn om te voorkomen dat we prematuur verplichtingen opnemen die onvoldoende door de praktijk gesteund worden.

We kunnen samengevat geen goedkeuring geven omdat:
- De verplichting vooral lijkt te zijn ingeven om dwingend draagvlak en massa te creëren, wat doorgaans geen goede en een risicovolle benadering is. Het komen tot verplichting middels Digikoppeling heeft altijd een aanloop en beproef termijn gekend. Die zou nu overgeslagen worden.
- Positionering als (aanbevolen) optie in Digikoppeling beter is dan verplichten in deze fase 
- De impact van verplichting onduidelijk is en potentieel negatief effecten heeft op taakuitvoering
- Er nog onvoldoende ervaring en vertrouwen opgebouwd is rondom FSC
- Verplichting pas aan de orde kan zijn indien er voldoende draagvlak en adoptie is

We kijken ernaar uit dit een succes te maken, maar willen er wel zorg voor dragen dat hierin de juiste stappen genomen worden.

### Welke termijn verwachten jullie nodig te hebben om aan het nieuwe Digikoppeling REST API profiel (met daarin opgenomen FSC ) te kunnen voldoen (d.w.z. wanneer het wijzigingsvoorstel wordt aangenomen).
Als JenV hebben we te maken met een groot aantal zelfstandige uitvoeringsorganisaties die elk deze standaard te implementeren hebben. De aandacht die er op dit moment is voor het inzetten van REST-API’s helpt in het vrij kunnen maken van resources maar dan nog dient er rekening gehouden te worden met een aanzienlijke doorlooptijd. 

## Organisatie Kadaster

### Wat is het standpunt van jullie organisatie ten aanzien van het wijzigingsvoorstel FSC  (na de (impact)analyse)
* [ ]  Akkoord met goedkeuring 
* [ ]  Niet akkoord met goedkeuring
* [X]  Neutraal

### Toelichting bij standpunt 

* Machtigen/rechtendelegatie is beperkt ingevuld

FSC staat toe dat bedrijven namens (overheids)organisaties een API mogen aanroepen. Welke data dan gemuteerd mag worden, bijvoorbeeld alleen van de gemeente die het bedrijf ingehuurd heeft voor een opdracht, lijkt geen onderdeel van de oplossing.

### Welke termijn verwachten jullie nodig te hebben om aan het nieuwe Digikoppeling REST API profiel (met daarin opgenomen FSC ) te kunnen voldoen (d.w.z. wanneer het wijzigingsvoorstel wordt aangenomen).*
_2 jaar____________

## Organisatie UWV

### Wat is het standpunt van jullie organisatie ten aanzien van het wijzigingsvoorstel FSC  (na de (impact)analyse)
* [X]  Akkoord met goedkeuring 
* [ ]  Niet akkoord met goedkeuring
* [ ]  Neutraal

### Toelichting bij standpunt  

Mooi initiatief en helder plan ik snap alleen niet waarom het enkel REST betreft en niet gelijk ook de SOAP services. Adoptie intern gaat tijd kosten maar lijkt zeker haalbaar gezien de technische kennis die vereist is. Logging is mogelijk ook een issue maar hier zijn we intern mee bezig om betere en consistente logging te waarborgen (ETA nog niet zeker) los van incidentenlogging bedoel ik dan__________

### Welke termijn verwachten jullie nodig te hebben om aan het nieuwe Digikoppeling REST API profiel (met daarin opgenomen FSC ) te kunnen voldoen (d.w.z. wanneer het wijzigingsvoorstel wordt aangenomen).*
_12 maanden ruwe schatting gezien huidige backlog

## Organisatie SNG

### Wat is het standpunt van jullie organisatie ten aanzien van het wijzigingsvoorstel FSC  (na de (impact)analyse)
* [ ]  Akkoord met goedkeuring 
* [X]  Niet akkoord met goedkeuring
* [ ]  Neutraal

### Toelichting bij standpunt 

SNG staat positief tegenover het opnemen van mandatering als verplicht concept in de DK standaard (overkoepelend, niet alleen voor REST). SNG is ook positief over het opnemen van FSC als optie / best practice voor het implementeren van een federated oplossing voor mandatering binnen het DK REST profiel. We begrijpen / ondersteunen de wens om standaardisatie in te voeren voor dit onderwerp; voorkomen dat er straks verschillende implementaties voor hetzelfde binnen DK worden ontwikkeld. Waarom dan ons (niet akkoord) standpunt?:
We zien significante uitdagingen op het gebied van beheerlast voor ‘HUBs’ / knooppunten, waarbij een groot aantal partijen worden bediend door één intermediair. Specifiek gaat het dan om de signing door de verantwoordelijke organisaties. Juridisch gezien zou deze signing moeten gebeuren door iemand binnen de verantwoordelijke organisatie die gemachtigd is om te besluiten tot mandatering. Dat betekent dat knooppunten / intermediairs terugkerend en zeer groot aantal ‘signings’ moeten verzamelen om de autorisatie / dienstverlening in stand te houden, terwijl de onderliggende overeenkomst nog steeds van kracht is. Voor zowel onszelf als voor sommige intermediairs die wij servicen zien wij daarin potentieel grote uitdagingen. Daar gaan we graag met de VNG over in gesprek, omdat een deel van onze zorg zit bij door gemeentes gemandateerde organisaties. Er wordt namelijk ook een inspanning verwacht van de verantwoordelijke organisatie/gemeente, terwijl die juist ontzorgt wil worden en daarom gebruik maken van een intermediair. Dat zou erin kunnen gaan resulteren dat knooppunten/intermediairs alsnog een verzameling aan certificaten voor verantwoordelijke partijen gaan aanhouden - wat juist niet de bedoeling is (en niet nodig in onze ervaring).
Samengevat zien we in FSC weliswaar een oplossing voor problemen in bepaalde usecases, maar komen daar andere problemen in andere usecases voor terug. Een andere overweging is dat FSC nog maar beperkt gebruikt wordt, in onze zogen is de directe stap naar opname als verplicht onderdeel (in de DK standaard) te vroeg qua proces. Wij zouden positief staan tegenover een middenweg: neem het op als mogelijkheid voor REST profielen, of wellicht verplicht/pas toe of leg uit INDIEN iemand een federatief mandateringsregister wilt realiseren binnen het DK REST profiel (ter voorkoming van meerdere oplossingen voor hetzelfde probleem). 

Maar het zou in onze beleving niet verplicht moeten zijn om mandatering middels een dergelijk federatief stelsel te realiseren. Het is ook mogelijk om dergelijke waarborgen te realiseren middels een juridisch bedrijfsproces, waarin een representatie van overeenkomsten worden gebruikt door de dienstaanbieder ten behoeve van mandatering zonder dat de verantwoordelijke organisaties daar technisch iets hoeft in te regelen; die hoeft alleen de overeenkomst voor mandatering de laten tekenen door een tekenbevoegd persoon en de dienstaanbieder moet controleren op het bestaan van die overeenkomst. 

### Welke termijn verwachten jullie nodig te hebben om aan het nieuwe Digikoppeling REST API profiel (met daarin opgenomen FSC ) te kunnen voldoen (d.w.z. wanneer het wijzigingsvoorstel wordt aangenomen).*
Om als dienstaanbieder FSC door te voeren in ons applicatie landschap zou betekenen dat we of een aparte manier van mandatering / autorisaties tbv REST API’s moeten implementeren of dat we ons volledige autorisatie model op de schop gooien (inclusief juridisch proces). Beide mogelijkheden vergen naast een ontwikkel inspanning een ketenimplementatie die naast bestaande roadmap geimplementeerd zou moeten worden. Aangezien er voor de betrokken organisaties geen directe extra toegevoegde waarde wordt gerealiseerd, maar wel een (terugkerende) inspanning wordt verwacht zien we daarin een uitdaging qua de prioritering.

Om als knooppunt een REST API met FSC te implementeren zien we technisch geen hele grote uitdaging (het is extra ontwikkelwerk, maar vergeleken met het implementeren van een API zal de extra last beperkt zijn), maar voor het inrichten van het benodigde beheerproces bij achterliggende organisaties zien we wel een significante doorlooptijd qua ketenuitrol. 
Voor beide gevallen is het noemen van een concrete periode, zonder afstemming met onze intermediairs/afnemers, niet verstandig. Voor een ketenuitrol van nieuwe uitwisselingen danwel significante wijzigingen in bestaande uitwisselingen rekenen we normaliter minimaal 1 jaar nadat wij specificaties hebben gepubliceerd en een testomgeving beschikbaar is. 

Oftewel, we verwachten niet op korte termijn te kunnen voldoen en zien de nodige hobbels in een implementatie traject.


## Organisatie Geonovum

### Wat is het standpunt van jullie organisatie ten aanzien van het wijzigingsvoorstel FSC  (na de (impact)analyse)
* [x]  Akkoord met goedkeuring 
* [ ]  Niet akkoord met goedkeuring
* [ ]  Neutraal

###  Toelichting bij standpunt  
Geonovum biedt als organisatie zelf geen APIs aan, we maken echter wel API specificaties en zien geen belemmering voor implementatie. FSC zou goed samen moeten kunnen werken op OGC API standaarden (nieuwe versie geostandaarden op PTOLU). Daarnaast zijn APIs met noodzaak voor tweezijdige authenticatie zeldzaam in het Geodomein. Dit komt vooral voor bij het bijhouden van basisregistraties. Daar zien we met name in rechtendelegatie een voordeel. 


### Welke termijn verwachten jullie nodig te hebben om aan het nieuwe Digikoppeling REST API profiel (met daarin opgenomen FSC ) te kunnen voldoen (d.w.z. wanneer het wijzigingsvoorstel wordt aangenomen).*
Beheerders van landelijke voorzieningen(Kadaster, TNO GDN, BIJ12) kunnen het beste de impact op hun systemen aangeven. Er wordt momenteel gewerkt aan het overstappen op APIs voor aanlevering aan BAG en BGT, precieze schatting van de termijnen is lastig maar vanuit Geonovum schatten we dat binnen 3 jaar mogelijk is.






