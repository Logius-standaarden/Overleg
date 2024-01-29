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


| Tijd | Onderwerp |
| --- | --- |
| 10:00 | Inloop        | 
| 10:30 | Welkom & Mededelingen        |    
| 10:40 | Wijzigingsvoorstel FSC : Federated Service Connectivity (presentatie) |
| 11:10 | Wijzigingsvoorstel FSC : Federated Service Connectivity (discussie) |
| 12:00 | Lunch|
| 12:45 | Wijzigingsvoorstel FSC : Advies TO aan Programmeringstafel GU t.a.v. FSC |
| 13:10 | Grote en kleine wijzigingen -zie onderstaand |
| 13:30 | Roadmap 2024-2025 |
| 13:45 | Rondvraag / Afsluiting |
| 14:00 | Einde |

## Onderwerpen

### Grote wijzigingen
* Digikoppeling-Koppelvlakstandaard-REST-API [issue #26] [Federatieve Service Connectiviteit opnemen in het Digikoppeling voor REST API's profiel](https://github.com/Logius-standaarden/Digikoppeling-Koppelvlakstandaard-REST-API/issues/26) (18 december 2023), _Status: In onderzoek_
  * [Wijzigingsvoorstel](https://github.com//Logius-standaarden/Digikoppeling-Koppelvlakstandaard-REST-API/pull/27/files)
* Digikoppeling-Koppelvlakstandaard-ebMS2 [issue #6] [Digikoppeling baseren op ebMS3](https://github.com/Logius-standaarden/Digikoppeling-Koppelvlakstandaard-ebMS2/issues/6) (3 februari 2022), _Status: In onderzoek_

### Kleine wijzigingen
* OIN-Stelsel [issue #5] [RSIN of Kvk nummer leidend voor OIN?](https://github.com/Logius-standaarden/OIN-Stelsel/issues/5) (29 maart 2022), _Status: Klaar voor release_
  * [Wijzigingsvoorstel](https://github.com//Logius-standaarden/OIN-Stelsel/pull/7/files)

### Overige punten
* Digikoppeling-Koppelvlakstandaard-GB [issue #13] [Gebruik van de S3 protocol om de payload te uploaden/downloaden](https://github.com/Logius-standaarden/Digikoppeling-Koppelvlakstandaard-GB/issues/13) (15 januari 2024)
* Digikoppeling-Koppelvlakstandaard-REST-API [issue #11] [Signing & Encryptie toevoegen aan RESTful API profiel](https://github.com/Logius-standaarden/Digikoppeling-Koppelvlakstandaard-REST-API/issues/11) (1 april 2022), _Status: In onderzoek_

## Toelichting


TO DO / OUD !

### Mededelingen

- ADR 2.0 in consultatie geweest incl. modulaire opbouw , Digikoppeling REST API profiel zal hierop worden aangepast
- Digipoort is onderzoek en voorbereiding aan het doen naar toepassing van APIs binnen de Digipoort koppelvlakken op basis van eDelivery REST.

### Toelichting bij Overige Punten

#### Signing & Encryptie toevoegen aan RESTful API profiel	

Werkgroep ADR Beveiliging (specifiek sub-werkgroep signing) heeft een vergelijking gemaakt van 2 standaarden voor signing van REST-API's :
[Vergelijking REST API Signing Standaarden](https://geonovum.github.io/KP-APIs/publicaties/REST_API_Signing_Standaarden) 

Laatste ontwikkelingen:
* De internationale standaard [httpbis-message-signatures](https://datatracker.ietf.org/doc/draft-ietf-httpbis-message-signatures/) komt dichter bij formele publicatie vanuit IETF als vastgestelde standaard
* Er is een concept ADR module voor JAdES gemaakt gebaseerd op het eDelivery API profiel : 

1.	(markdown) https://github.com/Geonovum/KP-APIs/blob/add-module-signing-jades/API-strategie-modules/signing-jades/ch01.md
2.	(pdf) https://github.com/Geonovum/KP-APIs/blob/add-module-signing-jades/API-strategie-modules/signing-jades/print-module-signing-jades.pdf

_Vraag aan het TO : zijn er op dit gebied ontwikkelingen binnen de eigen organisatie? (of specifiek op gebied van JAdES of Message Signatures?)_



### eDelivery EBMS3/AS4 stakeholderonderzoek 

Logius heeft opdracht gegeven voor het uitvoeren van een stakeholder onderzoek naar de impact van 
een overgang naar een eDelivery koppelvlakspecificatie voor Digikoppeling. Dit onderzoek wordt 
uitgevoerd door PBLQ. Peter Seignette van PBLQ ligt het onderzoek kort toe.

_Zie Rapport [Impactanalyse modernisering Digikoppeling ebMS - van ebMS2 naar eDelivery](https://github.com/Logius-standaarden/Overleg/blob/main/Digikoppeling/2023-12-14/Rapport%20Impactanalyse%20modernisering%20Digikoppeling%20ebMS%20-%20definitief%208%20december%202023.pdf)_





### Concept Roadmap 2024-2025
https://github.com/Logius-standaarden/Digikoppeling-Algemeen/blob/roadmap_2024-2026/Digikoppeling_Roadmap_2024_2025.md


_Verzoek aan het TO is commentaar en aanvullingen te geven op de opgenomen concept onderwerpen - Deze zullen nog begin 2024 definitief door het TO worden vastgesteld_
