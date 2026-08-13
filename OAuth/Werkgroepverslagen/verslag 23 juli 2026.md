# Vergadernotulen – Werkgroep FSC & OAuth alignment

**Onderwerp:** FSC & NLGov OAuth alignment werkgroep 
**Datum:** 23-07-2026 

---

## 1. Opening en doel van de bijeenkomst

De bijeenkomst stond in het teken van de key deliverables van de werkgroep. Het oorspronkelijke idee was om de tabel met use cases verder in te vullen en de door Wilbert aangedragen vragen te beantwoorden.  

Er is aandacht gevraagd voor het ontbreken van een duidelijk verslag van de vorige bijeenkomst. Meerdere deelnemers gaven aan dat hierdoor het risico bestaat dat discussies opnieuw worden gevoerd. De conclusie van de vorige sessie was dat het grote document nog te veel open vragen bevatte en dat deze in een volgende bijeenkomst in meer detail zouden worden bekeken. Dat was ook de insteek van deze sessie.

---

## 2. Terugblik op eerdere conclusies

Het oorspronkelijke doel van de werkgroep was te onderzoeken of de header hergebruikt kon worden. Dit bleek tot mogelijke conflicten te leiden, waarna alle use cases zijn doorgenomen. De conclusie was dat de header niet wordt hergebruikt.  

De use cases zijn daarna vooral gebruikt ter verduidelijking: wanneer wordt OAuth ingezet en wanneer FSC? Het oorspronkelijke doel om iets te consolideren of te wijzigen in FSC is voorlopig niet haalbaar. Wat resteert is een set use cases die nuttig is om aan derden uit te leggen wanneer welke standaard van toepassing is.

Met name de gecombineerde scenario’s (use case 2 en de bijbehorende varianten) leveren de meeste discussie op. Dit zijn de situaties waarin zowel FSC als OAuth relevant kunnen zijn.

---

## 3. Discussie over toepassingsgebied en interpretatie

Er is uitgebreid gesproken over de interpretatie van het werkingsgebied van FSC / Digikoppeling.

- Vanuit gemeenteland wordt FSC in de praktijk vaak als standaard gezien voor REST-API’s, tenzij er zwaarwegende redenen zijn om hiervan af te wijken. Dit komt onder meer tot uiting in aanbestedingen.
- Formeel is het werkingsgebied van Digikoppeling beperkter: het betreft met name de GDI (basisregistraties en daaraan gerelateerde voorzieningen) en sector-overstijgende gegevensuitwisseling, en alleen daar waar tweezijdige authenticatie nodig is.
- Het verschil tussen de formele afspraken en de beleving in de praktijk (met name binnen gemeenten) is precies wat de use cases moeten helpen verduidelijken.

Er is nadrukkelijk vastgesteld dat FSC niet “altijd” van toepassing is. Een volledig open publieke API (bijvoorbeeld de BAG) kan niet de eis stellen dat een burger over een PKI-certificaat en FSC-connector beschikt.

---

## 4. Voorstellen tot vereenvoudiging

Verschillende voorstellen zijn gedaan om de complexiteit te verminderen:

- OAuth / OpenID Connect consequent inzetten voor de beveiliging van de API zelf.
- FSC gebruiken voor het contractuele / trust-aspect (het “mogen gebruiken” van een API).
- De focus leggen op de vraag wanneer FSC wel of niet aan de orde is.

Tegelijkertijd is geconstateerd dat er twee perspectieven naast elkaar bestaan:

1. Het **formele** werkingsgebied (zoals vastgelegd bij Forum Standaardisatie / Digikoppeling).
2. Het **pragmatische** perspectief (consistentie en eenvoud in de implementatie).

Beide perspectieven zijn relevant en moeten in de uiteindelijke deliverable herkenbaar zijn.

---

## 5. Richting: adviserende beslisboom

In plaats van een uitgebreide, uitputtende tabel is gekozen voor het uitwerken van een **adviserende beslisboom**. Deze is bedoeld als hulpmiddel en heeft geen normatief karakter.

Relevante criteria die tijdens de discussie zijn genoemd:

- Is er sprake van een individu (eindgebruiker) of een organisatie?
- Is de uitwisseling sector-overstijgend?
- Is de uitwisseling organisatie-overstijgend?
- Is er sprake van rechten-delegatie door een eindgebruiker?
- Is tweezijdige authenticatie nodig?
- Zijn er binnen de eigen sector of organisatie al afspraken gemaakt die als override gelden?

Er is aandacht gevraagd voor heldere definities (onder meer “gebruiker” en “rechten-delegatie”), zonder dat deze tot een te theoretische of protocol-gedreven discussie leiden. De voorkeur gaat uit naar een top-down benadering vanuit functionele situaties.

De beslisboom moet richting geven aan de meest voorkomende situaties en niet pretenderen alle denkbare gevallen te dekken. Complexe of uitzonderlijke casussen blijven buiten scope; daarvoor kunnen specialisten worden geraadpleegd.

---

## 6. Gewenste deliverable

De werkgroep streeft naar:

- Een **adviserende beslisboom** voor een beperkt aantal generieke casussen.
- Een document dat richtinggevend is, niet normatief of uitputtend.
- Duidelijkheid over doelgroep en beoogd gebruik, zodat lezers realistische verwachtingen hebben.
- Beantwoording (impliciet of via kanttekeningen) van de eerder door Wilbert gestelde vragen.

Het document moet helpen om herhaalde discussies in toekomstige bijeenkomsten te voorkomen.

---

## 7. Afgesproken vervolgacties

| Actie | Wie | Wanneer |
|-------|-----|---------|
| Eerste opzet maken van de beslisboom / uitwerking van bestaande use cases | ??? | Na 10 augustus (na vakantie) |
| Concept rondsturen voor review | ??? | Na opstellen concept |
| Volgende bijeenkomst voorbereiden met duidelijke focus op uitwerking | Allen | Voor volgende sessie |

In de volgende bijeenkomst wordt niet opnieuw stilgestaan bij de vraag “waar ging het ook alweer over?”, maar wordt direct verder gewerkt aan de deliverable.

---

## 8. Overige opmerkingen

- Het onderscheid tussen formele verplichting en pragmatische toepassing moet in de boodschap van het document duidelijk terugkomen.
- Het document is ondersteunend van aard en geen formeel standaarddocument.
- Er is waardering uitgesproken voor de open en inhoudelijke discussie.

---

**Volgende bijeenkomst:** nader te bepalen  
**Opname:** beschikbaar
