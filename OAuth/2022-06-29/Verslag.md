# Verslag - Technische Architectuur Groep OAuth-NL

datum: 29-06-2022
status: concept

## Aanwezigen
| Voornaam  | Achternaam    | Organisatie |
| :-------- | :------------ | ----------: |
| Alexander | Green         |      Logius |
| Martin    | Van der Plas  |      Logius |
| Frank     | Terpstra      |    Geonovum |
| Bob       | te Riele      |        RVIG |
| Hans      | Oostrom       |    Waternet |
| Alexander | van der Woude |         KvK |
| Eelco     | Hotting       |         VNG |
| Peter     | Haasnoot      |      Logius |
| Remco     | Schaar        |      Logius |
| Frank     | van Es        |      Logius |
| Jan Jaap  | Zoutendijk    |      Ilionx |
| Erwin     | Reinhoud      |   Kennisnet |
| Jeroen    | Mol           |         RWS |
| Martin    | Borgman       |    Kadaster |
|  |  |  |


## Afwezig / Afgemeld
| Voornaam  | Achternaam    | Organisatie           |
| :-------- | :------------ | --------------------: |
| Lana      | Vredenduin    |              Enable U |
| Redouan   | Ahaloui       | Forum Standaardisatie |
| Arnoud    | Quanjer       |                   VNG |
| Marcel    | Adema         |     Wetterskipfryslan |
| Heiko     | Hudig         |               Politie |
| Pascal    | de Haan       |               Politie |
| Tony      | Sloos         |                       |
| Frits     |  Bouma        |                   DUO |
| Reinier   | Filé          |             Min. IenW |
| Joost     | Farla         |              Kadaster |
| Hans      | Hendrikman    |                  RVIG |
| Jaron     | Azaria        |                 Arpha |
| John      | Zwart         |                  RVDK |
| Patrick   | Reijnen       |                   KvK |
|  |  |  |



## De vastgestelde agenda van het overleg :
1. Welkom en korte voorstelronde.
2. Mededelingen.
3. Vaststellen notulen vorig overleg.
4. Doornemen RFC's / merge requests.
5. Demo avn de verbeterde opmaak voor versie 1.1.
6. Discussie mogelijke verbetering toepassingsgebied op de pas-toe-leg-uit lijst.
7. Inventarisatie gebruik in de praktijk zowel huidig als toekomstig Anders dan de DSO, TVS, DigiD Machtigen en de keten tussen politie, NFI en OM.
8. Voorgestelde Acties. 
9. Rondvraag en afsluiting.


## Verslag

### Agendapunt 1: Aftrap en kennismaking

De agenda wordt vastgesteld en iedereen stelt zich voor. 

### Agendapunt 2: Mededelingen

De volgende mededelingen worden gedaan:

1. Er is een publicatie toegevoegd op de pleio omgeving, zie ook https://digistandaarden.pleio.nl/blog het betreft een samenvatting van de OAuth-NL standaard; 
2. Er zijn  verwijzingen opgenomen naar de OAuth-NL standaard in de Security extensie (API-52) https://github.com/Geonovum/KP-APIs/blob/master/API-strategie-extensies/ext-security.md#authorization deze extentie is inmiddels ook "Stable";
3. Er zijn bij het Forum Standaardidatie vragen binnen gekomen over het toepassingsgebied. zie ook agendapunt 5;
4. Er wordt door Edwin Wisse een update gegeven over de status van het  MIDO en programmeringstafels. Zie ook de [gepubliceerde presentatie](https://github.com/Logius-standaarden/OAuth-NL_Vergaderstukken/blob/main/20220629/bijlagen%20slides.pptx);
5. Opzet SemVer als toevoeging voor de governance. Zie ook de [gepubliceerde presentatie](https://github.com/Logius-standaarden/OAuth-NL_Vergaderstukken/blob/main/20220629/bijlagen%20slides.pptx).

### Agendapunt 3:  Vaststellen Notulen overleg van 22-12-2021
De [notulen van het vorige overleg](https://github.com/Logius-standaarden/OAuth-NL_Vergaderstukken/blob/main/20211222/Verslag.md) zijn door de deelnemers vastgesteld.

### Agendapunt 4:  RFC's / merge requests
Zie ook [het overzicht van de huidige issues](https://github.com/Logius-standaarden/OAuth-NL-profiel/issues):
   - Issue [#7](https://github.com/Logius-standaarden/OAuth-NL-profiel/issues/7) heeft geleid tot [MR 21](https://github.com/Logius-standaarden/OAuth-NL-profiel/pull/21);
   - Issue [#8](https://github.com/Logius-standaarden/OAuth-NL-profiel/issues/8) heeft geleid tot [MR 20](https://github.com/Logius-standaarden/OAuth-NL-profiel/pull/20) en deze is inmiddels verwerkt in de development branch;
   - Issue [#11](https://github.com/Logius-standaarden/OAuth-NL-profiel/issues/11) wordt niet gesloten na toelichting maar er is een voorstel om dit te verduidelijken met een aanvulling in NL-Gov additionele content.

### Agendapunt 5: Verbeterde opmaak voor versie 1.1
Tijdens het overleg wordt de laatste versie van het profiel getoond, zie ook https://logius-standaarden.github.io/OAuth-NL-profiel/ de belangrijkste wijzigingen worden uitgelicht en de deelnemers reageren positief.

### Agendapunt 6: Discussie mogelijke verbetering toepassingsgebied op de pas-toe-leg-uit lijst:
   - toelichting voor inkopers;
   - voorkeur voor deze standaard boven SAML bij nieuwe ontwikkelingen.

### Agendapunt 7: Inventarisatie gebruik in de praktijk zowel huidig als toekomstig 
Anders dan de DSO, TVS, DigiD Machtigen en de keten tussen politie, NFI en OM wordt de standaard ook meegenomen in de ontwikkelingen bij:

- haal centraal (BRP-API) met toepassing van Netiq.
- Tennet, toepassing van een nieuw platform op basis van Keycloak en Kong.
- RWS als onderdeel van de toepassing van iShare

### Agendapunt 8: Voorgestelde Actie: 
   - opstellen 1 overall RFC voor een nieuwe versie 1.1 van de standaard om deze na review door de groep aan te bieden an het Forum standaardisatie. 
     - [Issue #11](https://github.com/Logius-standaarden/OAuth-NL-profiel/issues/11) wordt nog meegenomen in release 1.1
     - [Issue #13](https://github.com/Logius-standaarden/OAuth-NL-profiel/issues/13) wordt nog meegenomen in release 1.1


### Agendapunt 9: Rondvraag en afsluiting.
- Er wordt nog opgemerkt dat SSO Rijk ook mogelijk wordt ingezet bij Gemeenten
- Er wordt opgemerkt dat het gebruikelijk is om SAML te gebruiken voor de identificatie en dan daarna OAuth voor de Authorizatie van de geïdentificeerd entificeerde gebruiker bij de API. Zo is dit ook bij DSO geimplementeerd.
- Er is een toolset voor het testen van OIDC en ook een Fapi toolset voor compliancy
- Er is binnenkort een hackathon voor de OIDC standaard  
