# TO-DK

# Agenda

|  |   |
|------------------------|-------------------------------------|
| Betreft  | **Technisch Overleg Digikoppeling** |
| Vergaderdatum en -tijd | 08-12-2022 - 10:00 uur  |
| Vergaderplaats  | Webex  |

| Tijd | Onderwerp |
| --- | --- |
| 10:00-10:05 | Welkom & Mededelingen        |    
| 10:05-10:30 | OOTS toelichting door Ivar Vennekens & discussie |
| 10:30-10:50 | Grote en kleine wijzigingen, issues en pull requests <br>_Graag specifiek aandacht hierbij voor [deze aandachtspunten](#aandachtspunten-wijzigingen)._  | 
| 10:50-11:00 |[eDelivery REST API lessons learned](eDeliveryAPI.md)  |
| 11:00-11:10 |[Status API-58 in ADR extensie beveiliging](#status-api-58-in-adr-extensie-beveiliging)                         |
| 11:10-11:20 |[Gebruik eIDAS certificaten voor signing in Digikoppeling](#gebruik-eidas-certificaten-voor-signing-in-digikoppeling)|
| 11:20-11:30 |[Update Respec Generiek Profiel](#update-respec-generiek-profiel)|


# Onderwerpen

## Grote wijzigingen
* Digikoppeling-Koppelvlakstandaard-ebMS2 [issue #6] [Digikoppeling baseren op ebMS3](https://github.com/Logius-standaarden/Digikoppeling-Koppelvlakstandaard-ebMS2/issues/6) (03 Feb. 2022), _Status: In onderzoek_

## Kleine wijzigingen
* Digikoppeling-Koppelvlakstandaard-REST-API [issue #22] [Toelichting API-58](https://github.com/Logius-standaarden/Digikoppeling-Koppelvlakstandaard-REST-API/pull/22) (01 Dec. 2022), _Status: In review_
* Digikoppeling-Architectuur [issue #11] [Periodieke review](https://github.com/Logius-standaarden/Digikoppeling-Architectuur/pull/11) (30 Nov. 2022), _Status: In review_
* Digikoppeling-Handreiking-Adressering-en-Routering [issue #4] [RFC Voor wie werkt een SAAS eigenlijk?](https://github.com/Logius-standaarden/Digikoppeling-Handreiking-Adressering-en-Routering/issues/4) (22 Nov. 2022), _Status: In review_
* Digikoppeling-Handreiking-Adressering-en-Routering [issue #3] [PKI sleutel deponeren?](https://github.com/Logius-standaarden/Digikoppeling-Handreiking-Adressering-en-Routering/issues/3) (21 Oct. 2022), _Status: In review_
* Digikoppeling-Handreiking-Adressering-en-Routering [issue #2] [routeren op de berichtbody?](https://github.com/Logius-standaarden/Digikoppeling-Handreiking-Adressering-en-Routering/issues/2) (21 Oct. 2022), _Status: In onderzoek_
* Digikoppeling-Architectuur [issue #3] [Verantwoordelijkheid voor informatiebeveiliging](https://github.com/Logius-standaarden/Digikoppeling-Architectuur/pull/3) (06 Jul. 2022), _Status: In review_
* OIN-Stelsel [issue #5] [RSIN of Kvk nummer leidend voor OIN?](https://github.com/Logius-standaarden/OIN-Stelsel/issues/5) (29 Mar. 2022), _Status: In review_

## Overige punten
* Digikoppeling-Koppelvlakstandaard-REST-API [issue #11] [Signing & Encryptie toevoegen aan RESTful API profiel](https://github.com/Logius-standaarden/Digikoppeling-Koppelvlakstandaard-REST-API/issues/11) (01 Apr. 2022), _Status: In onderzoek_

# Toelichting


## Algemeen

Wijzigingsvoorstellen zijn gedocumenteerd in het issue. Klik in de overzichten grote en kleine wijzigingen op een issue en de discussie, en eventueel het bijbehorende pull request met wijzigingen zijn in te zien. Hier kan iedereen, dus zeker ook de leden van het Technisch Overleg, commentaar geven op een wijzigingsvoorstel.

## Aandachtspunten wijzigingen

Wij vragen het TO om deze voorstellen goed te keuren:

### Digikoppeling-Handreiking-Adressering-en-Routering
* [RFC Voor wie werkt een SAAS eigenlijk](https://github.com/Logius-standaarden/Digikoppeling-Handreiking-Adressering-en-Routering/issues/4) | [Voorgestelde aanpassing](https://github.com/Logius-standaarden/Digikoppeling-Handreiking-Adressering-en-Routering/pull/7/files)
* [PKI sleutel deponeren?](https://github.com/Logius-standaarden/Digikoppeling-Handreiking-Adressering-en-Routering/issues/3) | [Voorgestelde aanpassing](https://github.com/Logius-standaarden/Digikoppeling-Handreiking-Adressering-en-Routering/pull/6/files)
* [Routeren op de berichtbody](https://github.com/Logius-standaarden/Digikoppeling-Handreiking-Adressering-en-Routering/issues/2) | [Voorgestelde aanpassing](https://github.com/Logius-standaarden/Digikoppeling-Handreiking-Adressering-en-Routering/pull/5/files)

### Digikoppeling-Architectuur
* [Periodieke review](https://github.com/Logius-standaarden/Digikoppeling-Architectuur/pull/11) | [Voorgestelde aanpassing](https://github.com/Logius-standaarden/Digikoppeling-Architectuur/pull/11/files)
* [Verantwoordelijkheid voor informatiebeveiliging](https://github.com/Logius-standaarden/Digikoppeling-Architectuur/pull/3) | [Voorgestelde aanpassing](https://github.com/Logius-standaarden/Digikoppeling-Architectuur/pull/3/files)


## Status API-58 in ADR extensie beveiliging

Zie [Update ext-security.md API-58](https://github.com/Geonovum/KP-APIs/pull/464)

Voorstel is nav de bespreking van API-58 in de werkgroep Beveiliging van het Kennisplatform API's een toelichting toe te voegen aan API-58 in het Digikoppeling REST API profiel:
| Categorie | Principe | Extensie | Toelichting | Link |
| --- | --- | --- | --- | --- |
| Verplicht | API-58  No sensitive information in URIs | Security | Alleen verplicht indien er sprake is van logging in systemen die niet onder controle van de betrokken client- en serverorganisatie staan | [API-58 No sensitive information in URIs  ](https://docs.geostandaarden.nl/api/def-hr-API-Strategie-ext-20211013/#api-58)|

Zie [Toelichting API-58](https://github.com/Logius-standaarden/Digikoppeling-Koppelvlakstandaard-REST-API/pull/22) 

## Gebruik eIDAS certificaten voor signing in Digikoppeling

Vraag/Discussie: (hoe) worden eIDAS certificaten gebruikt op dit moment?

(
Zie huidige beschrijving gebruik PKIO

* WUS : https://publicatie.centrumvoorstandaarden.nl/dk/wus/#end-to-end-beveiliging
* ebMS : https://publicatie.centrumvoorstandaarden.nl/dk/ebms/#profile-requirement-item-signature-generation
)

## Update Respec Generiek Profiel

https://github.com/Logius-standaarden/respec-template

## Tot slot
Voor wie wil participeren in eDelivery in relatie to OOTS. De EU organiseert op 13 december een _projectathon_ over toepassing van eDelivery in OOTS:
- [eDelivery & OOTS Projectathon Process](https://ec.europa.eu/digital-building-blocks/wikis/pages/viewpage.action?pageId=610468539)
