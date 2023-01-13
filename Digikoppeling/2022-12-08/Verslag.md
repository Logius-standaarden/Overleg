# Verslag Technisch Overleg Digikoppeling

8 december 2022

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

### Wijzigingen

De volgende voorstellen zijn goedgekeurd door het TO:

#### Digikoppeling-Handreiking-Adressering-en-Routering
* [RFC Voor wie werkt een SAAS eigenlijk](https://github.com/Logius-standaarden/Digikoppeling-Handreiking-Adressering-en-Routering/issues/4) | [Voorgestelde aanpassing](https://github.com/Logius-standaarden/Digikoppeling-Handreiking-Adressering-en-Routering/pull/7/files)
* [PKI sleutel deponeren?](https://github.com/Logius-standaarden/Digikoppeling-Handreiking-Adressering-en-Routering/issues/3) | [Voorgestelde aanpassing](https://github.com/Logius-standaarden/Digikoppeling-Handreiking-Adressering-en-Routering/pull/6/files)
* [Routeren op de berichtbody](https://github.com/Logius-standaarden/Digikoppeling-Handreiking-Adressering-en-Routering/issues/2) | [Voorgestelde aanpassing](https://github.com/Logius-standaarden/Digikoppeling-Handreiking-Adressering-en-Routering/pull/5/files)

#### Digikoppeling-Architectuur
* [Periodieke review](https://github.com/Logius-standaarden/Digikoppeling-Architectuur/pull/11) | [Voorgestelde aanpassing](https://github.com/Logius-standaarden/Digikoppeling-Architectuur/pull/11/files)
* [Verantwoordelijkheid voor informatiebeveiliging](https://github.com/Logius-standaarden/Digikoppeling-Architectuur/pull/3) | [Voorgestelde aanpassing](https://github.com/Logius-standaarden/Digikoppeling-Architectuur/pull/3/files)


### Status API-58 in ADR extensie beveiliging

Zie [Update ext-security.md API-58](https://github.com/Geonovum/KP-APIs/pull/464)

Voorstel is nav de bespreking van API-58 in de werkgroep Beveiliging van het Kennisplatform API's een toelichting toe te voegen aan API-58 in het Digikoppeling REST API profiel.

TO is hiermee akkoord.

### Gebruik eIDAS certificaten voor signing in Digikoppeling

Vraag/Discussie: (hoe) worden eIDAS certificaten gebruikt op dit moment?

Op dit moment speelt dit niet bij de TO-leden.
