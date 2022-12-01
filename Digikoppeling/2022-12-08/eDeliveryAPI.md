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
Signing van de KPAPI werkgroep Beveiliging;

JAdES is gebaseerd op _Detached JWS_,  Appendix F - RFC 7515: JSON Web Signature (JWS)  (en daarmee op standaard JWS principes)
Zie : https://datatracker.ietf.org/doc/rfc7515/

De signing uitwerking in eDelivery is in principe bruikbaar voor de invulling van een JAdES 
Signing module voor ADR en Digikoppeling REST API profiel.

Zie ook de KPAPI handreiking van de werkgroep Signing [Vergelijking REST API Signing Standaarden](https://geonovum.github.io/KP-APIs/publicaties/REST_API_Signing_Standaarden/) voor een vergelijking van JAdES  met de standaard HTTP Message Signatures.

Zie voor de invulling van Signing sectie 5.2.2 in het _eDelivery REST API Profile Version 1.0_.

## API life cycle
Life cycle management van de eDelivery REST API is op grote lijnen overeenkomstig ADR regels.
- Net als [API rule 16](API-16) vereist het eDelivery REST API profiel het gebruik van OAS voor documentatie van API's. Er is wel een verschil in de gebruikte versie 3.1 tov 3.0
- Net als [API rule 18](API-18) vereist het eDelivery REST API profiel een deprication schedule, dit is uitvoeriger beschreven par 5.3.2. In de ADR wordt dit wel benoemd maar niet gespecificeerd. We kunnen rule 18 dus hiermee verrijken.
- Net als [API rule 19](API-19) vereist het eDelivery REST API profiel een transition period for new major versions, beschreven in par 5.3.1.2 ook dit onderwerp wordt in de ADR  wel benoemd maar niet zo uitvoerig gespecificeerd als in het eDelivery REST API profiel. We kunnen rule 19 dus hiermee verrijken.
- Net als [API rule 56](API-56) vereist het eDelivery REST API profiel SEMVER, beschreven in par 5.3.1.
- sunsetting van operations is niet expliciet benoemd in de ADR maar wel in het eDelivery REST API profiel. dit kunnen we in de ADR dus toevoegen.
- Net als [API rule 20](API-20) vereist het eDelivery REST API profiel een major version nummer in de URI

Verder is ook uitgebreider beschreven wat  backwards compatibility inhoud. 
Kortom de life cycle beschrijving is  uitgebreider dan die in de ADR en kan gebruikt worden om de ADR specifieker te maken op deze punten.

Zie 5.3 in het _REST API Profile Version 1.0_.

## OpenAPI
Implementatie van JaAdES en life cycle management zijn gespecificeerd in OpenAPI. De eisen die in het algemeen hier aan gebruik van OpenAPI worden gesteld maken de API beter testbaar.

Zie ook https://github.com/isa2-api4ips/rest-api-profile/blob/main/api-documentation/openapi.yml

Zie 6.3 in het _REST API Profile Version 1.0_.

# Links

- [Project API4IPS in ISA² action "Innovative Public Services" deliverables](https://ec.europa.eu/digital-building-blocks/wikis/display/EDELCOMMUNITY/Project+deliverables)
- [eDelivery & OOTS Projectathon Process](https://ec.europa.eu/digital-building-blocks/wikis/pages/viewpage.action?pageId=610468539)

