<!-----------------------------







   Dit bestand wordt automatisch gegenereerd.
   Handmatige toevoegingen worden overschreven.







----------------------------->
# Technisch Overleg Digikoppeling

donderdag 28 september 2023

## Agenda

|  |   |
|------------------------|-------------------------------------| 
| Betreft  | **Technisch Overleg Digikoppeling** |
| Vergaderdatum en -tijd | 28-09-2023 - 10:00-11:30 uur  |
| Vergaderplaats  | Microsoft Teams |


| Tijd | Onderwerp |
| --- | --- |
| 10:00 | Welkom & Mededelingen        |    
| 10:05 | Consultatie eDelivery AS4 profile 2.0                        | 
| 10:10| Grote en kleine wijzigingen -zie onderstaand |
| 10:40 | eDelivery EBMS3/AS4 stakeholderonderzoek (PBLQ) |
| 10:50 | Roadmap: huidig 2023-Q4  & nieuw (concept) 2024-2025 |
| 11:05 | Stand van zaken FSC |
| 11:15 | OIN stelsel ontwikkelingen  | 
| 11:25 | Rondvraag / Afsluiting |

## Onderwerpen

### Grote wijzigingen
* Digikoppeling-Beheermodel [issue #3] [Aanpassing beheermodel op BOMOS principes en MIDO governance](https://github.com/Logius-standaarden/Digikoppeling-Beheermodel/issues/3) (16 maart 2022), _Status: Gereed_
* Digikoppeling-Koppelvlakstandaard-ebMS2 [issue #6] [Digikoppeling baseren op ebMS3](https://github.com/Logius-standaarden/Digikoppeling-Koppelvlakstandaard-ebMS2/issues/6) (3 februari 2022), _Status: In onderzoek_

### Kleine wijzigingen
* OIN-Stelsel [issue #10] [Sub-OIN Beheerder](https://github.com/Logius-standaarden/OIN-Stelsel/issues/10) (20 december 2022), _Status: In review_
* OIN-Stelsel [issue #5] [RSIN of Kvk nummer leidend voor OIN?](https://github.com/Logius-standaarden/OIN-Stelsel/issues/5) (29 maart 2022), _Status: Klaar voor release_
  * [Wijzigingsvoorstel](https://github.com//Logius-standaarden/OIN-Stelsel/pull/7/files)

### Overige punten
* Digikoppeling-Koppelvlakstandaard-REST-API [issue #11] [Signing & Encryptie toevoegen aan RESTful API profiel](https://github.com/Logius-standaarden/Digikoppeling-Koppelvlakstandaard-REST-API/issues/11) (1 april 2022), _Status: In onderzoek_

## Toelichting



### Mededelingen

- ADR 2.0 in consultatie incl. modulaire opbouw , Digikoppeling REST API profiel zal hierop worden aangepast
- EBMS2 Vraag kadaster - Welke partijen gebruiken Clockwork ebMS?
-  Ontwikkelingen rond Compliance voorzieningen API/WUS/ebMS 

### Toelichting bij Overige Punten

#### Signing & Encryptie toevoegen aan RESTful API profiel	

Werkgroep ADR Beveiliging (specifiek sub-werkgroep signing) heeft een vergelijking gemaakt van 2 standaarden voor signing van REST-API's :
[Vergelijking REST API Signing Standaarden](https://geonovum.github.io/KP-APIs/publicaties/REST_API_Signing_Standaarden) 

Laatste ontwikkelingen:
* De internationale standaard [httpbis-message-signatures](https://datatracker.ietf.org/doc/draft-ietf-httpbis-message-signatures/) komt dichter bij formele publicatie vanuit IETF als vastgestelde standaard
* Er is een concept ADR module voor JAdES gemaakt gebaseerd op het eDelivery API profiel : 

1.	(markdown) https://github.com/Geonovum/KP-APIs/blob/add-module-signing-jades/API-strategie-modules/signing-jades/ch01.md
2.	(pdf) https://github.com/Geonovum/KP-APIs/blob/add-module-signing-jades/API-strategie-modules/signing-jades/print-module-signing-jades.pdf

_Graag de mening van het TO over de geschiktheid van de JAdES signing module voor het Digikoppeling REST API profiel_



### Consultatie eDelivery AS4 profile 2.0                        

_Last call_

The eDelivery team is opening two Public Consultations on the new draft Specifications of the [eDelivery AS4 profile 2.0](https://ec.europa.eu/digital-building-blocks/wikis/x/NabXGw) and [eDelivery SMP profile 2.0](https://ec.europa.eu/digital-building-blocks/wikis/x/xqfXGw). The proposed changes have already been presented in early May 2023 during the [eDelivery Informal Cooperation Forum](https://ec.europa.eu/digital-building-blocks/wikis/x/Wi7ZJw) ([slides available here](https://europa.eu/!q6vcQG)) and now members of the eDelivery community are invited to share their views, comments and suggestions on both proposals before the specifications are finalised and published.  

The community is invited to either post its feedback as comments on the public consultation pages linked underneath or send it by email to EC-EDELIVERY-SUPPORT@ec.europa.eu by the 20th October 2023.

Zie https://ec.europa.eu/digital-building-blocks/wikis/display/DIGITAL/2023/06/16/Your+views+are+important%3A+consultation+on+AS4+2.0+and+SMP+2.0

### eDelivery EBMS3/AS4 stakeholderonderzoek 

Logius heeft opdracht gegeven voor het uitvoeren van een stakeholder onderzoek naar de impact van 
een overgang naar een eDelivery koppelvlakspecificatie voor Digikoppeling. Dit onderzoek wordt 
uitgeveord door PBLQ. Peter Seignette van PBLQ ligt het onderzoek kort toe.

### Roadmap: huidig 2023-Q4  & nieuw (concept) 2024-2025

#### Huidige Roadmap 2022-2023
Zie voor geactualiseerde tijdlijn Roadmap Q4 :

https://github.com/Logius-standaarden/Digikoppeling-Algemeen/blob/update_Q4/Digikoppeling_Roadmap_2022_2023.md

_Bij akkoord van het TO voor de bijgewerkte Roadmap , zal deze versie worden gepubliceerd_


(Dikgedrukt zijn de lopende onderdelen)

#### Concept Roadmap 2024-2025
https://github.com/Logius-standaarden/Digikoppeling-Algemeen/blob/roadmap_2024-2026/Digikoppeling_Roadmap_2022_2023.md


_Verzoek aan het TO is commentaar en aanvullingen te geven op de opgenomen concept onderwerpen - Deze zullen nog begin 2024 definitief door het TO worden vastgesteld_


### Stand van zaken FSC 

Toelichting door FSC

### OIN stelsel ontwikkelingen

- Datakwaliteit
- Samenhang met Bronregistraties
- Gebruik van OIN, bv in PKIO, eHerkenning , PEPPOL eDelivery
- Rol van OIN register
