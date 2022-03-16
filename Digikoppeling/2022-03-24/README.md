# Technisch overleg

# Agenda

|  |   |
|------------------------|-------------------------------------|
| Betreft  | **Technisch Overleg Digikoppeling** |
| Vergaderdatum en -tijd | 24-03-2022 - 13:30 uur  |
| Vergaderplaats  | Webex  |
<br>
  

## Onderwerpen


| Tijd | Onderwerp | Opmerking |
| --- | --- | --- |
| 13:30-13:35 | Welkom & Mededelingen |     |
| 13:35-13:40 | Verslag vorig TO 23-9-2021:<br><br> [Verslag TO Digikoppeling 02-12-2021]|     |
| 13:40-14:05 | Roadmap: zie [Roadmap 2022/2023](https://github.com/Logius-standaarden/Digikoppeling-Technisch-Overleg/blob/main/2021/2021_12_02/Concept%20Roadmap%20Digkoppeling_2022-2023.md)<BR><br> \> Toevoegen RESTful API profiel aan Digikoppeling<br> \> Signing & Encryptie toevoegen aan RESTful API profiel<br> \> Aanvulling Digikoppeling governance<br> \> Verbeteren Informatievoorziening / Nieuwe wijze van Publiceren<br> \> Best Practice Identificatie van Organisaties, Organisatieonderdelen en voorzieningen<br> \> Analyse knelpunten Routering en Intermediairs in gegevensverkeer<br> \> Verkennen mogelijk gebruik ebMS3/AS4<br> \> Interoperabiliteit platformen WUS bij gebruik MTOM in combinatie met WS-Security (signing)<br> \> Doorontwikkeling RESPEC/Digikoppeling template voor publicatie van specificaties<br> \> Update Beheermodel / aansluiting op Logius Standaarden BOMOS generiek beheer model & governance <br> > Lange termijn visie : Hoe om te gaan met uitfasering/vervanging van profielen<br> > Periodiek actualiseren architectuur|     |
| 14:05-14:25 | - |     |
| 14:25-14:45 | Toepassing van ebMS3/AS4 (eDelivery profiel) ter vervanging van ebMS2. <br><br>Vraag is of en wanneer de oudere versie te vervangen is door de nieuwe  <br>_Wat dienen Logius en het TO te ondernemen (en wanneer) om naar een antwoord toe te kunnen werken._<br><br>\- [EMBS3 AS4 Presentatie TO September](https://github.com/Logius-standaarden/Digikoppeling-Technisch-Overleg/blob/main/2021/2021_12_02/TO%20DigiKoppeling%20eDelivery%20AS4.pdf)  <br>\- [Digikoppeling-ebMS3-Eindrapport-v1.0.1.pdf (Onderzoek 2018)](https://github.com/Logius-standaarden/Digikoppeling-Technisch-Overleg/blob/main/2021/2021_12_02/bijlage%204.2%20Digikoppeling-ebMS3-Eindrapport-v1.0.1.pdf) |     |
| 14:45-15:00 | Rondvraag & Afsluiting. |     |

# Wijzigingen

## Grote wijzigingen
* Digikoppeling-Beheermodel [issue #3] [Aanpassing beheermodel op MIDO governance](https://github.com/Logius-standaarden/Digikoppeling-Beheermodel/issues/3) (16 Mar. 2022), _Status: In bewerking_
* Digikoppeling-Koppelvlakstandaard-ebMS2 [issue #6] [Digikoppeling baseren op ebMS3](https://github.com/Logius-standaarden/Digikoppeling-Koppelvlakstandaard-ebMS2/issues/6) (03 Feb. 2022), _Status: In onderzoek_
* Digikoppeling-Algemeen [issue #1] [Toevoegen Rest API profiel](https://github.com/Logius-standaarden/Digikoppeling-Algemeen/issues/1) (01 Feb. 2022), _Status: Klaar voor release_

## Kleine wijzigingen
* Digikoppeling-Identificatie-en-Authenticatie [issue #4] [Correctie samenvatting](https://github.com/Logius-standaarden/Digikoppeling-Identificatie-en-Authenticatie/issues/4) (21 Feb. 2022)
* Digikoppeling-Algemeen [issue #2] [Aanpassen Bijlage OIN Tabel](https://github.com/Logius-standaarden/Digikoppeling-Algemeen/issues/2) (26 Jan. 2022), _Status: Klaar voor release_

# Toelichting



## Toelichting: hoe beheren we issues en wijzigingsvoorstellen

In het kader van de nieuwe governance willen we het proces van wijzigingsvoorstellen standaardiseren. We accepteren wijzigingsverzoeken als git issues. We labellen issues om scope, status en te agenderen overleg aan te geven. Onderstaande lijst zijn issues gelabelled voor het Technisch Overleg. Issues worden gegroepeerd naar scope. De lijst is automatisch gemaakt aan de hand van de labels.

We vragen het Technische Overleg advies of goedkeuring op de wijzigingsvoorstellen afhankelijk van de status.

## Toelichting komende release

Als toevoegen van de REST API koppelvlakspecificatie formeel is goedgekeurd door het OBDO kunnen we een release uitbrengen. Behandeling door het OBDO is geagendeerd voor 7 april 2022. Zie ook [Update Digikoppeling REST API Koppelvlak](https://digistandaarden.pleio.nl/groups/view/41aa788c-cd67-4b27-9154-373e9a83dd40/digikoppeling-community/discussion/view/6c1734c0-4f2c-499a-9b92-145f6392e2c9/update-uitbreiding-van-de-digikoppeling-standaard-met-het-rest-api-koppelvlak)

Opgenomen in de release worden:

* [Digikoppeling Architectuur 2.0](https://publicatie.centrumvoorstandaarden.nl/dk/architectuur/2.0vv/)
* [Digikoppeling - Koppelvlakspecificatie REST API 1.0](https://publicatie.centrumvoorstandaarden.nl/dk/restapi/)


De uitbreiding van Digikoppeling met het REST API koppelvlak is doorgevoerd in de Digikoppeling documentatie.
Naast het toevoegen van de REST API koppelvlakspecificatie en het aanpassen van het architectuurdocument nav deze toevoeging zijn ook waar nodig de overige documenten tekstueel aangepast voor de toevoeging van deze nieuwe koppelvlakspecificatie.
Zie hiervoor : 
* [Overzicht Wijzigingsvoorstellen en aanpassingen](https://github.com/Logius-standaarden/Overleg/blob/main/Digikoppeling/rfc.md).
* [Overzicht documenten komende release](https://logius-standaarden.github.io/Publicatie-Preview/Digikoppeling-Overzicht-Actuele-Documentatie-en-Compliance/Toevoegen_Rest_Api/#wat-zijn-de-huidige-versies-van-documenten).


### Verzoek aan het TO:
__Het TO wordt gevraagd om goedkeuring te verlenen aan het opnemen van deze wijzigingen in de komende release van Digikoppeling__

## StvZ lopende roadmap items


### Definitieve Roadmap

De concept roadmap is in het vorige overleg besproken en goedgekeurd.
Zie [Roadmap Digikoppeling](https://github.com/Logius-standaarden/Digikoppeling-Algemeen/blob/main/Digikoppeling_Roadmap_2022_2023.md)

#### Verzoek aan het TO:
__Het TO wordt gevraagd om de roadmap vast te stellen__

### Digikoppeling governance

Zie voorstel in [grote wijzigingen](#Grote-wijzigingen). [Schema beheerproces](Beheerproces.svg)

### Informatievoorziening

We streven naar een vereenvoudiging van onze informatievoorziening. 
* we willen https://publicatie.centrumvoorstandaarden.nl/ uitfaseren en overgaan naar https://gitdocumentatie.logius.nl/
* publicatie van agenda's via github

[Overzicht publicatiesites](Publicatie.png)

### Signing & Encryptie toevoegen aan RESTful API profiel

Onderzoek loopt in samenwerking met KP API werkgroep beveiliging

### Identificatie en Routering

Handreiking voor ondersteuning voor dit onderwerp is in ontwikkeling

### Interoperabiliteit platformen WUS bij gebruik MTOM in combinatie met WS-Security (signing)

Voorbeeld berichten van datapower zijn onderzocht. Aanpassingen op de WUS standaard om de interoperabiliteit te vergroten zouden grote impact hebben op bestaande implementaties die gebruik maken van andere platformen;

### StvZ Respec

Het [ReSpec-profiel](https://github.com/Logius-standaarden/respec) is stabiel en in gebruik in alle Digikoppeling-documenten. De wens is het profiel meer modulair op te zetten om onderhoud te vergemakkelijken en gebruik buiten Logius te faciliteren.

### Verkennen mogelijk gebruik ebMS3/AS4

Zie voorstel in [grote wijzigingen](#Grote-wijzigingen).

