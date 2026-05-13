# Referentiemodel Stelsel van Gemeentelijke Basisgegevens (RSGB)
Versie 2.02 — Deel I: Beschrijving  
Onderdeel van de GEMeentelijke Model Architectuur (GEMMA)

---

# Voorwoord

Burgers en bedrijven hoeven (straks) nog maar één keer hun gegevens aan de overheid te verstrekken. Landelijke basisregistraties zorgen voor het meervoudig gebruik hiervan binnen de overheid. Vóór die tijd dienen gemeenten minimaal hun basisgegevens op orde te hebben. Vanwege het belang van een goede gegevenshuishouding heeft KING medio 2007 versie 1.0 uitgebracht van het Referentiemodel Stelsel van Gemeentelijke Basisgegevens (RSGB). Daarmee speelden wij in op de overheidsbrede invoering van het landelijk stelsel van basisregistraties. Tevens verving dit het GFO Basisgegevens. In het voorjaar van 2008 hebben we met versie 1.1. het toepassingsgebied van het RSGB vergroot met de Basisregistratie WOZ (Waardering Onroerende Zaken). Voortschrijdend inzicht, de eerste ervaringen met het RSGB, ontwikkelingen in de (catalogi van de) landelijke basisregistraties en het ontwikkelen van de berichtenstandaard StUF-BG hebben ons aanleiding gegeven versie 2.0 van het RSGB uit te brengen. Dit objecten- of gegevensmodel ondersteunt gemeenten bij het stroomlijnen van hun gegevenshuishouding en de daarop gerichte processen voor beheer en gebruik. Ook voorziet het in standaarden voor gegevensuitwisseling, zodat gemeenten een samenhangende informatievoorziening kunnen opzetten. In versie 2.02 zijn wijzigingen doorgevoerd naar aanleiding van de aanpassingen die zijn doorgevoerd in de catalogus BAG (versie 2009) en het Logisch Ontwerp GBA (versie LO3.7). Deze wijzigingen zijn te vinden in een separaat document.
Beheer
De rapportage RSGB 2.0 is in mei 2009 vastgesteld door de StUF-regiegroep. Versie 2.02 betreft een patch m.b.t. Een aanpassing van niet-natuurlijke personen op verzoek van de StUF expertgroep.
Het beheer van het RSGB is per 1 januari 2010 overgenomen door KING, het KwaliteitsInstituut Nederlandse Gemeenten. Voor vragen, suggesties of opmerkingen kunt u contact opnemen met ons.
Commentaar op deze versie nemen we in de normale beheerprocedure van het RSGB mee. KING-specialisten beoordelen wijzigingsverzoeken en leggen ze ter advisering voor aan werkgroepen met een publiek-private samenstelling. Iedere belangstellende kan wijzigingsverzoeken indienen.

---

# Leeswijzer
 
De rapportage richt zich op iedereen die zich beroepsmatig bezighoudt met (het structureren van) de gemeentelijke informatievoorziening, het inrichten en beheren van basisregistraties en/of het tot stand brengen en beheren van gegevensuitwisseling.
De rapportage is opgebouwd overeenkomstig de gebruikelijke indeling van catalogi voor basisregistraties. Vanwege de omvang is zij in twee delen opgesplitst. Deel I beschrijft het RSGB op hoofdlijnen en licht het referentiemodel nader toe. In hoofdstuk 2 van deel I vindt u een overzicht van het objectenmodel en de daarmee samenhangende aspecten. In bijlage 1 lichten wij de wijzigingen toe ten opzichte van versie 1.1. In bijlage 2 geven we aan welke uit het GFO-BG afkomstige gegevens op welke wijze in het RSGB zijn opgenomen.
In Deel II vindt u de specificaties van de componenten waaruit het RSGB is opgebouwd: objecttypen (hoofdstuk 1), attribuutsoorten en relatiesoorten (hoofdstuk 2). Dit deel is vooral als ‘naslagwerk’ bedoeld.


---

# Samenvatting
De invoering van een overheidsbreed stelsel van basisregistraties is één van de meest ingrijpende ontwikkelingen waarmee gemeenten te maken hebben. Het Referentiemodel Stelsel van Gemeentelijke Basisgegevens (RSGB) biedt gemeenten en hun leveranciers houvast bij het invoeren en het gebruiken van deze gegevens.
Dit objectenmodel voor de gemeentelijke basisgegevens presenteert de samenhang tussen basisregistraties op een logische wijze. Maar gemeenten hebben meer gegevens nodig voor hun werkprocessen dan nu in de landelijke basisregistraties beschikbaar zijn. Het binnengemeentelijk stelsel is dan ook ‘rijker’ dan het landelijke stelsel.
Dit referentiemodel is onderdeel van de GEMmeentelijke Model Architectuur (GEMMA) van KING. De inhoud is in lijn met de Nederlandse OverheidsReferentieArchitectuur (NORA).

![#Stelse van Gemeentelijke Basisgegevens op hoofdlijnen](media/RSGB_op_hoofdlijnen.png)

## Inhoud

We hebben het RSGB gebaseerd op de Basisregistraties Adressen (BRA), Gebouwen (BGR), Personen (GBA), Bedrijven (NHR), Kadaster (BRK) en WOZ (BRWOZ) en op de grootschalige topografie die in het Informatiemodel Geografie (IMGeo) is gedefinieerd. We hebben dit aangevuld met gegevens van de voorloper van het referentiemodel, het GFO BasisGegevens uit 1998, waarbij het model bewust beperkt gehouden is.
Het referentiemodel is opgebouwd uit:
- objecttypen zoals ‘Verblijfsobject’ en ‘Ingeschreven persoon’;
- attribuutsoorten die eigenschappen van deze objecttypen beschrijven zoals ‘Bruto inhoud’ en ‘Voornamen’;
- relatiesoorten tussen deze objecttypen zoals ‘Ingeschreven persoon verblijft in Verblijfsobject’.

## Doelen

Het referentiemodel draagt er aan bij dat gemeenten en daarmee samenwerkende organisaties in staat zijn om de kern van hun gegevenshuishouding, de basisgegevens, in samenhang eenmalig te onderhouden en meervoudig te gebruiken bij de uitoefening van hun taken. Het stroomlijnen van de processen voor het beheer van deze gegevens biedt kansen voor efficiencyverbetering. Meervoudig gebruik van gegevens, waarbij vertrouwd kan worden op de kwaliteit van deze gegevens, is bijvoorbeeld van groot belang voor een goede dienstverlening. Verder vormt het referentiemodel de grondslag voor de berichtenstandaard StUF-B(asis)G(egevens). Leveranciers baseren hun software op deze standaard, zodat uitwisselbaarheid van basisgegevens wordt bereikt. Tot slot waarborgt het referentiemodel de uitwisseling van basisgegevens met het landelijk stelsel van basisregistraties en het benutten van dit stelsel in de gemeentelijke informatievoorziening.

## Invoering

Het is de bedoeling om het referentiemodel in de periode 2009 – 2010 geleidelijk in te voeren. KING verwacht dat leveranciers in die tijd hun software aanpassen aan de basisregistraties. Gedurende de genoemde periode zullen de versies van de berichtenstandaard StUF-BG op basis van het GFO-Basisgegevens en op basis van het RSGB naast elkaar bestaan, zodat een geleidelijke overgang mogelijk is. KING raadt gemeenten nadrukkelijk aan om de ontwikkeling van hun informatievoorziening te baseren op dit referentiemodel en niet alleen uit te gaan van één of meer (catalogi van) landelijke basisregistraties. Op deze manier kunnen gemeenten aansluiten bij het landelijk stelsel én wordt hun eigen informatievoorziening optimaal bediend. Het RSGB vult namelijk de gegevens uit het landelijke stelsel aan met gegevens die voor de gemeentelijke processen cruciaal zijn, maar niet in het landelijk stelsel worden geregistreerd.

---

# 1. Inleiding

## 1.1 Aanleiding
De invoering van een stelsel van basisregistraties bij de gehele overheid is zonder twijfel een van de meest ingrijpende ontwikkelingen waar gemeenten mee te maken hebben. Onder het motto ‘De overheid vraagt niet naar de bekende weg’, is wettelijk vastgelegd dat burgers en bedrijven basisgegevens nog maar éénmaal aan de overheid hoeven te verstrekken. Alle overheidsorganisaties zijn verplicht deze gegevens te gebruiken.
Voor gemeenten zijn de basisregistraties dáárom zo belangrijk, omdat zij niet alleen gebruiker ervan zijn, maar ook bronhouder van bijvoorbeeld de basisregistraties van Personen, Adressen en Gebouwen. De basisgegevens vormen nog maar het topje van de ijsberg van wat gemeenten aan gegevens nodig hebben om hun processen uit te voeren.
Om grip te krijgen op de meervoudig gebruikte gegevens, heeft een aantal Voorhoedgemeenten onder leiding van EGEM medio 2007 versie 1.0 uitgebracht van het Referentiemodel Stelsel van Gemeentelijke Basisgegevens (RSGB). Dit model was de opvolger van het ‘oude’ GFO-Basisgegevens van de Vereniging Nederlandse Gemeenten (VNG). In het voorjaar van 2008 hebben we met versie 1.1. het toepassingsgebied van het RSGB vergroot met de Basisregistratie WOZ (Waardering Onroerende Zaken). Daarmee speelden wij in op de overheidsbrede invoering van het landelijk stelsel van basisregistraties. Voortschrijdend inzicht, de eerste ervaringen met het RSGB, ontwikkelingen in de (catalogi van de) landelijke basisregistraties en het ontwikkelen van de berichtenstandaard StUF-BG hebben ons aanleiding gegeven versie 2.0 van het RSGB uit te brengen.

## 1.2 Opzet
KING presenteert met dit stelsel een standaard om het gebruik van basisgegevens binnen gemeenten en daarmee samenwerkende organisaties te bevorderen. We spreken binnen gemeenten over één samenhangend stelsel van basisgegevens en niet over een basisregistratie. Deze laatste term is gereserveerd voor de landelijke basisregistraties. Dit landelijke stelsel vormt echter wel het uitgangspunt voor het gemeentelijke model. Versie 2.0 van het RSGB is gebaseerd op de volgende, al dan niet definitieve, versies van de catalogi en vergelijkbare beschrijvingen van basisregistraties:
- Catalogus BasisRegistratie Adressen (BRA versie 4.0; Vrom, 2-2006),
- Catalogus Basis Gebouwen Registratie (BGR versie 4.0; Vrom, 2-2006),
- Logisch Ontwerp GBA versie 3.6 (11-2007) en concept-versie 3.7 v.w.b. de relatie GBA – BAG,
- Programma van eisen Handelsregister (HR; EZ, 6-2008 versie. 1.6) en de Gegevenscatalogus Nieuw HandelsRegister (concept; VVKvK, 7-2008),
- Catalogus BasisRegistratie Kadaster (BRK; Kadaster, 3-2009 versie. 1.0.4),
- Catalogus Basisregistratie WOZ (BRWOZ; Waarderingskamer, 4-2008, versie 1.3)
en in aanvulling hierop het
- GFO Basisgegevens (VNG, 1998).
De basisregistratie Topografie is niet in het referentiemodel opgenomen. We zijn uitgegaan van grootschalige geo-objecten, met andere woorden de toekomstige Basisregistratie Grootschalige Topografie. Daarvoor gebruikten we het document:
- Informatiemodel Geografie (concept IMGeo; Geonovum v/h Ravi, 3-2007 vs. 2.0).
Het model richt zich vooral op basisregistraties uit de eerste tranche van de inrichting van het stelsel. Pas wanneer er voldoende bekend is over een andere basisregistratie (tweede tranche en verder) wordt het model uitgebreid en aangepast.
Het Referentiemodel Stelsel van Gemeentelijke Basisgegevens is onderdeel van de GEMmeentelijke Model Architectuur (GEMMA) van KING. De inhoud is in lijn met de Nederlandse OverheidsReferentieArchitectuur (NORA).

## 1.3 Invoering
Toepassing van het referentiemodel heeft consequenties voor de gemeentelijke organisatie, haar processen, informatievoorziening, gegevenshuishouding en automatisering. Elke gemeente is autonoom in haar keuzes daarin en KING faciliteert de toepassing waar mogelijk. Het tempo van de invoering is vooral afhankelijk van het verwerken van het referentiemodel in de software die gemeenten gebruiken bij de uitvoering van hun taken.
De software die gemeenten op dit moment gebruiken is vaak (mede) gebaseerd op het eerder genoemde GFO-Basisgegevens. In de jaren 2009 – 2010 passen leveranciers naar verwachting hun software aan op de in te voeren basisregistraties. Dit betekent (ook) een overgang van het GFO-BG naar dit referentiemodel. Om die te ondersteunen, brengt KING tegelijkertijd met het RSGB 2.0 een nieuwe versie van de berichtenstandaard StUF-BG uit. Tijdens deze periode – en mogelijkerwijs langer – bestaat er een StUF-BG-versie op basis van het GFO-Basisgegevens (2.04) en een versie op basis van dit referentiemodel (3.10), waardoor een geleidelijke overgang mogelijk is. KING adviseert gemeenten om bij verdere ontwikkeling van hun informatievoorziening te anticiperen op deze overgang. Ze kunnen dan maatregelen treffen om er voor te zorgen dat in de overgangsperiode hun informatievoorziening overweg kan met beide versies van StUF.


**Méér dan de landelijke basisregistraties**
Het referentiemodel is een vertaling en een uitbreiding van het landelijk stelsel van basisregistraties met het oog op de gemeentelijke informatiebehoefte. Op onderdelen verschilt het dan ook van het landelijk stelsel. Wel zijn de landelijke basisregistraties bijna volledig opgenomen in het referentiemodel. KING raadt gemeenten dringend aan om bij de ontwikkeling van hun informatievoorziening uit te gaan van het referentiemodel en niet alleen van één, of meer, catalogi van landelijke basisregistraties. Op die manier sluiten zij aan bij het landelijk stelsel én kunnen zij hun eigen informatievoorziening optimaal faciliteren. Daarnaast gaat KING er van uit dat de leveranciers van gemeentelijke software niet alleen anticiperen op de landelijke basisregistraties maar ook het referentiemodel en de daarop gebaseerde versie van StUF-BG in de software verwerken.

---

# 2. Objectenmodel


In dit hoofdstuk bakenen we allereerst het stelsel van gemeentelijke basisgegevens af (paragraaf 2.1). We lichten het referentiemodel toe op basis van de objecttypen en hun relaties (paragraaf 2.3). We besteden ook bijzondere aandacht aan de doelen van dit stelsel (paragraaf 2.2) en aan de metagegevens (paragraaf 2.4). Het stelsel schetsen we in de nevenstaande figuur.

![#Schets van het stelsel](media/Schets_Stelsel.png)

## 2.1 Afbakening

Het stelsel van gemeentelijke basisgegevens is geen basisregistratie zoals bedoeld in het (landelijke) stelsel van basisregistraties. Het is de vertaling van dit stelsel naar de gemeentelijke informatievoorziening. Hierin is nadrukkelijk behoefte aan samenhang tussen de objecten en gegevens uit die basisregistraties èn behoefte aan specifieke gemeentelijke basisgegevens. Het RSGB is dan ook meer dan de optelsom van de landelijke basisregistraties. Dit is hieronder gevisualiseerd. Ook ondersteunt de gemeentelijke informatievoorziening diverse taakgebieden en bestaan er uiteenlopende informatiebehoeften. Voor sommige taakgebieden is, of wordt dit uitgewerkt in specifieke informatiemodellen. Deze zijn gerelateerd aan het stelsel van gemeentelijke basisgegevens doordat zij, waar dat zinvol is, een deel van deze objecten en gegevens bevatten.
Het kan voorkomen dat dergelijke taakspecifieke modellen ook zijn gebaseerd op gegevensuitwisseling met niet-gemeentelijke ketenpartners, die op hun beurt weer andere sectormodellen toepassen. De specificaties daarin zouden kunnen afwijken van die in dit referentiemodel. Om dat te voorkomen, lijkt het wenselijk om objecten en gegevens waarvoor dit geldt en die uitgewisseld worden tussen sectoren, op te nemen (en te specificeren) in het landelijk stelsel van basisregistraties. Door deze (gewijzigde) specificaties over te nemen in het referentiemodel ontstaat er weer harmonie tussen de informatiemodellen op de diverse niveaus en binnen de verschillende sectoren.

![](media/RSGB_Afbakening.png)



## 2.2 Doelen
**Samenvatting:**  
Het RSGB moet zorgen voor:  
- eenduidig onderhoud van basisgegevens  
- uitwisselbaarheid via StUF‑BG  
- aansluiting op landelijke basisregistraties  
Het is een logisch gegevensmodel, geen databaseontwerp.

## 2.3 Toelichting
**Samenvatting:**  
Het RSGB beschrijft objecttypen, relaties en generalisaties. Het volgt landelijke modellen maar voegt gemeentelijke objecttypen toe zoals GEMEENTE, WIJK, BUURT, OVERIG GEBOUWD OBJECT en OVERIG TERREIN.

### Tekenwijze
**Samenvatting:**  
Objecttypen worden weergegeven met rechthoeken, generalisaties met vet kader, en relaties met 1:1, 1:N of N:M notatie.

### Basisregistratie‑objecten
**Samenvatting:**  
Het RSGB bevat objecttypen uit BAG, BRP, NHR, BRK, WOZ en IMGeo. Gemeenten voegen aanvullende objecttypen toe voor hun eigen processen.

### Topografie
**Samenvatting:**  
IMGeo‑objecten zoals WEGDEEL, WATERDEEL, TERREINDEEL en KUNSTWERKDEEL worden opgenomen als zelfstandige geo‑objecten.

### Kadaster
**Samenvatting:**  
Kadastrale objecten worden gemodelleerd als KADASTRALE ONROERENDE ZAAK, opgebouwd uit KADASTRAAL PERCEEL en APPARTEMENTSRECHT.

### WOZ
**Samenvatting:**  
Het WOZ‑object staat centraal en is gekoppeld aan kadastrale objecten, WOZ‑belangen en WOZ‑waarden.

---

# 2.4 Opbouw

## 2.4.1 Metagegevens
**Samenvatting:**  
Metagegevens beschrijven betekenis, herkomst, historie en kwaliteit van gegevens.  
> “De gebruiker weet nu dat het woonadres van Cornelis Steenmans wellicht niet juist is.”

## 2.4.2 Historie
**Samenvatting:**  
Het RSGB volgt materiële en formele historie. Beide zijn nodig voor juridische reconstructie.

## 2.4.3 Afleidbare gegevens
**Samenvatting:**  
Sommige gegevens worden expliciet opgenomen omdat ze moeilijk afleidbaar zijn, zoals datum vestiging in Nederland.

## 2.4.4 Domeinwaarden of tabel
**Samenvatting:**  
Domeinwaarden worden bij attributen opgenomen, tenzij ze dynamisch zijn (zoals LAND).

---

# Bijlage 1: Relatie tot GFO Basisgegevens
**Samenvatting:**  
Vergelijking tussen RSGB en GFO‑BG. Veel objecttypen zijn herzien, vervallen of uitgebreid. Tabellen tonen per gegevensgroep hoe deze in het RSGB zijn opgenomen.

