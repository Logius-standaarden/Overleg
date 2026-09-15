<!-----------------------------







   :warning: Dit bestand wordt automatisch gegenereerd.
   :warning: Handmatige toevoegingen worden overschreven.







----------------------------->
# Technisch Overleg Digikoppeling

donderdag 24 september 2026



## Agenda 

| Betreft                | Technisch Overleg Digikoppeling |
| ---------------------- | ------------------------------- |
| Vergaderdatum en -tijd | 24-09-2026, 10:00-14:00        |
| Vergaderplaats         | Fysiek : Bar Beton Utrecht (Stationshal, Centraal Station Utrecht).  |                         |

| Tijd | Onderwerp |Spreker|
| --- | --- | --- |  
| 10:00| Welkom & Mededelingen <BR> - MIDO PT GU zaken <BR> - Beschikbaarheid G4 PKIo certificaten vanaf november  | Peter Haasnoot (Logius) |
| 10:05| [Verslag vorige vergadering](https://github.com/Logius-standaarden/Overleg/blob/main/Digikoppeling/2026-09-24/2026-6-18%20%20Verslag%20TO%20Digikoppeling%20v1.0..pdf)       |    Peter Haasnoot (Logius) |
| 10:10| Review Architectuur   | Peter Haasnoot (Logius) |
|10:15 | [Digikoppeling Toekomstvisie](#digikoppeling-toekomstvisie--scope-en-inzetgebied) <BR> - vervolg 24/6 Themadag Digikoppeling| Peter Haasnoot (Logius) | 
|10:45| GraphQL Onderzoek (Q4) <BR>- BKWI Karwei <BR> - Gemeenschappelijke Bron ontsluiting : https://ictu.github.io/GBO-GO/latest/| Nil Barua (Logius)  |
|10:55 | Pauze|
|11:05|  Grote Berichten| Alexander Green (Logius)  |
|11:15| Update werkgroep Versiebeheer Digikoppeling/FSC standaard & implementaties| Aarnout Pluijgers (BKWI)  |
|11:45| Bespreken (overige) Wijzigingsvoorstellen |Peter Haasnoot (Logius)|
|12:00 | Lunch|
|12:45| Architectuurprincipes Logging |Tim van der Lippe (Logius)|
|13:05 | FSC Stand van zaken & Beheer <BR> - [Opname EU Interoperability Solution Catalog ](https://interoperable-europe.ec.europa.eu/collection/api4dt/solution/federated-service-connectivity-core-specification])| Stas Mironov (Logius)|
|13:30 | Rondvraag / Afsluiting | Allen | 


## Aanmelden

Dit overleg is openbaar. Aanmelden kan door te mailen naar digikoppeling@logius.nl

## Onderwerpen

### Grote wijzigingen
* fsc-logging [issue #6] [Voeg `trace_id` toe aan log record](https://github.com/Logius-standaarden/fsc-logging/issues/6) (19 februari 2026), _Status: In onderzoek_

### Overige punten
* OIN-Stelsel [issue #51] [Verwijder geldigheidsduur SubOIN](https://github.com/Logius-standaarden/OIN-Stelsel/pull/51) (10 september 2026)
* OIN-Stelsel [issue #49] [RFC ...](https://github.com/Logius-standaarden/OIN-Stelsel/issues/49) (3 september 2026), _Status: In onderzoek_
* OIN-Stelsel [issue #42] [[RFC] Prefix definiëren voor de ETSI Legal Person Semantics Identifier](https://github.com/Logius-standaarden/OIN-Stelsel/issues/42) (8 april 2026), _Status: Gereed_
* Digikoppeling-Koppelvlakstandaard-GB [issue #19] [Toevoegen acknowledge bericht na bestandoverdracht.](https://github.com/Logius-standaarden/Digikoppeling-Koppelvlakstandaard-GB/issues/19) (10 februari 2026), _Status: In onderzoek_
* Digikoppeling-Koppelvlakstandaard-GB [issue #18] [Toevoegen POLL Principe](https://github.com/Logius-standaarden/Digikoppeling-Koppelvlakstandaard-GB/issues/18) (10 februari 2026), _Status: Ter goedkeuring_

## Toelichting


## Digikoppeling Toekomstvisie : Uitwerking nav Themadag 

zie (todo)

_De TO leden wordt gevraagd in te stemmen met het voorstel dan wel de richting van de doorontwikkeling van de Toekomstvisie_

## GraphQL

Onderzoek GraphQL is opgenomen op de Digikoppelikng Roadmap voor kwartaal 2026-4 : [Onderzoek GraphQL](https://gitdocumentatie.logius.nl/publicatie/dk/roadmap/2026-2027/#onderzoek-uitbreiding-digikoppeling-met-graphql)

Vanuit programma [Gemeenschappeliijke Bronontsluiting (GBO)](https://ictu.github.io/GBO/latest/) is specifiek gevraagd naar de mogelijkheden om GraphQL ook status te geven binnen de GDI standaarden;

Omdat GraphQL een waardevolle standaard is voor data resource georiënteerde architectuur is deze ook in de voorgestelde toekomstvisie opgenomen als een kandidaat voor opname onder Digikoppeling;
Er zijn ook al ideeën over wat waardevol is om in een GraphQL profiel op te nemen : bv het standaardiseren van error afhandeling;

Binnen het Kennisplatform API's is GraphQL ook al langere tijd op de radar. Daarom is het voorstel om een GraphQL profiel binnen / in samenwerking met  het Kennisplatform API's te ontwikkelen.
Bij de eerstvolgende bijeenkomst van het Kennisplatform API's in novemnber zal een sessie worden gewijd aan GraphQL en een oproep worden gedaan voor deelname aan de werkgroep (bij voldoende belangstelling)

_De leden van het TO wordt gevraagd in te stemmen met deze aanpak_ 

Ter informatie:
Op developer.overheid heeft Joost Farla een aantal artikelen geschreven over GraphQL

- https://developer.overheid.nl/blog/2026/07/30/graphql-1-introductie
- https://developer.overheid.nl/blog/2026/08/18/graphql-2-flexibiliteit-en-limieten
- https://developer.overheid.nl/blog/2026/08/26/graphql-3-schema-ontwerp
- https://developer.overheid.nl/blog/2026/09/02/graphql-4-afwegingskader

## Grote Berichten

In voorgaande TO's kwam naar voren dat Grote Berichten complex is om te implementeren.
Ook is het koppelvlak toegespitst op een messaging aanpak op basis van XML, zoals beschreven in [het leidend principe](https://gitdocumentatie.logius.nl/publicatie/dk/gb/3.8.1/#leidend-principe).
Daarom was er behoefte om een REST API equivalent te schrijven voor grote berichten.

Een initiele opzet hiervoor hebben we beschikbaar gemaakt als [ADR module Transfer](https://logius-standaarden.github.io/API-mod-transfer/).
Deze module maakt gebruik van bestaande HTTP RFC's en veelgebruikte headers zoals "Range" en "Content-Digest".
Logius heeft als haalbaarheidstoets deze module geimplementeerd in zowel Java als Dotnet, om daarmee ervaring op te doen uit de praktijk.
Uit deze twee voorbeelden blijkt dat het goed te doen is.

De leden van het TO worden gevraagd deze initiele versie door te nemen en aan te geven welke organisaties dit willen uitproberen in een prototype.
Nadat er een succesvolle implementatie is die naar tevredenheid van de organisatie(s) functioneert, willen we deze module vaststellen binnen Kennisplatform API's en daarna in een toekomstig TO Digikoppeling deze module toevoegen aan het REST API Profiel.

_De leden van het TO wordt gevraagd in te stemmen met deze aanpak_ 

## FSC Stand van zaken & Beheer

_De leden van het TO wordt gevraagd...._
