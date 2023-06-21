# Discussiestuk : OIN Stelsel - SubOIN registratie uitbreiden met veld reden & doel

## Aanleiding

Voor het Centraal OIN Register is als vezoek ontvangen :
“Een extra kolom toe voegen in het Centraal OIN Register (COR) waarin de taak/ het doel wordt opgeslagen van een SubOIN.
(Dit moet uitgevraagd worden bij het aanvragen van een subOIN)"

## Toelichting
Voorbeeld Scenario: Gemeente X voor participatiewet met applicatie A
* Bij vraag ‘Waarom vraagt u dit aan?’ wordt gekozen voor Een onderdeel van mijn organisatie
* Bij naam vult men bijv. in: Team Armoedebestrijding Gemeente X
* Bij nieuwe veld taak/doel vult men in: __participatiewet - uitkeren__

COR toont dan:

| Naam | Nummer | Reden | Taak / Doel| Status | Afgifte datum |
|---|---|---|---|---|---|
|  Team Armoede bestrijding Gemeente X |00000004000001500|Onderdeel Organisatie| Participatiewet-uitkeren|Actief|21-11-2021| 
 


### Een voorbeeld van subOIN’s in huidige COR:
<PRE>
SUBOIN per HOOFDOIN
OIN                      Naam                          SubOIN                       SubOIN.Naam
00000001001876387000          Gemeente Rotterdam            00000004126066364000          GSD Gemeente Rotterdam
00000001001876387000          Gemeente Rotterdam            00000004179545817000          Het Zorg- en Veiligheidshuis Rotterdam-Rijnmond
00000001001876387000          Gemeente Rotterdam            00000004180126081000          Burgerzaken Gemeente Rotterdam
00000001001876387000          Gemeente Rotterdam            00000004143141878000          GGD Rotterdam-Rijnmond
00000001001876387000          Gemeente Rotterdam            00000004173502349000          GBD Gemeente Rotterdam
00000001001876387000          Gemeente Rotterdam            00000004169512451000          Cluster Maatschappelijke Ontwikkeling afdeling Kredietbank Rotterdam
</PRE>
  

### Enkele voordelen van reden/doel registreren
* Het veld reden/doel helpt om de juiste autorisatie voor de verschillende berichtsoorten te geven;
* Het veld reden/doel kan helpen om misbruik/verkeerd gebruik te voorkomen/detecteren 
* Reden/doel centraal registreren kan de gebruiker helpen om overzicht te houden over de eigen aangevraagde suboins;

### Enkele aandachtspunten :
* Een subOIN (organisatieonderdeel of systeem) kan meerdere wettelijke taken hebben. In feite is alleen een reden/doel aan te geven per _koppeling_. Het is niet nodig per taak een subOIN aan te vragen.
* Als de invalshoek van 'doel' wettelijke taken zijn , vraagt dit om standaardisatie van naamgeving; als doel een __ vrij veld__ is waar ook andere invalshoeken worden gebruikt is het mogelijk gevaar dat allerlei contexten en classificaties door elkaar gebruikt worden waardoor , bv ook door dubbele naamgeving, niet duidelijk is welke betekenis wordt bedoeld of om welk domein het precies gaat 

## Vragen voor de discussie in het TO Digikoppeling:

* Is een dergelijke registratie van reden/doel wenselijk?
* Welke voordelen/nadelen aandachtspunten zijn er bij deze registratie


# Bijlage Relevante Achtergrondinformatie:

## Identificatie, authenticatie en autorisatie met het OIN en subOIN
_Auteur: Martin van der Plas (Logius)_


### Identificatie (wie ben je)
Het OIN vormt de identificatie van een organisatie en is gebaseerd op de juridische entiteit van een organisatie zoals vastgelegd door het KvK, de Belastingdienst, Logius of een andere organisatie.

Het subOIN biedt de mogelijkheid aan organisaties om delen van hun organisatie zelfstandig te registreren als identificeerbare eenheid. Bijvoorbeeld een afdeling

### Authenticatie (Ben je echt wie je zegt te zijn)
Authenticatie / authenticiteit wordt altijd gewaarborgd door de uitgever van het middel / certificaat waarin de identiteit is opgenomen. Voor gegevensuitwisseling doen we dit normaliter door het OIN of subOIN op te nemen in een  PKIOverheid-certificaat. De uitgever / TSP van het certificaat garandeert daarbij de authenticiteit.

Merk op dat een organisatie zelf verantwoordelijk en geautoriseerd is om subOINs aan te maken en PKIO Certificaten aan te vragen bij TSP met daarin een subOIN. Logius is niet in staat en niet verantwoordelijk voor de kenmerken die op verzoek van de organisatie bij het subOIN worden opgeslagen.

### Autorisatie (wat mag je)
Autorisatie is altijd een verantwoordelijkheid van de dienstaanbieder. Met het verstrekken van een (sub)OIN en een PKIO-certificaat ben je nog nergens toe geautoriseerd.

Voor de autorisatie dient men een verband te leggen tussen de dienst die wordt aangeboden en het OIN om zodoende de juridisch verantwoordelijke organisatie te duiden die van de dienst gebruik maakt. Aanvullend kan een subOIN worden gebruikt om een specifiek deel van de organisatie te identificeren.

### Aanvullende maatregelen
Om uit te sluiten dat een ander certificaat ook kan worden gebruikt voor dezelfde dienst kunnen aanvullende maatregelen worden genomen. Dit kan in de vorm van ‘certificate key-pinning’. Hierbij wordt een uniek kenmerk van het certificaat opgeslagen door de dienstaanbieder en dient bij iedere gegevensuitwisseling van hetzelfde unieke certificaat gebruikt te worden gemaakt. Dit sluit uit dat iemand anders van de betreffende organisatie met een ander certificaat gegevens uit kan wisselen met de specifieke dienst.  Dit kan zowel op de certificaat-id als de public-key.

Het verschil tussen het certificaat-id en de public-key is dat de public-key gelijk kan blijven in een nieuw certificaat wat wordt afgeleid van dezelfde private-key. Het certificaat-id is bij ieder nieuw certificaat uniek.

Een alternatief is nog het gebruik van oAuth waarbinnen fijnmazige kenmerken in tokens kunnen worden uitgewisseld tussen de uitgever van het token, de dienstafnemer en de dienst aanbieder

## Digikoppeling documentatie
Zie ook:
https://publicatie.centrumvoorstandaarden.nl/dk/gbachtcert/#achtergrond-4
