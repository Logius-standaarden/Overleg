# TO-DK



# Agenda

|  |   |
|------------------------|-------------------------------------|
| Betreft  | **Technisch Overleg Digikoppeling** |
| Vergaderdatum en -tijd | 29-09-2022 - 10:00 uur  |
| Vergaderplaats  | Webex  |

## Onderwerpen


| Tijd | Onderwerp |
| --- | --- |
| 10:00-10:05 | Welkom & Mededelingen |     
| 10:05-10:10 | Verslag vorig TO:<br> [Verslag TO Digikoppeling 23-06-2022](https://github.com/Logius-standaarden/Overleg/blob/main/Digikoppeling/2022-06-23/20220623_Verslag_Technisch_Overleg%20Digikoppeling.md) |   
| 10:10-10:20 | Bespreken [grote wijzigingen](#Grote-wijzigingen), zie ook toelichtingen [governance](#MIDO-governance) en [ebMS3](#ebMS3-transitie) |
| 10:20-11:00| Bespreken [kleine wijzigingen](#Kleine-wijzigingen) en [overige punten](#Overige-punten) |
|  |  Graag specifiek aandacht hierbij voor: |  
| 11:00-11:20 | Roadmap : [Stand van zaken Roadmap onderdelen](#stvz-lopende-roadmap-items) |     
| 11:20-11:30 | Rondvraag & Afsluiting. |     

# Punten

## Grote wijzigingen
* Digikoppeling-Beheermodel [issue #3] [Aanpassing beheermodel op BOMOS principes en MIDO governance](https://github.com/Logius-standaarden/Digikoppeling-Beheermodel/issues/3) (16 Mar. 2022), _Status: In bewerking_
* Digikoppeling-Koppelvlakstandaard-ebMS2 [issue #6] [Digikoppeling baseren op ebMS3](https://github.com/Logius-standaarden/Digikoppeling-Koppelvlakstandaard-ebMS2/issues/6) (03 Feb. 2022), _Status: In onderzoek_

## Kleine wijzigingen
* Digikoppeling-Koppelvlakstandaard-REST-API [issue #15] [Toevoegen API-58 No sensitive information in URIs ](https://github.com/Logius-standaarden/Digikoppeling-Koppelvlakstandaard-REST-API/issues/15) (16 Jun. 2022), _Status: In review_
* Digikoppeling-Algemeen [issue #10] [Best Practice Identificatie van Organisaties, Organisatieonderdelen en voorzieningen](https://github.com/Logius-standaarden/Digikoppeling-Algemeen/issues/10) (30 May. 2022), _Status: In bewerking_
* Digikoppeling-Algemeen [issue #9] [Analyse knelpunten Routering en Intermediairs in gegevensverkeer](https://github.com/Logius-standaarden/Digikoppeling-Algemeen/issues/9) (30 May. 2022), _Status: In bewerking_
* OIN-Stelsel [issue #5] [RSIN of Kvk nummer leidend voor OIN?](https://github.com/Logius-standaarden/OIN-Stelsel/issues/5) (29 Mar. 2022), _Status: In onderzoek_

## Overige punten
* Digikoppeling-Koppelvlakstandaard-REST-API [issue #11] [Signing & Encryptie toevoegen aan RESTful API profiel](https://github.com/Logius-standaarden/Digikoppeling-Koppelvlakstandaard-REST-API/issues/11) (01 Apr. 2022)

# Toelichting




(oud)

## Aanpassing beheermodel op BOMOS principes en MIDO governance

Wat is er veranderd... **TODO**

__Ter review__

## ebMS3 transitie

Stand van zaken... **TODO**

__Ter info__

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