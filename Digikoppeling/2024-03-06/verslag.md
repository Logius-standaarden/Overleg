# Verslag Technisch Overleg Digikoppeling

Woensdag 6 maart 2024

### Aanwezig

(32 personen) Peter Haasnoot (Logius)(vz), Sjaak Derksen (TNO), Han Welmer (TNO), Raymond Kers (JenV), Antoon Bijen (JustID), Heymen Nicolaij (PinkRoccade), Edward van Gelderen (VNG), Ronald Koster (VNG), Johan van der Velde (RDW), Karl de Boer (Enable-U), Herman Willemsen (Enable-U), Tom Vijlbrief (Kadaster), Tonkie Zwaan (BKWI), Frank Terpstra (Geonovum), Niels Dequeker (VNG), Pim Gaermers (VNG), Ivo Lodewijks (Sigmax), Erwin Kuiper (Dictu), Hans Sinnige (Rinis), Maarten Coemans (SNG), Ronny Kennis (BKWI), Bob te Riele ((RVIG), Jochem IJzermans (UWV), Erwin Reinhoud (Kennisnet), Gerald Groot Roessink (DUO), Adjay Narain (Min IenW), Mark Backer (VNG), Henk van Maanen (VNG), Martin van der Plas (Logius), Edwin Wisse (Logius), Alexander Green (Logius), Lizzy Wellink (secretaris)(Logius). 

### Afwezig (Met Berichtgeving)

Anja Geenen (UWV), S. van Voorn (RDW), Lana Vredenduin (Enable-U)(i.v.m. verlof), Ivar Wennekes (ICTU)(verzoek tot afhalen van de genodigdenlijst),

## Opening & Mededelingen (Vz)

Hartelijk welkom namens de voorzitter Peter Haasnoot - Logius Standaarden, op het live Technisch Overleg Digikoppeling te Utrecht. We nemen kort de agenda door, een tweetal onderwerpen zullen het grootste deel van de dag bepalen: het wijzigingsvoorstel FSC (Edward van Gelderen, Ronald Koster (VNG)) voor de pauze en eDelivery ebMS3 Wijzigingsvoorstel JustID (Raymond Kers, Antoon Bijen (JenV)) na de pauze. We sluiten af met de Roadmap en accordering daarop.

### Mededelingen

- Besluit tot vaststelling nieuw versie API Design Rules 2.0. is in de MIDO 
Programmeringstafel d.d. 14-2-24 goedgekeurd en gaat door naar het MIDO Programmeringsraad. Vervolgens zal deze worden ingediend voor opname op de PTLU (Pas toe-Leg uit) lijst van het Forum Standaardisatie.

- Digipoort is onderzoek en voorbereiding aan het doen naar toepassing van APIs binnen de Digipoort koppelvlakken op basis van eDelivery REST, cloudevents en S3 voor grote berichten. 

- Doel van dit overleg: Technisch Overleg is de plek waar wijzigingsvoorstellen worden geaccordeerd alvorens deze doorgang vinden naar het MIDO.

## Presentatie Wijzigingsvoorstel Fsc (Federatieve Service Connectivity) Door VNG (Edward Van Gelderen, Ronald Koster)

Edward van Gelderen (EvG) meldt dat de wijzigingsinformatie van de VNG vooraf op Github gepubliceerd is ter voorbereiding en dus vindbaar tevens als naslag.

EvG start met de voorgeschiedenis, van Common Ground (hervorming van de gemeentelijke informatievoorziening) in Haarlem, waaruit bleek dat 80% van de problemen met burgers en bedrijven gebaseerd is op verkeerd geraadpleegde data door kopieën van de bron, naar de vergemakkelijking van de koppeling middels in eerste instantie NLX software. Maar de adoptie liep traag en daarop is de hulp van o.a. Gartner ingezet voor een objectivering over NLX. Op basis van de aanbevelingen van Gartner is besloten NLX voort te zetten in de vorm van een standaard op landelijk niveau. De naam is daarmee ook aangepast van NLX naar FSC, Digikoppeling voor APIs.

Ronald Koster (RK) neemt het inhoudelijke deel door en start met als twee organisaties informatie gaan uitwisselen waarbij identificering, PKIo-certifciaten en 'van peer' via een Directory 'naar peer' gecommuniceerd wordt er problemen ontstaan als het IP-adres wijzigt. Voorwaarde is dan dat een IP-adres stabiel zou moeten zijn en om dat voor elkaar te krijgen zou je het kunnen whitelisten op IP-adressen wat nu veel voorkomt. Hoe gaan we ervoor zorgen dat we dit loslaten en wel met APIs gaan werken?

Dan dus de beheersbaarheid met FSC vergroten, staat gelijk aan multual TLS (mTLS), dus de certificaten natrekken i.p.v. IP-adressen whitelisten. Over de poorten kun je afspraken maken en opnemen in contracten (Service Connection).

Door dus de beheersbaarheid met FSC te vergroten, de focus hierbij ligt op multual TLS (mTLS), dus de certificaten natrekken i.p.v. IP adressen whitelisten. Over de poorten kun je afspraken maken en opnemen in contracten (Service Connection).

Doordat het nu om een standaard gaat is het veel laagdrempeliger tegenover de eerder genoemde NLX software (verplichting). FSC kun je in je in de eigen API Gateway implementeren, met als voordelen dat partijen hun eigen software kunnen laten staan, adoptie makkelijker gaat als het REST APIs zijn geworden en je een log aanlegt waarna teruggekoppeld kan worden aan APIs. En anders is het opgenomen in de contracten (Service Connection) bijvoorbeeld in het geval dat een partij gedelegeerd mag opereren.

### Vragen van de TO-leden

- Vraag specifiek of de OESE 21 project procedures gevolgd zijn, die zijn namelijk wettelijk vastgesteld vanaf 12-12-2023? Zou gelijken op standaard project aanpak, o.a. middels een 2-wekelijkse review per sprint wordt er standaard gemonitord.

  In elk geval moet de conclusie zijn dat je meer impact hebt als je samen hetzelfde doet dan individueel het beste. En natuurlijk willen EvG en RK met de nuance besluiten waar een stuk begrip, positie en prioriteiten altijd per organisatie meegenomen wordt.

- Nog een vraag (A.B.) aangaande security, behalve interne API's ook die richting externe organisatie gebruikt worden? In principe biedt OAuth een oplossing, waarbij de identiteit in het certificaat opgenomen is.

- Laatste vraag (H.vM) Wat als je FSC verbinding legt, als outway gecomprimeerd is dan kun je identificatie in certificaten vinden of ingetrokken worden.

Mooie heldere presentatie wat een hoop inzicht gaf. Dank aan VNG - EvG en RK. 

## 3. Discussie FSC Digikoppeling in het TO om FSC te beoordelen (Martin Van Der Plas)

MvdP start met een vijftal slides, waarlangs de aanpak van de discussie verloopt. Waarbij als kader BOMOS wordt aangegeven en in de BOMOS groeicurevegrafiek wordt aangeduid dat FSC zich in de introductiefase (5 fasen grafiek) bevindt. Dan is de context verder dat vanaf de Digikoppeling implementatie in 2012 Digikoppeling een paraplu betreft voor meerdere standaarden. De wijziging ten aanzien van FSC die we vandaag bespreken valt binnen het REST-profiel. Het betreft hier niet de overige BOMOS blokken zoals strategie, financiën en communicatie, maar richt zich puur op het operationele stuk.

Insteek was om a.d.h.v. opgehaalde vragen en commentaren van de TO-leden op de wijziging, en na clustering toe te werken naar instemming met consensus van alle TOleden. Het doel was om live een advies op te stellen voor de MIDO programmeringstafel middels publieke consultatie dit advies te delen en gedragen door ieders eigen organisatie. Tevens zou de publieke consultatie periode worden gestart.

Alle commentaren/vragen van de TO-leden samengevat gingen over; zorg over tijd en impact, verplichting, use cases, authenticatie, netwerk, documentatie, directory, contracten, beheerlast, delegatie en nog een aantal overige vragen. De vragen vielen uiteen in een deel impact van implementatie en anderzijds techniek. Er is samengevat behoefte aan een implementatie/uitvoeringstoets of iets dergelijks. Er dient vastgesteld te worden dat enkele partijen misten zoals Belastingdienst en UWV.

_Actiepunt:_ Vanuit Logius wordt de opgehaalde informatie uitgewerkt en gedeeld op Github.

Met dank aan Martin/Peter voor de begeleiding en verzorging van deze discussie worden de belangrijkste punten genoteerd:
_Actiepunt:_ POC rechtendelegatie bij de BAG, rapport van Geonovum, wordt ter lering gedeeld met TO-DK-leden.

_Besluit:_ N.a.v. de gevoerde discussie is afgesproken om er eerst met deze groep uit te komen voordat er een publieke consultatie wordt gedaan. Dit o.a. om (onnodige) onrust in buitenwereld (en eigen domein) te voorkomen en om eerst met eigen achterban (J&V) en deze TO groep te komen tot een beter beeld wat betreft implementatie impact. Eind april inventarisatie klaar van eenieder, daarna nog een maand tijd om een advies met eventueel toelichting voor te bereiden voor volgend TO-Digikoppeling d.d. 29 mei. (nl/bv, beoordeling functionaliteit, wat is nodig , beeld van de tijdlijnen / beeld van implementatie impact). 

_Actiepunt:_ VNG zal t.b.v. toegankelijkheid voor ontwikkelaars de GitLab omgeving bijwerken (documentatie, referenties, auditable, etc).

_Opmerking:_ Voorkeur om aantal directories te beperken verbetervoorstel vs. vanwege open standaard de hoeveelheid directories openlaten.

## Presentatie eDselivery ebMS3 Wijzigingsvoorstel JustID impactanalyse (Raymond Kers, Antoon Bijen - Jenv)

Ter introductie van deze presentatie verwijst Edwin Wisse naar het rapport door PBLQ gepresenteerd en de aangepaste versie ervan zal gepubliceerd worden op Github. Het gaat hier om de overgang naar eDelivery (waar vanuit Europa op aangestuurd wordt). Daarnaast zijn ook vragen door Sander Fieten eerder gesteld op Github en is er genoeg aanleiding om dit met elkaar te bespreken.

Raymond Kers, domeinhouder op gegevensuitwisseling IT JenV, noemt vooral dat het om het grootste ministerie gaat. De schets van de grootte van het ministerie, 60+ diensten, agentschappen, zelfstandige bestuursorganen, 2-3 ministers, onderschrijft de complexiteit in besluitvorming die dat met zich meebrengt.

De Justitie Berichten Service (JUBES) faciliteert 40 miljoen berichten per jaar om maar een idee te geven.

Antoon Bijen, gemeenschappelijke diensten, beheerder JustID, begint met te zeggen dat het ebMS2 bolwerk standaard verouderd is en dat Justitie voor een beslispunt staat om in de toekomst te investeren, daarmee rekening houdend met de Europese ontwikkelingen op eDelivery, Peppol (gebruikt SML/SMP), etc. Maar bij het opvolgen van de Europese verordeningen die elkaar snel opvolgen zal het een uitdaging zijn.

De ketens van JenV behelzen de Strafrecht-, Migratie-, Jeugd- en Europese keten en gaat om 1 miljard berichten per jaar intern.

In de keten van de JenV organisatie zijn tal van API initiatieven nu als oplossing geboden. Parallel aan alle eerder genoemde zijn de eerder genoemde Europese wensen eDelivery, eCodex ontwikkeling en zit JenV in een impactanalyse om hier overwegingen in te maken. Samenvattend gaat het om CPA's aanmaken, ebMS onderhoud, ebMS3 onderzoek, API's als oplossingen.

Dank aan Min JenV, Raymond Kers en Antoon Bijen.

## Roadmap 2024-2025

Peter Haasnoot, coördinator van het GU team Logius Standaarden, presenteert de Roadmap 2024-2025 en vraagt om op- of aanmerkingen, en bij geen verder commentaar is er een akkoord op de Roadmap zoals gepresenteerd.

## Rondvraag

- Verzoek tot twee maal per jaar een 'live' Technisch Overleg wordt gehonoreerd, de volgende zal medio september 2024 zijn.

- Aandacht gevraagd voor Graphql apis als onderwerp. De vraag is naar een concrete use case, dan kan er een werkgroep gestart worden en kan er vervolg aan gegeven worden.

Sluiting vergadering om 14:00 uur

Volgende TO-Digikoppeling is online op 29 mei a.s. van 10:30-12:00 uur 

## Actielijst

| Nr     | Actie                                                                                                                          | Naam           | O/G |
|--------|--------------------------------------------------------------------------------------------------------------------------------|----------------|-----|
| 324/01 | Vanuit Logius wordt de opgehaalde informatie uitgewerkt en gedeeld op Github.                                                  | Martin vd Plas | G   |
| 324/02 | POC rechtendelegatie bij de BAG, rapport van Geonovum, wordt ter lering gedeeld met TO-DK leden                                | Frank Terpstra | O   |
| 324/03 | VNG zal t.b.v. toegankelijkheid voor ontwikkelaars de  GitLab omgeving bijwerken (documentatie, referenties,  auditable, etc). | VNG            | O   |

### Voorbereiding bespreking wijzigingsvoorstel FSC in TO Digikoppeling 29/5

| Nr | Data           | Actie                                                                                      | Voor                       |
|----|----------------|--------------------------------------------------------------------------------------------|----------------------------|
| 1  | Tot 30 April   | Beoordeling wijzigingsvoorstel FSC / impactanalyse                                         | Allen (per Organisatie)    |
| 2  | 30 April       | Uiterlijk 30 April resultaten delen met Logius Standaarden Beheer Digikoppeling Standaard. | Allen (per Organisatie)    |
| 3  | 1 Mei - 22 Mei | Samenvoegen en delen impactanalyses                                                        | Logius Standaarden  Beheer |
| 4  | 29 Mei         | Bespreken wijzigingsvoorstel FSC in TO Digikoppeling                                       | Allen                      |

FSC-inhoudelijke vragen over de technische werking kunnen direct worden voorgelegd aan team FSC

(Verzoek is ook om voorafgaand aan het volgend TO Digikoppeling alle vragen over de technische werking voor te leggen aan team FSC)

