# Verslag Technisch Overleg Digikoppeling

12 devember 2022

## Aanwezigen

| Achternaam     | Voornaam  | Organisatie     |
|----------------|-----------|-----------------|
| Bijen          | Antoon    | Justid          |
| De Boer        | Karl      | enable-u        |
| De Bruijn      | Rick      | Logius          |
| Green          | Alexander | Logius          |
| Groot Roessink | Gerald    | DUO             |
| Haasnoot       | Peter     | Logius          |
| IJzermans      | Jochem    | UWV             |
| Kuiper         | Erwin     | Dictu           |
| Pauw           | Elzo      | UWV             |
| Quanjer        | Arnoud    | VNG             |
| Reinhoud       | Erwin     | Kennisnet       |
| Van den Brink  | Melis     | Belastingdienst |
| Van der Plas   | Martin    | Logius          |
| Van der Velde  | Johan     | RDW             |
| Van Kester     | Jos       | VNG             |
| Vennekens      | Ivar      | Ictu            |
| Welmer         | Han       | TNO             |
| Wisse          | Edwin     | Logius          |

## Onderwerpen

### OOTS toelichting door Ivar Vennekens

Slides zijn [hier](2022-12-08_SDG_OOTS_TO-DK.pptx) te vinden (pptx).

Vraag Wisse: eDelivery REST API. Volgens document EU is het nog pilot. Heeft het een officiële status?

Vennekens: Het is officieel opgenomen in het testplatform. Specificaties nog niet in beton gegoten, maar kans op wijziging lijkt me klein.

Groot Roessink: Browser redirect wordt toegepast?

Vennekens: Gebruiker wordt doorgestuurd naar andere URL, maar dit is front-end. Volgt de emrex systematiek.

Van den Brink: RegRep vooral SOAP XML, hoe verhoudt zich dat met REST?

Vennekens: Berichten via OOTS zijn volledig gespecificeerd in RegRep Query protocol. De manier van uitwisseling kan via AS4, maar nu ook via REST.

Groot Roessink: Aanvulling: RegRep is vrij recent gestandaardiseerd. Bedoeld voor request-respons in tegenstelling tot AS4-asynchroon.

Van der Plas: Zijn de evidence broker en data service directory Europees centraal systemen?

Vennekens: Centraal aangeboden, maar nationale voorzieningen zijn toegestaan. Verwijzing is wel altijd centraal.
