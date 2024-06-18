### Achtergrond

Gemeenten hebben een nieuwe, moderne, gezamenlijke informatievoorziening nodig voor het uitwisselen van gegevens. Want het huidige stelsel voor gegevensuitwisseling maakt het lastig om snel en flexibel te vernieuwen, te voldoen aan privacywetgeving en efficiënt om te gaan met data. Dat staat de verbetering van de gemeentelijke dienstverlening in de weg.

Vanuit die behoefte is Common Ground ontstaan. In de kern gaat het Common Ground over de hervorming van de gemeentelijke informatievoorziening, door op een andere manier om te gaan met gegevens. Zo koppelen we data los van werkprocessen en applicaties. En we bevragen data bij de bron, in plaats van ze veelvuldig te kopiëren en op te slaan. Met de herinrichting van de informatievoorziening kunnen gemeenten hun dienstverlening en bedrijfsvoering ingrijpend verbeteren. Dat stelt ze in staat om op een moderne en flexibele manier in te spelen op maatschappelijke opgaven. Inmiddels is dat verankerd in de informatiekundige visie Common Ground.

Om het data bij de bron principe mogelijk te maken zijn er API's nodig. En door deze beweging richting API's ontstaan er vraagstukken die elke organisatie moet gaan beantwoorden. Zoals; Hoe maak ik een veilige verbinding met een API? hoe beheer ik deze verbindingen? hoe kan ik kenbaar maken dat ik een API aanbied? etc. Als we weten dat elke organisatie deze vragen moet gaan beantwoorden is het niet meer dan logisch om naar een oplossing te zoeken die door elke organisatie gebruikt kan worden zodat het wiel niet ontelbare malen opnieuw uitgevonden moet worden. 
Een mogelijke oplossing tot deze vraagstukken is software geworden met de naam NLX.

NLX, als landelijke integratie faciliteit (feitelijk gaat het over het connectiviteitsdeel – integratie is meer dan connectiviteit) is vanaf het prille begin integraal onderdeel van Common Ground geweest. Het is een van de functies in de derde laag in het Common Ground vijflagenmodel waarmee laagdrempelig toepassing en data gescheiden kan worden. Een oplossing als NLX, die gegevens van (overheids)organisaties verbindt, is nog niet beschikbaar. Geïnspireerd door het bewezen succes van de Estlandse X-Road besloot een aantal gemeenten om onderzoek te doen naar een X-Road voor Nederland. Vandaar NLX.

NLX ontwikkelde zich de afgelopen jaren bij VNG Realisatie door het in te zetten als validatie middel voor experimenten rondom uniforme connectiviteit. We richtten ons op de strategie van verplichte software voor gemeenten, haar ketenpartners en haar leveranciers. Het idee achter verplichte software was dat iedereen gemakkelijk bij zou kunnen dragen aan deze software. Hoe minder verschillende implementaties, hoe minder complex het landschap is en dus hoe wendbaarder (dit deel van) het landschap is. Hoewel veel verschillende organisaties beproevingen succesvol uitgevoerd hebben, bleef de echte adoptie in productie uit.

2022 - Objectiveringsonderzoek door Gartner

In 2022 heeft VNG Realisatie een objectiveringsonderzoek over NLX laten uitvoeren door Gartner. De onderzoeksvragen waren:

1. In hoeverre zijn een uitwissel- en integratiemechanisme benodigd voor de realisatie van de visie Common Ground? In welke mate is er behoefte bij gemeenten en andere overheidsinstellingen voor de voorgestelde standaardisatie?
2. Hoe kan de benodigde software het best beschikbaar worden gesteld voor succesvolle implementatie en kan er worden aangesloten op open standaarden en/of software oplossingen die in de markt beschikbaar zijn?
3. Wat zijn de implicaties voor succesvolle implementatie en welke handvatten zijn hierbij van belang?

Dit onderzoek leverde waardevolle inzichten op over waarom de adoptie van NLX achterbleef en heeft richting gegeven aan het connectiviteitsvraagstuk van Common Ground. De belangrijkste conclusies waren:
 
1. NLX als standaard is nodig; NLX als software is enkel nodig voor de API Directory en de test suite als onderdeel van de NLX standaard. Waar nog als sub conclusie genoemd wordt dat de beschikbaarheid van de referentie-implementatie (waarmee de NLX software bedoeld werd) een versnellend effect zal hebben op de adoptie van de standaard;
2. Communicatie over de NLX standaard moet worden toegesneden op de behoeften van de verschillende stakeholdergroepen;
3. Om de standaard bruikbaar te maken, moeten generieke en overheidsstandaarden verder gecontextualiseerd worden voor het Common Ground ecosysteem;

In het [volledige rapport](https://commonground.nl/file/download/6fef7d23-64d2-45f4-9ee8-403168e53897/gartner-objectivering-nlx-v1.pdf) is de redenatie terug te lezen samen met nog meer (deel) conclusies en aanbevelingen.
In de lijn van de conclusies van Gartner is het pad van verplichte software verlaten. Alle ervaringen en lessen van de afgelopen jaren zijn opgeschreven in de vorm van de standaard genaamd Federated Service Connectivity (FSC).

### Wat standaardiseert FSC

1. Hoe de identiteit van een organisatie wordt bepaald en vertrouwd.
3. Hoe een autorisatie om te mogen koppelen met een API gegeven, geweigerd of ontnomen wordt.
5. Hoe organisaties in een netwerk de API's, en elkaar kunnen vinden.
6. Hoe een verbinding naar een API veilig kan worden opgezet.
7. De inhoud van logregels  en wanneer deze moeten worden weggeschreven.
8. Hoe een intermediair namens een andere organisatie een API kan consumeren en/of publiceren.

### Waarom Digikoppeling

Digikoppeling standaardiseert de uitwisseling van gegevens (services) tussen (overheids)organisaties en heeft een profiel specifiek voor (REST) API’s. Hierin wordt het gebruik voorgeschreven van de API Design Rules, mTLS, PKIO en OINs. Het volgen van Digikoppeling is een stap naar technische interoperabiliteit. Met technische interoperabiliteit wordt het verschijnsel bedoeld dat organisaties op technisch niveau samen kunnen werken op een voorspelbare manier waardoor deze samenwerking ondersteund wordt door geautomatiseerde processen. Als twee organisaties data gaan uitwisselen via APIs zijn er geen discussies nodig over welke netwerk protocollen en poorten gebruikt worden, hoe de autorisatie is geregeld etc. Deze discussies zijn tijdrovend, duur en kunnen bij gebrek aan kennis leiden tot onveilige data uitwisseling. Het is maatwerk en daardoor draagt het bij aan de inflexibiliteit van de informatieketens van organisaties. De experimenten binnen het VNG programma Common Ground rondom gegevensuitwisseling en hoe dat bijdraagt aan technische interoperabiliteit hebben uitgewezen dat verdergaande standaardisatie nodig is om stappen te zetten richting technische interoperabiliteit. Deze lessen zijn opgeschreven in de FSC standaard en beschrijven specifieke keuzen hoe management en dataverkeer van API’s georganiseerd zou kunnen worden. FSC bevat een beschrijving (de standaard), een testsuite, een directory en een implementatie (tbv het testen van de standaard, het demonstreren van de standaard en ter versnelling van de adoptie).  Het adopteren van FSC in Digikoppeling zorgt voor diepere en bredere uniformering rondom connectiviteit en daarmee grotere stappen richting technische interoperabiliteit. 

### Wat voegt FSC toe aan Digikoppeling

1. Een directory waarin API's gepubliceerd en gevonden kunnen worden.
2. Toegang tot een API beheren middels digitale contracten.
3. Uniforme logging rondom verzoeken aan een API. 
4. Delegatie. I.e. hoe een organisatie namens een andere organisatie mag handelen.
 
Links naar de FSC standaard en extensies:

- [Core (de basis)](https://commonground.gitlab.io/standards/fsc/core/draft-fsc-core-00.html)
- [Logging](https://commonground.gitlab.io/standards/fsc/logging/draft-fsc-logging-00.html)

[Pull request voor de wijziging aan het profiel Digikoppeling voor REST API's](https://github.com/Logius-standaarden/Digikoppeling-Koppelvlakstandaard-REST-API/pull/27) 

### Verplichtingskader

Technische interoperabiliteit is gebaat bij de adoptie van een werkwijze door de massa. De behoefte voor individuele (maatwerk) oplossingen bij het uitwisselen van informatie neemt af onder invloed van het aantal organisaties wat eenzelfde werkwijze hanteert. De toegevoegde waarde van een standaard werkwijze neemt toe met het aantal organisaties wat deze adopteert. In dat kader valt te beargumenteren dat de toevoeging van FSC (en in de toekomst andere standaard werkwijzen in de scope van het Federatieve Data Stelsel) zo verplichtend mogelijk vastgesteld zou moeten worden. Dit zou via een wettelijk kader kunnen of via een streefbeeldafspraak. Er zit echter ook een keerzijde aan het zo verplichtend mogelijk maken van een standaard: het dwingt organisaties vanaf het eerste moment in een transitie, die hoogstwaarschijnlijk voor het overgrote merendeel van de organisaties niet goed past bij de staande prioriteiten. Dat roept weerstand op en is daardoor contraproductief. Waarschijnlijk heeft een ‘pas toe of leg uit’ verplichting aan het begin van de adoptie van een standaard de grootste kans om deze goed te ondersteunen. De eerste organisaties / informatieketens die toch al in een transitie zitten, kunnen de early adopters zijn op basis van een intrinsieke motivatie om haar connectiviteit te moderniseren. Vanuit die early adopters breidt de adoptie dan als een olievlek uit. Organisaties voor wie het moment van vaststellen door staande prioriteiten niet logisch is om direct te veranderen, hebben de mogelijkheid om de adoptie te starten op een moment wat past. In de toekomst zou het verplichtingskader wellicht verhoogt kunnen worden om redenen die dan ondersteunend zijn aan de adoptie.

### Naam

Ronald Koster

### Email

ronald.koster@vng.nl

### Organisatie

VNG
