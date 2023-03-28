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

dhr. Kuijpers van Dictu is afwezig en geïnteresseerd in andere deelnemers die kennis en ervaring hebben met API Management. Om in contact te komen kan men rechtstreeks mailen of een bericht sturen aan digikoppeling@logius.nl.

## Verslag vorig TO

https://github.com/Logius-standaarden/Overleg/blob/main/Digikoppeling/2022-12-08/Verslag.md

Het verslag van het overleg  dd 8 december 2022 is doorgenomen en er zijn geen opmerkingen.

## Stand van zaken Roadmap
https://github.com/Logius-standaarden/Digikoppeling-Algemeen/blob/roadmap_2023/Digikoppeling_Roadmap_2022_2023.md#tijdlijn-roadmap-digikoppeling-standaarden

De dikgedrukte kruisjes geven de verwachte uitloop van onderwerpen aan.

Als TO akkoord gaat wordt geactualiseerde versie gepubliceerd.

### Signing & Encryptie toevoegen aan Digikoppeling - "Reliable REST API profiel"

Signing & Encryptie: dit onderdeel loopt in samenwerking met Kennisplatform API’s Werkgroep Beveiliging. Het is een kleine subwerkgroep, bij interesse is men welkom om aan te schuiven. Een vergelijking tussen JAdES en HTTP Message Signatures is gepubliceerd op:

https://geonovum.github.io/KP-APIs/publicaties/REST_API_Signing_Standaarden/

Er wordt momenteel een pilot bij de Politie uitgevoerd met HTTP Message Signatures. De uitkomsten zullen meegenomen worden bij het maken van verdere keuzes voor het Reliable REST API profiel.

### Aanvulling Digikoppeling governance

Edwin Wisse: Overgegaan in GDI naar Programmeringstafel als tactische laag en Programmeringstafel strategisch. Lagen gevolgd uit MIDO. Vanmiddag vindt een Programmeringstafel overleg plaats. Het resultaat zal teruggekoppeld worden met TO. TO behoudt de rol van operationele laag. [(zie bijlage hieronder)](#bijlage-governance)

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

Vanmiddag bij de Programmeringstafel ligt vraag over impact. Vraag over impact op verschillende stakeholders moeilijk te dekken door enkel het Technisch Overleg. Ook dit punt wordt besproken in de Programmeringstafel [(zie bijlage hieronder)](#bijlage-governance)

**Antoon Bijen:** Een migratie heeft ontzettend veel impact. ebMS2 heeft functionaliteit welke mist in ebMS3: CPA om afspraken vast te leggen. Vraag aan Programmeringstafel: willen afnemers dit wel?

**Hans Sinnige:** De CPA-functionaliteit wordt in eDelivery door SML/P aangeboden. (Dit is deels vergelijkbare functionaliteit, dit werkt wel anders).

### Doorontwikkeling ReSpec

Onze Logius stagiair (Rick de Bruin) heeft een generiek profiel gemaakt dat is toegepast bij DK beheermodel. Dit profiel is gemakkelijker toepasbaar voor andere organisaties ([template](https://github.com/Logius-standaarden/ReSpec-template)).

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



## Bijlage: Governance

### Uit het verslag van de programmeringstafel

Standaarden binnen de GDI (Presentatie Maarten van der Veen en Edwin Wisse). 

Voor het beheren van een standaard is afstemming op operationeel, tactisch én strategisch niveau nodig. Op dit moment is alleen de operationele laag ingevuld. Ter besluitvorming aan tafel worden diverse zaken voorgelegd, in grote lijnen kan de tafel zich vinden in de onderwerpen. Het geeft de tafel ook een mogelijkheid om scherper af te bakenen welke rol de tafel kan spelen. Opmerkingen van de tafel: 
* Het ligt voor de hand dat de tafel de PGDI adviseert over grote wijzigingen; 
* Het is lastig om vanuit de stukken goed te kunnen bepalen wat er onder grote of kleine wijzigingen valt; 
* De formele besluitvorming over deze opzet van de governance, moet echter via OBDO en daarna mogelijk de staatssecretaris lopen. De tafels en de PGDI zijn nl. adviesorganen zonder beslisbevoegdheid. Het akkoord dat wordt gevraagd is feitelijk een positief advies. 
* Het ontwikkelen van een standaard is één, het beheer, bijhouden en stimuleren van gebruik is in de praktijk voor succes essentieel, graag ook aandacht voor adoptie van standaarden; 
* De tafel vraagt verheldering over de rollen van de beheerorganisatie Logius versus Forum standaardisatie. 
* Overige suggesties van onder meer de Belastingdienst, Kadaster en DUO worden schriftelijk verstrekt aan Logius. 
* Ook beleidsdepartementen vragen hoe zij het beste met dit soort vraagstukken om kunnen gaan. 

Naar aanleiding van het agendapunt beslist de tafel als volgt: 
Governance GDI standaarden: 
1. Besluitvorming wordt aangepast in advisering dit werkt door in de andere vragen. Vraag drie wordt geschrapt. Logius krijgt de vraag zelf initiatief te nemen om een voorstel op te stellen waarmee de achterban en uitvoeringsorganisaties van leden geraadpleegd kunnen worden (en niet als open vraag). Tevens wordt ook aandacht gevraagd om scherper de scheiding van rollen tussen afd. standaarden en Forum standaardisatie mee te nemen in de verdere uitwerking. 

Modernisering Digikoppeling ebMS koppelvlak: 
1. Dit wordt aangepast in: de PT GU vraagt om een zo breed mogelijke impactanalyse met stakeholders en hun achterban. Initiatief hiervan ligt bij Logius. Tevens wordt afgesproken de opzet van de impactanalyse voor te leggen aan de tafel, dit wordt als actiepunt opgenomen; 
2. Planning: op een zo kort mogelijke termijn, maar wel realistisch. 

### Opmerkingen van Belastingdienst, Kadaster en DUO 

_Een aantal uitvoeringsorganisaties was afwezig bij de vergadering maar hadden wel een aantal vragen en opmerkingen bij het agendapunt. Deze zijn in de vergadering besproken._

*	Geef in de roadmap het verschil aan tussen grote wijzigingen (waar de PGDI over beslist) en kleine wijzigingen (die voor de tafel zijn). Goed om kleine wijzigingen in principe door de beheerorganisatie Logius af te laten doen. Wel opletten dat wijzigingen die een 'zeer kleine impact' lijken te hebben, soms in de praktijk toch groter gaan worden. Dan ontstaat het risico dat de beheerorganisatie gaandeweg serieuze wijzigingen ongemerkt en onbewust doorvoert. Suggestie: neem in het beheermodel een maatregel op om dit te voorkomen.
*	We missen nog inzicht en overzicht van de bestaande en te verwachte standaarden. Verzoek om daarin te voorzien.
*	De voorgestelde governance kan pas in werking treden als ook de PGDI ermee akkoord gaat.
*	Voorgesteld wordt om aan organisaties zelf over te laten om te migreren. We zien echter geen echte driver voor de organisaties om een werkende ebms2 koppeling 'zomaar' te gaan vervangen voor een nieuwe techniek, zeker als ze die nog niet in huis hebben.
*	Dan nog een min of meer tekstuele: In hetzelfde stuk modernisering ebms, staat (pag. 2) dat de NL en EU standaard in de pas lopen en mogelijk dezelfde standaard zijn. Dit klinkt wat strijdig met de tekst in het beheerstuk waarin staat dat eDelivery niet een alternatief voor Digikoppeling is maar dat beide standaarden elkaar aanvullen. Dat lijkt ook beter dan twee dezelfde standaarden uitwerken, als dit klopt is het beter om alleen een verwijzing naar de eDelivery standaard opnemen.
*	Dat Logius belangrijke rol heeft in het beheer van standaarden staat wat mij niet ter discussie. Wat opzet over het hoofd lijkt te zien is dat GDI (nu en straks nog meer) gevoed zal worden door input (zeker waar het afspraken en standaarden betreft) uit de sectoren. Sommige van die afspraken worden generiek (en daarmee meer GDI), maar vraag is waar de transitie van sector naar generiek ligt.
*	Concreet voorbeeld is de geo-sector: die omvat zo ongeveer de helft van de basisregistraties. Met Geonovum (onder aansturing van het GI-beraad dat adviseert aan de minister voor VRO als coördinerend bewindspersoon, namens alle partijen in de geo-sector) worden veel afspraken, standaarden en soms zelfs voorzieningen ontwikkeld. Die standaarden lopen netjes de weg langs Bureau Forum Standaardisatie (BFS) dat gepositioneerd is binnen Logius. Op een gegeven moment zijn de API’s uit onze sector zo generiek geworden dat overdracht is geweest van ons afsprakenstelsel rond API’s naar Logius, maar dat laat onverlet dat ook in de GDI er nog steeds sectorale oplossingen zijn. Ik spreek uit mijn ervaring als voorzitter van de programmaraad Geonovum, maar ik kan me voorstellen dat bijvoorbeeld in de sociale sector (bijv. BKWI) hetzelfde speelt.
*	Daarmee wordt overigens totale opzet van standaarden niet ingewikkelder, maar kan afhankelijk van de sector/vraagstuk beheer en ontwikkeling ook bij een andere partij liggen (ook al raakt dat de GDI).
*	Stuk is nu heel erg geschreven op inbedding bij Logius (ik had ook meer tekst over BFS verwacht), terwijl ook standaardenwereld steeds federatiever wordt met de groei van de digitale overheid.
*	In welke mate worden de operationele besluiten afgestemd met afnemers?
*	In welke mate is er rekening gehouden met Frameworks zoals REST API’s van vandaag de dag? Dit is actuelere kennis die aansluit bij wat er op scholen wordt geleerd en op de arbeidsmarkt meer beschikbaar is. Hier loopt de EU wetgeving op achter. Investeren we hier niet in een verouderde koppelvlakspecificatie?
