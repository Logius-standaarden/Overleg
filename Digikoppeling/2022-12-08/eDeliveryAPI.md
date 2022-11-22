# eDelivery REST API, lessons to be learned

## Kader en inleiding

Binnen de EU is digitalisering een thema waar, zeker de laatste jaren, steeds 
meer nadruk op is komen te liggen. EU beleid is wordt vastgesteld in directives, 
regels die door de lidstaten geïmplementeerd moeten worden en in acts, die 
impact kunnen hebben op lidstaten maar die geen verplicht karakter hebben. 
Voor digitalisering zijn de Digital Services Act (DSA), de Digital Markets Act (DMA) 
en Digital Governance Act (DGA) van belang. 
Om deze acts mogelijk te maken heeft de EU een aantal projecten en werkgroepen. 
eDelivery is hierin een bouwsteen. Onlangs heeft EU Digit de documentatie gepubliceerd
van een pilot project waarbij een REST API eDelivery koppelvlak is ontwikkeld en getest.

## Architectuur

Om in de pilot een concrete implementatie te maken van de eDelivery API zijn keuzes 
gemaakt, bijvoorbeeld in het gebruik van velden die binnen gebruikte standaarden 
vrij gelaten waren. Daarmee is een aantal profielen gemaakt die kunnen worden 
gebruikt om standaarden als oAuth, OpenAPI en Jades op een standaard manier toe 
te passen. Het gebruik van de profielen (en de profielen zelf) kunnen in de 
API architectuur van het KP API's worden opgenomen.

De architecture topologies ...

API life cycle...

## Authorisatie
oAuth lessons learned en vervolg

## OpenAPI

## Signing
eDelivery profiel maakt gebruik van JAdES . De eDelivery invulling is gedeeld met de (sub)werkgroep 
signing van de KPAPI werkgroep beveiliging;

De signing uitwerking in eDelivery is in principe bruikbaar voor de invulling van een JAdES 
Signing module voor ADR en Digikoppeling REST API profiel.

Zie ook Vergelijking REST API Signing Standaarden (geonovum.github.io) voor een vergelijking van 
JAdES  met de standaard HTTP Message Signatures.
