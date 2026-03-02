# Inhoudsopgave
1. [Reactie vanuit JustID t.a.v. FSC](##reactie-vanuit-justid-tav-fsc)
2. [Reactie vanuit Kadaster t.a.v. FSC](#example2)

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
 
# Reactie vanuit Kadaster t.a.v. FSC

## Vraag
Deze vraag gaat over FSC logging: in de standaard FSC logging wordt een TransactionID gedefinieerd. Kadaster is van mening dat dit overlapt met de W3C Trace Context. Het voorstel is dan dus ook om hier gebruiken we hier de W3C Trace Context voor te gebruiken. Veel componenten in het landschap ondersteunen deze standaard waaronder Open Telemetry (OTEL).
 

