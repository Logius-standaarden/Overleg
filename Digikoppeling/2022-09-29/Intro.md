## Aanpassing beheermodel op BOMOS principes en MIDO governance

Het Digikoppeling beheermodel is geheel herschreven. Het nieuwe beheermodel is gebaseerd op de [BOMOS template](https://github.com/Logius-standaarden/BOMOS-voorbeeld-beheermodel). Het beheermodel behandelt achtereenvolgens de BOMOS componenten strategie, tactiek, operationeel, implementatieondersteuning en communicatie. Daarmee wordt duidelijker gemaakt hoe Digikoppeling BOMOS toepast. In de nieuwe versie is ook de nieuwe governance structuur beschreven. Deze is passend gemaakt binnen de GDI governance.

Daarnaast zijn de algemene operationele aspecten zoals toepassing van respec, gebruik van Github actions and pages beschreven. Tevens is de versienummering toegelicht. Nieuw is dat in de versienummering we uitgaan van [Semantic Versioning](https://semver.org/).

__Ter review__

## ebMS3 transitie

Om de business case voor transitie door stakeholders te kunnen maken zijn we op zoek naar use cases voor toepassing van eDelivery (ebMS3/AS4) als koppelvlakspecificatie. Tevens leggen we contacten in de EU om de eDelivery ontwikkelingen nauw te kunnen volgen.

__Ter info__

## RSIN of Kvk nummer leidend voor OIN?

We hebben onderzocht of een OIN nummer gebaseerd zou moeten zijn op het RSIN of het KvK nummer. De vraag kwam op omdat in de implementatie nu de facto een voorkeur wordt gegeven aan KvK nummers omdat deze eenvoudig via de interface zijn op te vragen. De vraag was om dit formeel te documenteren. In het [Digikoppeling Identificatie en Authenticatie document](https://github.com/Logius-standaarden/Digikoppeling-Identificatie-en-Authenticatie) staat echter dat het RSIN de voorkeur heeft als identificerend nummer. Documentatie van het OIN stelsel wordt hierop aangepast. [Gedocumenteerd in het issue met link naar het pull request](https://github.com/Logius-standaarden/OIN-Stelsel/issues/5). 

## StvZ lopende roadmap items

### Digikoppeling governance

Zie hierboven en issue onder [grote wijzigingen](#Grote-wijzigingen). [Schema beheerproces](media/Beheerproces.svg)

### Informatievoorziening

We streven naar een vereenvoudiging van onze informatievoorziening.
* we willen https://publicatie.centrumvoorstandaarden.nl/ uitfaseren en overgaan naar https://gitdocumentatie.logius.nl/
* publicatie van agenda's via github

[Overzicht publicatiesites](media/Publicatie.png)

### Signing & Encryptie toevoegen aan RESTful API profiel

Onderzoek loopt in samenwerking met KP API werkgroep beveiliging

### Identificatie en Routering

Handreiking voor ondersteuning voor dit onderwerp is in ontwikkeling
(Zie apart agenda punt)

### Interoperabiliteit platformen WUS bij gebruik MTOM in combinatie met WS-Security (signing)

Voorbeeld berichten van datapower zijn onderzocht. Aanpassingen op de WUS standaard om de interoperabiliteit te vergroten zouden grote impact hebben op bestaande implementaties die gebruik maken van andere platformen. In het overleg 23-6-2022 is besloten de standaard op dit punt niet aan te passen

### Doorontwikkeling RESPEC/Digikoppeling template voor publicatie van specificaties

Het [ReSpec-profiel](https://github.com/Logius-standaarden/respec) is stabiel en in gebruik in alle Digikoppeling-documenten. De wens is het profiel meer modulair op te zetten om onderhoud te vergemakkelijken en gebruik buiten Logius te faciliteren.

### Onderzoek verwijzing naar de 'ADR API Security Extensie' vanuit de Digikoppeling Beveiligingsvoorschriften		 	 	 	 

Onderzoek loopt.

Toelichting relatie REST-API profiel en ADR extensies:

Het Digikoppeling REST-API profiel is gebaseerd op het normatieve deel van de ADR, daarnaast worden enkele (relevante) regels overgenomen uit de (informatieve) ADR extensies;
(Deze regels worden daarmee voor het Digikoppeling REST-API profiel normatief.)

![DK](media/Digikoppeling%20gebaseerd%20op%20ADR.drawio.svg)

### Update Beheermodel / aansluiting op Logius Standaarden BOMOS generiek beheer model & governance	 	 	 	 	 

Ontwikkeling BOMOS generiek model loopt. Er is een [template beheermodel](https://github.com/Logius-standaarden/BOMOS-voorbeeld-beheermodel) voor BOMOS. Het beheermodel Digikoppeling wordt op basis hiervan herschreven.

### Verkennen mogelijk gebruik ebMS3/AS4

Zie hierboven en issue onder [grote wijzigingen](#Grote-wijzigingen).
