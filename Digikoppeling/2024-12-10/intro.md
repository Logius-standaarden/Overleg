### Mededelingen

- Nieuwe Collega's

### Releaseplan

- [Digikoppeling Releaseplan](https://github.com/orgs/Logius-standaarden/projects/4)
- [Consultatie nieuwe Release](https://github.com/Logius-standaarden/Openbare-Consultaties/tree/master/20240919_Digikoppeling)

### FSC


...

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

1. XML kan ook via het DK REST API Koppelvlak
1. Signing en Encryptie zijn toegevoegd aan het REST-API koppelvlak in de komende release
4. Reliable messaging is buiten scope van het huidige WUS profiel

#### Voorstel vanuit Beheer

| Status | Toelichting | Datum |
| -------|--------------|------|
| END-OF-SUPPORT / Uit te faseren | ||
| END-OF-LIFE / Uitgefaseerd | | |


### Update Roadmap 2024-2025

https://github.com/Logius-standaarden/Digikoppeling-Algemeen/blob/roadmap_2024-2026/Digikoppeling_Roadmap_2024_2025.md
Toelichting actuele stand van zaken 
