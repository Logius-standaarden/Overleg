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

In ISA<sup>2</sup> is een pilot uitgevoerd om een eDelivery REST API profiel op te 
stellen en te beproeven. De documentatie van de pilot is onlangs gepubliceerd door EU Digit. 
De documentatie geeft een aantal oplossingen die ook in ADR, NL-oAuth en in het 
Digikoppeling REST API profile kunnen worden toegepast. Twee van de documenten zijn bijgevoegd: 
_ISA² IPS REST API Profile Version 1.0_ en _REST API Pilot: Implementation Overview_

## Architectuur
Om in de pilot een concrete implementatie te maken van de eDelivery API zijn keuzes 
gemaakt, bijvoorbeeld in het gebruik van velden die binnen gebruikte standaarden 
vrij gelaten waren. Daarmee is een aantal profielen gemaakt die kunnen worden 
gebruikt om standaarden als oAuth, OpenAPI en Jades op een standaard manier toe 
te passen. Het gebruik van de profielen (en de profielen zelf) kunnen in de 
API architectuur van het KP API's worden opgenomen.

## Authorisatie
oAuth 2.0 en OpenID zijn verplicht in het eDelivery profile. Er zijn restricties op 
oAuth gezet, het is daarmee een volwaardig profiel. Een aantal verschillende cases 
zijn uitgewerkt in  _architecture topologies_. Er zijn vier verschillende topologiën,
respectievelijk met interne  en externe authorization servers en identity providers. 
In de eDelivery _REST API specificatie_ en in de _implementation overview_ wordt 
eenvoudigwweg verwezen naar deze topologiën. Daardoor is duidelijk bij implementatie 
te zien welke configuratie relevant is.

Zie secties onder 5.1 in het _REST API Profile Version 1.0_.

We hebben hiervoor [een wijzigingsvoorstel op oAuth ingediend](https://github.com/Logius-standaarden/OAuth-NL-profiel/issues/27)

In sectie 5.4.1.2 _Resource identifiers_ staat een stuk over gebruik van hash values als
identifiers. Dit biedt mogelijk een oplossing voor een issue uit het Kennisplatform API's:
https://github.com/Geonovum/KP-APIs/pull/464 

## Signing
eDelivery profiel maakt gebruik van JAdES voor Signing. De eDelivery invulling is gedeeld met de (sub)werkgroep 
Signing van de KPAPI werkgroep beveiliging;

De signing uitwerking in eDelivery is in principe bruikbaar voor de invulling van een JAdES 
Signing module voor ADR en Digikoppeling REST API profiel.

JAdES is gebaseerd op _Detached JWS_,  Appendix F - RFC 7515: JSON Web Signature (JWS)  (en daarmee op standaard JWS/JWE principes)
Zie : https://datatracker.ietf.org/doc/rfc7515/

Zie ook de KPAPI handreiking van de werkgroep Signing [Vergelijking REST API Signing Standaarden](https://geonovum.github.io/KP-APIs/publicaties/REST_API_Signing_Standaarden/) voor een vergelijking van JAdES  met de standaard HTTP Message Signatures.

Zie voor de invulling van Signing sectie 5.2.2 in het _eDelivery REST API Profile Version 1.0_.

## API life cycle
Life cycle management van de eDelivery REST API is op grote lijnen overeenkomstig 
ADR regels. Wat is backwards compatible? 
De life cycle beschrijving is wel uitgebreider dan die in de ADR en kan gebruikt
worden om de ADR specifieker te maken op dit punt.

Zie 5.3 in het _REST API Profile Version 1.0_.

## OpenAPI
Implementatie van JaAdES en life cycle management zijn gespecificeerd in OpenAPI. De eisen die in het algemeen hier aan gebruik van OpenAPI worden gesteld maken de API beter testbaar.

Zie ook https://github.com/isa2-api4ips/rest-api-profile/blob/main/api-documentation/openapi.yml

Zie 6.3 in het _REST API Profile Version 1.0_.
