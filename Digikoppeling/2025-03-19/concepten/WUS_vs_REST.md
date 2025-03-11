# Vergelijking  Digikoppeling WUS (WS-I) en REST-API profiel 

In deze notitie wordt ingegaan op de vraag _"Kan het Digikoppeling WUS profiel vervangen worden door het Digikoppeling REST-API profiel"_
Dit in het kader van de vraag of het Digikoppeling WUS profiel uitgefaseerd zou kunnen worden binnen de Digikoppeling standaard (Zie  [TO Digikoppeling - Uitfasering WUS](https://github.com/Logius-standaarden/Overleg/tree/main/Digikoppeling/2024-12-10#uitfasering-wus)
)

## Functionaliteit WUS (WS-I)

In hoeverre biedt het REST-API profiel vergelijkbare functionaliteit als het Digikoppeling WUS profiel:

### WS-Security

WS-Security biedt Signing & Encryptie en End-to-end security ,  ook Encryptie per berichtdeel

_Invulling door REST-API_
  
Het REST API profiel v2  biedt ondersteuning voor signing en encryptie. Encryptie per berichtdeel wordt niet ondersteund in JSON
(Wel zou in dit geval XML kunnen worden gebruikt voor de bericht structuur en hierbij encryptie op delen toepassen, maar dit is geen onderdeel van de huidige REST-API specificatie)

### WS-AtomicTransaction

Voor ACID-transacties (bv bij multi step processen)

Dit hoort wel bij de WS-I standaarden maar is __niet expliciet onderdeel__ van de huidige DK WUS specificatie (omdat dit oorspronkelijk bedoeld was voor bevragingen en niet voor transacties)

_Invulling door REST-API_

Het REST API profiel v2 biedt hier geen specifieke ondersteuning voor, dit zou aanvullend bij implementatie moeten worden ingevuld met technieken die op de REST-API context aansluiten;

### WS-ReliableMessaging 

Voor gegarandeerde aflevering van berichten ; Dit hoort wel bij de WS-I standaarden maar is __niet expliciet onderdeel__ van de huidige DK WUS specificatie 

_Invulling door REST-API_

Het REST API profiel v2 biedt hier geen specifieke ondersteuning voor, dit zou aanvullend bij implementatie moeten worden uitgewerkt;
(HTTP biedt vanuit de standaard return codes die aangeven of een actie wel of niet geslaagd is)

### Stateful interacties

Bijvoorbeeld langlopende sessies met statusinformatie

_Invulling door REST-API_

Het REST API profiel v2 biedt hier geen specifieke ondersteuning voor, dit zou aanvullend bij implementatie moeten worden uitgewerkt;
(bijvoorbeeld token gebaseerd en/of een stateful backend)

### WSDL gebaseerde clients

Dit voor stricte contract validatie en code generatie in verschillende programmeer talen

_Invulling door REST-API_

REST kent OPENAPI specificatie en JSON Schema met tot op bepaalde hoogte vergelijkbare functionaliteit;
(WSDL kent een meer formele en stricte contract validatie)


## Conclusie

Wat betreft _"Kan het Digikoppeling WUS profiel vervangen worden door het Digikoppeling REST-API profiel"_

DK WUS SOAP services die niet sterk afhankelijk zijn van encryptie van bericht onderdelen, reliable messaging, multi step transacties en stateful interacties, denk hierbij bijvoorbeeld aan "bevragingen" (en simpele "transacties") zijn te vervangen door DK REST-API services;

Voor DK WUS SOAP services die gebruik maken van aanvullende WS-I functionaliteiten en die juist wel sterk leunen op deze functionaliteiten zou het nodig zijn om de benodigde extra functionaliteit bovenop het DK REST-API (zelf) extra te implementeren, Ook in de REST-API context zijn hier patronen en technieken voor beschikbaar;

Opmerking hierbij is dat het huidige DK WUS profiel zelf geen invulling of ondersteuning biedt voor Reliable Messaging of AtomicTransactions; 

Wat betekent dit voor het uitfaseren van het DK WUS profiel binnen de Digikoppeling standaard

Samengevat : services met bevragingen en simpele transacties zijn relatief eenvoudig te realiseren met de DK-REST-API Koppelvlakstandaard , services met complexe transacties en specifieke eisen mbt betrouwbare aflevering vragen om extra aandacht vergeleken met WS-I standaarden (en moeten buiten de DK REST-API standaard op een bepaalde manier worden gerealiseerd).

Hoewel het in principe mogelijk zou zijn om het Digikoppeling REST-API Koppelvlak uit te breiden met functionaliteit op het gebied van bv complexe transacties en betrouwbare aflevering is dit niet op korte termijn te verwachten (in REST context zijn hier nog geen internationale standaarden voor).

__Voorstel vanuit beheer__

Beperken van het aantal koppelvlakken door uitfaseren van DK-WUS brengt meer standaardisatie van koppelvlakken binnen de GDI,
Vanuit beheer Digikoppeling is daarom het voorstel:

DK WUS (nu al) de status 'uit te faseren' geven in het kader van life-cycle management en vanuit de gedachte dat bij nieuwbouw hier rekening mee gehouden kan worden en tijdig op gestuurd kan worden - met een ruime overgangstermijn om ook de complexere use-cases tijd te geven om een passende uitwerking te vinden.

In het kader van Life-Cycle Management van de Koppelvlakstandaarden krijgt het DK WUS Koppelvlak de status "Uit te faseren" als volgt:

Koppelvlak Standaard| Status | Toelichting | Einde Ondersteuning| Einde Gebruik |
|----| -------|--------------|------|---|
|Digikoppeling WUS |  Uit te faseren | Het DK WUS koppelvlak dient te worden uit gefaseerd |  01-01-2027  | 01-01-2032|

•	Na 01-01-2027 is gebruik nog toegestaan voor legacy applicaties tot 01-01-2032 - echter de organisatie is zelf verantwoordelijk voor functionele en security updates;


Digikoppeling koppelvlakken:
- DK REST_API profiel: Met name geschikt voor (synchrone) services en een data resource perspectief, bv bevragingen
- DK EBMS (2/3) profiel : Met name geschikt voor (asynchrone) services met "messaging" perspectief 
- DK WUS : Status uit te faseren [TO Digikoppeling - Uitfasering WUS](https://github.com/Logius-standaarden/Overleg/tree/main/Digikoppeling/2024-12-10#uitfasering-wus)

 


