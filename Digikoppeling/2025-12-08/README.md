<!-----------------------------







   :warning: Dit bestand wordt automatisch gegenereerd.
   :warning: Handmatige toevoegingen worden overschreven.







----------------------------->
# Technisch Overleg Digikoppeling

maandag 8 december 2025

_Status : Concept_

## Agenda 

| Betreft                | Technisch Overleg Digikoppeling |
| ---------------------- | ------------------------------- |
| Vergaderdatum en -tijd | 08-12-2025, 13:00-15:00        |
| Vergaderplaats         | Online Bijeenkomst |      |

| Tijd | Onderwerp |Spreker|
| --- | --- | --- |  
| 13:00| Welkom & Mededelingen  
| 13:05| [Verslag vorige vergadering](https://github.com/Logius-standaarden/Overleg/blob/main/Digikoppeling/2025-12-08/2025-09-09%20%20Verslag%20TO%20Digikoppeling_v1.0.pdf)       |    Peter Haasnoot (Logius) |
| 13:10 | [Digikoppeling Toekomstvisie](#digikoppeling-toekomstvisie--scope-en-inzetgebied) <BR>| Peter Haasnoot (Logius) | 
| 13:25 | [Digikoppeling Roadmap 2026-2027](https://github.com/Logius-standaarden/Digikoppeling-Algemeen/blob/roadmap-2026-2027/roadmap/onderwerpen.md) <BR>| Peter Haasnoot (Logius) | 
| 13:35| REST-API profiel - onderdeel signing header| Tim van der Lippe (Logius)|
| 13:45  | Post Quantum Cryptografie & TLS 1.3 |  Nil Barua (Logius)| 
| 14:00 | Pauze | Allen|
|14:05| FSC sub-werkgroep update | Stas Mironov (Logius)|
|14:10 |  FSC Major release <br> [Wijzigingsvoorstellen](#fsc-wijzigingsvoorstellen) <BR> _Wijziging wordt ter goedkeuring aan het TO voorgelegd_ | Ronald Koster (RINIS)  |
|14:25  | Rondvraag / Afsluiting | Allen | 
|15:00 | Einde |

## Aanmelden

Dit overleg is openbaar. Aanmelden kan door te mailen naar digikoppeling@logius.nl

## Onderwerpen

### Grote wijzigingen
* fsc-test-suite [issue #3] [Properties](https://github.com/Logius-standaarden/fsc-test-suite/pull/3) (23 november 2025), _Status: Ter goedkeuring_
* fsc-core [issue #53] [allow outways based on domain name](https://github.com/Logius-standaarden/fsc-core/pull/53) (31 oktober 2025), _Status: Ter goedkeuring_
* fsc-core [issue #48] [Lokaal Testen van Federative Service Connectivity (FSC) Compliance](https://github.com/Logius-standaarden/fsc-core/issues/48) (26 september 2025)

### Kleine wijzigingen
* Digikoppeling-Beveiligingsstandaarden-en-voorschriften [issue #19] [Nieuwe G4 PKIoverheid roots beschikbaar](https://github.com/Logius-standaarden/Digikoppeling-Beveiligingsstandaarden-en-voorschriften/issues/19) (1 december 2025)
* fsc-logging [issue #1] [add additional data to transaction log record](https://github.com/Logius-standaarden/fsc-logging/pull/1) (12 november 2025), _Status: Ter goedkeuring_
* fsc-core [issue #55] [Add error code for unknown FSC version](https://github.com/Logius-standaarden/fsc-core/pull/55) (4 november 2025), _Status: Ter goedkeuring_
* Digikoppeling-Algemeen [issue #21] [FSC aanvullen met nieuw profiel diginetwerk](https://github.com/Logius-standaarden/Digikoppeling-Algemeen/issues/21) (10 september 2025), _Status: In bewerking_
* fsc-core [issue #12] [Minor compatibility changes met OAuth NL GOV](https://github.com/Logius-standaarden/fsc-core/issues/12) (4 maart 2025), _Status: In bewerking_

### Overige punten
* Digikoppeling-Koppelvlakstandaard-REST-API [issue #52] [Mogelijk OAuth toevoegen aan koppelvlak](https://github.com/Logius-standaarden/Digikoppeling-Koppelvlakstandaard-REST-API/issues/52) (12 september 2025), _Status: In bewerking_

## Toelichting




## Digikoppeling Toekomstvisie : Scope en inzetgebied

### Update 08/12/2025

- Toekomstvisie en Life-Cycle_Management op de koppelvlakstandaarden wordt afgestemd met MIDO WG Architectuur GU en MIDO Programmeringstafel, eerstvolgende bespreking februari 2026 (Zie ook [Toekomstvisie Scenario's](https://github.com/Logius-standaarden/Overleg/blob/main/Digikoppeling/2025-12-08/2025_12_08_Scenario%E2%80%99s%20Toekomstvisie%20Digikoppeling%20Koppelvlak%20Standaarden.pdf))
- Met J&V en RINIS is gesproken over de tijdlijnen in [PBLQ Rapport Impactanalyse modernisering Digikoppeling ebMS: 
van ebMS2 naar eDelivery (ebMS3/AS4)](https://github.com/Logius-standaarden/Overleg/blob/main/Digikoppeling/2024-03-06/Rapport%20Impactanalyse%20modernisering%20Digikoppeling%20ebMS%20-%20v1.1%20definitief%2019%20januari%202024.pdf) en eerdere Notitie. Deze worden niet haalbaar geacht, eerst ervaring opdoen met de nieuwe koppelvlakken en een beeld krijgen van wat bij een overgang komt kijken voordat uitfasering en tijdlijnen worden gekozen wordt aanbevolen;


### Bijlage : stukken bij vorige vergadering 09/09/2025

In de [MIDO Domeinarchitectuur Gegevensuitwisseling](https://github.com/MinBZK/gdi-gegevensuitwisseling) zijn enkele mogelijke vernieuwingen en uitbreidingen voor Digikoppeling genoemd;

In de vorige sessie bespraken we gezamenlijk deze punten met als doel de toekomstvisie Digikoppeling nader te bepalen, in deze sessie bespreken we dit verder.

Zie Notitie : [Toekomstvisie Digikoppeling](https://github.com/Logius-standaarden/Overleg/blob/main/Digikoppeling/2025-09-09/2025-09-09_Toekomstvisie%20Digikoppeling.md)

Zie ook : 
- [2025-03-19-TO-Digikoppeling-poll-results](https://github.com/Logius-standaarden/Overleg/blob/main/Digikoppeling/2025-06-10/2025-03-19-TO-Digikoppeling-poll-results.pdf)
- [Enquete ebMS2/3 Polls-per-participant-2025-06-10_TO_Digikoppeling](https://github.com/Logius-standaarden/Overleg/blob/main/Digikoppeling/2025-09-09/Polls-per-participant-2025-06-10_TO_Digikoppeling_Totaal.xlsx)



## PKIO G4 certificaten, Post Quantum Cryptografie , TLS 1.3

### TLS 1.3

Discussie - is aanscherping van TLS 1.3 richtlijn wenselijk n.a.v. [nieuwe NSCS richtlijnen](https://www.ncsc.nl/documenten/publicaties/2025/juni/01/ict-beveiligingsrichtlijnen-voor-transport-layer-security-2025-05) 

Huidige TLS afspraken : [Digikoppeling beveiligingsvoorschriften](https://gitdocumentatie.logius.nl/publicatie/dk/beveilig/2.0.1/#tls-transport-layer-security)

## FSC Wijzigingsvoorstellen

_Ter goedkeuring voorgelegd aan het TO:_

- [Recap properties](https://github.com/Logius-standaarden/fsc-core/pull/25) + [nieuwe extensie voor een referentie naar een bestaand (papieren) contract](https://github.com/Logius-standaarden/fsc-external-contract-reference) + [bijbehorende test cases](https://github.com/Logius-standaarden/fsc-test-suite/pull/3)
- [FSC logging update](https://github.com/Logius-standaarden/fsc-logging/pull/1)
- [Nieuwe error codes in Open FSC](https://github.com/Logius-standaarden/fsc-core/pull/55)
- [Open FSC versie in het contract opgenomen](https://github.com/Logius-standaarden/fsc-core/pull/51)
- [Outway autorisatie op basis van een domeinnaam](https://github.com/Logius-standaarden/fsc-core/pull/53)
- Nieuwe digikoppeling groep update (Rinis)
- [Test-suite in core standaard](https://github.com/Logius-standaarden/fsc-test-suite)
