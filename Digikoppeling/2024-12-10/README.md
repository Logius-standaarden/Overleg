<!-----------------------------







   :warning: Dit bestand wordt automatisch gegenereerd.
   :warning: Handmatige toevoegingen worden overschreven.







----------------------------->
# Technisch Overleg Digikoppeling

dinsdag 10 december 2024

## Agenda 

| Betreft                | Technisch Overleg Digikoppeling |
| ---------------------- | ------------------------------- |
| Vergaderdatum en -tijd | 10-12-2024, 10:00-11:45         |
| Vergaderplaats         | online                          |

| Tijd | Onderwerp |Spreker|
| --- | --- | --- |  
| 10:00| Welkom & Mededelingen        |    Peter Haasnoot |
| 10:05| [Verslag vorige vergadering](https://github.com/Logius-standaarden/Overleg/blob/main/Digikoppeling/2024-12-10/2024-09-19%20%20Verslag%20TO%20Digikoppeling%20v1.0..pdf)       |    Peter Haasnoot |
| 10:10 | [Wijzigingsvoorstel FSC](https://github.com/Logius-standaarden/Digikoppeling-Koppelvlakstandaard-REST-API/issues/26) <BR>- Stand van Zaken,  Zie [Behandeling FSC in MIDO](#fsc-wijzigingsvoorstel)| Peter Haasnoot | 
| 10:40| Consultatie & Releaseplan      |    Alexander Green |
| 10:50| Grote en kleine wijzigingen | Peter Haasnoot / Alexander Green | 
| 11:00 | _Pauze_ | _Allen_ |
| 11:05  | eDelivery ebMS3 Wijzigingsvoorstel - Stand van Zaken / Vervolg | Peter Haasnoot / Nil Barua| 
| 11:15  | Uitfaseren koppelvlakstandaarden (WUS)<BR> - _Behandelen [reactie vanuit DICTU](#reactie-dictu)_| Peter Haasnoot |
| 11:25 | [Roadmap 2024-2025](https://github.com/Logius-standaarden/Digikoppeling-Algemeen/blob/roadmap_2024-2026/Digikoppeling_Roadmap_2024_2025.md#tijdlijn-roadmap-digikoppeling-standaarden) <BR>- Best practice Gebruik OAuth i.c.m. Digikoppeling REST_API|Peter Haasnoot|
| 11:30 | Uitbreidingen - bijv. Digikoppeling uitbreiden met [GraphQL](https://graphql.org/)   | Allen | 
| 11:40  | Rondvraag / Afsluiting | Allen | 
| 11:45 | Einde |

## Onderwerpen

### Grote wijzigingen
* Digikoppeling-Koppelvlakstandaard-GB [issue #13] [Gebruik van de S3 protocol om de payload te uploaden/downloaden](https://github.com/Logius-standaarden/Digikoppeling-Koppelvlakstandaard-GB/issues/13) (15 januari 2024), _Status: In onderzoek_
* Digikoppeling-Koppelvlakstandaard-REST-API [issue #26] [Federatieve Service Connectiviteit opnemen in het Digikoppeling voor REST API's profiel](https://github.com/Logius-standaarden/Digikoppeling-Koppelvlakstandaard-REST-API/issues/26) (18 december 2023), _Status: In bewerking_
  * [Wijzigingsvoorstel](https://github.com//Logius-standaarden/Digikoppeling-Architectuur/pull/14/files)
* Digikoppeling-Koppelvlakstandaard-ebMS2 [issue #6] [Digikoppeling baseren op ebMS3](https://github.com/Logius-standaarden/Digikoppeling-Koppelvlakstandaard-ebMS2/issues/6) (3 februari 2022), _Status: In onderzoek_

### Kleine wijzigingen
* Digikoppeling-Architectuur [issue #16] [Update b_dk_bijlage_begrippen.md](https://github.com/Logius-standaarden/Digikoppeling-Architectuur/pull/16) (27 september 2024), _Status: Ter goedkeuring_
* OIN-Stelsel [issue #21] [Begrippenkader OIN](https://github.com/Logius-standaarden/OIN-Stelsel/issues/21) (25 maart 2024), _Status: In bewerking_
  * [Wijzigingsvoorstel](https://github.com//Logius-standaarden/OIN-Stelsel/pull/20/files)

## Toelichting


### Mededelingen

- Nieuwe Collega's

### Consultatie & Releaseplan

- [Consultatie nieuwe Release](https://github.com/Logius-standaarden/Openbare-Consultaties/tree/master/20240919_Digikoppeling)

- [Digikoppeling Releaseplan](https://github.com/orgs/Logius-standaarden/projects/4)

Uit de publieke consultatie zijn geen opmerkingen gekomen, Het TO wordt gevraagd akkoord te gaan met het opnemen van de voorgenomen wijzigingen in de volgende release - conform het releaseplan

### FSC Wijzigingsvoorstel

#### Behandeling MIDO Programmeringstafel Gegevensuitwisseling
"Federated Service Connectivity (FSC) standaard opnemen in het Digikoppeling REST-API profiel als aanbevolen" is 20/11 behandeld bij de MIDO Programmeringstafel Gegevensuitwisseling

Advies vanuit MIDO WG Architectuur Gegevensuitwisseling was FSC op te nemen als verplicht 

De Programmeringstafel GU heeft de MIDO Programmeringsraad geadviseerd om FSC op te nemen in het Digikoppeling REST-API profiel als verplicht (onder het pas-toe-of-leg-uit beleid van het Forum Standaardisatie zoals dat geldt voor Digikoppeling).


#### Stukken MIDO Programmeringstafel Gegevensuitwisseling 20/11

- [Aanbiedingsformulier Aanbieden FSC standaard.pdf](https://pgdi.nl/files/view/ecbd5947-f632-4d94-aa16-cc5c486d47e5/20241120-pt-gu-4a.pdf)

- [Logius Notitie Aanbieden FSC standaard_v1.1.pdf](https://pgdi.nl/files/view/e900f4d0-52d4-4d57-9542-fe6abe984d8c/20241120-pt-gu-4b.pdf)

- [Bijlage A - FSC Kwalitatieve businesscase & Implementatie.pdf](https://pgdi.nl/files/view/62ffdc35-702c-4997-b3fd-fbd290a112cc/20241120-pt-gu-4c.pdf)

- [Bijlage B - Behandeling in Technisch Overleg Digikoppeling & Scenario’s.pdf](https://pgdi.nl/files/view/ea2ed7e8-b50a-4769-a528-ffe1218d7d28/20241120-pt-gu-4d.pdf)

- [Advies van Werkgroep Gegevensuitwisseling over FSC.pdf](https://pgdi.nl/files/view/0c6d1df1-6db9-4407-aebd-eda726033804/20241120-pt-gu-4e.pdf)

#### Advies van MIDO Programmeringstafel Gegevensuitwisseling aan Programmeringsraad

- [MIDO Programmeringsraad : fsc-standaard-opnemen-in-digikoppeling-rest-api-profiel.pdf]( https://pgdi.nl/files/view/af4d8546-1787-43bc-b23e-83a099a2a5f7/20241212-pgdi-06-fsc-standaard-opnemen-in-digikoppeling-rest-api-profiel.pdf)



### eDelivery stand van zaken en vervolg (ter informatie)

Het PBLQ rapport is na bespreking in het TO geagendeerd in de Programmeringstafel GU van 27 maart. Leden van de programmeringstafel hebben
voorgesteld de eDelivery _standaard_ los te koppelen van het _construct_. Het construct omvat de componenten en diensten die nodig zijn een eDelivery 
netwerk op te zetten.
Het construct eDelivery is nog onderwerp van nader onderzoek en afhankelijk van besluitvorming in het MIDO

### Uitfasering WUS

#### Aanleiding/Achtergrond

Aanleiding om dit onderwerp te bespreken:
- Ondersteuning van WS-I in de grote platformen loopt terug
- De wens is geuit in eerdere TO discussies om het aantal koppelvlakken te verminderen (en het nieuwe API koppelvlak is een alternatief voor WUS)
  
#### Reactie DICTU

Op de agendering van het onderwerp in het vorige TO is een reactie van DICTU ingebracht:

> _Op dit moment geen voorstander van het uitfaseren van WUS:_
> 
> 1.	XML kun je controleren tegen een XSD. Op dit moment is daar voor REST nog geen standaard voor (JSON Schema is nog geen standaard).
> 1.  Op dit moment hebben we geen standaard voor signing en encryptie in REST (staat nu op de agenda), dus heb je voorlopig WUS nog nodig als standaard
> 1.	SOAP/XML kent functies. In de ADR staat een aanwijzing voor functies (GET of POST) maar dat is niet zo goed beschreven als dat bij SOAP wel is.
> 1.	Reliable Messaging is een feature in WUS en niet in REST (maar ik vraag me af of dit in de praktijk wordt gebruikt?)
> 
> _Naar mijn idee is het daarom op dit moment te vroeg om WUS uit te faseren._

Opmerking vanuit beheer hierbij als input voor de bespreking:

> - XML kan ook via het DK REST-API Koppelvlak
> - Signing en Encryptie zijn toegevoegd aan het DK REST-API koppelvlak in de komende  Digikoppeling release
> - Reliable messaging is buiten scope van het huidige WUS profiel

#### Voorstel vanuit Beheer

In het kader van Life-Cycle Management van de Koppelvlakstandaarden krijgt het DK WUS Koppelvlak de status "Uit te faseren" als volgt:

Koppelvlak Standaard| Status | Toelichting | Einde Ondersteuning| Einde Gebruik |
|----| -------|--------------|------|---|
|Digikoppeling WUS |  Uit te faseren | Het DK WUS koppelvlak dient te worden uit gefaseerd |  01-01-2027  | 01-01-2032|


•	Na 01-01-2027 is gebruik nog toegestaan voor legacy applicaties tot 01-01-2032 - echter de organisatie is zelf verantwoordelijk voor functionele en security updates;




### Update Roadmap 2024-2025

https://github.com/Logius-standaarden/Digikoppeling-Algemeen/blob/roadmap_2024-2026/Digikoppeling_Roadmap_2024_2025.md
Toelichting actuele stand van zaken 
