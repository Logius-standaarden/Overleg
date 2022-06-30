# Technisch overleg



# Agenda

|  |   |
|------------------------|-------------------------------------|
| Betreft  | **Technisch Overleg Digikoppeling** |
| Vergaderdatum en -tijd | 23-06-2022 - 10:00 uur  |
| Vergaderplaats  | Webex  |

## Onderwerpen


| Tijd | Onderwerp |
| --- | --- |
| 10:00-10:05 | Welkom & Mededelingen |     
| 10:05-10:10 | Verslag vorig TO:<br> [Verslag TO Digikoppeling 24-03-2022](https://github.com/Logius-standaarden/Overleg/blob/main/Digikoppeling/2022-03-24/20220324_Verslag_Technisch_Overleg%20Digikoppeling.md) |   
| 10:10-10:20 | Bespreken [grote wijzigingen](#Grote-wijzigingen), zie ook toelichtingen [governance](#MIDO-governance) en [ebMS3](#ebMS3-transitie) |
| 10:20-11:00| Bespreken [kleine wijzigingen](#Kleine-wijzigingen) en [overige punten](#Overige-punten) |
|  |  Graag specifiek aandacht hierbij voor: |   
|             | [Toevoegen API-58  No sensitive information in URIs](https://github.com/Logius-standaarden/Digikoppeling-Koppelvlakstandaard-REST-API/issues/15)<BR> _[We vragen het TO om de RFC goed te keuren]_  <br>  |
|             | _[We vragen het TO de volgende uitwerkingen te reviewen:]_ <br>- [Analyse knelpunten Routering en Intermediairs in gegevensverkeer](https://github.com/Logius-standaarden/Digikoppeling-Algemeen/issues/9) <br>- [Best Practice Identificatie van Organisaties, Organisatieonderdelen en voorzieningen](https://github.com/Logius-standaarden/Digikoppeling-Algemeen/issues/10) |
|             | [Interoperabiliteit platformen WUS bij gebruik MTOM in combinatie met WS-Security (signing)](https://github.com/Logius-standaarden/Digikoppeling-Algemeen/issues/6) <BR> Zie [Toelichting](#toelichting-interoperabiliteit-mtom) <BR>_[We vragen het TO om akkoord te gaan met het advies vanuit beheer om de standaard niet aan te passen]_  <br>  |
|  | [Voorstel uitbrengen van patch versies van documenten](https://github.com/Logius-standaarden/Digikoppeling-Algemeen/issues/11) <BR> _[We vragen het TO om het voorstel goed te keuren]_|   
| 11:00-11:20 | Roadmap : [Stand van zaken Roadmap onderdelen](#stvz-lopende-roadmap-items) |     
| 11:20-11:30 | Rondvraag & Afsluiting. |     

# Punten

## Grote wijzigingen
* Digikoppeling-Beheermodel [issue #3] [Aanpassing beheermodel op MIDO governance](https://github.com/Logius-standaarden/Digikoppeling-Beheermodel/issues/3) (16 Mar. 2022), _Status: In bewerking_
* Digikoppeling-Koppelvlakstandaard-ebMS2 [issue #6] [Digikoppeling baseren op ebMS3](https://github.com/Logius-standaarden/Digikoppeling-Koppelvlakstandaard-ebMS2/issues/6) (03 Feb. 2022), _Status: In onderzoek_

## Kleine wijzigingen
* Digikoppeling-Algemeen [issue #11] [Voorstel uitbrengen van patch versies van documenten](https://github.com/Logius-standaarden/Digikoppeling-Algemeen/issues/11) (16 Jun. 2022), _Status: In review_
* Digikoppeling-Koppelvlakstandaard-REST-API [issue #15] [Toevoegen API-58 No sensitive information in URIs ](https://github.com/Logius-standaarden/Digikoppeling-Koppelvlakstandaard-REST-API/issues/15) (16 Jun. 2022), _Status: In review_
* Digikoppeling-Algemeen [issue #10] [Best Practice Identificatie van Organisaties, Organisatieonderdelen en voorzieningen](https://github.com/Logius-standaarden/Digikoppeling-Algemeen/issues/10) (30 May. 2022), _Status: In bewerking_
* Digikoppeling-Algemeen [issue #9] [Analyse knelpunten Routering en Intermediairs in gegevensverkeer](https://github.com/Logius-standaarden/Digikoppeling-Algemeen/issues/9) (30 May. 2022), _Status: In bewerking_
* OIN-Stelsel [issue #5] [Kvk nummer leidend voor OIN?](https://github.com/Logius-standaarden/OIN-Stelsel/issues/5) (29 Mar. 2022), _Status: In onderzoek_

## Overige punten
* Digikoppeling-Koppelvlakstandaard-REST-API [issue #11] [Signing & Encryptie toevoegen aan RESTful API profiel](https://github.com/Logius-standaarden/Digikoppeling-Koppelvlakstandaard-REST-API/issues/11) (01 Apr. 2022)
* Digikoppeling-Algemeen [issue #6] [Interoperabiliteit platformen WUS bij gebruik MTOM in combinatie met WS-Security (signing)](https://github.com/Logius-standaarden/Digikoppeling-Algemeen/issues/6) (29 Mar. 2022), _Status: In onderzoek_
* OAuth-NL-profiel [issue #13] [PKCE beschrijving in Sectie 2.3.1 klopt niet](https://github.com/Logius-standaarden/OAuth-NL-profiel/issues/13) (19 Aug. 2020)
* OAuth-NL-profiel [issue #7] [3.2.1 JWT Bearer Tokens - "sub" claim](https://github.com/Logius-standaarden/OAuth-NL-profiel/issues/7) (19 Nov. 2019), _Status: Klaar voor release_

# Toelichting




## MIDO governance

Logius wil strategische vragen agenderen voor de programmeringstafel Gegevensuitwisseling. De rol, het doel en de bezetting van de programmertafel zijn nog in ontwikkeling. Er is een eerste programmeringstafel GU geweest, een kick-off waarbij nog geen inhoudelijke punten zijn besproken. Eind juni volgt een tweede overleg waarbij we nog geen punten vanuit standaardisatie gaan agenderen omdat we nog in overleg zijn welk soort wijzigingsvoorstellen geschikt zijn om te agenderen.

__Ter info__

## ebMS3 transitie

De openstaande vraag over transitie naar ebMS3 is een strategische vraag. Op welke termijn en tegen welke kosten kunnen de stakeholders over naar een nieuwe versie van hun koppeling. We stellen deze vraag in de programmeringstafel, maar de programmeringstafels zijn nog in ontwikkeling. Ook is voor een programmeringstafel een bredere vraag relevant: hoe ontwikkelen we de koppelvlakspecificaties verder en hoe faseren we specificaties uit?

We willen dit punt agenderen wanneer we ook een alternatief scenario kunnen geven. Een aantal Nederlandse overheden heeft een _API first_ strategie aangenomen. Bij het uitfaseren van een ebMS2 gebaseerd koppelvlak zijn er twee mogelijkheden voor een overheid: transitie naar een ebMS3 koppelvlak of over gaan naar een REST API koppelvlak.

__Ter discussie met het TO: bieden we (blijvend) alle huidige koppelvlakspecificaties aan en hoe kunnen we verouderde specificaties uitfaseren?__

## Toelichting Interoperabiliteit MTOM

Voorbeeld berichten van datapower zijn onderzocht. Aanpassingen op de WUS standaard om de interoperabiliteit te vergroten zouden grote impact hebben op bestaande implementaties die gebruik maken van andere platformen. Advies vanuit Digikoppeling Beheer is daarom om geen aanpassingen op de standaard door te voeren en dit issue te sluiten.<BR>Zie ook de [Analyse/uitwerking](https://github.com/Logius-standaarden/Digikoppeling-Algemeen/issues/6) van het issue.<BR>
__Vraag aan het TO: Is het TO akkoord met voorstel om geen aanpassingen aan de standaard te doen op dit punt?__

## StvZ lopende roadmap items

### Digikoppeling governance

Zie hierboven en issue onder [grote wijzigingen](#Grote-wijzigingen). [Schema beheerproces](media/Beheerproces.svg)

### Informatievoorziening

We streven naar een vereenvoudiging van onze informatievoorziening.
* we willen https://publicatie.centrumvoorstandaarden.nl/ uitfaseren en overgaan naar https://gitdocumentatie.logius.nl/
* publicatie van agenda's via github

[Overzicht publicatiesites](media/Publicatie.png)

### Signing & Encryptie toevoegen aan RESTful API profiel

Onderzoek loopt in samenwerking met KP API werkgroep beveiliging

### Identificatie en Routering

Handreiking voor ondersteuning voor dit onderwerp is in ontwikkeling
(Zie apart agenda punt)

### Interoperabiliteit platformen WUS bij gebruik MTOM in combinatie met WS-Security (signing)

Voorbeeld berichten van datapower zijn onderzocht. Aanpassingen op de WUS standaard om de interoperabiliteit te vergroten zouden grote impact hebben op bestaande implementaties die gebruik maken van andere platformen;
(Zie apart agenda punt)

### Doorontwikkeling RESPEC/Digikoppeling template voor publicatie van specificaties

Het [ReSpec-profiel](https://github.com/Logius-standaarden/respec) is stabiel en in gebruik in alle Digikoppeling-documenten. De wens is het profiel meer modulair op te zetten om onderhoud te vergemakkelijken en gebruik buiten Logius te faciliteren.

### Onderzoek verwijzing naar de 'ADR API Security Extensie' vanuit de Digikoppeling Beveiligingsvoorschriften		 	 	 	 

Onderzoek loopt.

Toelichting relatie REST-API profiel en ADR extensies:
  
Het Digikoppeling REST-API profiel is gebaseerd op het normatieve deel van de ADR, daarnaast worden enkele (relevante) regels overgenomen uit de (informatieve) ADR extensies;
(Deze regels worden daarmee voor het Digikoppeling REST-API profiel normatief.)
  
![DK](media/Digikoppeling%20gebaseerd%20op%20ADR.drawio.svg)

### Update Beheermodel / aansluiting op Logius Standaarden BOMOS generiek beheer model & governance	 	 	 	 	 

Ontwikkeling BOMOS generiek model loopt. Er is een [template beheermodel](https://github.com/Logius-standaarden/BOMOS-voorbeeld-beheermodel) voor BOMOS. Het beheermodel Digikoppeling wordt op basis hiervan herschreven. 

### Verkennen mogelijk gebruik ebMS3/AS4

Zie hierboven en issue onder [grote wijzigingen](#Grote-wijzigingen).
