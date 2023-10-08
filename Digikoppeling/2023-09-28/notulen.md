# Technisch Overleg Digikoppeling

28 september 2023

## Aanwezigen

| Naam | Organisatie |
| --- | --- |
| Bijen, Antoon | Justid |
| Green, Alexander | Logius |
| Haasnoot, Peter | Logius |
| IJzermans, Jochem | UWV |
| Karl de Boer | Enable-U |
| Koster, Ronald | VNG |
| Mark Backer | VNG |
| Minnecré, Piet Hein | PBLQ |
| Pauw, Elzo | UWV |
| Reinhoud, Erwin | Kennisnet |
| Rutte, Laura | BKWI |
| Sander Fieten | Casquis |
| Sinnige, Hans | RINIS |
| Strijker, Mark | Kadaster |
| Van Gelderen, Edward | VNG |
| Van Kester, Jos | VNG |
| Vijlbrief, Tom | Kadaster |
| Voorn, Sebastian van | RDW |
| Wisse, Edwin | Logius |

## Notulen vorig TO

[TO Digikoppeling 22 juni 2023](https://github.com/Logius-standaarden/Overleg/blob/main/Digikoppeling/2023-06-22/Verslag.md)

## Mededelingen

### ADR 2.0

Peter Haasnoot: Van de standaard "API Design Rules" die bij het Kennisplatsform API's wordt ontwikkeld wordt momenteel versie 2.0 voorbereid. Deze zal binnenkort in consultatie gaan. De belangrijkste wijziging is de modulaire opbouw, waarbij de voorheen losse extensies nu in modules gegoten zijn om samenhang te bevorderen. Wanneer het door de benodigde gremia is goedgekeurd zal het Digikoppeling API profiel hierop worden aangepast.

### Vraag Kadaster: ebMS2-adapter

Kadaster is opzoek naar partijen met ervaring met de Clockwork ebMS-software. Alle inbreng wordt zeer op prijs gesteld en mag naar Tom Vijlbrief en/of Mark Strijker.

### Compliancevoorzieningen

Er is geen compliancevoorziening voor het Digikoppeling Rest-API koppelvlak zoals er voor ebMS2 is. Wel kunnen de regels uit de "API Design Rules" (core) getest worden op developer.overheid.nl. Veiligheidsregels zoals het gebruik van tweezijdig TLS kan echter nog niet getoetst worden. Een oproep aan de leden of er ontwikkelingen bekend zijn op dit gebied en of er behoefte is aan een volwaardige compliancevoorziening.

### Vraag RDW: Mandateringsregister

Sebastiaan van Voorn doet een oproep om ervaring uit de wisselen over de opzet en praktijkzaken rondom mandateringsregisters. Een groot aantal partijen sluit aan bij de RDW voor berichtenuitwisseling. Naast partijen die over een PKIO-certificaat beschikken zijn er ook veel tussenpartijen. We willen kijken welke partijen welke diensten gebruiken en welke tussenpartij zij daarvoor hebben en die willen wij dan gaan mandateren, daar zij vaak beschikking hebben over het PKIO-certificaat van de achterliggende partij.

### Consultatie eDelivery AS4 profile 2.0

Vanuit de EU is er het verzoek commentaar te leveren op eDelivery AS4 2.0 en SMP 2.0. Peppol wil in ieder geval niet overgaan naar AS4 2.0, omdat er een breaking change in zit. Dat is een punt van aandacht aangezien wij het voornemen hebben om met Digikoppeling richting eDelivery te gaan.

Sander Fieten meldt dat er gekozen is voor cryptografische algoritmen die niet breed ondersteund worden, waardoor deze missen in implementaties.

## eDelivery EBMS3/AS4 stakeholderonderzoek (PBLQ)

Piet Hein Minnecré geeft een presentatie over de impactanalyse die PBLQ uitvoert op de overgang van ebMS2 naar eDelivery (ebMS2/AS4). Resultaat wordt voor eind 2023 opgeleverd en omvat het volgende:

- Huidige situatie (aantal gebruikers, implementatie, leveranciers).
- De scenario's voor de overgangsperiode.
- Welke termijnen zijn haalbaar?

Vanwege het beperkte aantal interviews en het grote aantal partijen is gekozen om ook een enquête te houden onder de stakeholders. Hierin wordt gevraagd tegen welke knelpunten zij aanlopen en mocht dit vragen om verdere verdieping, dat staan er nog een aantal interviews gereserveerd.

De aanwezigen werd gevraagd naar suggesties voor partijen om te benaderen.

Tom Vijlbrief: Veel gemeenten hebben een koppeling niet in eigen beheer, maar via een leverancier. Zijn deze leveranciers binnen scope?

Piet Hein Minnecré: Deze hebben wij nadrukkelijk in beeld. Zowel de gespecialiseerde leveranciers als de leveranciers die wat breder gemeenten ondersteunen.

Mark Backer: Het is ook relevant naar gemeenten zelf te gaan. Vanuit de VNG hebben wij niet het complete beeld hoe het bij een gemeente uit gaat pakken. Kijk naar grote, middelgrote en kleine gemeenten zodat je daar meer divers in bent. Je moet ze misschien minder technische vragen stellen, maar meer organisatorisch.

Piet Hein Minnecré: Dat is zeker een beeld van de impact die wij willen bepalen. Het gaat niet alleen om de techniek.

Antoon Bijen: Ik verwacht eerlijk gezegd dat je het domein Justitie op de lijst hebt staan, want wij maken ook gebruik van ebMS.

Piet Hein Minnecré: Wij hebben jullie zeker op de lijst staan. Ben jij ook de geijkte persoon om het gesprek mee te voeren?

Antoon Bijen: In eerste instantie wel. We kunnen altijd kijken wie er bij aan kan haken.

### Opmerking Enable-U

Er is een bepaalde infrastructuur nodig voordat je kunt starten met grootschalig AS4-verkeer, bijvoorbeeld een gezamenlijke registry of een registry per intermediair; Het hele mandateringsproces eigenlijk waar we het ook over hadden In het kader van de FSC-standaard. Er moeten keuzes in gemaakt worden.

### Vraag use-case eDelivery

In de programmeringstafel staat bij VNG en RINIS een actiepunt om een eDelivery use-case uit te werken. Vraag aan het TO of zij ook inbreng hebben in de mogelijkheden van eDelivery.

## Wijzigingen

### Aanpassing beheermodel Digikoppeling

De MIDO-structuur is in het beheermodel aangebracht. Boven het TO is een tactisch overleg (de programmeringstafels) en dan is er de programmeringsraad. We hebben het voorstel zelf langs de tafels, de raad en afgelopen week ook langs het OBDO gestuurd. De uitkomst is dat het ODBO ook akkoord is gegaan met de nieuwe governance, die de beslissingsbevoegdheid voor deel van de de Logius standaarden heeft gedelegeerd naar de programmeringsraad.

### Digikoppeling baseren op ebMS3

De volgende stap is de reeds genoemde stakeholderonderzoek.

### RSIN of KVK-nummer leidend voor OIN?

We hadden in de documentatie staan dat RSIN de voorkeur heeft voor het genereren van een OIN. Er stond zelfs dat wanneer een organisatie eerst allen een KVK-nummer heeft en daarna een RSIN krijgt het OIN moet worden aangepast. Om praktische redenen hebben we dit aangepast, omdat het veranderen van een OIN een geweldige impact heeft met een erg kleine meerwaarde. De forumlering is aangepast dat een bestaand OIN niet aangepast wordt. Daarnaast is opgenomen dat de voorkeur gaat naar het baseren op KVK-nummer. Wanneer een organisatie met zowel een KVK-nummer als RSIN heeft bij aanvraag van een OIN zal het gebaseerd worden op het KVK-nummer. De reden is onder meer dat in de praktijk reeds zo te werk ging in het uitdelen van OIN's bij Logius. We hebben de documentatie dus in lijn gebracht met de praktijk en we hebben verwarrende punten verwijderd.

_Wijziging geaccepteerd door TO_

### Sub-OIN-beheerder

Naar aanleiding van een vraag of een sub-OIN-beheerder ook sub-OIN's mag uitdelen voor andere organisaties is er een wijziging om verwarring weg te nemen. Een kleine verscherping in de documentatie is om expliciet aan te geven dat een sub-OIN onder het hoofd-OIN van een sub-OIN-beheerder wordt aangemaakt.

_Wijziging geaccepteerd door TO_

## Overige punten

### Signing & Encryptie toevoegen aan RESTful API profiel

Enige tijd geleden is een vergelijking gemaakt tussen JAdES en httpbis-message-signatures. De vergelijking wordt steeds bijgehouden, want de ontwikkelingen gaan vrij stug door. In de internationale standaard httpbis verschijnen bijvoorbeeld regelmatig updates. Versie 19 van deze standaard gaat binnenkort van draft naar formeel vastgesteld binnen de IETF. In een pilot van een API-profiel in eDelivery is JadES uitgewerkt en het resultaat is één-op-één toegepast in een concept module.

Er ligt een keuze tussen twee standaarden of mogelijk een combinatie. Naar verwachting zal dit verder in de Werkgroep Beveiliging besproken worden. Oproep aan leden met ontwikkelingen in eigen organisatie die signing raken om deel te nemen aan de werkgroep.

Tom Vijlbrief: Wij gebruiken allerlei AdES-standaarden (XAdES, PadES), maar nog geen JAdES.

Elze Pauw: Binnen UWV gebruiken wij nog geen JAdES, maar gaan wij nu wel een proof-of-concept opzetten. Gekeken wordt naar mogelijke beperkingen binnen onze API Gateway. Terugkoppeling volgt.

Karl de Boer: Geen ervaring met Jades, afhankelijk van het besluit zullen wij dit direct implementeren.

## Roadmap

Er is een aanpassing voorgesteld op de huidige roadmap waarin expliciet wordt aangegeven wat er in Q4 nog doorloopt. Encryptie zal naar verwachting doorlopen, omdat dit nog niet is uitgekristalliseerd in een concreet profiel. Het verkennen van mogelijk gebruik ebMS3/AS4 gaat nu over in het eerder genoemde stakeholderonderzoek. Er staat ook een concept voor de roadmaps 2024-2025. Het verzoek is hier commentaar op aanvullingen op te geven. De volgende roadmap zal begin 2024 door het TO definitief worden vastgesteld.

## Stand van zaken FSC

Edward van Gelderen deelt de volgende punten over de voortgang rond Digikoppeling voor API's en FSC:

>- De referentie implementatie ter versnelling van de adoptie is gereleased
>- Iedere donderdag met een team van RINIS en Logius een stavaza gesprek
>  - Veel gesprekken op diverse tafels
>  - Kadaster delegatie beproeving
>  - Diverse gemeentelijke beproevingen
>  - Via RINIS straks beproevingen met de leden van RINIS
>- Gesprekken met de beveilingswerkgroep van het Kenniscentrum voor API's:
>  - FAPI (Financiële standaard/afspraken)
>    - is vooral voor eindgebruikers
>  - OpenIDConnect
>    - is vooral voor eindgebruikers
>  - Dynamic Client Registration
>    - niet van toepassing want we hebben geen onbekende clients
>  - RFC 8693 Token Exchange
>    - wij gebruiken certificaten voor identiteit. Wel kunnen we wat veldnamen in de token gelijktrekken voor herkenbaarheid
>  - NL GOV Assurance profile for OAuth 2.0
>    - wij gebruiken de client credential flow en zijn daar compliant aan, maar in het profiel wordt nu alleen over identiteit via tokens gesproken en we zijn in gesprek om daar identiteit via certificaten aan toe te voegen.
>  - NL GOV Assurance Profile for OIDC
>    - ligt bij de implementerende organisatie, niet bij de standaard en niet bij de referentie implementatie

Op woensdagen is om de week een sprint review wat gericht is op de functionele kant. Op de andere woensdagen is een inloopuurtje dat gericht is op de techniek.

## OIN-stelselontwikkelingen

Voor het OIN-stelsel is een onderzoek geweest vanuit de VKA. Het beheerteam onderneemt een aantal zaken op het gebied van datakwaliteit. Uit het onderzoek kwam ook de gewenste samenhang met bronregisters voor identiteit van organisaties. Metadata van organisaties in het OIN-registers dient de vorm aan te nemen van links naar de bronregisters waar de actuele gegevens te vinden zijn.

Verder zien we dat OIN ook gebruikt wordt in andere contexten dan enkel Digikoppeling, namelijk in PKIO, eHerkenning en PEPPOL eDelivery.

Een recente ontwikkeling is dat er bij Single Digital Gateway ook OIN's gebruikt gaan worden.

## Rondvraag

### Toepassing van PKIO private root

Gevraagd werd of men problemen ervaart met de huidige private root variant van de PKIO. Geen problemen gemeld.

Karl de Boer: Tegenwoordig wel even de hobbel nemen en dan werkt het.

### API met meerdere autorisaties

Eenzelfde databron kan voor verschillende doelgroepen verschillende eisen aan autorisatie of identificatie stellen. Er is geen behoefte dit in verdiepende sessies verder te behandelen, omdat dit als implementatiespecifiek wordt beschouwd waardoor een generieke oplossing niet interessant is. Deelnemers geven aan onderscheid aan te maken aan de voorkant, waarbij de achterliggende business logica gelijk blijft.
