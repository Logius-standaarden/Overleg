# Verslag Technisch Overleg Notificeren/Cloudevents

Vergaderdatum en tijd	7 december 2023 09:30-11:00 uur						
 
Vergaderplaats	Remote, Cisco Webex

Aanwezig:
(17 personen) Edwin Wisse (Logius)(vz), Rijk van Haaften (Kadaster), Martin van der Plas (Logius Standaarden), Peter Haasnoot (Logius Standaarden), Bas Kooij (Logius Productiehuis), Frank Zwart (Logius Productiehuis), Joeri Bekker (Maykin media), Karl de Boer (Enable U), Hamid Farhadi Maharluei (demo BRO TNO), René Cham (Logius portfolio-ontwikkeling), Perry Meezen (Logius Productiehuis), Sjaak Derksen (TNO), Ad Gerrits (VNG), Dennis Nass (Kadaster), Frits Maas (KvK), Lizzy Wellink (secretaris)(Logius).
Gast: Hamid Farhadi Maharluei (demo BRO TNO)

Afwezig (met berichtgeving):
Marian van Ansem (min BZK), Pauline van Zadelhoff (KvK), Alexander Grren (gedeeltelijk)

#	Opening & mededelingen (vz)

- Hartelijk welkom namens de voorzitter Edwin Wisse – Logius Standaarden, op het 2e Technisch Overleg Cloudevents.
  Een tweetal presentaties zullen het grootste deel van dit overleg vullen en daarnaast mededelingen en de architect
  praatplaat van Bas Kooij (Logius Productiehuis).
- Doel: Technisch Overleg is de plek waar wijzigingsvoorstellen kunnen worden voorgedragen en op Gitbhub de inleg
  ervan kan worden gedaan. Mocht er aanleiding toe zijn dan kan het ook langs de programmeringstafels of het MIDO
  (Meerjarige Infrastructuur Digitale Overheid)(Strategie).
- Aansluitend is het Technisch overleg ‘Terugmelden’, waarbij een voorstel wordt gedaan om deze niet meer te
  organiseren en DMKS dus niet verder te ontwikkelen. Voor terugmelden verwijzen we naar OAuth en Digikoppeling.

# Issues en wijzigingsvoorstellen (Github) (vz)

Doorgenomen punten:
- Ad Gerrits, VNG: Ingebracht punt per mail eind augustus, over het proces achter de toekomst van de standaard.
  We hebben een governance structuur waarbij we wijzigingsvoorstellen (overeenkomstig BOMOS) agenderen op
  operationeel (TO), tactisch (programmeringstafel GU) en strategisch (programmeringsraad GDI) niveau.
  De ambitie is om standaarden regelmatig op de agenda te krijgen bij de verschillende overleggen. De grote
  wijzigingen komen dan ter besluitvorming op strategisch niveau. Kleine wijzigingen worden op operationeel/tactisch
  niveau (het Technisch Overleg) goedgekeurd en worden ter kennisgeving geagendeerd op strategisch niveau.
  Het OBDO dient altijd geïnformeerd te worden over wijzigingen dus daar komt het ook ter kennisgeving langs.
  Je kunt wijzigingsvoorstellen indienen als issue bij de relevante repository. Voor CloudEvents is dat
[https://github.com/Logius-standaarden/NL-GOV-profile-for-CloudEvents](https://github.com/Logius-standaarden/NL-GOV-profile-for-CloudEvents).
  Een issue komt dan op de agenda (aan de hand van een label wat Logius aan het issue toekent) van het TO en
  als het een grote wijziging is op de “hogere”  overleggen.
- Ad Gerrits, VNG: PTOLU-lijst (Pas toe of leg uit) van het Forum voor Standaardisatie, en de kans voor het NL GOV profile
  om op die lijst te komen gaat het erom dat er ook aantoonbare toepassing van de standaard is. Vandaag dus actueel
  dat het Kadaster en BRO nu een presentatie geven over de toepassing. Verder is het bij Logius opgenomen in de
  (toekomstige) architectuur voor notificeren en terugmelden. De mogelijkheid om het CloudEvents profiel naar
  het Forum te brengen komt daarmee dichterbij. Eerst de verkenning om daarna een publieke consultatie te starten
  onder gebruikers van Cloudevents. Met daarbij de opmerking dat Cloudevents niet de enige standaard is die geldt
  voor notificeren.
  
Kleine wijzigingen
- CloudEvents-NL-Guidelines [issue #4] [https://github.com/Logius-standaarden/CloudEvents-NL-Guidelines/blob/develop/NL-GOV-Guideline-for-CloudEvents-Webhook.mdRFC ...](https://github.com/Logius-standaarden/CloudEvents-NL-Guidelines/issues/4) (13 oktober 2023), _Status: In onderzoek_

  Sjaak Derksen (TNO, PO Basisregistratie) De eerste oplossing is om dit aan te passen, bij-lage wordt meegeleverd en gedocumenteerd.
  De presentatie straks zal daar dieper op in-gaan. Oauth kan worden toegevoegd of een PKI achtig mechanisme.

  **Actiepunt**: Martin vd Plas, Sjaak Derksen, Ad Gerrits willen wel meedenken.
  Binnen het NL Gov profiel moet je ook weer aandacht hebben voor de manier van opnemen.

- NL-GOV-profile-for-CloudEvents [issue #6] [#appendix-1-use-of-json-http-and-webhook ](https://github.com/Logius-standaarden/NL-GOV-profile-for-CloudEvents/issues/6) (4 januari 2023), _Status: Gereed_

  Ad Gerrits heeft nog een opmerking van algemene aard op de toelichting op de Logius website daar waar het gaat om het vernoemen van partijen.
  Dient zo neutraal mogelijk te zijn opgenomen en dus beperken wat de standaard betreft en niet teveel partij kiezen. 

  **Actiepunt**: Edwin neemt dit op met communicatie.

-	NL-GOV-profile-for-CloudEvents [issue #3] [Als gebruiker van de standaard wil ik een neutrale beschrijving zodat ik zelf kan bepalen met welk doel ik de standaard toepas ](https://github.com/Logius-standaarden/NL-GOV-profile-for-CloudEvents/issues/3) (17 oktober 2022), _Status: In onderzoek_

  Er was nog een vraag van min JenV (Jeffrey Gortmaker, migratieketen) binnengekomen over toepassing vnan CLoudEvents. 
  Kort antwoord (Edwin): standaard kan in architectuur opgenomen worden voor event-driven werken.

  Als laatste meldt Edwin dat de projectinformatie van de VNG overgedragen aan Logius op Github gepubliceerd staat en dus vindbaar.

# Presentatie Kadaster over hun gebruik van de notificatiestandaard CloudEvents (Dennis Nass)(BRK)

Specifieke verandering in de BRK bijvoorbeeld over rechtszekerheid, is heden ten dage actief zoeken, maar middels dit project notificatie wordt dat actief op de hoogte stellen van specifieke aanpassingen in de basisregistratie kadaster. Een directe push near-real-time van een notificatie in de BRK. De notificatie wordt via email of API gedaan, info. arm, en de aanvullende informatie kan worden opgevraagd middels andere kanalen zoals Kadaster-online of HaalCentraal API. Voor meerdere objecten leveren we 1 notificatie.
Door het Kadaster gemaakte keuzes:
-	Push of Pull strategie – functioneel een push, technisch een pull
-	Pre-filtering of filtering achteraf – moment van filtering, doelbinding dus pre-filtering
-	Digilevering (XML) wel vervangen door Cloudevents, tijdelijke oplossing is nu email maar geeft geen aflevergarantie.
-	BRK notificatie API & NL GOV profile ‘Notificeren binnen de overheid’. Dataobjects kan veel meer behelzen, specificatie is publiekelijk te benaderen. Afwachten waar digilevering naartoe gaat.
Mooie duidelijke presentatie wat een hoop inzicht gaf.
 
# Architectuur praatplaat (Bas Kooij)

Praatplaat notificeren, schematisch overzicht wordt getoond door Bas, en dient van rechts naar links gelezen te worden. 
-	Brondata van de registratie via ebMS.
-	Event-driven notificeren via rest API
Discussie loopt met federatief datastelsel. Eigenlijk is ebMS te complex, en het koppelen op een rest API zal
makkelijker zijn. Ad Gerrits voegt eraan toe Websub niet geschikt is voor dit doel, wel voor feeds.
Cloudevents community heeft een werkgroep die hierover in beraad is. Belangrijk om deze ontwikkeling te volgen.

# Notificaties in de BRO (standaard CloudEvents) (Sjaak Derksen)

Hoe gaan we om met digilevering bij BRO (Basisregistratie Ondergrond)? Namelijk de afscherming van gegevens 
bemoeilijken de data, en ebMS is te massief voor implementatie, expertise moeilijk te vinden, etc dus voldoende 
reden om op zoek te gaan.

Minimale informatie overdragen en de aanvullende info (gebruikers d.m.v. ID’s) ophalen, waarmee het 
notificatiekanaal niet wordt belast met inhoud. Met maximaal gebruik bestaande technologie.

Verschillende berichten: transactie, terugmelding, in onderzoek. Laatste 2 berichten voor in de toekomst.

Transactieregister, iedere 5 minuten worden de transacties gescand aan de BRO gekoppelde info. Autorisatie tussen abonnee en broker, ophalen van autorisatie details, ophalen van  autorisatiecode, periodiek scannen leidt tot hernieuwen access- en refreshtokens en eventuele accesstoken. 
Toekomst: integratie met Logius Digilevering, Robuust maken van de oplossing, Koppeling met ‘standaard’ IAM providers, developer overheid.
In de projectdocumentatie ‘21/’22 notificatieservices van VNG is alles te vinden.

Collega Hamid Farhadi Maharluei verzorgt de demo (provisioning en traffic) aan het einde van de presentatie.

Gemeenschappelijke zorg is de transportonafhankelijkheid. Mooi om aan de hand van een demo meer inzichten te verkrijgen.

# Rondvraag

geen

Sluiting vergadering om 11:15 uur (kleine uitloop)

Dit TO gaat door als TO CloudEvents (en niet meer als TO Notificeren). 
Volgende TO 7 maart 2024 a.s. van 09:30-11:00 uur. 

