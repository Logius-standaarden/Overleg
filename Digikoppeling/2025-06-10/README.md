<!-----------------------------







   :warning: Dit bestand wordt automatisch gegenereerd.
   :warning: Handmatige toevoegingen worden overschreven.







----------------------------->
# Technisch Overleg Digikoppeling

dinsdag 10 juni 2025


# Concept / In Ontwikkeling

## Agenda

| Betreft                | Technisch Overleg Digikoppeling |
| ---------------------- | ------------------------------- |
| Vergaderdatum en -tijd | 10-06-2025, 10:00-12:00         |
| Vergaderplaats         | online |                         |

| Tijd | Onderwerp |Spreker|
| --- | --- | --- |  
| 10:00| Welkom & Mededelingen   <BR> -  _Consultatie WUS uitfasering_|    Peter Haasnoot (Logius) |
| 10:05| [Verslag vorige vergadering](https://github.com/Logius-standaarden/Overleg/blob/main/Digikoppeling/2025-03-19/2024-12-10%20%20Verslag%20TO%20Digikoppeling%20v1.0.pdf)       |    Peter Haasnoot (Logius) |
| 10:10 | [Digikoppeling Toekomstvisie : Stand van zaken](#digikoppeling-toekomstvisie) <BR>| Peter Haasnoot (Logius) | 
| 10:20  | [Overgang ebMS2 naar eDelivery ebMS3/AS4](#overgang-ebms2-naar-edelivery-ebms3as4) - Stand van Zaken / Vervolg  | Peter Haasnoot / Nil Barua (Logius)| 
| 10:30 | [Releaseplan Digikoppeling](https://github.com/orgs/Logius-standaarden/projects/4)      |    Alexander Green (Logius) |
| 10:35 | [Onderzoek S3 - Grote Berichten](#onderzoek-s3---grote-berichten) | Alexander Green (Logius) |
| 10:45  | OIN Stelsel - wijzigingen mbt buitenlandse partijen & nieuw OIN beleid<BR> | Peter Haasnoot  / Nil Barua (Logius)|
| 10:55 | _Pauze_ | _Allen_ |
|11:05| FSC Stand van zaken & Beheer | Stas Mironov (Logius)|
|11:10 | [FSC Wijzigingsvoorstellen](https://github.com/Logius-standaarden/fsc-core/pulls?q=is%3Apr+is%3Aopen+created%3A%3C%3D2025-02-01) | Ronald Koster (VNG)  |
|11:50  | Rondvraag / Afsluiting | Allen | 
|12:00 | Einde |

## Aanmelden

Dit overleg is openbaar. Aanmelden kan door te mailen naar digikoppeling@logius.nl

## Onderwerpen

### Grote wijzigingen
* Digikoppeling-Koppelvlakstandaard-GB [issue #13] [Gebruik van de S3 protocol om de payload te uploaden/downloaden](https://github.com/Logius-standaarden/Digikoppeling-Koppelvlakstandaard-GB/issues/13) (15 januari 2024), _Status: In onderzoek_
* Digikoppeling-Koppelvlakstandaard-ebMS2 [issue #6] [Digikoppeling baseren op ebMS3](https://github.com/Logius-standaarden/Digikoppeling-Koppelvlakstandaard-ebMS2/issues/6) (3 februari 2022), _Status: In onderzoek_

### Kleine wijzigingen
* OIN-Stelsel [issue #21] [Begrippenkader OIN](https://github.com/Logius-standaarden/OIN-Stelsel/issues/21) (25 maart 2024), _Status: In bewerking_

## Toelichting



## Digikoppeling Toekomstvisie : Scope en inzetgebied

In de [MIDO Domeinarchitectuur Gegevensuitwisseling](https://github.com/MinBZK/gdi-gegevensuitwisseling) zijn enkele mogelijke vernieuwingen en uitbreidingen voor Digikoppeling genoemd;

In de vorige sessie bespraken we gezamenlijk deze punten met als doel de toekomstvisie Digikoppeling nader te bepalen, in deze sessie een korte terugkoppeling;


## Overgang ebMS2 naar eDelivery ebMS3/AS4

### Bijlage - eDelivery 2.0
[eDelivery 2.0](https://ec.europa.eu/digital-building-blocks/sites/pages/viewpage.action?pageId=848625744) is eind vorig jaar uitgebracht


### Bijlage - PBLQ Rapport Impactanalyse Digikoppeling : Overgang ebMS2 naar eDelivery (ebMS3/AS4)

[PBLQ Rapport Impactanalyse modernisering Digikoppeling ebMS: 
van ebMS2 naar eDelivery (ebMS3/AS4)](https://github.com/Logius-standaarden/Overleg/blob/main/Digikoppeling/2024-03-06/Rapport%20Impactanalyse%20modernisering%20Digikoppeling%20ebMS%20-%20v1.1%20definitief%2019%20januari%202024.pdf)

## Onderzoek S3 - Grote Berichten

Alhoewel S3 niet open source is, bestaan er wel open source alternatieven die de S3 API nabootsen. Een populair alternatief is [MinIO](https://github.com/minio/minio) dat bij Digipoort is toegepast. Het is een open source project dat “S3 compatible” is door zelf een API te hebben gebouwd dat de S3 API volgt qua berichtformaat van een groot deel van de mogelijke operaties op basis van de publieke API-documentatie van Amazon.

## Uitfaseren koppelvlakstandaarden (WUS)

_(Concept)_



