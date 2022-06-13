# Technisch overleg

Concept

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
| 10:05-10:10 | Toelichting Grote Wijzigingen   | 
| 10:10-10:15 | Digikoppeling-Algemeen [issue #9] [Analyse knelpunten Routering en Intermediairs in gegevensverkeer](https://github.com/Logius-standaarden/Digikoppeling-Algemeen/issues/9) <BR> _[Verzoek aan het TO is de (concept) uitwerking te reviewen]_|  
| 10:15-10:25 | Digikoppeling-Algemeen [issue #10] [Best Practice Identificatie van Organisaties, Organisatieonderdelen en voorzieningen](https://github.com/Logius-standaarden/Digikoppeling-Algemeen/issues/10) <BR> _[Verzoek aan het TO is de (concept) uitwerking te reviewen]_|
| 10:25-10:30 | OIN-Stelsel [issue #5] [Kvk nummer leidend voor OIN  ](https://github.com/Logius-standaarden/OIN-Stelsel/issues/5) |  
| 10:30-10:40 |  Digikoppeling-Algemeen [issue #6] [Interoperabiliteit platformen WUS bij gebruik MTOM in combinatie met WS-Security (signing)](https://github.com/Logius-standaarden/Digikoppeling-Algemeen/issues/6) <BR> Zie [Toelichting](#toelichting-MTOM) |   
| 10:40-10:45 | Voorstel publicatie van PATCH releases <BR> _[Goedkeuring door TO]_|   
| 10:45-11:15 | Roadmap : [Stand van zaken Roadmap onderdelen](#stvz-lopende-roadmap-items) |     
| 11:15-11:30 | Rondvraag & Afsluiting. |     

# Punten

## Grote wijzigingen
* Digikoppeling-Koppelvlakstandaard-REST-API [issue #11] [Signing & Encryptie toevoegen aan RESTful API profiel](https://github.com/Logius-standaarden/Digikoppeling-Koppelvlakstandaard-REST-API/issues/11) (01 Apr. 2022)
* Digikoppeling-Beheermodel [issue #3] [Aanpassing beheermodel op MIDO governance](https://github.com/Logius-standaarden/Digikoppeling-Beheermodel/issues/3) (16 Mar. 2022), _Status: In bewerking_
* Digikoppeling-Koppelvlakstandaard-ebMS2 [issue #6] [Digikoppeling baseren op ebMS3](https://github.com/Logius-standaarden/Digikoppeling-Koppelvlakstandaard-ebMS2/issues/6) (03 Feb. 2022), _Status: In onderzoek_

## Kleine wijzigingen
* Digikoppeling-Algemeen [issue #10] [Best Practice Identificatie van Organisaties, Organisatieonderdelen en voorzieningen](https://github.com/Logius-standaarden/Digikoppeling-Algemeen/issues/10) (30 May. 2022), _Status: In bewerking_
* Digikoppeling-Algemeen [issue #9] [Analyse knelpunten Routering en Intermediairs in gegevensverkeer](https://github.com/Logius-standaarden/Digikoppeling-Algemeen/issues/9) (30 May. 2022), _Status: In bewerking_
* OIN-Stelsel [issue #5] [Kvk nummer leidend voor OIN  ](https://github.com/Logius-standaarden/OIN-Stelsel/issues/5) (29 Mar. 2022), _Status: In onderzoek_

## Overige punten
* Digikoppeling-Algemeen [issue #6] [Interoperabiliteit platformen WUS bij gebruik MTOM in combinatie met WS-Security (signing)](https://github.com/Logius-standaarden/Digikoppeling-Algemeen/issues/6) (29 Mar. 2022), _Status: In onderzoek_

# Toelichting



## MIDO governance

Logius wil strategische vragen agenderen voor de programmeringstafel Gegevensuitwisseling. De rol, het doel en de bezetting van de programmertafel zijn nog in ontwikkeling.

## ebMS3 transitie

## SaaS en OIN

## KvK nummers in OIN

## StvZ lopende roadmap items


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
(Zie apart agenda punt)

### Interoperabiliteit platformen WUS bij gebruik MTOM in combinatie met WS-Security (signing)

Voorbeeld berichten van datapower zijn onderzocht. Aanpassingen op de WUS standaard om de interoperabiliteit te vergroten zouden grote impact hebben op bestaande implementaties die gebruik maken van andere platformen;
(Zie apart agenda punt)

### Doorontwikkeling RESPEC/Digikoppeling template voor publicatie van specificaties	

Het [ReSpec-profiel](https://github.com/Logius-standaarden/respec) is stabiel en in gebruik in alle Digikoppeling-documenten. De wens is het profiel meer modulair op te zetten om onderhoud te vergemakkelijken en gebruik buiten Logius te faciliteren.

### Onderzoek verwijzing naar de 'ADR API Security Extensie' vanuit de Digikoppeling Beveiligingsvoorschriften		 	 	 	 

Onderzoek loopt

### Update Beheermodel / aansluiting op Logius Standaarden BOMOS generiek beheer model & governance	 	 	 	 	 

Ontwikkeling BOMOS generiek model loopt.

### Verkennen mogelijk gebruik ebMS3/AS4

Zie voorstel in [grote wijzigingen](#Grote-wijzigingen).
