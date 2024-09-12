<!-----------------------------







   :warning: Dit bestand wordt automatisch gegenereerd.
   :warning: Handmatige toevoegingen worden overschreven.







----------------------------->
# Technisch Overleg Digikoppeling

donderdag 19 september 2024


## Agenda (concept)

|  |   |
|------------------------|-------------------------------------| 
| Betreft  | **Technisch Overleg Digikoppeling** |
| Vergaderdatum en -tijd | 19-09-2024 - 10:00-14:00 uur  |
| Vergaderplaats  | Inview Amersfoort, ( Stadsring 140 , Amersfoort ) |



| Tijd | Onderwerp |Spreker|
| --- | --- | --- |
| 9:45 | Inloop        | 
| 10:00| Welkom & Mededelingen        |    Peter Haasnoot |
| 10:05 | [Wijzigingsvoorstel FSC](https://github.com/Logius-standaarden/Digikoppeling-Koppelvlakstandaard-REST-API/issues/26) <BR>- Stand van Zaken<BR>- [Consultatie](https://github.com/Logius-standaarden/Openbare-Consultaties/tree/master/Digikoppeling%20REST-API%20profiel%20-%20Opnemen%20FSC%20Standaard) : Bespreking [Resultaat Consultatie](Resultaat_Publieke_Consultatie_FSC_toevoegen_Digikoppeling_REST-API.md) | Peter Haasnoot |
| 10:30 | [Digikoppeling Releaseplanning](https://github.com/orgs/Logius-standaarden/projects/4) | Alexander Green | 
| 10:40 | Grote en kleine wijzigingen <BR> - Grote Berichten : Gebruik van S3 protocol   <BR> - Begrippenkader OIN (ter Goedkeuring) <BR>- Signing & Encryptie toevoegen aan RESTful API profiel (ter Goedkeuring) | Peter Haasnoot / Alexander Green | 
| 11:10 | Pauze |Allen| 
| 11:20 | Toelichting OIN Beleid (ter Informatie) | Peter Haasnoot| 
| 11:35 | Review Beveiligingsvoorschriften (ter Goedkeuring) |Alexander Green| 
| 11:45 | Review Architectuur (ter Goedkeuring) | Peter Haasnoot|
| 12:00 | Lunch|
| 12:45 | eDelivery ebMS3 Wijzigingsvoorstel - Stand van Zaken / Vervolg | Edwin Wisse | 
| 13:15 | [Roadmap 2024-2025](https://github.com/Logius-standaarden/Digikoppeling-Algemeen/blob/roadmap_2024-2026/Digikoppeling_Roadmap_2024_2025.md#tijdlijn-roadmap-digikoppeling-standaarden) <BR>- Best practice Gebruik OAuth icm Digikoppeling REST_API|Peter Haasnoot|
| 13:30 | Discussie: <BR>Uitfaseren koppelvlakstandaarden (WUS)<BR>| Allen |
| 13:45 | Rondvraag / Afsluiting | Allen | 
| 14:00 | Einde |

## Onderwerpen

### Grote wijzigingen
* Digikoppeling-Koppelvlakstandaard-GB [issue #13] [Gebruik van de S3 protocol om de payload te uploaden/downloaden](https://github.com/Logius-standaarden/Digikoppeling-Koppelvlakstandaard-GB/issues/13) (15 januari 2024), _Status: In onderzoek_
* Digikoppeling-Koppelvlakstandaard-REST-API [issue #26] [Federatieve Service Connectiviteit opnemen in het Digikoppeling voor REST API's profiel](https://github.com/Logius-standaarden/Digikoppeling-Koppelvlakstandaard-REST-API/issues/26) (18 december 2023), _Status: In onderzoek_
  * [Wijzigingsvoorstel](https://github.com//Logius-standaarden/Digikoppeling-Architectuur/pull/14/files)
* Digikoppeling-Koppelvlakstandaard-REST-API [issue #11] [Signing & Encryptie toevoegen aan RESTful API profiel](https://github.com/Logius-standaarden/Digikoppeling-Koppelvlakstandaard-REST-API/issues/11) (1 april 2022), _Status: In onderzoek_
  * [Wijzigingsvoorstel](https://github.com//Logius-standaarden/Digikoppeling-Koppelvlakstandaard-REST-API/pull/30/files)
* Digikoppeling-Koppelvlakstandaard-ebMS2 [issue #6] [Digikoppeling baseren op ebMS3](https://github.com/Logius-standaarden/Digikoppeling-Koppelvlakstandaard-ebMS2/issues/6) (3 februari 2022), _Status: In onderzoek_

### Kleine wijzigingen
* Digikoppeling-Beveiligingsstandaarden-en-voorschriften [issue #7] [2024 Q3 Review Beveiligingsvoorschriften](https://github.com/Logius-standaarden/Digikoppeling-Beveiligingsstandaarden-en-voorschriften/pull/7) (10 september 2024)
* OIN-Stelsel [issue #21] [Begrippenkader OIN](https://github.com/Logius-standaarden/OIN-Stelsel/issues/21) (25 maart 2024), _Status: In bewerking_
  * [Wijzigingsvoorstel](https://github.com//Logius-standaarden/OIN-Stelsel/pull/20/files)
* Digikoppeling-Architectuur [issue #15] [Review q1-q2 2024](https://github.com/Logius-standaarden/Digikoppeling-Architectuur/pull/15) (16 januari 2024), _Status: Klaar voor release_

## Toelichting


### Mededelingen

### Grote / Kleine wijzigingen

#### Signing & Encryptie toevoegen aan RESTful API profiel (ter Goedkeuring)

De ADR modules voor Signing en Encryptie zijn geconsulteerd en vervolgens vastgesteld als stabiel binnen het Kennisplatform API's. 

- [ADR-HTTP Message and payload signing with JAdES](https://docs.geostandaarden.nl/api/cv-hr-API-Strategie-mod-signing-jades-20240417/)
- [ADR-HTTP Payload encryption](https://docs.geostandaarden.nl/api/cv-hr-API-Strategie-mod-encryption-20240417/)

In het wijzigingsvoorstel [Signing & Encryptie toevoegen aan RESTful API profiel](https://github.com/Logius-standaarden/Digikoppeling-Koppelvlakstandaard-REST-API/pull/30/files) wordt verwezen naar deze modules.

( Zie ook : [Vergelijking REST API Signing Standaarden](https://geonovum.github.io/KP-APIs/publicaties/REST_API_Signing_Standaarden/ ) )

### Review Architectuur (ter Goedkeuring)
Conform de [Roadmap Digikoppeling](https://github.com/Logius-standaarden/Digikoppeling-Algemeen/blob/roadmap_2024-2026/Digikoppeling_Roadmap_2024_2025.md) is in Q1 een review uitgevoerd. 

Voornaamste aanpassingen:
- Verduidelijking van de tekst
- Context (van overheids initiatieven en programma's) is aangegeven
- Aansluiting op REST API gerelateerde onderwerpen
- NORA Architectuur principes zijn bijgewerkt naar de nieuwe versie van de NORA

_Verzoek aan het Technisch Overleg is deze voorgestelde aanpassingen goed te keuren, deze zullen dan in een volgende versie van de standaard (na publieke consultatie), worden doorgevoerd en gepubliceerd_

### Review Beveiligingsvoorschriften (ter Goedkeuring)

In Q3 is een review voor de beveiligingsvoorschriften uitgevoerd. 

De NCSC TLS richtlijnen uit 2021 zijn nog steeds leidend;

Voornaamste wijzigingen:
- Algemene inleiding toegevoegd
- Verwijderen verstreken deadline voor uitzonderingen TLS
- Verwijzing naar NCSC/AIVD Post Quantum Cryptografie adviezen toegevoegd;

_Verzoek aan het Technisch Overleg is deze voorgestelde aanpassingen goed te keuren, deze zullen dan in een volgende versie van de standaard (na publieke consultatie), worden doorgevoerd en gepubliceerd_


### Update Roadmap 2024-2025 
https://github.com/Logius-standaarden/Digikoppeling-Algemeen/blob/roadmap_2024-2026/Digikoppeling_Roadmap_2024_2025.md


Toelichting actuele stand van zaken 
