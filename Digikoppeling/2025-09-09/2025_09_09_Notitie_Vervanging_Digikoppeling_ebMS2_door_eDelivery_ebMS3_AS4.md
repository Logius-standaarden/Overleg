# 2025_09_09 Notitie Vervanging Digikoppeling ebMS2 door eDelivery ebMS3/AS4	

_Een eerdere versie van deze notitie is als voorstel ook behandeld in het TO 19/3/2025 , in dit TO wordt het in aangepaste vorm ingebracht ter besluitvorming_

## Inleiding
Omdat de standaard ebMS2 niet meer doorontwikkeld wordt en ondersteuning in de markt terugloopt is er onderzoek gedaan naar de mogelijkheid om de Digikoppeling ebMS2 koppelvlakstandaard te vervangen door ebMS3 en dan met name het eDelivery ebMS3/AS4 profiel. (Zie link naar PBLQ onderzoek : [Impactanalyse modernisering Digikoppeling ebMS: van ebMS2 naar eDelivery (ebMS3/AS4)](https://github.com/Logius-standaarden/Overleg/blob/main/Digikoppeling/2024-03-06/Rapport%20Impactanalyse%20modernisering%20Digikoppeling%20ebMS%20-%20v1.1%20definitief%2019%20januari%202024.pdf) ).
In deze notitie wordt specifiek ingegaan wat nodig is binnen de Digikoppeling standaard om eDelivery ebMS3/AS4 als koppelvlakstandaard in te voeren, wat nodig is aan ondersteunende voorzieningen en welke keuzes/besluiten nodig zijn bij de migratie naar de nieuwe standaard;

Het onderzoeksrapport is besproken in het MIDO bij de Programmeringstafel GU, hier is afgesproken dat de koppelvlakstandaard los gezien wordt van het eDelivery construct (dwz de benodigde centrale voorzieningen en (stelsel) afspraken); Dit om voortgang mogelijk te maken op de standaard in afwachting van ontwikkelingen rond de architectuur visie op eDelivery in de GDI;

In deze notitie wordt dieper ingegaan op de inbedding van de standaard in Digikoppeling, hiermee wordt ook duidelijk wat verder nodig is aan voorzieningen/afspraken, deze notitie is daarmee ook input voor de visie op de GDI architectuur en de besluitvorming omtrent gebruik van het Digikoppeling eDelivery ebMS3/AS4 koppelvlak standaard in de GDI;

## Opname van het eDelivery ebMS3/AS4 profiel binnen Digikoppeling
Het eDelivery ebMS3/AS4 profiel kan 1 op 1 opgenomen worden als document binnen de standaard;
4 December 2024 is de nieuwe versie 2.0 vastgesteld : [eDelivery 2.0 profile specifications officially adopted](https://ec.europa.eu/digital-building-blocks/sites/pages/viewpage.action?pageId=848625744)

Een voorbeeld workflow in ebMS3/AS4 is:

|Stap                   | Toelichting |
|-----------------------|-------------------------|
|1.	Overeenstemming	    | Uitwisselen van messaging parameters (bv security, endpoints) |
|2.	Configuratie 		     | Elke partij configureert het eigen AS4 compatible systeem met de overeengekomen parameters |
|3.	Certificaat uitwisseling	| Digitale certificaten worden uitgewisseld voor authenticatie en encryptie |
|4.	Bericht uitwisseling 	    | Berichten worden uitgewisseld conform AS-protocol en messaging parameters |
|5.	Betrouwbaarheid 	        | AS4 ondersteunt reliable messaging dmv acknowledgements en retries |

Het PBLQ Impactanalyse Onderzoeksrapport geeft aan:
_“Er moet nog een definitieve keuze worden gemaakt voor de adresboek- en mandateringssystematiek in de nieuwe situatie. In de huidige situatie wordt dit ingevuld door een Collaboration Protocol Agreement (CPA). In de beoogde situatie zijn er verschillende opties voor deze functionaliteit mogelijk, zoals een Service Metadata Locator (SML)/Service Metadata Publisher (SMP) systematiek of een soortgelijke CPA systematiek.”_

Wat betreft deze keuze, een deel van de CPA functionaliteit wordt ingevuld door het eDelivery AS4 profiel:


|CPA-functionaliteit	|	eDelivery AS4-dekking|
|-----------------------|-------------------------|
|Transportprotocollen	|	HTTPS is verplicht. |
| Beveiligingsvereisten	 |	WS-Security, X.509-certificaten voor ondertekening en encryptie, wederzijdse TLS voor authenticatie. |
| Berichtenverpakking	|	SOAP met MIME-bijlagen. |
| Betrouwbaarheid 	|	ebMS3-betrouwbaarheid met ontvangstbewijzen, herhalingen en duplicaatdetectie. |
| Foutverwerking		|	SOAP-fouten en herhalingsmechanismen. |
| Bedrijfsproces en rollen	|	Wordt verondersteld out-of-band te zijn gedefinieerd; profiel ondersteunt berichtenuitwisseling voor specifieke rollen. |
| Interoperabiliteit	|	Gestandaardiseerd profiel zorgt voor interoperabiliteit tussen systemen. |
| Dynamische discovery	|	bv out-of-band; optioneel gebruik van SMP voor dynamische endpoint discovery |

Voor het gebruik van het eDelivery AS4 profiel in de Digikoppeling context zijn er de volgende opties: 

1. Geen centraal adresboek: Endpoints en certificaten worden ‘out of band’ bilateraal tussen partijen uitgewisseld
2. Geen centraal adresboek: Gebruik van ebCore Agreement update (nieuw in v2.0) : Messaging configurations worden over een AS4 kanaal uitgewisseld 
3. Een centraal adresboek:   Gebruik van Service Metadata Locator (SML)/Service Metadata Publisher (SMP) als een centraal adresboek

### 1 Geen centraal adresboek: Endpoints en certificaten worden ‘out of band’ bilateraal tussen partijen uitgewisseld
Nadeel is dat dit in vergelijking met de huidige werking van ebMS2/CPA meer handmatig beheer vraagt;
Een voordeel van deze optie is dat het eDelivery ebMS3/AS4 profiel sneller kan worden ingevoerd onder Digikoppeling en dat partijen die over willen stappen al koppelingen kunnen omzetten naar de nieuwe koppelvlakstandaard Digikoppeling ebMS3/AS4;

### 2 Geen centraal adresboek: Gebruik van ebCore Agreement update (nieuw in v2.0)
Een interessante uitbreiding in eDelivery v2.0 is het gebruik van ebCore Agreements, dit biedt bepaalde functionaliteit vergelijkbaar met het huidige CPA.
Met daarbij de optie om ook updates aan Agreements via een vast protocol uit te voeren (en te automatiseren).
Een voordeel van ebCore Agreements is dat beheer (bv configuratie en certificaat vervanging) meer ge-automatiseerd kan worden en dus minder handmatig werk vraagt;

Ook werken ebCore Agreements bilateraal , vergelijkbaar met CPA en is er geen centrale voorziening noodzakelijk (zoals bij SMP/SML)

Zie bijlage A ebCore Agreements voor een overzicht van de ondersteunde functionaliteit

### 3 Een centraal adresboek:   Gebruik van Service Metadata Locator (SML)/Service Metadata Publisher (SMP) als een centraal adresboek
Certificaten en parameters kunnen in dit geval via centrale voorzieningen voor Metadata  (SML/SMP) uitgewisseld worden.
Hiervoor is in ieder geval een landelijk SMP en SML voor Digikoppeling nodig. (Het een optie is om een bestaand centraal Europees SML te gebruiken en alleen een landelijk SMP te voeren, maar een dergelijke afhankelijkheid van 1 centraal systeem waar ook veel andere domeinen op aansluiten is minder wenselijk);
Voordeel van een centraal adresboek is de ‘discovery’ functionaliteit, op 1 plaats zijn de beschikbare diensten en communicatie parameters te vinden;

Een opmerking hierbij is dat in de huidige situatie ebMS2/CPA geen centraal adresboek wordt gebruikt , en dat het invoeren en beheren van SML/SMP als centrale voorziening een bepaalde doorlooptijd en beheerkosten met zich meebrengt; 
Dit is bepalend voor de planning van de migratie en het daadwerkelijk kunnen overgaan op een nieuw Digikoppeling ebMS3/AS4 koppelvlak;

## Advies
Vanuit beheer van Digikoppeling stellen we voor om in te zetten op invoer van het AS4 profiel onder Digikoppeling met als uitgangspunt dat dit in beginsel conform optie 3 wordt ingevoerd; 
Maar dat niet gewacht wordt met de invoering/aanpassing van de standaard tot een centraal adresboek is gerealiseerd - Dit maakt het mogelijk om op relatief korte termijn al te starten met migratie (en hierbij gebruik te maken van optie 1 & 2);

 Het tijdpad voor de invoering van een centraal adresboek (SMP/SML) is afhankelijk van de besluitvorming in het MIDO , maar een indicatie hiervoor is ca 4 maanden na goedkeuring ;

## Bijlage A ebCore Agreements
De volgende functionaliteit wordt in het eDelivery AS4 profiel 2.0 ondersteund:
This eDelivery Profile Enhancement uses an extended subset of the OASIS specification to securely update:
-	long-lived signing certificates.
-	long-lived encryption certificates.
-	short-lived encryption certificates.

Optionally, using an extension, it also supports secure updates of:

-	Endpoint address URLs.
-	Messaging profiles or profile versions.
-	Security algorithms and related parameters.
-	Network security (whitelisting) address updates. 

Zie https://ec.europa.eu/digital-building-blocks/sites/display/DIGITAL/eDelivery+AS4+-+2.0#eDeliveryAS42.0-ebCoreAgreementUpdate

  
 
