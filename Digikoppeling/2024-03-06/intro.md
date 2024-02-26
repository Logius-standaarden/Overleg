
### Mededelingen

- ADR versie 2.0 met modulaire opbouw en opname van modules Geo en Transport security wordt in het MIDO behandeld voor vaststelling. Het Digikoppeling REST API profiel zal worden aangepast voor aansluiting op de nieuwe versie
- Digipoort is onderzoek en voorbereiding aan het doen naar toepassing van APIs binnen de Digipoort koppelvlakken op basis van eDelivery REST.

### Toelichting bij Overige Punten

#### Signing & Encryptie toevoegen aan RESTful API profiel 

Werkgroep ADR Beveiliging (specifiek sub-werkgroep signing) heeft een vergelijking gemaakt van 2 standaarden voor signing van REST-API's :
[Vergelijking REST API Signing Standaarden](https://geonovum.github.io/KP-APIs/publicaties/REST_API_Signing_Standaarden) 

Laatste ontwikkelingen:
* De internationale standaard [httpbis-message-signatures](https://datatracker.ietf.org/doc/draft-ietf-httpbis-message-signatures/) komt dichter bij formele publicatie vanuit IETF als vastgestelde standaard
* Er is een concept ADR module voor JAdES gemaakt gebaseerd op het eDelivery API profiel : 
Zie : https://geonovum.github.io/KP-APIs/publicaties/review/module-signing-jades/

* Er is een concept ADR module voor encryptie gemaakt (gebaseerd op JWE) :
Zie : https://github.com/Geonovum/KP-APIs/blob/add-module-encryption/API-strategie-modules/encryption/ch01.md

Deze modules zijn toegevoegd aan de lijst optionele modules van de ADR van het Kennisplatform API's voor verdere uitwerking.
In het Digikoppeling REST-API profiel zullen deze modules gebruikt worden icm met verdere profilering. 

_Vraag aan het TO : zijn er op dit gebied ontwikkelingen binnen de eigen organisatie?_


### eDelivery EBMS3/AS4 stakeholderonderzoek en EU nieuws

PBLQ heeft een update van hun eindrapport opgeleverd met de input van JenV/Justid. _Zie Rapport [Impactanalyse modernisering Digikoppeling ebMS - van ebMS2 naar eDelivery, v1.1](https://github.com/Logius-standaarden/Overleg/blob/main/Digikoppeling/2024-03-06/Rapport%20Impactanalyse%20modernisering%20Digikoppeling%20ebMS%20-%20v1.1%20definitief%2019%20januari%202024.pdf). Logius heeft ontwikkelingen afgestemd met het EU eDelivery team.

Het EU eDelivery team heeft een update gegeven over de [AS4 en SMP 2.0 profielen](https://ec.europa.eu/digital-building-blocks/sites/pages/viewpage.action?pageId=711492329). Onder meer over de consultatie van 2023, TO lid Sander Fieten heeft op beiden een reactie gegeven. Verder heeft de EU een [_Adoption timeline for eDelivery AS4 and SMP 2.0 profiles_](https://ec.europa.eu/digital-building-blocks/sites/pages/viewpage.action?pageId=708411562) gepubliceerd.

### Definitieve Roadmap 2024-2025 
https://github.com/Logius-standaarden/Digikoppeling-Algemeen/blob/roadmap_2024-2026/Digikoppeling_Roadmap_2024_2025.md

_Verzoek aan het TO is akoord te geven op de definitieve roadmap , de roadmap zal vervolgens in de MIDO programmeringstafel Gegevensuitwisseling worden vastgesteld__
