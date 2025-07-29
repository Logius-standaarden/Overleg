<!-----------------------------







   :warning: Dit bestand wordt automatisch gegenereerd.
   :warning: Handmatige toevoegingen worden overschreven.







----------------------------->
# Technisch Overleg Digikoppeling

dinsdag 9 september 2025



## Agenda _Concept_

| Betreft                | Technisch Overleg Digikoppeling |
| ---------------------- | ------------------------------- |
| Vergaderdatum en -tijd | 09-09-2025, 10:00-13:30        |
| Vergaderplaats         | Fysieke Bijeenkomst - Utrecht - Bar Beton |                         |

| Tijd | Onderwerp |Spreker|
| --- | --- | --- |  
| 10:00| Welkom & Mededelingen   <BR>- [Review Architectuur Q2](https://gitdocumentatie.logius.nl/publicatie/dk/roadmap/2024-2025/#periodiek-actualiseren-architectuur) afgerond |    Peter Haasnoot (Logius) |
| 10:05| [Verslag vorige vergadering](https://github.com/Logius-standaarden/Overleg/blob/main/Digikoppeling/2025-03-19/2025-03-19%20%20Verslag%20TO%20Digikoppeling%20v1.0..pdf)       |    Peter Haasnoot (Logius) |
| 10:10| [Openbare Consultaties](https://github.com/Logius-standaarden/Openbare-Consultaties) :  _Consultatie WUS uitfasering_      |    Peter Haasnoot (Logius) |
| 10:20 | [Digikoppeling Toekomstvisie](#digikoppeling-toekomstvisie--scope-en-inzetgebied) <BR>| Dennis Passage / Peter Haasnoot (Logius) | 
| 10:45  | [Overgang ebMS2 naar eDelivery ebMS3/AS4](#overgang-ebms2-naar-edelivery-ebms3as4) - Invoering Standaard & Ondersteunende voorzieningen  | Peter Haasnoot / Nil Barua (Logius)| 
| 11:15  | TLS 1.3 , XML Signing/Encryptie | Peter Haasnoot / Nil Barua (Logius)| 
|11:30| (Overige) lopende wijzigingsvoorstellen Digikoppeling | Alexander Green (Logius)|
|12:00| Lunch | Allen|
|12:45| FSC Stand van zaken & Beheer | Stas Mironov (Logius)|
|13:00 | [FSC Wijzigingsvoorstellen](https://github.com/Logius-standaarden/Overleg/blob/main/Digikoppeling/2025-06-10/intro.md#fsc-wijzigingsvoorstellen) <BR> _Wijziging wordt ter goedkeuring aan het TO voorgelegd_ | Ronald Koster (VNG)  |
|13:30  | Rondvraag / Afsluiting | Allen | 
|13:45 | Einde |

## Aanmelden

Dit overleg is openbaar. Aanmelden kan door te mailen naar digikoppeling@logius.nl

## Onderwerpen

### Grote wijzigingen
* Digikoppeling-Beveiligingsstandaarden-en-voorschriften [issue #17] [XML Signing voorstel TO](https://github.com/Logius-standaarden/Digikoppeling-Beveiligingsstandaarden-en-voorschriften/pull/17) (9 juli 2025), _Status: Ter goedkeuring_
* Digikoppeling-Koppelvlakstandaard-GB [issue #13] [Gebruik van de S3 protocol om de payload te uploaden/downloaden](https://github.com/Logius-standaarden/Digikoppeling-Koppelvlakstandaard-GB/issues/13) (15 januari 2024), _Status: In onderzoek_
* Digikoppeling-Koppelvlakstandaard-ebMS2 [issue #6] [Digikoppeling baseren op ebMS3](https://github.com/Logius-standaarden/Digikoppeling-Koppelvlakstandaard-ebMS2/issues/6) (3 februari 2022), _Status: In onderzoek_

### Kleine wijzigingen
* OIN-Stelsel [issue #21] [Begrippenkader OIN](https://github.com/Logius-standaarden/OIN-Stelsel/issues/21) (25 maart 2024), _Status: In bewerking_

## Toelichting



## Digikoppeling Toekomstvisie : Scope en inzetgebied

In de [MIDO Domeinarchitectuur Gegevensuitwisseling](https://github.com/MinBZK/gdi-gegevensuitwisseling) zijn enkele mogelijke vernieuwingen en uitbreidingen voor Digikoppeling genoemd;

In de vorige sessie bespraken we gezamenlijk deze punten met als doel de toekomstvisie Digikoppeling nader te bepalen, in deze sessie bespreken we dit verder

Zie ook : [2025-03-19-TO-Digikoppeling-poll-results](https://github.com/Logius-standaarden/Overleg/blob/main/Digikoppeling/2025-06-10/2025-03-19-TO-Digikoppeling-poll-results.pdf)


## Overgang ebMS2 naar eDelivery ebMS3/AS4

### Bijlage - eDelivery 2.0
[eDelivery 2.0](https://ec.europa.eu/digital-building-blocks/sites/pages/viewpage.action?pageId=848625744) is eind vorig jaar uitgebracht


### Bijlage - PBLQ Rapport Impactanalyse Digikoppeling : Overgang ebMS2 naar eDelivery (ebMS3/AS4)

[PBLQ Rapport Impactanalyse modernisering Digikoppeling ebMS: 
van ebMS2 naar eDelivery (ebMS3/AS4)](https://github.com/Logius-standaarden/Overleg/blob/main/Digikoppeling/2024-03-06/Rapport%20Impactanalyse%20modernisering%20Digikoppeling%20ebMS%20-%20v1.1%20definitief%2019%20januari%202024.pdf)

## Onderzoek S3 - Grote Berichten

Alhoewel S3 niet open source is, bestaan er wel open source alternatieven die de S3 API nabootsen. Een populair alternatief is [MinIO](https://github.com/minio/minio) dat bij Digipoort is toegepast. Het is een open source project dat “S3 compatible” is door zelf een API te hebben gebouwd dat de S3 API volgt qua berichtformaat van een groot deel van de mogelijke operaties op basis van de publieke API-documentatie van Amazon.

## FSC Wijzigingsvoorstellen

_Ter goedkeuring voorgelegd aan het TO:_






