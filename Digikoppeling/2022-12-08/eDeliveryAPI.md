# eDelivery REST API, lessons to be learned

## Kader en inleiding

Binnen de EU is digitalisering een thema waar, zeker de laatste jaren, steeds 
meer nadruk op is komen te liggen. EU beleid is wordt vastgesteld in directives, 
regels die door de lidstaten geïmplementeerd moeten worden en in acts, die 
impact kunnen hebben op lidstaten maar die geen verplicht karakter hebben. 
Voor digitalisering zijn de Digital Services Act (DSA), de Digital Markets Act (DMA) 
en Digital Governance Act (DGA) van belang. 
Om deze acts mogelijk te maken heeft de EU een aantal projecten en werkgroepen. 
eDelivery is hierin een bouwsteen. 

In ISA^2 is een pilot uitgevoerd om een eDelivery REST API profiel op te stellen en 
te beproeven. De documentatie van de pilot is onlangs gepubliceerd door EU Digit. 
De documentatie geeft een aantal oplossingen die ook in ADR, NL-oAuth en in het 
Digikoppeling REST API profile kunnen worden toegepast.

## Architectuur

Om in de pilot een concrete implementatie te maken van de eDelivery API zijn keuzes 
gemaakt, bijvoorbeeld in het gebruik van velden die binnen gebruikte standaarden 
vrij gelaten waren. Daarmee is een aantal profielen gemaakt die kunnen worden 
gebruikt om standaarden als oAuth, OpenAPI en Jades op een standaard manier toe 
te passen. Het gebruik van de profielen (en de profielen zelf) kunnen in de 
API architectuur van het KP API's worden opgenomen.

## Authorisatie
oAuth 2.0 en OpenID zijn verplicht in het eDelivery profile. Er zijn restricties op 
oAuth gezet, het is een volwaardig profiel. Aan een aantal verschillende cases zijn 
_architecture profiles_ gehangen. Er zijn vier verschillende topologien, met of zonder 
authorisation server etc. In de eDelivery REST API specificatie verwijzen ze verder 
naar de topologien. Daardoor is duidelijk voor iemand die implementeert om te zien 
welke configuratie relevant is.

## OpenAPI

## API life cycle
Life cycle management van de eDelivery REST API is overeenkomstig ADR regels. 
Wat is backwards compatible? De life cycle beschrijving is wel uitgebreider dan die
in de ADR en kan gebruikt worden om de ADR specifieker te maken op dit punt.

## Signing
eDelivery profiel maakt gebruik van JAdES . De eDelivery invulling is gedeeld met de (sub)werkgroep 
signing van de KPAPI werkgroep beveiliging;

De signing uitwerking in eDelivery is in principe bruikbaar voor de invulling van een JAdES 
Signing module voor ADR en Digikoppeling REST API profiel.

Zie ook Vergelijking REST API Signing Standaarden (geonovum.github.io) voor een vergelijking van 
JAdES  met de standaard HTTP Message Signatures.
