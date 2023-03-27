# Technisch Overleg Digikoppeling

Donderdag 9 maart 2023 te Amersfoort

## Aanwezigen

| Achternaam    | Voornaam  | Organisatie |
|---------------|-----------|-------------|
| Bijen         | Antoon    | Justid      |
| Coemans       | Maarten   | SNG         |
| Fieten        | Sander    | Casquis     |
| Green         | Alexander | Logius      |
| Haasnoot      | Peter     | Logius      |
| IJzermans     | Jochem    | UWV         |
| Kruijs        | Paul      | Logius      |
| Pauw          | Elzo      | UWV         |
| Reinhoud      | Erwin     | Kennisnet   |
| Rutte         | Laura     | BKWI        |
| Sinnige       | Hans      | RINIS       |
| Van der Plas  | Martin    | Logius      |
| Van der Velde | Johan     | RDW         |
| Welmer        | Han       | TNO         |
| Wisse         | Edwin     | Logius      |
| Zwaan         | Tonkie    | BKWI        |

## Welkom & Mededelingen

dhr. Kuijpers van Dictu afwezig en geïnteresseerd in API Management.

## Verslag vorig TO

https://github.com/Logius-standaarden/Overleg/blob/main/Digikoppeling/2022-12-08/Verslag.md

Geen opmerkingen

## Stand van zaken Roadmap
https://github.com/Logius-standaarden/Digikoppeling-Algemeen/blob/roadmap_2023/Digikoppeling_Roadmap_2022_2023.md#tijdlijn-roadmap-digikoppeling-standaarden

De dikgedrukte kruisjes geven de verwachte uitloop van onderwerpen aan.

Als TO akkoord gaat wordt geactualiseerde versie gepubliceerd.

### Signing & Encryptie toevoegen aan RESTful API profiel

Signing & Encryptie sit onderdeel loopt in samenwerking met Kennisplatform API’s Werkgroep Beveiliging. Het is een kleine subwerkgroep, bij interesse in men welkom om aan te schuiven. Een vergelijking tussen JAdES en HTTP Message Signatures is gepubliceerd:

https://geonovum.github.io/KP-APIs/publicaties/REST_API_Signing_Standaarden/

Er wordt momenteel een pilot bij de Politie uitgevoerd met HTTP Message Signatures. De uitkomsten zullen meegenomen worden bij het maken van een keuze tussen de twee.

### Aanvulling Digikoppeling governance

Edwin Wisse: Overgegaan in GDI naar Programmeringstafel als tactische laag en Programmeringstafel strategisch. Lagen gevolgd uit MIDO. Vanmiddag vindt een Programmeringstafel overleg plaats. Het resultaat zal teruggekoppeld worden met TO. TO behoudt de rol van operationele laag.

<details>
<summary>Tabel MIDO-structuur</summary>
  
| **Gremium**  | **Accent**   | **Rol participant**  | **Ondersteuning door beheerder (Logius)** |
|     ---      |    ----      |         ---          |                   ---                     |
| **Community** (omvang beperkt) | Inhoud -- delen    | 1. Volgen van ontwikkelingen.<br/> 2. Leveren van input voor de doorontwikkeling van de standaard. |  1. Informatie m.b.t. specificaties en beheer open delen met community.<br/> 2. Deelnemen aan stuurgroep en werkgroepen |
| Technisch Overleg (Operationeel, 4x per jaar) | Inhoud - afstemmen | 1. Inhoudelijk ontwikkelen van standaard onderdelen en bijbehorende documentatie. <br/>2. Voorbereiden van de release- planning. <br/>3. Prioriteiten stellen voor de ontwikkeling, roadmap van nieuwe releases van de standaarden.<br/> 4. Goedkeuring van aanpassingen op de standaard.<br/> 5. Advies aan programmeringstafel en -raad over wijzigingsvoorstellen. | 1. Analyseren, ontwerpen en uitwerken van specificaties. <br/>2. Volgen en beïnvloeden van aanpalende standaarden. <br/>3. Organiseren bijeenkomsten. <br/>4. Opstellen en verspreiden notulen. <br/>5. Beschikbaar stellen specificaties. |
| Programmeringstafel | Besluitvormend - adviserend | 1. Vaststellen roadmap van de standaard.<br/> 2. Vaststellen major/minor releases van de standaard.| 1. Analyseren, ontwerpen en uitwerken van beleidszaken, (release)planning. |
| Programmeringsraad | Besluitvormend | 1. Goedkeuren van grote wijzigingen: Introductie nieuwe koppelvlak standaarden en uitfasering bestaande koppelvlak standaarden. <br/> 2.Vaststellen beheermodel van de standaard.<br/> 3. Vaststellen externe publicaties over het standaardenbeleid en releases. | 1. Advisering en inbreng via secretariaat MIDO. <br/>2. Publiceren standaarden en andere Standaard-informatie |

</details>

### Verbeteren Informatievoorziening / Nieuwe wijze van Publiceren

Een nieuwe wijze van publiceren is beschikbaar gesteld. De website publicatie.centrumvoorstandaarden.nl willen we uitfaseren. Het is voorbereid; de werkversies verwijzen naar de nieuwe locaties op logius.nl waar de publicatieversies reeds beschikbaar zijn ([paginalijst](https://github.com/Logius-standaarden/publicatie#publicatie)).

De online community digistandaarden.pleio.nl is een vrij rustige omgeving. Het voorstel is om Pleio af te voeren ([bericht op Pleio](https://digistandaarden.pleio.nl/discussion/view/6a7f566b-911f-4bb6-bfc1-cd95e9b195c7/afsluiten-digistandaarden-pleio)). TO toont geen bezwaar.

### Verkennen mogelijk gebruik ebMS3/AS4

Vanmiddag bij de Programmeringstafel ligt vraag over impact. Vraag over impact op verschillende stakeholders moeilijk te dekken door enkel het Technisch Overleg.

**Antoon Bijen:** Een migratie heeft ontzettend veel impact. ebMS2 heeft functionaliteit welke mist in ebMS3: CPA om afspraken vast te leggen. Vraag aan Programmeringstafel: willen afnemers dit wel?

**Hans Sinnige:** De CPA-functionaliteit wordt in eDelivery door SML/P aangeboden. (Dit is deels vergelijkbare functionaliteit, dit werkt wel anders).

### Doorontwikkeling ReSpec

Een stagiair heeft een generiek profiel gemaakt dat is toegepast bij DK beheermodel. Gemakkelijker toepasbaar voor andere organisaties ([template](https://github.com/Logius-standaarden/ReSpec-template)).

### Update Beheermodel

Update beheermodel valt onder aansluiten op MIDO governance.

### Lange termijn visie

Lange termijn visie: discussie over uitfasering/vervanging van profielen.

## Grote en kleine wijzigingen, issues en pull requests

### Migratie van ebMS2 naar ebMS3/AS4

Edwin Wisse licht het voorstel toe om het Digikoppeling koppelvlak te migreren van de verouderde ebMS2-standaard naar het ebMS3/AS4-profiel zoals dat reeds wordt toegepast in eDelivery en PEPPOL.

## Presentatie eDelivery ebms3/as4

https://github.com/Logius-standaarden/Overleg/blob/main/Digikoppeling/2023-03-09/media/eDelivery%20AS4.pdf

## Casus Digikoppeling REST-API profiel i.c.m. OAuth

<details>
  <summary>Casus Client met PKIO</summary>
  <img src="https://raw.githubusercontent.com/Logius-standaarden/Overleg/20230309/Digikoppeling/2023-03-09/media/DK%20REST%20en%20OAUTH-API%20Flow.drawio.svg" alt="Diagram Casus Client met PKIO">
</details>
<details>
  <summary>Casus Loket met SAML</summary>
  <img src="https://raw.githubusercontent.com/Logius-standaarden/Overleg/20230309/Digikoppeling/2023-03-09/media/DK%20REST%20en%20OAUTH-Loket%20flow.drawio.svg" alt="Diagram Casus Loket met SAML">
</details>

## Hoe om te gaan met tussenpartijen/softwareleveranciers bij Digikoppeling patronen

**Johan van der Velde:** Wij merken dat overheidspartijen die aansluiten hun certificaat geven aan een software leverancier. Kunnen wij afdwingen dat een leverancier zichzelf moet identificeren in plaats van over certificaat van een andere partij te beschikken?

Suggestie sub-OIN toe te passen

**Tonkie Zwaan:** Wij doen beide: Teken het bericht met sub-oin en mTLS met sub-oin.

**Martin van der Plas:** Met een mandateringsregister verleg je het probleem van de tussenpartijen/softwareleveranciers: Hoofd-oin houder blijft verantwoordelijk voor aanschaf certificaat.

**Johan van der Velde:** Kan het via een mandateringsregister?

**Martin van der Plas:** Met een mandateringsregister verleg je het probleem van de tussenpartijen/softwareleveranciers naar de aanbieder van het mandateringsregister. Aangezien dat vaak een overheidspartij is ligt de aansprakelijkheid en de waarborg die we met PKIO hebben belegd bij de TSPs nu weer bij ons. Bovendien creëer je vaak een single point of failure en een hele verzameling nieuwe risico's die weer moeten worden afgedekt. Wil je alles goed regelen dan wordt het niet goedkoper of beter dan de oplossing met subOINs en PKIO-certificaten.

## Discussie/Poll Digikoppeling in 2030

[Resultaten poll](https://github.com/Logius-standaarden/Overleg/blob/main/Digikoppeling/2023-03-09/media/2023_03_09_TO-Digikoppeling-poll-results.pdf)

In Discussie & Wrap-up genoemde behoeften & onderwerpen voor roadmap Digikoppeling:

-	Notificaties 

-	Machtigingen / oplossing voor sleutelbos probleem SAAS levernaciers

-	OAuth gebruik in Digikoppeling REST_API

-	WUS Signing – wannneer wel/niet gebruiken (meer) in documentatie toelichten (wordt regelmatig onnodig gebruikt bij koppelingen)

- Beveiligingsvoorschriften relateren aan BIO

