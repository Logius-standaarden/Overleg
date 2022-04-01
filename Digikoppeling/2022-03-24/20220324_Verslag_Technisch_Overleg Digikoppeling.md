# Verslag Technisch Overleg 24-03-2022

Aanwezigen
==========

| Achternaam| Voornaam| Organisatie|
| --- | --- | --- |
| Backer | Mark | VNG |
| Bijen | Antoon | Justid |
| Fieten | Sander | Chasquis Consulting |
| Green | Alexander | Logius |
| Groot Roessink | Gerald | DUO |
| Haasnoot | Peter | Logius |
| IJzermans | Jochem | UWV |
| Kuiper | Erwin | Dictu |
| Nicolaij | Heymen | PinkRoccade |
| R | Erwin | Kennisnet |
| Rutte | Laura | BKWI |
| Sinnige | Hans | Rinis |
| Terpstra | Frank | Geonovum |
| van der Plas | Martin | Logius |
| van der Velde | Johan | RDW |
| Vijlbrief | Tom | Kadaster |
| Wisse | Edwin | Logius |
| Zwaan | Tonkie | BKWI |

Mededelingen
============

*Peter Haasnoot*

> Is er animo om het Technisch Overleg in hybride vorm te ervaren?

Enquête komt.

Verslag vorig TO
================

*Peter Haasnoot*

Geen bezwaren vanuit aanwezigen.

Toelichting Beheer
==================

*Edwin Wisse*

> In het kader van de nieuwe governance willen we het proces van wijzigingsvoorstellen standaardiseren. We accepteren wijzigingsverzoeken als GitHub issues. We labellen issues om scope, status en te agenderen overleg aan te geven.

Zien jullie dit als een goede manier van werken?

**Van der Velden:** Goede vooruitgang

*Verdere toelichting en demo door Edwin*

**Groot Roessink:** Goede aanpak. Denk dat deze manier misschien wel bij de community groeit.

**Wisse:** Openheid is belangrijk. De standaardisatie moet meer aandacht krijgen bij de programmeringstafels.

**Vijlbrief:** Lijkt mij ook een prima werkwijze!

**Fieten:** Eens, lijkt mij ook een goede manier van werken. Door het open te hebben op GitHub is voor iedereen de status van de issue duidelijk.

**Sinnige:** Ziet er goed uit!

**IJzermans:** Eens, goede insteek en vastlegging.

Toelichting komende release
===========================

*Peter Haasnoot*

> Doel is maandag na het OBDO deze set van documentatie te publiceren. verleent het TO hieraan goedkeuring?

Besluit : TO gaat akkoord

Roadmap
=======

Besluit : TO gaat akkoord met de roadmap

StvZ lopende roadmap items
==========================

Digikoppeling governance
------------------------

*Edwin Wisse*

Toelichting beheerproces aan de hand van schema

**Groot Roessink:** Hoe is DUO aangehaakt op de programmeringstafels? **Aandachtspunt**

**Zwaan: Kan er een overzicht van de huidige vertegenwoordiging gemaakt/gedeeld worden?**

**Actiepunt: overzicht van de huidige vertegenwoordiging**

Informatievoorziening
---------------------

*Edwin Wisse*

> We streven naar een vereenvoudiging van onze informatievoorziening.

Signing & Encryptie toevoegen aan RESTful API profiel
-----------------------------------------------------

*Peter Haasnoot*

> *Wie past Signing / XAdES toe?*

**Vijlbrief:** gebruiken wij bij het notariaat

**Groot Roessink:** XSADes wordt toepgepast bij uitgave diploma's in internationaal context via POST.

**Van der Velde:** ook een post van xml met signing. Prima om voor te stellen dat het ook JSON (JAdES) wordt.

**Terpstra:** ik mis altijd de optie om bij JSON een deel van de payload te signen. Wat gebruiken anderen? Is signing enkel over hele payload? Signing altijd in root voor interoperabiliteit daar het uitvissen van de signature anders maatwerk per toepassing vergt. HMAC is ook relevant.

**Van der Velde:** Gebruiken nu intern HMAC maar willen daar vanaf.

**Van der Plas:**  JOSE framework gebruikt JWT.

**Vijlbrief:** we hebben ook dossiers met een overzicht van de files in het dossier en de hashes. Dit overzicht wordt dan weer gesigned.

**Haasnoot:** Wie heeft er interesse in deelname van de werkgroep Security?

**Groot Roessink:** Ook verified credentials zijn een middel om handtekeningen te zetten.

**Actiepunt: Nagaan verifiable claims ontwikkeling van W3C bij ICTU**

**Actiepunt: Groot Roessink en Vijlfbrief uitnodigen voor de werkgroep Security, ze regelen een vertegenwoordiging vanuit hun organisatie.**

WUS / MTOM
----------

> Voorbeeldberichten van DataPower zijn onderzocht. Aanpassingen op de WUS-standaard om de interoperabiliteit te vergroten zouden grote impact hebben op bestaande implementaties die gebruik maken van andere platformen.

**Nicolaij:** Graag de standaard leidend laten zijn.

**Groot Roessink:** Hebben we beeld wie wat gebruikt?

**Haasnoot:** Daar hebben we geen complete lijst van. Wie gebruikt wat?

**Van der Velde:** Vooral WCF - WCF lijkt wel een beetje EOL - gebrek aan verdere kennis en inzicht. Zal navragen wat de impact is.

**Fieten:** Vragen over de volgorde van toepassing van MTOM en WS Security.

**Toezegging: stukken van het TO ook in Github opnemen en issues aanmaken**\
**Vraag Martin P :  bij wie speelt dit issue, wat gaat er mis als we niets doen? > de vraag speelt niet bij de TO leden. dit is vooral bij DataPower (IBM) implementaties een issue.**

ReSpec
------

**Green:** toelichting en oproep om Respec te hergebruiken

ebMS3
-----

*Edwin Wisse*

> Digikoppeling maakt gebruik van ebMS2. Deze standaard is verouderd en wordt niet meer verder ontwikkeld. De vervangende standaard ebMS3 is vereenvoudigd en wordt ook in de Europese eDelivery standaard toegepast (dwz in het profiel ebMS3/AS4).

**Wisse:** Inzicht op basis van de WG bijeenkomst die is gehouden; Technisch genoeg redenen om dit te willen. Veel voordelen en argumenten om dit te implementeren.

**Backer:** Kijk niet naar volume maar naar aantal koppelvlakken. Gemeenten moeten de keuze hebben. ebMS3 mag er naast maar het moet mogelijk zijn naar REST toe te bewegen conform de wens van de Gemeenten.

**Groot Roessink:** het probleem ligt niet bij de basisregistraties maar bij Gemeenten.

> De Europese eDelivery standaard is gebaseerd op ebMS3/AS4. Voor Europees berichtenverkeer wordt de eDelivery standaard gebruikt.

**Groot Roessink:** *Four corner* betekent: aansluiten aan de grens via nationale access points. In principe moet je internationale uitwisseling met je nationale protocol doen. Dus meerwaarde van aansluiten op internationaal is er niet voor Nederlandse partijen.

**Terpstra:** Breder uitzetten via GitHub. Landelijke voorzieningen benaderen over de vraag of we moeten migreren? Is er draagvlak?

Dus uitvraag vóór de programmeringstafel? Omgevingsloket, welke landelijke voorzieningen gebruiken ebMS2 en zouden over moeten? Het is maar een heel klein deel van het dataverkeer.

In welke ketens zit het ebMS verkeer? Is daar draagvlak? Justitie (Antoon) is de grote gebruiker.

Impact komt echter voort uit het aantal koppelvlakken, niet uit het verkeer via die koppelingen. Landelijke registraties zouden de keuze moeten bieden. Er is nu een alternatief in de standaard, maar nog niet overal in de implementaties. Bijvoorbeeld: BAG gebruikt een SOAP koppeling. Gemeenten krijgen een rekening van de softwareleveranciers. Aantal koppelingen is groot.

**Backer: Voorkeur: rek het zo lang mogelijk zodat gemeenten over kunnen naar REST APIs?**

**Vraag aan de tafel: welke strategie willen we? EbMS2 rekken zodat je over kan naar REST APIs? Of over naar een nieuwe ebMS3 versie? Willen basisregistraties meerdere protocollen naast elkaar?**

**Fieten:** Migreren naar API's kost ook inspanning, je mist in API's functies die al wel in ebMS 3 zitten. 

**Backer:** Bij gemeenten: het loopt via REST, ebMS2-hopje als moetje en dan weer verder via REST API.

**Conclusie: Leg de strategische vraag neer bij de programmeringstafels op een hoger niveau**\
**(de geld en tijd kwestie is minder relevant want niets doen is geen optie en iedere verandering kost tijd en geld)**
