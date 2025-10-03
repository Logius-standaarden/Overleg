<!-----------------------------







   :warning: Dit bestand wordt automatisch gegenereerd.
   :warning: Handmatige toevoegingen worden overschreven.







----------------------------->
# Technisch Overleg OAuth

donderdag 9 oktober 2025

## Agenda

| Tijd  | Onderwerp                                     |
| ----- | --------------------------------------------- |
| 10:00 | Mededelingen                                  |
| 10:10 | Bespreken [onderstaande punten](#punten)      |
| 10:40 | Bespreken [toepassingsgebied](#toepassingsgebied)|
| 10:50 | Bespreken [onderstaande issues](#onderwerpen) |
| 11:10 | Rondvraag / Afsluiting                        |

## Mededelingen

- Updates vanuit domein toegang: voortgang uitfaseren oude koppelvlakken 
- OIDC versnellen - focus

## Punten

Inhoudelijk aandacht voor de volgende punten:
- RAR
- Feedback van de solution architect van het integratieteam bij de Politie
- DPoP vs mTLS
  - sender-constrained
  - schaalbaarheid doordat RS alleen tokens hoeft te checken i.p.v. certificaten
- Heeft OAuth plek in DK?

## Toepassingsgebied

Tijdens het intakegesprek bij het Forum is aan ons gevraagd of de huidige versie van het functioneel toepassings gebied (oorspronkelijk uit 2017) nog wel correct en/of relevant was.

:pushpin: Gelieve dit voorstel alvorens het overleg door te nemen en indien gewenst reageren:
- https://github.com/Logius-standaarden/OAuth-NL-profiel/issues/126

## Aanmelden

Dit overleg is openbaar. Aanmelden kan door te mailen naar api@logius.nl

## Onderwerpen

### Overige punten
* OIDC-NLGOV [issue #31] [Sender constrained access tokens wel of juist niet verplicht stellen in NLGOV](https://github.com/Logius-standaarden/OIDC-NLGOV/issues/31) (27 mei 2025)
* OAuth-NL-profiel [issue #106] [[iGOV] Afschaffen van public clients in het profiel](https://github.com/Logius-standaarden/OAuth-NL-profiel/issues/106) (22 april 2025), _Status: In onderzoek_
* OIDC-NLGOV [issue #12] [[bug] De betekenis van 'sub' is niet compatibel met de OAuth 2.0 standaard](https://github.com/Logius-standaarden/OIDC-NLGOV/issues/12) (3 december 2024), _Status: In onderzoek_
* OAuth-NL-profiel [issue #59] [Use cases voor: Rich Authorization request (RAR, rfc9396)](https://github.com/Logius-standaarden/OAuth-NL-profiel/issues/59) (2 augustus 2024), _Status: In bewerking_
