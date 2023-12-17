# Verslag Technisch Overleg Terugmelden

Vergaderdatum en tijd	7 december 2023 11:00-11:30 uur						
 
Vergaderplaats	Logius Oranje 0.034 + Remote, Cisco Webex

Aanwezig:
(9 personen) Edwin Wisse (Logius)(vz), Rijk van Haaften (Kadaster), Eric van Mullekom (Kadaster), Bob te Riele (VNG), Martin van der Plas (Logius Standaarden), Bas Kooij (Logius Productiehuis), Frank Zwart (Logius Productiehuis), René Cham (Logius portfolio-ontwikkeling), Lizzy Wellink (secretaris)(Logius).

Afwezig (met berichtgeving):
Marian van Ansem (min BZK), Peter Haasnoot (Logius), Alexander Green (Logius) 

1.	Opening & mededelingen (vz)

Hartelijk welkom namens de voorzitter Edwin Wisse – Logius Standaarden, en een excuus voor het verlaat aanvangen 
van deze vergadering door uitloop van de voorafgaande vergadering TO Cloudevents.

Er wordt gevraagd om instemming met het voorstel om het TO Terugmelden niet meer te organiseren en DMKS dus 
niet verder te ontwikkelen. Middels de architectuur-praatplaat Terugmelden van Bas Kooij 
(Logius Productiehuis) zullen we de discussie doorlopen. 

Voor Terugmelden verwijzen we verder naar TO’s Oauth en Digikoppeling.
- Het komende TO Digikoppeling is op 14 december a.s., van 11:00-12:00 uur
- Het komende TO OAuth wordt voor het eerst bijeengeroepen do 25 januari, van 15:00-16:30 uur.

2.	Achitectuur praatplaat (Github) (Bas Kooij)

Doorgenomen punten:

Architectuur Praatplaat terugmelden, schematisch overzicht wordt getoond door Bas en dient 
vanaf melder van rechts naar links gelezen te worden. 
Zo kunnen we de discussie vernieuwingsvoorstel met federatief datastelsel afstemmen, 
via Digimelding, uitbreiding wel/niet, gaat toch teveel via Digimelding.
Bas bespreekt flow, van boven naar beneden wordt het steeds meer gedetailleerd/ specialistisch. 
Ingevoerd in een voorziening, meekijken zoals bij de dienstverlener binnen. En daarna wordt de 
melding doorgevoerd. Status notificaties (afmelding, update)

Via API-call events aanmaken via API-events die weer terug worden gekoppeld.
Event driven – event broker – architectuur, DMKS kan worden vervangen door API’s en door Cloudevents
Oauth als vervanger van e-Herkenning gaat overigens niet op, als reactie op een vraag, 
door een verschillende koppeling voor aanvrager.

Stelling: instemming met concentreren op andere standaarden, 
DMKS (koppelvlak tussen systeem landelijke voorziening en de bronhouder applicatie) niet 
meer doorontwikkelen. Ook op te vatten als End of Support. 

**Beslissing**: Rondje gemaakt en unanieme instemming (v Haaften, Kooij, te Riele, van Mullekom, van der Plas, Zwart, Cham, Wisse).

**Actiepunt**: Het DMKS moet in een algemene melding hierover voorzien.
**Actiepunt**: Vraag bij Marian van Ansem, visie, wat moet Logius bieden? In de Logius centrale terugmeldvoorziening.

Vraag: Omdat we verder geen TO meer hebben maar het laten terugkomen in de TO OAuth en TO Cloudevents, wat doen we dan met open data? 
Kan worden afgevangen middels een lijst met afspraken.
(Martin Voorbeeld) 342 gemeenten via een SSO (Single Sign On) i.p.v. via een e-Herkenning.

**Actiepunt**: Op het Kennisplatform verwijzing maken om daar de ontwikkelingen te volgen. Overigens is het Kennisplatform v3 recentelijk gelanceerd, gisteren 6/12/23.

# Rondvraag

Geen opmerkingen of vragen.

Sluiting vergadering om 11:50 uur
