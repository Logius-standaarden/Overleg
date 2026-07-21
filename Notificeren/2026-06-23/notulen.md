# Technisch Overleg CloudEvents

23 juni 2026

## Deelnemers

### Aanwezig

(8 personen) Stas Mironov (Logius)(vz), Marc Buis (JustID), Menno van Grinsven (Belastingdienst), René Cham (portfolio Logius), Tim van der Lippe (Logius), Alexander Green (Logius), Peter Haasnoot (Logius), Lizzy Wellink (secretaris)(Logius).

### Afwezig (danwel met berichtgeving)

Joeri Bekker (Maykinmedia.nl), Jarich Ypma (PinkRoccade), Rijk van Haaften (Kadaster), Bas Kooij (Logius Productiehuis), Niels Willemse (Logius Productiehuis), Bob te Riele (RvIG), Tom Vijlbrief (Kadaster), Engelbert Wijnhoven (PinkRoccade), Dennis Nass (Kadaster), Mirian van Ansem (Min BZK, beleid), Ron van den Enden (PinkRoccade),

## Opening & mededelingen (Stas Mironov)

Hartelijk welkom namens de voorzitter, Stas Mironov – Logius Standaarden, bij het Technisch Overleg CloudEvents/Notificeren.

Voor de stukken en agenda wordt verwezen naar de Github omgeving: [Overleg/Notificeren/2026-06-23](https://github.com/Logius-standaarden/Overleg/tree/main/Notificeren/2026-06-23)

### Goedkeuring notulen

De vorige notulen d.d. 26-3-2026 zijn zonder verdere opmerkingen vastgesteld. De notulen dienen voor vastlegging van besluiten, wijzigingen, (werk- en/of proces)afspraken, etc. (verzoeken tot aanpassingen richten aan <api@logius.nl> of <Lizzy.Wellink@Logius.nl>.

### Mededelingen/ Interessante ontwikkelingen

- Woensdag 18 maart 2026, is de nieuwe versie van CloudEvents NLgov profiel, versie 1.1. minorversie, vastgesteld in de Programmeringstafel Gegevensuitwisseling (PT GU);
- Volgend uit het jaarlijks verzoek vanuit het Forum Standaardisatie, t.b.v. [Monitor Open Standaarden](https://www.forumstandaardisatie.nl/metingen/monitor), is input gegeven over de standaard. Daarnaast ook melding van de ontwikkelingen komend kwartaal, halfjaar, etc.;
- Marc Buis (JustID) voegt in dit kader toe dat er een webshop wordt beproefd met ketenpartners in een POC met het notificatieconcept. Gaat om samenwerking met JenV migratieketen en IDN keten, gebruikmakend van CloudEvents subscriptionAPI, staat op de POCAgenda om deze koers uit te zetten;

:pushpin: **actiepunt** Marc Buis: terug laten komen op agenda TO eind v/h jaar en ervaringen delen/voortgang

- Reserveringsaanvraag ingebracht door Architecten GU-domein vanuit Logius (o.a. met Dennis Passage), bij het innovatiebudget richting het MIDO, voor een beproeving, CloudEvents, AyncAPI, FSC, i.h.k.v. toekomstige werking van Digilevering. Dit als een broker (zoals bij FDS genoemd) als beproeving in Q1 2027 in de Monitor opgenomen. Kunnen één of meerdere ketens opteren als een broker.

## Update werkgroep Notificeren (Stas Mironov)

- Er zijn twee werkgroepen na de opsplitsing, Architectuur Notificeren en Async API o.l.v. Frank Terpstra Geonovum (<https://www.formdesk.com/geonovum/notificeren>). En de werkgroep o.l.v. Danny Greefhorst (FDS), meer praktisch, o.a. handreiking. Begin deze maand is de werkgroep officieel afgesloten door Danny Greefhorst, en zijn de aanbevelingen, toevoegingen, nuanceringen, architectuurdocumententen opgeleverd. Deze zijn te vinden op landingspage (<https://www.noraonline.nl/wiki/Architectuur_Notificeren_in_het_Federatief_Datastelsel>), en in het totaal opgenomen. Alles is nu op één plek te vinden.
- abonneringsstandaarden, blijft een gat waar we in de toekomst nog naar kunnen kijken.

Afwachten visievorming bij BZK.

## Twee issues onder Kleine wijzigingen

### Required value for specversion refers to previous version [#52](https://github.com/Logius-standaarden/NL-GOV-profile-for-CloudEvents/issues/52)

Ingebracht door Jorg Mutter (JenV OM), per mail over required value for spec version, en gaf intern (met collega Alexander Green) ook discussie. Dit geeft aanleiding om het TO om advies te vragen. Leek handig om te ontkoppelen van CNCF en puur NL-Gov versionering in dit veld te stoppen

Het gaat hier om het veld `specversion`, en de redenering erachter zou moeten refereren naar het bovenliggend profiel, en dan kom je op een 1.0.2. (MUST, versie 1.0.) of moet het de versie zijn van het Nederlands profiel 1.1.?

Kunnen we met één versie af of moeten we het bovenliggende profiel ook noemen.

De spec is CloudEvents en een NLgov profiel 1.1. kunnen naast elkaar bestaan? Gaat dat goed met tools etc. of gebruik je de spec en het profiel door elkaar en leidt dat niet tot verwarring. Of kan je nog in een extra veld de versie toevoegen en het daarmee op te lossen? Wil je een extra veld?

:pushpin: **Actiepunt:** Verder onderzoeken en Logius zal een oplossing inbrengen volgend TO

### Sequence attribute required or optional? [#53](https://github.com/Logius-standaarden/NL-GOV-profile-for-CloudEvents/issues/53)

- Gaat om een interpretatie-verschil. Twee van de extensie attributen zijn inbegrepen als optional attributen in het NLgov profiel. Of wat is de interpretatie van ‘required’?
- Defining extensions – geen verplichte attributen
- Sequence + sequence type 3.5.1.1 – wel verplicht. Bijvoorbeeld opgelost door ‘Required when sequence extension used’ toevoeging.

Vanuit TO-leden: Je zou altijd een toelichting in een tekstblok kunnen meegeven hoe je een extensie moet interpreteren. Toelichting daarop dat er een core is en extensies zijn, daarmee refereer je altijd aan het origineel óf verplicht om de goedgekeurde versies door het Forum te noemen. Maar geeft onduidelijkheid dat wel.

We zetten de comments nog open tot eind van de maand. Na overleg laten we het doel zijn om twee keuzes te elimineren tot één. We pakken hem op als beheerkwestie door Logius en nemen de behandeling / structurering zelf ter hand.

:pushpin: **Actiepunt:** Logius zal een structurering/duidelijkheid/voorstel schrijven

## Presentatie (Marc Buis)

Marc Buis leidt ons door de situatie bij JustID middels een presentatie. Hij licht toe dat zij zouden in de Jeugdzorg en Veiligheidssector CloudEvents willen gebruiken en W3C Provenance nu is ingezet. Vandaag gaan we langs

Maar je kan aan Provenance bussiness kennis toevoegen. W3C Provenance voegt toe: digitale objecten, semantiek wordt toegepast en domeinafhankelijk:

- Attributed, derived, associated, generated, used, acted on behalf of

Geeft bepaalde causaliteit in je domein en kan je dus ‘tracen’ hoe beslissingen zijn genomen. Bewijs, activities toevoegen etc. ook als dit fysiek is.

Drie perspectieven op je landschap. Verantwoordelijkheidsperspectief (de aanzetter), procesperspectief (KGD, hoe is proces gelopen), entity laag (waar is het voor gebruikt, is het veranderd).

Moeilijk om zaken te achterhalen, gegevens zijn er vaak wel maar worden steeds moeilijker gevonden. Vaste dataset / de werkwijze die we hebben omarmd is nu grote bulk info door de keten duwen gezien de ~4000 organisatie bij JenV is dit niet wenselijk. Maar je wil verbeteren dat je met elkaar een gezamenlijke dataset deelt, dat je het beschikbaar maakt voor ketenpartners.

In API-land (de oude ebMS koppelingen worden API’s) dan wordt het op zichzelf staande brokken data terwijl je wil dat het aan elkaar linkt. Hierbij overzie je het historische aspect van gegevens (haal bij de bron), je zou dus betrouwbaarder moeten kunnen tijdreizen.

Als overheid zijn we verantwoordelijk om zaken uit te leggen, auditing en compliance zijn zo van die zaken, behoefte om in events iets te gaan betekenen.

Conclusie is: naar standaardisatie toe, verklaart de wens richting CloudEvents toe.

48:00 Hoe is het met het proces gegaan. Informatie ophalen. Blijft zoeken naar relaties tussen data, dat je data kan pinnen. Indexering van je landschap, en hoe rijker je dat doet met Provenance hoe beter doorzoekbaar die wordt. Dynamische catalogus van je landschap. Behoefte om persoonsgegevens beschermen met autorisatie e/o cryptografie.

:pushpin: **Actiepunt:** Marc Buis informeren over Logboek Data Verwerking (innovatieproject), rapport transparantieapp app van Geonovum delen, trace-index

Basis- activity, entity, agents, onderwerp van je CloudEvent, zoals de oplossing eruit zou moeten zien. Marc laat een voorbeeld zien, e-akkoord (handtekening), echtheid document, track and trace in het experiment Wietteelt. Gemeentes en wiettelers gaan aangesloten worden (alles afhankelijk van het beleid maar zoiets).

Schrijven van event (WRITE), leesdeel (READ) is zoals het wordt vertaald naar Provenance met een ‘business logica’-deel. Voor wietteelt en jeugdzorg geldt dit als zorg. Marc laat de demo-omgeving zien wat wel tot de verbeelding spreekt.

De voorzitter geeft aan zeker verder te willen praten en oppert om een afspraak te maken met Danny Greefhorst (trekker van de werkgroep Notificeren) en wil toevoegen. :pushpin: **Actiepunt** Logius/Stas

En als mededeling dat de kick-off werkgroep temporele historie (werkgroep bij het [Kennisplatform API’s](https://developer.overheid.nl/communities/kennisplatform-apis)) binnenkort is en je kunt aanmelden als je op het formulier ‘historie’ aanvinkt.

Mooiste case zou zijn via het het CBG (College ter Beoordeling van Geneesmiddelen) waarbij wetenschappelijk onderzoek ter goedkeuring van geneesmiddelen wordt gebruikt ook voor goedkeuring/afkeuring/tests i.h.k.v. vertrouwelijkheid van gegevens.

Om er een extensie van te maken wat zou het vervolg zijn, via CloudEvents formaliseren en als optioneel/aanbevolen en dat we hem in de standaard opnemen.

## Specificatie gewenst van URN formats (VNG – Joeri Bekker)

Wijzigingsvoorstel vanuit Joeri Bekker, dit issue loopt bij Common Ground. Dit punt wordt nu gezien de tijd niet behandeld. Volgend TO pakken we het weer op.

## Rondvraag (vz)

Nog een rondje op/aanmerkingen:

- Via Michiel Trimpe uitnodigen Mark de Boer van FTV nog uitnodigen?
- Specificatie gewenst van URN formats (VNG – Joeri Bekker)
- [Notulen van werkgroep Notificeren](https://github.com/Geonovum/KP-APIs/tree/master/overleggen/Werkgroep%20Notificeren/Notulen)

De voorzitter Stas Mironov dankt eenieder voor zijn bijdrages en deelname.

Sluiting vergadering om 11:15 uur.
