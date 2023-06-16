# Technisch Overleg Terugmelden, 23 mei 2023

Aanwezig: Hein Baan (Kadaster), Alexander Green, Edwin Wisse (Logius)

Webex: Mirian van Ansem (BZK), Harm Olthof (GKG, GEON), Ronald van Dijk (Belastingdienst), 
Jan Karel van gent (KvK), Martin van der Plas en Dennis Passage (Logius)

## Opening en welkom

Dit Technisch Overleg is een herstart van het Technisch Overleg DMKS. Het heeft enige jaren 
stilgelegen, de DMKS standaard is uitontwikkeld. Dit overleg is bedoeld om een herstart van de
standaardontwikkeling te verkennen. Er is in een aantal pilots en diensten ervaring opgedaan met
diensten gebaseerd op API's.

## Gegevensknooppunt Groningen, Harm Olthof

In het Gegevensknooppunt Groningen (GKG) zijn DMKS koppelingen gelegd met de HR, BAG en BRP 
basisregistraties. Partijen in het GKG hebben van 2019 tot 2021 een pilot _Waterketenkaart_ 
uitgevoerd. Hierin hebben GEON, Logius samen met lokale overheden ook een pilot voor 
terugmelding uitgevoerd. Doel van de pilot is het onderzoeken of de stelselcatalogus en 
Digimelding voor niet-basisregistraties kunnen worden gebruikt en of terugmelding helpt bij 
kwaliteitsverbetering. In de waterketenkaart worden rioleringsgegevens gedeeld tussen gemeenten 
en waterschappen. 

Er kunnen meldingen gedaan worden voor:
1. ontbrekend object
2. object onterecht opgenomen
3. dubbel object
4. onjuiste classificatie
5. overige constatering

Meldingen konden via een (webgis) kaart gedaan worden. Meldingen worden via DMKS doorgegeven 
aan de basisregistraties. Een van de geleerde lessen was dat locatie niet ondersteund werd door 
de Logius dienst. Dit is opgelost door een x en y-coordinaat toe te gebruiken. 

## Stand van zaken Kennisplatform API's, Martin van der Plas

Toelichting van de recente onderverdeling van de _API Design Rules_ in modules. Er zijn modules voor 
encryptie en signing voor vertrouwelijke informatie en modules.

Ronald van Dijk stelt de vraag hoe een DMKS-API opgenomen zou worden.

Martin van der Plas: Voor autorisatie en authenticatie zou de Digikoppeling REST API specificatie 
voldoende moeten zijn. 
[De repository van de Digikoppeling REST API specificatie staat op git](https://github.com/Logius-standaarden/Digikoppeling-Koppelvlakstandaard-REST-API).

Dennis Passage stelt de vraag of PKIO nodig is voor Digikoppeling REST API. Dit is in ieder geval 
voor overheden het geval. Voor gegevensverkeer tussen burgers en overheden is Oauth toepasbaar.

Voor het TO de vraag: wordt de terugmeldspecificatie een module binnen de API Design Rules of wordt 
het een afzonderlijke standaard (die wel de API Design Rules toepast).

## Makkelijk melden, Dennis Passage

Presentatie over de _Makkelijk melden_ pilot. In de _Makkelijk melden_ pilot is een vereenvoudigde invoer portaal ontwikkeld om terugmeldingen op de BRP laagdrempeliger te maken. Het as-is Digimelding was één geheel waarin systeem 
en gebruikersinterface (portal) geïntegreerd waren. De invoerschermen waren uitgebreid en bleken in 
de praktijk remmend voor gebruik. Met de politie en woningcorporaties is samengewerkt om een eenvoudiger 
invoerdienst te maken aan de hand van klantreizen. Hiervoor is de portal losgemaakt van het Digimelding systeem. 

Op de vraag van Jan Karel van Gent of burgers ook toegang zouden kunnen krijgen tot _Makkelijk melden_ gaf Dennis Passage aan dat de pilot daar niet voor bedoeld was.

## Verbeter de Kaart, Hein Baan

Presentatie en demonstratie van _Verbeter de Kaart_, de terugmelddienst van Kadaster. Ook hier 
was vóór het project een groot invulformulier de interface vergelijkbaar met het Digimelding 
formulier. Achter _Verbeter de Kaart_ zitten een API (de terugmelding API) die terugmeldingen 
vanuit de gebruikersinterface ontvangt. Er is nog een bronhouder API die het beheerscherm (de terugmeldbeheerapplicatie) ondersteunt. 
De terugmelding API ondersteunt het indienen en opvragen van een terugmelding. De bronhouder API geeft 
toegang tot niet-openbare informatie om bronhouders meldingen te laten verwerken. De bronhouder API 
maakt gebruik van OAuth voor authorisatie en sluit aan op DMKS.

Gebruikers voegen een melding toe via de kaart (zoals bij de Waterketenpilot van GKG). Bronhouders 
krijgen een overzicht van de meldingen voor hun basisregistratie. Omdat de BAG en BRT vele bronhouders kent 
kunnen meldingen doorgezet worden naar andere bronhouders. 

_Verbeter de Kaart_ bleek tot veel meer meldingen te leiden. Onzinnige meldingen zijn klein in aantal 
en daardoor geen probleem. 

## Vervolg en proces, Edwin Wisse

Toelichting op het beheerproces. Toelichten van indienen en behandelen van wijzigingsvoorstellen. 

Open vragen die bedoeld waren voor de discussie worden via mail gedeeld.

Er wordt een [repository aangemaakt om kennis te delen over een Terugmeld API](https://github.com/Logius-standaarden/Terugmelden-API).
