# RFC-lijst
## RFC: Aanpassen Bijlage OIN Tabel
Aanpassen Bijlage OIN Tabel conform OIN Beleid

[Aanpassingen in de documentatie](https://github.com/Logius-standaarden/Overleg/blob/main/Digikoppeling/rfc.md#rfc-aanpassen-bijlage-oin-tabel)
### Aangepaste documenten

#### Digikoppeling-Identificatie-en-Authenticatie
[Pull request](https://github.com/Logius-standaarden/Digikoppeling-Identificatie-en-Authenticatie/pull/3) | [Preview](https://logius-standaarden.github.io/Publicatie-Preview/Digikoppeling-Identificatie-en-Authenticatie/RFC-2022-001-OIN-Tabel-update)
<details><summary>Wijzigingen</summary>

```diff
diff --git a/ch05_Identiteit en nummer.md b/ch05_Identiteit en nummer.md
index beb7477..00d5509 100644
--- a/ch05_Identiteit en nummer.md	
+++ b/ch05_Identiteit en nummer.md	
@@ -104,6 +104,6 @@ Rechtspersoonlijkheid) eenvoudig een subOIN aanvragen voor
 Met nadruk stellen we dat deze mogelijkheid facultatief. Ook is duidelijk
 gemaakt hoe en wanneer organisaties een OIN kunnen krijgen als ze niet aan een
 van hierboven gestelde eisen kunnen doen, zoals buitenlandse partijen of
-organisaties uit het onderwijs. In de Digikoppeling Voorwaarden[] worden de
+organisaties uit het onderwijs. In de Digikoppeling Voorwaarden worden de
 voorwaarden voor uitgifte en gebruik van het OIN exact beschreven.
 
diff --git a/ch06_Bijlage 1.md b/ch06_Bijlage 1.md
index d18b1ce..ae8c1a1 100644
--- a/ch06_Bijlage 1.md	
+++ b/ch06_Bijlage 1.md	
@@ -21,18 +21,26 @@ De waarde van het OIN in het OIN Register en in het veld subject.serialNumber is
 inclusief de prefix en suffix en daarbij behorende voorloopnullen. Door het
 gehele nummer te gebruiken wordt zeker gesteld dat het nummer uniek is.
 
-| Prefix   | Identificerend nummer                   | Bron                                                                                                                                                       |
-|---|---|---|
-| **00000001** | RSIN                                    | Handelsregister                                                                                                                                            |
-| **00000002** | Fi-nummer                               | Het fiscaal nummer wordt verstrekt door de Belastingdienst aan de organisatie zelf<sup>10</sup> (alleen voor organisaties die niet in het Handelsregister staan).  |
-| **00000003** | KvK nummer                              | Handelsregister<sup>11</sup>                                                                                                                                       |
-| **00000004** | subnummer                               | subOIN register                                                                                                                                            |
-| **00000005** | Onderdelen van de Staat der Nederlanden | nog aan te wijzen                                                                                                                                          |
-| **00000006** | Onderdelen van het Rijk                 | nog aan te wijzen                                                                                                                                          |
-| **00000007** | BRIN nummer                             | De Basisregistratie Instellingen (BRIN) is een register van onderwijsinstellingen dat door DUO wordt beheerd in opdracht van het Ministerie van OCW.       |
-|**00000008** | Buitenlandse nummers                    | Buitenlandse nummers                                                                                                                                       |
+
+## Prefix tabel
+
+Een aangesloten overheidsregister krijgt een prefix (per uniek nummer) als het register wordt toegevoegd aan het OIN-stelsel. Dit wordt ook een OIN register genoemd. De prefix tabel wordt als aparte lijst beheerd door de beheerder van het OIN-stelsel en wordt gepubliceerd op de website.
+
+
+
+| **Prefix** | **Identificerend nummer** | **Bron**|
+|------------|-----------------------------------------|---|
+| **00000001** | RSIN| Handelsregister |
+| **00000002** | Fi-nummer | Het fiscaal nummer wordt verstrekt door de Belastingdienst aan de organisatie zelf<sup>10</sup>. Het Fi-nummer kan worden gebruikt in het het geval voor onderdelen van de Staat der Nederlanden die niet ingeschreven in het Handelsregister zoals de Tweede Kamer der Staten-Generaal of de Algemene Rekenkamer. Het FI-nummer wordt verstrekt door de organisatie zelf |
+| **00000003** | KvKnummer| Handelsregister<sup>11</sup>. Het KvKnummer wordt gebruikt door private partijen in de communicatie met de overheid. |
+| **00000004** | subnummer | SubOIN register |
+| **00000005** | vrij | nog aan te wijzen |
+| **00000006** | Logius OIN Hoofdnummer | Door Logius uitgegeven OIN Hoofdnummers aan organisaties die in aanmerking komen voor een OIN maar waarvoor geen geschikt nummer uit de overige prefix categorieën beschikbaar is<sup>12</sup>.  |
+| **00000007** | BRIN nummer | De Basisregistratie Instellingen (BRIN) is een register van onderwijsinstellingen dat door DUO wordt beheerd in opdracht van het Ministerie van OCW.|
+| **00000008** | Buitenlandse nummers| Op verzoek van een SubOIN-beheerder door Logius uitgegeven nummers voor buitenlandse organisaties die niet in het Handelsregister zijn ingeschreven|
 | **00000009** | UZI-nummer| Het Unieke Zorgverlener Identificatie Register (UZI-register) is de organisatie die de unieke identificatie van zorgaanbieders en indicatieorganen in het elektronisch verkeer mogelijk maakt.|
-| **00000099** | Test OIN’s                              | Elke organisatie mag een test OIN gebruiken mits voorzien van deze prefix.                                                                                 |
+| **00000099** | Test OIN's| Elke organisatie mag een test OIN gebruiken mits voorzien van deze prefix.|
+
 
 <sup>10</sup>: In uitzonderlijke gevallen kan het Fi-nummer worden gebruikt indien
     verstrekt door de organisatie zelf. Dit is b.v. het geval bij onderdelen van
@@ -48,6 +56,10 @@ gehele nummer te gebruiken wordt zeker gesteld dat het nummer uniek is.
 - Het KvK-nummer kan in het Handelsregister van de KvK na opgave door de
     aanvrager gecontroleerd worden door Logius.
 
+
+ <sup>12</sup>:  Logius OIN Hoofdnummer: Voor organisaties uit het caribisch deel van het Koninkrijk der Nederlanden is dit nummer opgebouwd als 4 posities landnummer gevolgd door 5 posities volgnummer, conform landentabel BRP.
+
+
 Voorbeelden:
 
 OIN o.b.v. RSIN: 00000001123456789000
diff --git a/js/config.js b/js/config.js
index 079abdc..b0d421e 100644
--- a/js/config.js
+++ b/js/config.js
@@ -10,7 +10,7 @@ var respecConfig = {
   // EO: Einde ondersteuning, verouderde versie, vervangen door nieuwe versie
   // TG: Versie teruggetrokken
   // BASIS, GN-BASIS: 'geen status'
-  specStatus: "DEF",
+  specStatus: "WV",
 
   // SpecType currently supported
   // NO: "Norm"
@@ -45,8 +45,8 @@ var respecConfig = {
   // A YYYY-MM-DD date. When a previousPublishDate is specified, this is typically required as well in order to generate the "Previous Version"
   //previousMaturity: "WV",
 
-  publishVersion: "1.4.1",
-  // previousPublishVersion: "1.4",
+  publishVersion: "1.4.2",
+  previousPublishVersion: "1.4.1",
 
   // license can be one of the following: cc0, cc-by or cc-by-nd((default)) (see https://github.com/Geonovum/respec/wiki/license )
   license: 'cc-by-nd',

```

</details>
