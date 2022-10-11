# Verslag Technisch Overleg Digikoppeling

29 september 2022

## Aanwezigen

| Achternaam     | Voornaam  | Organisatie |
|----------------|-----------|-------------|
| Backer         | Mark      | VNG         |
| Bijen          | Antoon    | Justid      |
| De Boer        | Karl      | enable-u    |
| De Bruijn      | Rick      | Logius      |
| Green          | Alexander | Logius      |
| Groot Roessink | Gerald    | DUO         |
| Haasnoot       | Peter     | Logius      |
| IJzermans      | Jochem    | UWV         |
| Kuiper         | Erwin     | Dictu       |
| Reinhoud       | Erwin     | Kennisnet   |
| Sinnige        | Hans      | Rinis       |
| Van der Plas   | Martin    | Logius      |
| Van der Velde  | Johan     | RDW         |
| Vijlbrief      | Tom       | Kadaster    |
| Welmer         | Han       | TNO         |
| Wisse          | Edwin     | Logius      |


## Introductie

Haasnoot meldt dat er de volgende dag een bijeenkomst is van Kennisplatform API's.

Er zijn geen opmerkingen over het verslag van het vorig TO.

## Grote wijzigingen

### RFC: Toevoegen API-58 No sensitive information in URIs

Green presenteert de RFC waarin de verwijzing naar regel API-58 is opgenomen. Daarnaast wordt een voorstel getoond van een toelichting om POST te gebruiken voor bevragingen waarmee de query in de body wordt opgenomen in plaats van de URI. Gevraagd wordt of de TO-leden akkoord zijn.

Bijen: Afspraak naamgeving end-point om bevraging te onderscheiden van het aanmaken van een record?

Vijlbrief: Eens met de toevoeging.

Reinhoud: Jullie zorgen ook voor aansluiting Kennisplatform op dit punt?

Haasnoot: Wij zorgen voor afstemming en sync tussen Digikoppeling en het Kennisplatform API's.

De Boer: Akkoord

Groot Roessink: We zijn akkoord en verfijning kan later

Haasnoot: Hierbij deze RFC goedgekeurd voor verdere verwerking.

### Aanpassing beheermodel

Wisse toont Digikoppeling beheermodel ter review. Governancestructuur is herzien, maar loopt voor op praktijk.
Versienummering extra aandacht. Proberen SemVer te volgen. Commentaar is welkom.

Akkoord uit chat. GitHub blijft beschikbaar voor opmerkingen.

### Transitie ebMS3

Wisse: We hebben het punt ingebracht bij de programmeringstafel. punt splitsen in ebMS2 uitfaseren en ebMS3 infaseren.

De Boer: Bij het uitfaseren van ebMS2 dient AS4 wel alle functionaliteit te behouden.

Van der Plas: end-of-support is nog niet EOL.

Bijen: Alleen ebMS2 uitfaseren is niet de bedoeling; Je moet gefaseerd overgaan.

Martin: Toelichting uitfaseren is eerst end of support over x jaar en daarna end of life over y jaar.

De Boer: maak die jaren niet te lang anders gebeurt er niets.

Van der Plas: De besluiten over investeringen zijn een bestuurlijk vraagstuk en liggen niet bij ons. De kosten kunnen groot zijn voor organisaties.

De Boer: bij ons is ebMS3 al ingebouwd en kan zonder meerkosten worden gebruikt. ook conversie tussen ebMS2 en ebMS3 wordt gefaciliteerd.

## Kleine wijzigingen

### Best Practice Identificatie van Organisaties, Organisatieonderdelen en voorzieningen

Best practice is al in uitwerking. Te bespreken opmerking Gerald: kan handreiking uitgebreid worden tot best practice. 

### Analyse knelpunten Routering en Intermediairs in gegevensverkeer

Groot Roessink: Concrete casus waarbij we dit willen toepassen (onderwijs). Analyse bekeken, goed, maar ontbreekt conclusie/voorkeur. Optie 2 wordt gewisseld tussen eindverantwoordelijke geeft … aan SAAS-leverancier (sleutelbosprobleem). Vergeleken met Edukoppeling mist verzender. Bij WUS staat niet specifiek de verzender en ontvanger. Bij Edukoppeling doen we het allebei ook bij REST. From en To parameter wordt gebruikt bij Edukoppeling, bij Digikoppeling enkel ontvanger. Leek me handig te verwijzen naar dit concrete werkende voorbeeld.

Haasnoot: to staat vermeld in voorbeeld, maar mist inderdaad nog uit tekst.

Reinhoud: in Edukoppeling is onderwijscontext. Het zou beter zijn als je een BP hebt onafhankelijk van onderwijs. Voor zover prima.

### RSIN of Kvk nummer leidend voor OIN?

De Boer: maken zelf OIN op basis van KVK met prefix.

Groot Roessink: was RSIN niet bedoelt als vervanging van KvK-nummer?

Van der Plas: HR bedoelt voor handel in NL. RSIN is van Belastingdienst en BD is ook in internationale hoek.

Haasnoot: Overheidsorganisaties hebben niet allemaal een KvK-nummer.

## eDelivery ontwikkelingen

Wisse vertelt over het informal cooperation network eDelivery ([website](https://ec.europa.eu/digital-building-blocks/wikis/display/EDELCOMMUNITY/Project+deliverables)) met toelichting van Sinnige:

Het Informal Coorporation Network bestaat uit partijen die eDelivery toepassen of geïnteresseerd zijn. Superactieve groep dat sinds corona stil is gevallen. Recente herstart werd teruggekropen door EC. Er zijn lidstaten die het echt weer op de agenda willen hebben. Pik de dingen die zij goed doen bv signing profielen.

Haasnoot: Dit is gedeeld met de subwerkgroep Signing van kennisplatform API's

Groot Roessink: Fijn om te weten. in het onderwijs wordt hier ook naar gekeken. In de implementing act is het opzetten van Once Only Technical System (OOTS) gateway naar een sectoraal knooppunt benoemd. Een API-gerelateerde preview en consent wordt opgezet en dan is er daarna levering via AS4. De feitelijke protocol conversie is niet spannend.

Sinnige: ICN gaat hier niet over.

Backer: Meer kennisdeling zou op prijs gesteld worden bij volgend TO.

Groot Roessink: Voorstel om Ivar Vennekens? te vragen, de Architect van BNC - Bureau Nationaal Coordinator SDG
