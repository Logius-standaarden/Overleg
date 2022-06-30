# Verslag Technisch Overleg Digikoppeling 23-06-2022

## Aanwezigen

| Achternaam | Voornaam | Organisatie |
| --- | --- | --- |
| Bijen | Antoon | Justid |
| Coemans | Maarten | SNG |
| de Boer | Karl | enable-u |
| Fieten | Sander | Chasquis Consulting |
| Green | Alexander | Logius |
| Groot Roessink | Gerald | DUO |
| Haasnoot | Peter | Logius |
| Han | Welmer | TNO |
| IJzermans | Jochem | UWV |
| Kuiper | Erwin | Dictu |
| Pauw | Elzo | UWV |
| Reinhoud | Erwin | Kennisnet |
| Sinnige | Hans | Rinis |
| Terpstra | Frank | Geonovum |
| van der Velde | Johan | RDW |
| Vijlbrief | Tom | Kadaster |
| Wisse | Edwin | Logius |

## Besproken punten

### Transitie EBMS3

**Groot Roessink:**  Worden de ontwikkelingen bij Once Only Technical System gevolgd omtrent ebMS3/AS4?

**Karl de Boer:**  API geen vervanging voor ebMS; Mist ondersteuning voor o.a. retries en intermediairs. We zijn voor een overgang naar ebMS3, maar er zal een periode van parallel bestaan zijn.

**Wisse:**  Hoelang parallel?

**De Boer:**  Tussen 1 à 2 jaar.

**Bijen:**  5 of 10 jaar.

**Wisse:**  De vraag achter de vraag: &quot;Hoe gaan we om met koppelvlakuitfasering?&quot;

**Bijen:**  Twee aparte onderwerpen: overgang naar ebMS3 en uitfasering ebMS2.

**De Boer:**  Uitfaseren van WUS is nog niet aan de orde.

**Coemans:**  Er staat transitie naar ebMS3 of API. Waarom niet WUS?

**Wisse:**  De gedachte was dat er niet van ebMS2 naar WUS wordt overgestapt.

**Coemans:**  Wordt uitfasering gehandhaafd?

**De Boer:**  Wie besluit overgang ebMS2 naar ebMS3?

**Wisse:**  Vanuit OBDO. Operationeel advies van TO. Tactisch, strategisch bij Programmeringstafel, beslissing bij OBDO.

### Toevoegen API-58 No sensitive information in URIs

**Bijen:**  Best practice voor alternatief queries in URI?

**Coemans:**  POST een object

**De Boer:**  Haal centraal gaat iedere bevraging via JSON POSTS (soort GraphQL) uit security redenen (niet ADR gebaseerd).

_Voorstel geaccepteerd_

### We vragen het TO de volgende uitwerkingen te reviewen
- [Analyse knelpunten Routering en Intermediairs in gegevensverkeer](https://github.com/Logius-standaarden/Digikoppeling-Algemeen/issues/9)
- [Best Practice Identificatie van Organisaties, Organisatieonderdelen en voorzieningen](https://github.com/Logius-standaarden/Digikoppeling-Algemeen/issues/10)

**Kuiper:**  Is het wenselijk dat je een certificaat aan SAAS partij geeft?

**Haasnoot:**  Sleutelbosprobleem. Scope te groot voor taak. Oplossing is subOIN. Certificaat per afdeling voor fijnmazige scope.

**Kuiper:**  Machtigingen meest ideale oplossing.

**Reinhoud:**  Bij onderwijs. Verwerker heeft eigen PKIO certificaat d.m.v. machtigingsreigister.

**Haasnoot:**  NLX heeft ook machtigingconcept.

**Bijen:**  SubOIN staat wel in best practice, maar niet in analyse.

### MTOM

**Reinhoud:**  partijen met verschillende manieren dienen het zelf op te lossen?

**Welmer:**  Intermediair systeem introduceren als de standaard niet ondersteund wordt als technische oplossing.

_Akkoord standaard niet aan te passen._

### Patchdocumentatie

_Akkoord_

## Roadmap Items

### Signing/encryptie

**Coemans:**  Encryptie heeft alleen toegevoegde waarde als het bericht end-to-end voor de eindgebruiker versleuteld dient te worden. Wanneer voegt end-to-end niets toe boven tweezijdig TLS en is het overbodig? Het zou mooi zijn als in de documentatie hier aandacht aan wordt gegeven.

### ReSpec

**Roessink:**  Nationaal profiel metadata. Voorstel om profiel samen te voegen.

**Terpstra:**  Betrek Jan van Gelder bij samenwerkingsinitiatieven.

**Haasnoot:**  Ja we werken  intensief samen met Geonovum/Jan van Gelder bij doorontwikkeling van een generiek NL GOV profiel

## Rondvraag

Eerdere discussie over API-58 gaat verder. Coemans deelt ideeën via e-mail.

**Terpstra:**  Tevreden met discussie over signing. Verzoek aan mensen om gebruik te delen (wanneer wel, wanneer niet); Biedt waarde naast technisch aspect.

Coemans deelt link: [https://stackoverflow.com/questions/5020704/how-to-design-restful-search-filtering](https://stackoverflow.com/questions/5020704/how-to-design-restful-search-filtering)

**Haasnoot:**  beeld/geluid prima? (_iedereen tevreden_). Overgrote deel TO heeft voorkeur Webex. Wellicht één grote samenkomst fysiek, verder hybride.
