# TO-DK

# Agenda

|  |   |
|------------------------|-------------------------------------|
| Betreft  | **Technisch Overleg Digikoppeling** |
| Vergaderdatum en -tijd | 09-03-2023 - 10:30-13:30 uur  |
| Vergaderplaats  | Amersfoort - _Congrescentrum Eenhoorn Barchman Wuytierslaan 2, 3818 LH Amersfoort_ |


| Tijd | Onderwerp |
| --- | --- |
| 10:30-10:35 | Welkom & Mededelingen        |    
| 10:35-10:40 | Verslag vorig TO:<br> [Verslag TO Digikoppeling 2022-12-08](https://github.com/Logius-standaarden/Overleg/blob/main/Digikoppeling/2022-12-08/Verslag.md) |   
| 10:40-11:00 | Stand van zaken Roadmap : [Roadmap](https://github.com/Logius-standaarden/Digikoppeling-Algemeen/blob/main/Digikoppeling_Roadmap_2022_2023.md) |
| 11:00-11:05 | Grote en kleine wijzigingen, issues en pull requests   | 
| 11:05-11:20 |  Presentatie eDelivery ebms3/as4 - case Domibus , aandachtspunten bij gebruik van eDelivery ebms3/as4 specificatie binnen Digikoppeling of als Digikoppeling ebms3/as4 profiel |
| 11:20-11:35 | Casus Digikoppeling REST-API profiel icm OAuth - ( bijvoorbeeld eDelivery API profiel & casus KOOP ) |
| 11:35-11:50 | Hoe om te gaan met tussenpartijen/softwareleveranciers bij Digikoppeling patronen |
| 11:50-12:00 | Discussie/Poll Digikoppeling in 2030 - Toekomstvisie / Ontwikkelingen |
| 12:00-12:30 | Lunch |
| 12:30-13:15 | Discussie Digikoppeling in 2030 / Inventarisatie (nieuwe) onderwerpen voor Roadmap Digikoppeling|
| 13:15-13:30 | Wrap-up Toekomstvisie / afsluiting |

# Onderwerpen

## Grote wijzigingen
* Digikoppeling-Koppelvlakstandaard-ebMS2 [issue #6] [Digikoppeling baseren op ebMS3](https://github.com/Logius-standaarden/Digikoppeling-Koppelvlakstandaard-ebMS2/issues/6) (03 Feb. 2022), _Status: In onderzoek_

## Kleine wijzigingen
* OIN-Stelsel [issue #5] [RSIN of Kvk nummer leidend voor OIN?](https://github.com/Logius-standaarden/OIN-Stelsel/issues/5) (29 Mar. 2022), _Status: In review_
  * [Wijzigingsvoorstel](https://github.com//Logius-standaarden/OIN-Stelsel/pull/7/files)

## Overige punten
* Digikoppeling-Koppelvlakstandaard-REST-API [issue #11] [Signing & Encryptie toevoegen aan RESTful API profiel](https://github.com/Logius-standaarden/Digikoppeling-Koppelvlakstandaard-REST-API/issues/11) (01 Apr. 2022), _Status: In onderzoek_

# Toelichting



## Algemeen

Wijzigingsvoorstellen zijn gedocumenteerd in het issue. Klik in de overzichten grote en kleine wijzigingen op een issue en de discussie, en eventueel het bijbehorende pull request met wijzigingen zijn in te zien. Hier kan iedereen, dus zeker ook de leden van het Technisch Overleg, commentaar geven op een wijzigingsvoorstel.

## Roadmap Stand van zaken

Zie voor geactualiseerde tijdlijn Roadmap : [Roadmap 2023](https://github.com/Logius-standaarden/Digikoppeling-Algemeen/blob/roadmap_2023/Digikoppeling_Roadmap_2022_2023.md#tijdlijn-roadmap-digikoppeling-standaarden) - dikgedrukt zijn de onderdelen die (door)lopen

### Toevoegen RESTful API profiel aan Digikoppeling	__- (Afgerond)__

Zie [Digikoppeling Koppelvlakstandaard REST-API](https://publicatie.centrumvoorstandaarden.nl/dk/restapi/)

### Signing & Encryptie toevoegen aan RESTful API profiel	

Werkgroep Beveiliging (specifiek sub-werkgroep signing) heeft een vergelijking gemaakt van 2 standaarden voor signing van REST-API's :
[Vergelijking REST API Signing Standaarden](https://geonovum.github.io/KP-APIs/publicaties/REST_API_Signing_Standaarden)

Momenteel doet Politie ervaring op met het gebruik van de standaard : [httpbis-message-signatures](https://datatracker.ietf.org/doc/draft-ietf-httpbis-message-signatures/) voor intern gebruik;
Deze ervaring zal meegenomen worden bij de verdere keuzes en invulling van signing binnen het REST-API profiel
 
### Onderzoek verwijzing naar de 'ADR API Security Extensie' vanuit de Digikoppeling Beveiligingsvoorschriften	__- (Afgerond)__

Zie [Toevoegen API-58 No sensitive information in URIs](https://github.com/Logius-standaarden/Digikoppeling-Koppelvlakstandaard-REST-API/issues/15)

### Aanvulling Digikoppeling governance

We hebben onze governance beschreven in nieuwe beheermodellen (zie hieronder). In de Programmeringstafel van later vandaag hebben we een memo geagendeerd over [de nieuwe governance volgens MIDO](Memo%20Governance%20Logius%20Standaarden.pdf).

### Verbeteren Informatievoorziening / Nieuwe wijze van Publiceren

We willen pleio afvoeren. Op onze aankondiging op pleio hebben we verder geen reactie gekregen dus we gaan onze pleio site sluiten. Tenzij het TO daar bezwaar tegen heeft. Verder: onze publicatiewebsite was centrumvoorstandaarden.nl en wordt gitdocumentatie.logius.nl/publicaties.

### Best Practice Identificatie van Organisaties, Organisatieonderdelen en voorzieningen	__- (Afgerond)__

Zie [Digikoppeling Handreiking Adressering en Routering](https://publicatie.centrumvoorstandaarden.nl/dk/bpadres/)

### Analyse knelpunten Routering en Intermediairs in gegevensverkeer __- (Afgerond)__

Zie [Analyse knelpunten Routering en Intermediairs](https://github.com/Logius-standaarden/Digikoppeling-Handreiking-Adressering-en-Routering/blob/main/documenten/Analyse_knelpunten_Routering_Intermediairs.md)

### Verkennen mogelijk gebruik ebMS3/AS4	

Om de impact van een overgang naar ebMS3/AS4 in te kunnen schatten hebben we een vraag naar de impact uitgezet in een [memo over modernisering Digikoppeling ebMS](Memo%20Modernisering%20Digikoppeling%20ebMS.pdf) voor de Programmeringstafel van vandaag. 

### Interoperabiliteit platformen WUS bij gebruik MTOM in combinatie met WS-Security (signing) __- (Afgerond)__

### Doorontwikkeling RESPEC/Digikoppeling template voor publicatie van specificaties	

### Update Beheermodel / aansluiting op Logius Standaarden BOMOS generiek beheer model & governance			

### Lange termijn visie : Hoe om te gaan met uitfasering/vervanging van profielen			

### Periodiek actualiseren architectuur__- (Afgerond)__



### Inventarisatie nieuwe onderwerpen voor Roadmap

* Periodieke review beveiligingsvoorschriften
* Certificaat wisseling
* Onderhoud en versiebeheer van koppelingen
* Standaarden en voorzieningen voor onboarding

(
Bij het Kennisplatform API's waren mn de volgende onderwerpen genoemd:

API:

- filtering
- discovery
- management
- extensies / modules op lijst veelgebruikte standaarden (plaatsen)
- orchestratie (gelaagde API's / data combineren)
- security, rechten delegatie (saas, organisaties delegeren rechten aan leveranciers)
- (baseren op) semantische info modellen
- relatie ADR/API strategie met ODATA/GraphQL en grpc
)
