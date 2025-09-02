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
| 10:00| Welkom & Mededelingen   <BR>- [Review Architectuur Q2](https://gitdocumentatie.logius.nl/publicatie/dk/roadmap/2024-2025/#periodiek-actualiseren-architectuur) afgerond (alleen [tekstuele verbeteringen](https://github.com/Logius-standaarden/Digikoppeling-Architectuur/pull/26/files)) |    Peter Haasnoot (Logius) |
| 10:05| [Verslag vorige vergadering](https://github.com/Logius-standaarden/Overleg/blob/main/Digikoppeling/2025-09-09/2025-06-10%20%20Verslag%20TO%20Digikoppeling%20v1.0.pdf)       |    Peter Haasnoot (Logius) |
|10:10| [Onderzoek S3 Grote Berichten](#onderzoek-s3---grote-berichten)| Alexander Green (Logius)|
| 10:20 | [Digikoppeling Toekomstvisie](#digikoppeling-toekomstvisie--scope-en-inzetgebied) <BR>| Dennis Passage / Peter Haasnoot (Logius) | 
| 10:45  | [Overgang ebMS2 naar eDelivery ebMS3/AS4](#overgang-ebms2-naar-edelivery-ebms3as4) - Invoering Standaard & Ondersteunende voorzieningen  | Peter Haasnoot / Nil Barua (Logius)| 
| 11:15  | [Wijzigingsvoorstel XML Signing/Encryptie - TLS 1.3](#xml-signing--encryptie---tls-13) |  Nil Barua (Logius)| 
|11:30| [Wijzigingsvoorstel WUS uitfasering - Stand van Zaken ](#uitfasering-wus)      |    Peter Haasnoot (Logius) |
|12:00| Lunch | Allen|
|12:45| FSC Stand van zaken & Beheer | Stas Mironov (Logius)|
|13:00 | [FSC Wijzigingsvoorstellen](#fsc-wijzigingsvoorstellen) <BR> _Wijziging wordt ter goedkeuring aan het TO voorgelegd_ | Niels de Queker (VNG)  |
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



## Onderzoek S3 - Grote Berichten

Alhoewel S3 niet open source is, bestaan er wel open source alternatieven die de S3 API nabootsen. Een populair alternatief is [MinIO](https://github.com/minio/minio) dat bij Digipoort is toegepast. Het is een open source project dat “S3 compatible” is door zelf een API te hebben gebouwd dat de S3 API volgt qua berichtformaat van een groot deel van de mogelijke operaties op basis van de publieke API-documentatie van Amazon.


## Digikoppeling Toekomstvisie : Scope en inzetgebied

In de [MIDO Domeinarchitectuur Gegevensuitwisseling](https://github.com/MinBZK/gdi-gegevensuitwisseling) zijn enkele mogelijke vernieuwingen en uitbreidingen voor Digikoppeling genoemd;

In de vorige sessie bespraken we gezamenlijk deze punten met als doel de toekomstvisie Digikoppeling nader te bepalen, in deze sessie bespreken we dit verder.

Zie [Toekomstvisie Digikoppeling](https://github.com/Logius-standaarden/Overleg/blob/main/Digikoppeling/2025-09-09/2025-09-09_Toekomstvisie%20Digikoppeling.md)

_Het TO wordt gevraagd goedkeuring te geven aan de toekomstvisie, deze zal dan basis zijn voor de toekomstige aanpassingen en ontwikkelrichting van de standaard en de roadmap voor 2026-2027_

Zie ook : 
- [2025-03-19-TO-Digikoppeling-poll-results](https://github.com/Logius-standaarden/Overleg/blob/main/Digikoppeling/2025-06-10/2025-03-19-TO-Digikoppeling-poll-results.pdf)
- [Enquete ebMS2/3 Polls-per-participant-2025-06-10_TO_Digikoppeling](https://github.com/Logius-standaarden/Overleg/blob/main/Digikoppeling/2025-09-09/Polls-per-participant-2025-06-10_TO_Digikoppeling_Totaal.xlsx)


## Overgang ebMS2 naar eDelivery ebMS3/AS4

Zie Notitie : [Notitie_Vervanging_Digikoppeling_ebMS2_door_eDelivery_ebMS3_AS4](https://github.com/Logius-standaarden/Overleg/blob/main/Digikoppeling/2025-09-09/2025_09_09_Notitie_Vervanging_Digikoppeling_ebMS2_door_eDelivery_ebMS3_AS4.md)

_Het TO wordt gevraagd in te stemmen met het voorstel om ebMS3/AS4 als vervanger van ebMS2 toe te voegen aan de standaard_

### Bijlage - eDelivery 2.0
[eDelivery 2.0](https://ec.europa.eu/digital-building-blocks/sites/pages/viewpage.action?pageId=848625744) is eind vorig jaar uitgebracht


### Bijlage - PBLQ Rapport Impactanalyse Digikoppeling : Overgang ebMS2 naar eDelivery (ebMS3/AS4)

[PBLQ Rapport Impactanalyse modernisering Digikoppeling ebMS: 
van ebMS2 naar eDelivery (ebMS3/AS4)](https://github.com/Logius-standaarden/Overleg/blob/main/Digikoppeling/2024-03-06/Rapport%20Impactanalyse%20modernisering%20Digikoppeling%20ebMS%20-%20v1.1%20definitief%2019%20januari%202024.pdf)


## XML Signing & Encryptie - TLS 1.3

### Wijziginsvoorstel XML Signing & Encryptie
Ter goedkeuring voorgelegd aan het TO:

[Wijzigingsvoorstel XML Signing & Encryptie](https://github.com/Logius-standaarden/Digikoppeling-Beveiligingsstandaarden-en-voorschriften/pull/17)

[Preview / Diff - Wijzigingsvoorstel XML Signing & Encryptie](https://services.w3.org/htmldiff?doc1=https://logius-standaarden.github.io/Digikoppeling-Beveiligingsstandaarden-en-voorschriften&doc2=https://logius-standaarden.github.io/Publicatie-Preview/Digikoppeling-Beveiligingsstandaarden-en-voorschriften/Nil-NMB01-patch-1#xml-signing)

### TLS 1.3

Discussie - is aanscherping van TLS 1.3 richtlijn wenselijk n.a.v. [nieuwe NSCS richtlijnen](https://www.ncsc.nl/documenten/publicaties/2025/juni/01/ict-beveiligingsrichtlijnen-voor-transport-layer-security-2025-05) 

Huidige TLS afspraken : [Digikoppeling beveiligingsvoorschriften](https://gitdocumentatie.logius.nl/publicatie/dk/beveilig/2.0.1/#tls-transport-layer-security)

## Uitfasering WUS

Vanuit de publieke consultatie waren we geen opmerkingen, het voorstel is 20/8 in de programmeringstafel GU besproken. De programmeringstafel GU heeft gevraagd eerst nader onderzoek te doen naar de impact op GDI en organisaties - voordat dit formeel kan worden aangenomen.

## FSC Wijzigingsvoorstellen

_Ter goedkeuring voorgelegd aan het TO:_

[Add properties object to Grants & update hashing algorithm (breaking)](https://github.com/Logius-standaarden/fsc-core/pull/25)






