# Technisch Overleg Digikoppeling

14 december 2023

## Aanwezigen

| Naam                 | Organisatie |
|----------------------|-------------|
| Backer, Mark         | VNG         |
| Bijen, Antoon        | Justid      |
| De Boer, Karl        | Enable-U    |
| Emous, Ruth          | PBLQ        |
| Fieten. Sander       | Chasquis    |
| Green, Alexander     | Logius      |
| IJzermans, Jochem    | UWV         |
| Maas, Frits          | KVK         |
| Minnecré, Piet Hein  | PBLQ        |
| Seignette, Peter     | PBLQ        |
| Reinhoud, Erwin      | Kennisnet   |
| Sinnige, Hans        | RINIS       |
| Van der Plas, Martin | Logius      |
| Van Gelderen, Edward | VNG         |
| Van Kester, Jos      | VNG         |
| Velde, Johan van der | RDW         |
| Wellink, Lizzy       | Logius      |
| Welmer, Han          | TNO         |
| Wisse, Edwin         | Logius      |
| Zwaan, Tonkie        | BKWI        |

## Notulen vorig TO

[TO Digikoppeling 28 september 2023](https://github.com/Logius-standaarden/Overleg/blob/main/Digikoppeling/2023-09-28/notulen.md)

## Onderwerpen

### eDelivery EBMS3/AS4 stakeholderonderzoek (PBLQ)
Het rapport van de impact analyse over de transitie van ebMS2 naar ebMS3/AS4 is beschikbaar gemaakt:
* [Rapport Impactanalyse modernisering Digikoppeling ebMS](https://github.com/Logius-standaarden/Overleg/blob/main/Digikoppeling/2023-12-14/Rapport%20Impactanalyse%20modernisering%20Digikoppeling%20ebMS%20-%20definitief%208%20december%202023.pdf)
* [Roadmap Impactanalyse Modernisering Digikoppeling ebMS](https://github.com/Logius-standaarden/Overleg/blob/main/Digikoppeling/2023-12-14/Roadmap%20Impactanalyse%20Modernisering%20Digikoppeling%20ebMS%20-%20bijlage%20definitief%20rapport.pdf)

Justitie werkt aan een interne impact analyse; Antoon Bijen meldt dat hij het eerste stuk reeds heeft opgeleverd en deelt dat naar verwachting 20% van de koppelingen hierdoor geraakt zouden worden. Binnen enkele weken kan het stuk gedeeld kunnen worden.

Sander Fieten: Betekent die 20% dat een deel van de koppelingen niet overgezet gaat worden?

Antoon Bijen: Het zou een optie kunnen zijn om eerst de koppelingen aan te passen die binnen het toepassingsgebied van Digikoppeling passen en de interne koppelingen nog niet.

### Grote en kleine wijzigingen

#### Digikoppeling baseren op ebMS3

Impact analyse is reeds behandeld.

#### Signing & Encryptie toevoegen aan RESTful API profiel

De Werkgroep Security van het kennisplatform API’s werkt aan een module voor Signing & Encryptie. Op dit moment is men nog opzoek naar feedback/ervaring om in de module te kunnen verwerken. In de eerstvolgende werkgroep zal dit onderwerp verder besproken worden.

Karl de Boer: Wij wachten op besluitvorming zodat wij kunnen beginnen met implementeren.

### Roadmap: (concept) 2024-2025

#### Digikoppeling REST API profiel baseren op ADR 2.0

Binnen de werkgroep Design Rules is REST API Design Rules versie 2.0 gelanceerd. Hier zijn een aantal minor wijzigingen in aangebracht waaronder de opmaak en de structuur, maar ook een aantal inhoudelijke wijzigingen. De geomodule is vastgesteld en verplicht gesteld voor API’s gebaseerd op geodata. Een tweede inhoudelijke wijziging is het verplicht stellen van de Transport Security module. Dit bevat onder andere een verplichting tot het gebruik van TLS.

#### Signing & Encryptie toevoegen aan RESTful API profiel

Reeds besproken

#### Implementatie invoering eDelivery/ebMS3/AS4

Reeds besproken

#### Aansluiting FSC standaard op Digikoppeling

De standaard is omgezet van IETF-formaat naar een formaat dat meer in samenloopt met Digikoppeling. Er wordt gewerkt aan een begeleidende tekst in de Digikoppeling REST API koppelvlakstandaard.

#### Best practice Gebruik OAuth icm Digikoppeling REST_API

Oauth 2.0 biedt mogelijkheden tot gedetaileerde rechtendelegatie. Er is een Nederlands profiel geschreven op deze standaard (NLGOV). Hierin mist nog de Client Credentials Flow voor Machine-to-Machine-verkeer. Er staat een wijzigingsvoorstel klaar om deze toe te voegen. Wanneer dit gedaan is zou het als autorisatieoptie aan het REST API koppelvlak van Digikoppeling toegevoegd kunnen worden. Een Best Practice document staat voor de tweede helft van 2024 in de planning.

Edward van Gelderen merkt op dat dit enorme raakvlakken heeft met FSC.

Karl de Boer voegt toe dat bij Haal Centraal ook uitgegaan wordt van de Client Credentials Flow.

#### Opmerking

De volgende bijeenkomst van het Kennisplatsform API’s is 27 februari 2024 te Utrecht.

https://www.geonovum.nl/over-geonovum/agenda/kennisplatform-apis

