### Mededelingen

- Nieuwe Collega's

### Releaseplan

- [Digikoppeling Releaseplan](https://github.com/orgs/Logius-standaarden/projects/4)
- [Consultatie nieuwe Release](https://github.com/Logius-standaarden/Openbare-Consultaties/tree/master/20240919_Digikoppeling)

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
  
#### Reactie DICTU ,

Op de agendering van het onderwerp in het vorige TO is een reaktie van DICTU ingebracht:

_Op dit moment geen voorstander van het uitfaseren van WUS:_

1.	XML kun je controleren tegen een XSD. Op dit moment is daar voor REST nog geen standaard voor (JSON Schema is nog geen standaard).
1.  Op dit moment hebben we geen standaard voor signing en encryptie in REST (staat nu op de agenda), dus heb je voorlopig WUS nog nodig als standaard
1.	SOAP/XML kent functies. In de ADR staat een aanwijzing voor functies (GET of POST) maar dat is niet zo goed beschreven als dat bij SOAP wel is.
1.	Reliable Messaging is een feature in WUS en niet in REST (maar ik vraag me af of dit in de praktijk wordt gebruikt?)

_Naar mijn idee is het daarom op dit moment te vroeg om WUS uit te faseren._

Opmerking vanuit beheer hierbij als input voor de bespreking:

1. XML kan ook via het DK REST-API Koppelvlak
1. Signing en Encryptie zijn toegevoegd aan het DK REST-API koppelvlak in de komende  Digikoppeling release
4. Reliable messaging is buiten scope van het huidige WUS profiel

#### Voorstel vanuit Beheer

| Status | Toelichting | Datum |
| -------|--------------|------|
|  Uit te faseren | Het DK WUS koppelvlak dient te worden uit gefaseerd |  xx-xx-xx Einde Ondersteuning |
|  Buiten gebruik | Het DK WUS koppelvlak is verwijderd uit de actuele versie van de standaard | xx-xx-xx End-of-Life |


### Update Roadmap 2024-2025

https://github.com/Logius-standaarden/Digikoppeling-Algemeen/blob/roadmap_2024-2026/Digikoppeling_Roadmap_2024_2025.md
Toelichting actuele stand van zaken 
