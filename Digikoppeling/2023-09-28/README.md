# TO-DK

# Agenda

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
| 11:15 | OIN scenario onafhankelijke maatregelen mbt de standaard | 
| 11:25 | Rondvraag / Afsluiting |

# Onderwerpen

## Grote wijzigingen
* Digikoppeling-Beheermodel [issue #3] [Aanpassing beheermodel op BOMOS principes en MIDO governance](https://github.com/Logius-standaarden/Digikoppeling-Beheermodel/issues/3) (16 Mar. 2022), _Status: Gereed_
* Digikoppeling-Koppelvlakstandaard-ebMS2 [issue #6] [Digikoppeling baseren op ebMS3](https://github.com/Logius-standaarden/Digikoppeling-Koppelvlakstandaard-ebMS2/issues/6) (03 Feb. 2022), _Status: In onderzoek_

## Kleine wijzigingen
* OIN-Stelsel [issue #10] [Sub-OIN Beheerder](https://github.com/Logius-standaarden/OIN-Stelsel/issues/10) (20 Dec. 2022)
* OIN-Stelsel [issue #5] [RSIN of Kvk nummer leidend voor OIN?](https://github.com/Logius-standaarden/OIN-Stelsel/issues/5) (29 Mar. 2022), _Status: Uitwerking door derden_
  * [Wijzigingsvoorstel](https://github.com//Logius-standaarden/OIN-Stelsel/pull/7/files)

## Overige punten
* Digikoppeling-Koppelvlakstandaard-REST-API [issue #11] [Signing & Encryptie toevoegen aan RESTful API profiel](https://github.com/Logius-standaarden/Digikoppeling-Koppelvlakstandaard-REST-API/issues/11) (01 Apr. 2022), _Status: In onderzoek_

# Toelichting



## Mededelingen

- ADR 2.0 in consultatie incl. modulaire opbouw , Digikoppeling REST API profiel zal hierop worden aangepast


## Grote Wijzigingen

### Bij [Digikoppeling baseren op ebMS3](https://github.com/Logius-standaarden/Digikoppeling-Koppelvlakstandaard-ebMS2/issues/6)

(__vorige toelichting TO__:
We hebben de transitie van ebMS2 naar ebMS3/AS4 geagendeerd in de Programmeringstafel. 
Naar aanleiding van de discussie in de vergadering is Logius gevraagd een impactanalyse te laten opstellen. 
Dit wordt toegelicht in **[toelichting aanpak ebMS transitie](impact_ebMS.md)**.
)

## Kleine Wijzingen

Bij ....

## Consultatie eDelivery AS4 profile 2.0                        

## MIDO governance standaarden 

## eDelivery EBMS3/AS4 stakeholderonderzoek 

## Roadmap: huidig 2023-Q4  & nieuw (concept) 2024-2025


### Huidige Roadmap 2022-2023
Zie voor geactualiseerde tijdlijn Roadmap :

https://github.com/Logius-standaarden/Digikoppeling-Algemeen/blob/update_Q4/Digikoppeling_Roadmap_2022_2023.md

(Dikgedrukt zijn de lopende onderdelen)

### Concept 2024-2025
https://github.com/Logius-standaarden/Digikoppeling-Algemeen/blob/roadmap_2024-2026/Digikoppeling_Roadmap_2022_2023.md

## Signing & Encryptie toevoegen aan RESTful API profiel	

Werkgroep ADR Beveiliging (specifiek sub-werkgroep signing) heeft een vergelijking gemaakt van 2 standaarden voor signing van REST-API's :
[Vergelijking REST API Signing Standaarden](https://geonovum.github.io/KP-APIs/publicaties/REST_API_Signing_Standaarden)

Laatste ontwikkelingen:
* De internationale standaard [httpbis-message-signatures](https://datatracker.ietf.org/doc/draft-ietf-httpbis-message-signatures/) komt dichter bij formele publicatie vanuit IETF als vastgestelde standaard
* Er is een concept ADR module voor JAdES gemaakt gebaseerd op het eDelivery API profiel : 

1.	(markdown) https://github.com/Geonovum/KP-APIs/blob/add-module-signing-jades/API-strategie-modules/signing-jades/ch01.md
2.	(pdf) https://github.com/Geonovum/KP-APIs/blob/add-module-signing-jades/API-strategie-modules/signing-jades/print-module-signing-jades.pdf

_Graag de mening van het TO over de geschiktheid van JAdES signing voor het Digikoppeling REST API profiel_


## Stand van zaken FSC 

## OIN scenario onafhankelijke maatregelen mbt de standaard  

## Gebruik van OAuth in DK API profiel beveiliging naast mTLS 

