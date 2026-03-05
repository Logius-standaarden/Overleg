# Inhoudsopgave
1. [Reactie vanuit JustID t.a.v. FSC](##reactie-vanuit-justid-tav-fsc)
2. [Reactie vanuit Kadaster t.a.v. FSC](#reactie-vanuit-kadaster-tav-fsc)
3. [Reactie vanuit Kadaster t.a.v. reliable messaging / API](#reactie-vanuit-kadaster-tav-reliable-messaging-tekstuele-verduidelijking)
4. [Reactie vanuit Min J&V t.a.v. sensitive information in URL](#reactie-vanuit-min-jv-tav-sensitive-information-in-url)
5. [Reactie vanuit Logius n.a.v. vragen vanuit Rechtspraak t.a.v. bestaande implementaties zonder FSC](#reactie-vanuit-logius-nav-vragen-vanuit-rechtspraak-tav-bestaande-implementaties-zonder-fsc)

# Reactie vanuit JustID t.a.v. FSC

## Aanleiding 
Naar aanleiding van de beproeving van de FSC-standaard in de "Proof of Concept Flexibel Digitaal Uitwisselen", vragen wij aandacht voor twee structurele beperkingen in de huidige FSC-specificaties. 
 
### Issue 1: Onverenigbaarheid van mTLS-eisen met zone-gebaseerde netwerkarchitectuur

#### Probleem
De FSC-standaard (o.a. FSC-Core v1.1.2) schrijft een strikte peer-to-peer mTLS-verbinding voor tussen de Outway en de Inway. De achterliggende noodzaak is dat partijen elkaars PKI overheid-certificaat (en het daarin vervatte OIN) direct moeten kunnen valideren.
 
In de praktijk van het Diginetwerk (als koppelnetwerk) hanteren veel overheidsorganisaties echter een strategie waarbij zij achterliggende organisaties ontsluiten via een beveiligde zone (DMZ), zoals het JUBIT-domein bij JenV. Hierbij wordt een intermediair ingezet, zoals de Justitie Berichten Service (JUBES).
 
##### Knelpunt 
Om te voldoen aan beveiligingseisen (zoals de BIO) is voor verkeer tussen zones vaak een 'protocol break' vereist voor inspectie en veilige routering. Zodra deze intermediair wordt ingezet, "zien" de ontvangende partijen enkel het certificaat van de intermediair en niet meer het oorspronkelijke certificaat van de afzender.
 
De huidige tekst in FSC-Core v1.1.2 stelt:
"All connections between Peers leverage mTLS" en "The Inway MUST verify the certificate of the Outway".
 
Deze eis blokkeert de inzet van FSC in scenario's waar een protocol break op een gateway noodzakelijk is.
 
##### Mogelijke oplossing
Ondersteun de optie van gedelegeerde authenticatie. Hierbij valideert de intermediair (gateway) de verbinding en geeft de identiteitsgegevens van het oorspronkelijke certificaat door in een gestandaardiseerde, cryptografisch ondertekende HTTP-header aan de achterliggende Inway. De Inway accepteert deze identiteit op basis van een vertrouwensrelatie met de gateway.

 
### Issue 2: Beveiligingsrisico door bidirectionele verbindingsvereiste FSC Directory

#### Probleem
Een tweede knelpunt betreft de communicatie tussen de FSC Directory en de FSC Managers. In de huidige opzet wordt uitgegaan van een bidirectionele verbinding. De FSC Directory moet verbinding kunnen maken met de Managers om services te publiceren en te beheren.
 
##### Knelpunt 
Vanuit security-perspectief is het onnodig openzetten van inbound verbindingen naar een intern domein (zoals de Manager-locatie) ongewenst. Het vereist complexe firewall-configuraties en vergroot de kans op een aanval. Net als bij Issue 1 bemoeilijkt dit de passage door DMZ-zones en gateways, aangezien inbound verkeer naar kritieke componenten streng gereguleerd is.
 
##### Mogelijke oplossing 
Maak de communicatie tussen de FSC Directory en de Managers unidirectioneel (outbound vanuit de Manager).

* De Manager initieert de verbinding naar de Directory (polling of push-model).
* Dit voorkomt het onnodig openzetten van inbound poorten op het interne netwerk van de aangesloten organisatie.
* Het opzetten van een outbound verbinding is technisch eenvoudiger, veiliger en sluit beter aan bij de netwerkbeveiligingsrichtlijnen binnen de overheid.

_Voorstel vanuit beheer is dit verder te behandelen in de Sub Werkgroep FSC en mee te nemen in de behandeling voor een volgende versie van de standaard_ 

 
# Reactie vanuit Kadaster t.a.v. FSC

## Vraag
Deze vraag gaat over FSC logging: in de standaard FSC logging wordt een TransactionID gedefinieerd. Kadaster is van mening dat dit overlapt met de W3C Trace Context. Het voorstel is dan dus ook om hier gebruiken we hier de W3C Trace Context voor te gebruiken. Veel componenten in het landschap ondersteunen deze standaard waaronder Open Telemetry (OTEL).

_Voorstel vanuit beheer is dit verder te behandelen in de Sub Werkgroep FSC en mee te nemen in de behandeling voor een volgende versie van de standaard_ 

# Reactie vanuit Kadaster t.a.v. Reliable Messaging (Tekstuele verduidelijking)

## Vraag
Kan bij de tekst over 'reliable' messaging in de toelichting worden aangegeven dat met REST-API's ook betrouwbare overdracht kan worden gerealiseerd:

_Hoewel REST op protocolniveau geen 'reliable' profiel bevat  zoals ebMS2 (ten behoeve van gegarandeerde aflevering van berichten), is het echter een dusdanig robuust communicatieprotocol dat met toevoeging van bijvoorbeeld conversatie- en/of publish-subscribe patronen (en technologie) zeer betrouwbare communicatie kan worden gerealiseerd._

Voorgestelde tekst aanpassing:
https://github.com/Logius-standaarden/Digikoppeling-Architectuur/pull/30

# Reactie vanuit Min J&V t.a.v. sensitive information in URL

In vorige versies van het profiel was opgenomen bij de regel API-58 No sensitive information in URIs : 	
_Alleen verplicht indien er sprake is van logging in systemen die niet onder controle van de betrokken client- en serverorganisatie staan_

In de laatste versie is dit niet meer opgenomen, maar dit is wel een wenselijke uitzondering;

Toelichting vanuit Beheer:
In samenwerking met de indiener is dit aangepast in de ADR , het is dan niet meer nodig om dit in het REST-API profiel op te nemen;
Zie : [Clarify how TLS works and when sensitive information in URIs should not be used](https://github.com/Logius-standaarden/API-Design-Rules/pull/277/changes)

De aanpassing is behandeld in het TO ADR 3/3/2026 en zal in de volgende release ADR worden meegenomen;

# Reactie vanuit Logius n.a.v. vragen vanuit Rechtspraak t.a.v. bestaande implementaties zonder FSC

Bij de FSC toeliching  was bij de release 30-1-2025 opgenomen:
_(2) Voor bestaande implementaties is het toegestaan tot 1/1/2027 gebruik te maken van versie 1.1 van de Digikoppeling REST-API Koppelvlakstandaard_

Zie : [Gebruik van Federated Service Connectivity Standaard (FSC) in bestaande implementaties](https://logius-standaarden.github.io/Openbare-Consultaties/2026-01-Digikoppeling-FSC/dk/api/#federated-service-connectivity-standaard-fsc)

Dit was opgenomen om bij de introductie van FSC begin 2025 expliciet aan te geven bij de verplichting dat bestaande Digikoppeling REST-API implementaties zonder FSC niet per direct moesten voldoen aan de verplichting maar nog een bepaalde tijd hadden om over te gaan op FSC; 
Maar deze genoemde einddatum geeft nu vragen vanuit bv Rechtspraak: is dit een (strakke) deadline waarna bepaalde koppelingen mogelijk niet meer gaan werken?;

Voorstel vanuit beheer is om dit punt (2) niet langer op te nemen en alleen te verwijzen naar het pas-toe-of-leg-uit-beleid: https://www.forumstandaardisatie.nl/pas-toe-leg-uit-beleid 
waar de verplichting onder valt;




