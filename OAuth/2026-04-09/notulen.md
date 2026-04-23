# Technisch Overleg OAuth

9 april 2026

## Aanwezigen

- Alexander Green
- Andre van den Nouweland
- Erwin Reinhoud
- Frank Terpstra
- Martin Borgman
- Martin van der Plas
- Nil Barua
- Stas Mironov
- Tristan Smits

## Mededelingen

Nil geïntroduceerd als nieuw teamlid voor het OAuth-profiel. Vanaf het volgende Technisch Overleg neemt hij de trekkersrol voor van Stas.

Versie 1.1 met ongewijzigd toepassingsgebied richting Forum Standaardisatie. De betrokken experts zijn ermee akkoord gegaan.
Logius wil een onderzoek starten naar het daadwerkelijke gebruik van de standaard, omdat er nu te weinig concrete use-cases/referentie-implementaties zijn om de doorontwikkeling goed te sturen.
Frank stelt voor dat de mensen van developer.overheid.nl wellicht kunnen helpen het geautomatiseerd in kaart te brengen zoals met het API-register.
Ook is voorgesteld metadata in nieuwe YAML-bestanden mee te nemen om gebruik van standaarden beter zichtbaar te maken.

OAuth-claims binnen FSC worden beproefd en verdere uitwerking zal vooral in FSC-werkgroepen plaatsvinden.

## Evaluatie toevoeging Nederlands profiel ([#131](https://github.com/Logius-standaarden/OAuth-NL-profiel/issues/131))

Discussie of het Nederlandse profiel nog voldoende eigen meerwaarde heeft naast iGov, of dat toegewerkt moet worden naar een veel slanker profiel of addendum met alleen de echt Nederlandse aanvullingen.

In het issue staan de toevoegingen van het Nederlandse profiel ten opzichte van het iGov-profiel destijds.
Voor zover de tijd het toeliet werden de punten langsgelopen.
Van meerdere is geconcludeerd dat deze inmiddels in iGov zijn opgenomen.
Daarentegen zijn PKIoverheid en NCSC-richtlijnen genoemd als mogelijke rechtvaardiging voor een Nederlandse aanvulling.

## iGov update ([#130](https://github.com/Logius-standaarden/OAuth-NL-profiel/issues/130))

Stas meldt dat iGov actief wordt doorontwikkeld en dat Nederlandse input wordt meegenomen.
Besproken of het logischer is om meer bij iGov aan te sluiten en het Nederlandse profiel van een fork tot een daadwerkelijk profiel op een profiel af te slanken.
Gemeld werd dat het iGov-profiel wellicht her en der "haakjes" behoeft om lokale invulling te kunnen geven.

In het issue staan de punten uit de update. Verschillende werden inhoudelijk besproken.

Borgman: Achterhaalde cypher suites moet je niet willen ondersteunen, tenzij het niet anders kan (ondersteuning populaire verouderde devices).

MvP: DPoP met TLS is even veilig als mTLS.

Tristan: Mee eens. Hooguit zouden de tokens onderschept kunnen worden.

## Verzoek tot usecases

Dit onderwerp werd reeds bij de mededelingen besproken.
Nil meldt nog wel dat Identity and Access Management breder wordt opgepakt binnen Logius wat kansen biedt dit profiel te bespreken als alternatief voor SAML.
Daarnaast werd het ICTU-project ["Generieke Bronontsluiting"](https://github.com/ICTU/GBO) kort toegelicht waarbij dit profiel mogelijk ook toegepast zou worden.

## Beslisboom OAuth vs Digikoppeling ([#126](https://github.com/Logius-standaarden/OAuth-NL-profiel/issues/126))

Kort aangestipt. Toepassingsgebied blijft met versie 1.1 gelijk en de beslisboom kan waarschijnlijk elders, bijvoorbeeld Werkgroep Beveiliging, verder worden opgepakt.

## Actiepunten

- Logius werkt een onderzoek uit naar gebruik en adoptie van het profiel.
- Logius maakt voorzet tot slankere profielvorm, bijvoorbeeld als addendum op iGov in plaats van een fork.
- :pushpin: **Huiswerk voor leden:** Volgend TO beslissing kunnen nemen over de vorm van het profiel: addendum op iGov of fork behouden?
- Relevante uitbreidingen in het Nederlandse profiel worden ingebracht in de iGov-werkgroep.
- In agenda volgend TO duidelijker aangeven om welke besluiten er wordt gevraagd.
