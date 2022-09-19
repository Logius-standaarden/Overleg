## Algemeen

Wijzigingsvoorstellen zijn gedocumenteerd in het issue. Klik in de overzichte grote en kleine wijzigingen op een issue en de discussie, en eventueel het bijbehorende pull request met wijzigingen zijn in te zien. Hier kan iedereen, dus zeker ook de leden van het Technisch Overleg, commentaar geven op een wijzigingsvoorstel.

## Publieke consultatie RFC Toevoegen API-58 No sensitive information in URIs

Uit de publieke consultatie is als opmerking gekomen dat het wenselijk is om aan te geven hoe gevoelige informatie in URI's dient te worden overgebracht.
Dit is ook als Voorstel/Pull Request aangegeven bij de extensie security van de ADR. Voor het RFC API-58 No sensitive information in URI's is daarom voorgesteld om in dit geval HTTP POST te gebruiken.<BR>
 - [Voorstel nav resultaat publieke consultatie ](https://github.com/Logius-standaarden/Digikoppeling-Koppelvlakstandaard-REST-API/pull/20/files#diff-f9866e428c8e44bb537ed5fdddcbc14d754a99c615463c6d7c7f5dd1a7e2ee22) <BR>
 - [Preview voorgestelde aanpassing](https://logius-standaarden.github.io/Publicatie-Preview/Digikoppeling-Koppelvlakstandaard-REST-API/API-58-BP/#afspraken-api-design-rules-extensies)

 __Ter goedkeuring__

## Aanpassing beheermodel op BOMOS principes en MIDO governance

Het Digikoppeling beheermodel is geheel herschreven. Het nieuwe beheermodel is gebaseerd op de [BOMOS template](https://github.com/Logius-standaarden/BOMOS-voorbeeld-beheermodel). Het beheermodel behandelt achtereenvolgens de BOMOS componenten strategie, tactiek, operationeel, implementatieondersteuning en communicatie. Daarmee wordt duidelijker gemaakt hoe Digikoppeling BOMOS toepast. In de nieuwe versie is ook de nieuwe governance structuur beschreven. Deze is passend gemaakt binnen de GDI governance.

Daarnaast zijn de algemene operationele aspecten zoals toepassing van respec, gebruik van Github actions and pages beschreven. Tevens is de versienummering toegelicht. Nieuw is dat in de versienummering we uitgaan van [Semantic Versioning](https://semver.org/).

__Ter review__, bijlage over Semantic Versioning __Ter goedkeuring__

## ebMS3 transitie

Om de business case voor transitie door stakeholders te kunnen maken zijn we op zoek naar use cases voor toepassing van eDelivery (ebMS3/AS4) als koppelvlakspecificatie. Tevens leggen we contacten in de EU om de eDelivery ontwikkelingen nauw te kunnen volgen.

__Ter info__

## RSIN of Kvk nummer leidend voor OIN?

We hebben onderzocht of een OIN nummer gebaseerd zou moeten zijn op het RSIN of het KvK nummer. De vraag kwam op omdat in de implementatie nu de facto een voorkeur wordt gegeven aan KvK nummers omdat deze eenvoudig via de interface zijn op te vragen. De vraag was om dit formeel te documenteren. In het [Digikoppeling Identificatie en Authenticatie document](https://github.com/Logius-standaarden/Digikoppeling-Identificatie-en-Authenticatie) staat echter dat het RSIN de voorkeur heeft als identificerend nummer. Documentatie van het OIN stelsel wordt hierop aangepast. [Gedocumenteerd in het issue met link naar het pull request](https://github.com/Logius-standaarden/OIN-Stelsel/issues/5).

## StvZ lopende roadmap items

### Digikoppeling governance

Zie hierboven en issue onder [grote wijzigingen](#Grote-wijzigingen).

### Informatievoorziening

We streven naar een vereenvoudiging van onze informatievoorziening.
* Plan is om de documentatie te gaan publiceren via https://gitdocumentatie.logius.nl/.

[Overzicht publicatiesites](media/Publicatie.png)

### Signing & Encryptie toevoegen aan RESTful API profiel

Onderzoek loopt in samenwerking met KP API werkgroep beveiliging.

### Identificatie en Routering

Handreiking voor ondersteuning voor dit onderwerp is ontwikkeld.
(Zie apart agenda punt)

### Doorontwikkeling RESPEC/Digikoppeling template voor publicatie van specificaties

Het [ReSpec-profiel](https://github.com/Logius-standaarden/respec) is stabiel en in gebruik in alle Digikoppeling-documenten. De wens is het profiel meer modulair op te zetten om onderhoud te vergemakkelijken en gebruik buiten Logius te faciliteren. 

Zie ook het [ReSpec-Logius-template](https://github.com/Logius-standaarden/respec-template)
### Onderzoek verwijzing naar de 'ADR API Security Extensie' vanuit de Digikoppeling Beveiligingsvoorschriften		 	 	 	 

Onderzoek is afgerond, uit het onderzoek is de _RFC API-58 No sensitive information in URIs_ gekomen als kandidaat regel om op te nemen (zie apart agenda punt)

Toelichting relatie REST-API profiel en ADR extensies:

Het Digikoppeling REST-API profiel is gebaseerd op het normatieve deel van de ADR, daarnaast worden enkele (relevante) regels overgenomen uit de (informatieve) ADR extensies;
(Deze regels worden daarmee voor het Digikoppeling REST-API profiel normatief.)

![DK](media/Digikoppeling%20gebaseerd%20op%20ADR.drawio.svg)

### Update Beheermodel / aansluiting op Logius Standaarden BOMOS generiek beheer model & governance	 	 	 	 	 

Ontwikkeling BOMOS generiek model loopt. Er is een [template beheermodel](https://github.com/Logius-standaarden/BOMOS-voorbeeld-beheermodel) voor BOMOS. Het beheermodel Digikoppeling wordt op basis hiervan herschreven.

### Verkennen mogelijk gebruik ebMS3/AS4

Zie hierboven en issue onder [grote wijzigingen](#Grote-wijzigingen).

## eDelivery ontwikkelingen

De EU heeft een _informal cooperation network_ eDelivery. Hierin worden
ontwikkelingen rondom eDelivery besproken. Daarnaast heeft de EU in kader
van het ISA^2 programma een pilot uitgevoerd naar een REST API profiel
voor eDelivery.
[De documentatie van dit REST API profiel is onlangs gepubliceerd](https://joinup.ec.europa.eu/collection/api4dt/document/isa2-ips-rest-api-profile), er is ook een
[git repository](https://github.com/isa2-api4ips/rest-api-profile).
