<!-----------------------------







   :warning: Dit bestand wordt automatisch gegenereerd.
   :warning: Handmatige toevoegingen worden overschreven.







----------------------------->
# Technisch Overleg Digikoppeling

woensdag 6 maart 2024

## Agenda

|  |   |
|------------------------|-------------------------------------| 
| Betreft  | **Technisch Overleg Digikoppeling** |
| Vergaderdatum en -tijd | 06-03-2024 - 10:00-14:00 uur  |
| Vergaderplaats  | Beatrix gebouw - Jaarbeursplein 6 - Utrecht - |


| Tijd | Onderwerp |Spreker|
| --- | --- | --- |
| 10:00 | Inloop        | 
| 10:15 | Welkom & Mededelingen        |    Peter Haasnoot |
| 10:20 | Wijzigingsvoorstel FSC : [Federated Service Connectivity](https://github.com/Logius-standaarden/Digikoppeling-Koppelvlakstandaard-REST-API/issues/26) (presentatie)] |Edward van Gelderen, Ronald Koster |
| 10:50 | Wijzigingsvoorstel FSC : Federated Service Connectivity (discussie) | Martin van der Plas |
| 11:45 | Wijzigingsvoorstel FSC : Advies TO aan Programmeringstafel GU t.a.v. FSC|Allen| 
| 12:00 | Lunch|
| 12:45 | eDelivery ebMS3 Wijzigingsvoorstel JustID impactanalyse- | Raymond Kers , Antoon Bijen | 
| 13:30 | [Roadmap 2024-2025](https://github.com/Logius-standaarden/Digikoppeling-Algemeen/blob/roadmap_2024-2026/Digikoppeling_Roadmap_2024_2025.md#tijdlijn-roadmap-digikoppeling-standaarden) |Peter Haasnoot|
| 13:45 | Rondvraag / Afsluiting |
| 14:00 | Einde |

## Onderwerpen

### Grote wijzigingen
* Digikoppeling-Koppelvlakstandaard-REST-API [issue #26] [Federatieve Service Connectiviteit opnemen in het Digikoppeling voor REST API's profiel](https://github.com/Logius-standaarden/Digikoppeling-Koppelvlakstandaard-REST-API/issues/26) (18 december 2023), _Status: In onderzoek_
  * [Wijzigingsvoorstel](https://github.com//Logius-standaarden/Digikoppeling-Koppelvlakstandaard-REST-API/pull/27/files)
* Digikoppeling-Koppelvlakstandaard-ebMS2 [issue #6] [Digikoppeling baseren op ebMS3](https://github.com/Logius-standaarden/Digikoppeling-Koppelvlakstandaard-ebMS2/issues/6) (3 februari 2022), _Status: In onderzoek_

### Overige punten
* Digikoppeling-Koppelvlakstandaard-REST-API [issue #11] [Signing & Encryptie toevoegen aan RESTful API profiel](https://github.com/Logius-standaarden/Digikoppeling-Koppelvlakstandaard-REST-API/issues/11) (1 april 2022), _Status: In onderzoek_

## Toelichting



### Mededelingen

- ADR versie 2.0 met modulaire opbouw en opname van modules Geo en Transport security wordt in het MIDO behandeld voor vaststelling. Het Digikoppeling REST API profiel zal worden aangepast voor aansluiting op de nieuwe versie
- Digipoort is onderzoek en voorbereiding aan het doen naar toepassing van APIs binnen de Digipoort koppelvlakken op basis van eDelivery REST.

### Toelichting bij Overige Punten

#### Signing & Encryptie toevoegen aan RESTful API profiel 

Werkgroep ADR Beveiliging (specifiek sub-werkgroep signing) heeft een vergelijking gemaakt van 2 standaarden voor signing van REST-API's :
[Vergelijking REST API Signing Standaarden](https://geonovum.github.io/KP-APIs/publicaties/REST_API_Signing_Standaarden) 

Laatste ontwikkelingen:
* De internationale standaard [httpbis-message-signatures](https://datatracker.ietf.org/doc/rfc9421/) is gepubliceerd vanuit IETF als Proposed Standard (per Feb 2024) als rfc9421
* Er is een concept ADR module voor JAdES gemaakt gebaseerd op het eDelivery API profiel : 
Zie : [KP-APIs/API-strategie-modules/signing-jades/](https://geonovum.github.io/KP-APIs/API-strategie-modules/signing-jades/)

* Er is een concept ADR module voor encryptie gemaakt (gebaseerd op JWE) :
Zie : [KP-APIs/API-strategie-modules/encryption/](https://geonovum.github.io/KP-APIs/API-strategie-modules/encryption/)

Deze modules zijn toegevoegd aan de lijst optionele modules van de ADR van het Kennisplatform API's voor verdere uitwerking.
In het Digikoppeling REST-API profiel zullen deze modules gebruikt worden icm met verdere profilering. 

_Vraag aan het TO : zijn er op dit gebied ontwikkelingen binnen de eigen organisatie?_


### eDelivery EBMS3/AS4 stakeholderonderzoek en EU nieuws

PBLQ heeft een update van hun eindrapport opgeleverd met de input van JenV/Justid. _Zie Rapport [Impactanalyse modernisering Digikoppeling ebMS - van ebMS2 naar eDelivery, v1.1](https://github.com/Logius-standaarden/Overleg/blob/main/Digikoppeling/2024-03-06/Rapport%20Impactanalyse%20modernisering%20Digikoppeling%20ebMS%20-%20v1.1%20definitief%2019%20januari%202024.pdf). Logius heeft ontwikkelingen afgestemd met het EU eDelivery team.

Het EU eDelivery team heeft een update gegeven over de [AS4 en SMP 2.0 profielen](https://ec.europa.eu/digital-building-blocks/sites/pages/viewpage.action?pageId=711492329). Onder meer over de consultatie van 2023, TO lid Sander Fieten heeft op beiden een reactie gegeven. Verder heeft de EU een [_Adoption timeline for eDelivery AS4 and SMP 2.0 profiles_](https://ec.europa.eu/digital-building-blocks/sites/pages/viewpage.action?pageId=708411562) gepubliceerd.

### Definitieve Roadmap 2024-2025 
https://github.com/Logius-standaarden/Digikoppeling-Algemeen/blob/roadmap_2024-2026/Digikoppeling_Roadmap_2024_2025.md

_Verzoek aan het TO is akoord te geven op de definitieve roadmap , de roadmap zal vervolgens in de MIDO programmeringstafel Gegevensuitwisseling worden vastgesteld__
