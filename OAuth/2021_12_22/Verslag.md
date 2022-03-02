# Verslag - Technische Architectuur Groep OAuth-NL

datum: 22-12-2021
status: concept

## Aanwezigen
| Voornaam  | Achternaam   | Organisatie |
| :-------- | :----------- | ----------: |
| Alexander | Green        |      Logius |
| Martin    | Van der Plas |      Logius |
| Frank     | Terpstra     |    Geonovum |
| Hans      | Hendrikman   |        RVIG |
| Hans      | Oostrom      |    Waternet |
| John      | Zwart        |        RVDK |
| Patrick   | Reijnen      |         KvK |
| Peter     | Haasnoot     |      Logius |
| Remco     | Schaar       |      Logius |
| Heiko     | Hudig        |     Politie |
| Lana      | Vredenduin   |    Enable U |
| Jan Jaap  | Zoutendijk   |    Enable U |

## Afwezig / Afgemeld
| Voornaam | Achternaam | Organisatie |
| :------- | :--------- | ----------: |
| Frank    | van Es     |      Logius |
| Arnoud   | Quanjer    |         VNG |
| Joost    | Farla      |    Kadaster |
| Erwin    | Reinhoud   |   Kennisnet |
| Martin   | Borgman    |    Kadaster |
| Bob      | te Riele   |        RVIG |
| Jaron    | Azaria     |       Arpha |



## De vastgestelde agenda van het overleg :
1. Aftrap en kennismaking

2. Presentatie beheermodel - zie [Beheermodel OAuth-NL (logius-standaarden.github.io)](https://logius-standaarden.github.io/OAuth-Beheermodel/)

3. Vaststellen beheermodel

4.	Werkgroep client credentials flow samenstellen

5. Doornemen openstaande issues - zie https://github.com/Logius-standaarden/OAuth-NL-profiel/issues )

6. Toelichten Pleio omgeving voor Interesse Groep (IG) - zie de [digistandaarden community (pleio.nl)](https://digistandaarden.pleio.nl/groups/view/20c41e94-9a56-423e-b8fb-14a62355858f/api-standaarden)

7. Inventarisatie gebruik in de praktijk zowel huidig als toekomstig

8. Rondvraag en afsluiting

   


## Verslag

### 1. Agendapunt 1: Aftrap en kennismaking

De agenda wordt vastgesteld en iedereen stelt zich voor. Een aantal mededelingen:

- in Pleio zijn de OAuth-NL en ADR initatieven samngevoegd tot de groep API standaarden. hier komt op termijn de OIDC standaard nog bij.
- Een aantal mensen heeft de afspraak voorlopig geaccepteerd of zich afgemeld en aangegeven volgende keer wel graag deel te nemen. In het verslag zijn deze personen opgenomen als afwezig/afgemeld. 
- De term NLGov gaat mogelijk nog een hoge vlucht nemen, ik heb al van twee andere (niet direct gerelateerde)standaarden gehoord die dat in hun naam willen opnemen.

### 2. Agendapunt 2: Presentatie beheermodel

[De powerpoint](https://logius-standaarden.github.io/OAuth-Beheermodel/) met de highlights en modellen zoals gepubliceerd op github wordt doorgenomen en er volgt een korte discussie en wat toelichting in de chat:

- MIDO staat voor Meerjarenprogramma Infrastructuur Digitale Overheid en ziet op de Generieke Digitale Infrastructuur.

- OBDO staat voor Overheidsbreed Beleidsoverleg Digitale Overheid

- er wordt gerefereerd aan de https://www.noraonline.nl/wiki/Gemeenschappelijke_Overheidsarchitectuur_(GO) en https://www.noraonline.nl/wiki/Identity_%26_Access_Management_(IAM).
- er wordt aandacht gevraagd voor de publieke review van de NORA en Martin geeft aan dat deze nog wordt gereviewd om te borgen dat de standaarden van BFS (Bureau Forum Standaardisatie) goed in beeld worden gebracht in de NORA. zie ook: https://www.noraonline.nl/wiki/Publieke_review_Kernwaarden_van_Dienstverlening_en_bijbehorende_Kwaliteitsdoelen_en_Architectuurprincipes?pk_campaign=Gebruikersraad
- Aandachtspunten nav de presentatie door John: is het mogelijk om de interactiepatronen van het profiel in een algemeen toegankelijke impressie weer te geven. Zie ook het pdf voorbeeld wat is gedeeld [(link)](https://github.com/Logius-standaarden/OAuth-NL_Vergaderstukken/tree/main/20211222)



### 3. Agendapunt 3: Vaststellen beheermodel

Het beheermodel wordt vastgesteld door de aanwezigen. De definitieve versie is gepubliceerd op https://logius-standaarden.github.io/OAuth-Beheermodel/



### 4. Agendapunt 4: Werkgroep client credentials flow

Jan Jaap geeft aan ook deel te willen nemen aan de werkgroep. Er is een korte discussie over de historie waarom deze niet eerder is opgenomen en welke andere generieke mogelijkheden nog relevant zijn voor een werkgroep, bijvoorbeeld Scopes.

### 5. Agendapunt 5: Doornemen openstaande issues

 De openstaande issues zoals beschikbaar op https://github.com/Logius-standaarden/OAuth-NL-profiel/issues worden doorgenomen.

- [Issue #17](https://github.com/Logius-standaarden/OAuth-NL-profiel/issues/17) is gesloten, deze was dubbel.
- voor [Issue #8 is een MR gemaakt](https://github.com/Logius-standaarden/OAuth-NL-profiel/issues/8)
- [Issue #11](https://github.com/Logius-standaarden/OAuth-NL-profiel/issues/11) kunnen we toelichten en sluiten
- [Issue #7](https://github.com/Logius-standaarden/OAuth-NL-profiel/issues/7) pakken Martin en Remco samen op.
- [Issue #3](https://github.com/Logius-standaarden/OAuth-NL-profiel/issues/3) wordt door de werkgroep client credentials flow opgepakt.

### 6. Agendapunt 6: Toelichten Pleio omgeving voor Interesse Groep (IG) - 
- zie de [digistandaarden community (pleio.nl)](https://digistandaarden.pleio.nl/groups/view/20c41e94-9a56-423e-b8fb-14a62355858f/api-standaarden).

- de recent aangepaste pagina's en werking/indeling van de groepen is toegelicht.

### 7. Agendapunt 7: Inventarisatie gebruik in de praktijk zowel huidig als toekomstig

- Jan Jaap licht toe dat de OAuth & OIDC standaarden bij DSO worden gebruikt. of ook de NL-Gov profielen worden gebruikt is niet helemaal zeker. Ook is er een wens vanuit gemeent Tilburg on de standaarden toe te gaan passen.
- Remco meld dat de standaarden bij de TVS worden gebruikt en dat logius ze intern gebruikt voor DigiD Machtigen. wellicht kan Frank van Es dit in een volgend overleg toelichten.
- Heiko geeft aan dat de standaarden intern bij de politie worden gebruikt en ook in de keten met het NFI en het OM is men bezig de standaarden toe te passen, dit is echter de eerste use case.

### 8. Agendapunt 8: Rondvraag en afsluiting

- geen bijzonderheden
