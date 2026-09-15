## Digikoppeling Toekomstvisie : Uitwerking nav Themadag 

Zie Notitie [Toekomstbeeld Digikoppeling](https://github.com/Logius-standaarden/Overleg/blob/main/Digikoppeling/2026-09-24/2026_09_15_Toekomstbeeld%20Digikoppeling_concept.pdf)

In dit document wordt een toekomstbeeld geschetst voor de Digikoppeling standaard. Input hiervoor is de themamiddag Toekomstbeeld Digikoppeling van 24/6 (zie: [Verslag themamiddag Toekomstbeeld Digikoppeling 24/6](https://github.com/Logius-standaarden/Overleg/blob/main/Digikoppeling/2026-09-24/20260624_Themadag%20Digikoppeling_verslag.md) )

_De TO leden wordt gevraagd in te stemmen met het voorstel voor de richting van de doorontwikkeling van de Toekomstvisie_



## GraphQL

Onderzoek GraphQL is opgenomen op de Digikoppelikng Roadmap voor kwartaal 2026-4 : [Onderzoek GraphQL](https://gitdocumentatie.logius.nl/publicatie/dk/roadmap/2026-2027/#onderzoek-uitbreiding-digikoppeling-met-graphql)

Vanuit programma [Gemeenschappeliijke Bronontsluiting (GBO)](https://ictu.github.io/GBO/latest/) is specifiek gevraagd naar de mogelijkheden om GraphQL ook status te geven binnen de GDI standaarden;

Omdat GraphQL een waardevolle standaard is voor data resource georiënteerde architectuur is deze ook in de voorgestelde toekomstvisie opgenomen als een kandidaat voor opname onder Digikoppeling;
Er zijn ook al ideeën over wat waardevol is om in een GraphQL profiel op te nemen : bv het standaardiseren van error afhandeling;

Binnen het Kennisplatform API's is GraphQL ook al langere tijd op de radar. Daarom is het voorstel om een GraphQL profiel binnen / in samenwerking met  het Kennisplatform API's te ontwikkelen.
Bij de eerstvolgende bijeenkomst van het Kennisplatform API's in novemnber zal een sessie worden gewijd aan GraphQL en een oproep worden gedaan voor deelname aan de werkgroep (bij voldoende belangstelling)

_De leden van het TO wordt gevraagd in te stemmen met deze aanpak_ 

Ter informatie:
Op developer.overheid heeft Joost Farla een aantal artikelen geschreven over GraphQL

- https://developer.overheid.nl/blog/2026/07/30/graphql-1-introductie
- https://developer.overheid.nl/blog/2026/08/18/graphql-2-flexibiliteit-en-limieten
- https://developer.overheid.nl/blog/2026/08/26/graphql-3-schema-ontwerp
- https://developer.overheid.nl/blog/2026/09/02/graphql-4-afwegingskader

## Grote Berichten

In voorgaande TO's kwam naar voren dat Grote Berichten complex is om te implementeren.
Ook is het koppelvlak toegespitst op een messaging aanpak op basis van XML, zoals beschreven in [het leidend principe](https://gitdocumentatie.logius.nl/publicatie/dk/gb/3.8.1/#leidend-principe).
Daarom was er behoefte om een REST API equivalent te schrijven voor grote berichten.

Een initiele opzet hiervoor hebben we beschikbaar gemaakt als [ADR module Transfer](https://logius-standaarden.github.io/API-mod-transfer/).
Deze module maakt gebruik van bestaande HTTP RFC's en veelgebruikte headers zoals "Range" en "Content-Digest".
Logius heeft als haalbaarheidstoets deze module geimplementeerd in zowel Java als Dotnet, om daarmee ervaring op te doen uit de praktijk.
Uit deze twee voorbeelden blijkt dat het goed te doen is.

De leden van het TO worden gevraagd deze initiele versie door te nemen en aan te geven welke organisaties dit willen uitproberen in een prototype.
Nadat er een succesvolle implementatie is die naar tevredenheid van de organisatie(s) functioneert, willen we deze module vaststellen binnen Kennisplatform API's en daarna in een toekomstig TO Digikoppeling deze module toevoegen aan het REST API Profiel.

_De leden van het TO wordt gevraagd in te stemmen met deze aanpak_ 

## FSC Signing Service (v1.0.0, concept)

FSC Signing Service is een extensie op FSC Core waarmee organisaties zonder eigen FSC Manager toch als Delegator kunnen deelnemen aan een FSC Group. Een Signing Service is zelf een Peer die een multi-tenant Manager exploiteert en namens Managed Peers Contracten aanmaakt, ontvangt en ondertekent. 
Ondertekenen kan pas nadat een bevoegd vertegenwoordiger zich heeft geauthenticeerd via een vertrouwde authenticatiedienst (bv eHerkenning of eIDAS); de handtekening bevat een authentication proof zonder persoonsgegevens, dat andere Peers via de audit trail API kunnen verifiëren. 
De scope is beperkt - de Delegatee en de niet-gedelegeerde provider houden een eigen Manager. De extensie vervangt `External Contract Reference` door cryptografisch verifieerbare delegatie.

- [het conceptdocument](https://gitlab.com/rinis-oss/fsc/signing-service/-/blob/main/docs/fsc-signing-service-extension-v1.0.0.md?ref_type=heads&plain=0)
- [Notulen FSC sub-WG](https://github.com/Logius-standaarden/Overleg/blob/main/FSC/notulen/20260716.md#3-demonstratie-proof-of-concept-signing-service)
- [Presentatie](../../../main/FSC/presentaties/delegation-high-level-design-v1.2.pdf)
