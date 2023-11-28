<!-----------------------------







   Dit bestand wordt automatisch gegenereerd.
   Handmatige toevoegingen worden overschreven.







----------------------------->
# Technisch Overleg Digikoppeling

donderdag 14 december 2023

## Agenda

|  |   |
|------------------------|-------------------------------------| 
| Betreft  | **Technisch Overleg Digikoppeling** |
| Vergaderdatum en -tijd | 14-12-2023 - 11:00-12:00 uur  |
| Vergaderplaats  | Microsoft Teams |


| Tijd | Onderwerp |
| --- | --- |
| 11:00 | Welkom & Mededelingen        |    
| 11:05 | eDelivery EBMS3/AS4 stakeholderonderzoek (PBLQ) |
| 11:30 | Roadmap: (concept) 2024-2025 |
| 11:40 | Grote en kleine wijzigingen -zie onderstaand |
| - | Stand van zaken FSC |
| - | OIN stelsel ontwikkelingen  | 
| 11:55 | Rondvraag / Afsluiting |

## Onderwerpen

### Grote wijzigingen
* Digikoppeling-Beheermodel [issue #3] [Aanpassing beheermodel op BOMOS principes en MIDO governance](https://github.com/Logius-standaarden/Digikoppeling-Beheermodel/issues/3) (16 maart 2022), _Status: Gereed_
* Digikoppeling-Koppelvlakstandaard-ebMS2 [issue #6] [Digikoppeling baseren op ebMS3](https://github.com/Logius-standaarden/Digikoppeling-Koppelvlakstandaard-ebMS2/issues/6) (3 februari 2022), _Status: In onderzoek_

### Kleine wijzigingen
* Digikoppeling-Beveiligingsstandaarden-en-voorschriften [issue #4] [[ebcore] Additional XML Security Uniform Resource Identifiers (URIs)](https://github.com/Logius-standaarden/Digikoppeling-Beveiligingsstandaarden-en-voorschriften/issues/4) (24 oktober 2023)
* OIN-Stelsel [issue #10] [Sub-OIN Beheerder](https://github.com/Logius-standaarden/OIN-Stelsel/issues/10) (20 december 2022), _Status: In review_
  * [Wijzigingsvoorstel](https://github.com//Logius-standaarden/OIN-Stelsel/pull/13/files)

### Overige punten
* Digikoppeling-Koppelvlakstandaard-REST-API [issue #11] [Signing & Encryptie toevoegen aan RESTful API profiel](https://github.com/Logius-standaarden/Digikoppeling-Koppelvlakstandaard-REST-API/issues/11) (1 april 2022), _Status: In onderzoek_

## Toelichting



### Mededelingen

- ADR 2.0 in consultatie geweest incl. modulaire opbouw , Digikoppeling REST API profiel zal hierop worden aangepast


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



### eDelivery EBMS3/AS4 stakeholderonderzoek 

Logius heeft opdracht gegeven voor het uitvoeren van een stakeholder onderzoek naar de impact van 
een overgang naar een eDelivery koppelvlakspecificatie voor Digikoppeling. Dit onderzoek wordt 
uitgeveord door PBLQ. Peter Seignette van PBLQ ligt het onderzoek kort toe.





### Concept Roadmap 2024-2025
https://github.com/Logius-standaarden/Digikoppeling-Algemeen/blob/roadmap_2024-2026/Digikoppeling_Roadmap_2024_2025.md


_Verzoek aan het TO is commentaar en aanvullingen te geven op de opgenomen concept onderwerpen - Deze zullen nog begin 2024 definitief door het TO worden vastgesteld_


### Stand van zaken FSC 


### OIN stelsel ontwikkelingen

- Datakwaliteit
- Samenhang met Bronregistraties
- Gebruik van OIN, bv in PKIO, eHerkenning , PEPPOL eDelivery
- Rol van OIN register
