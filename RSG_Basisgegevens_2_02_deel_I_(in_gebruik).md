# Referentiemodel Stelsel van Gemeentelijke Basisgegevens (RSGB)

Versie 2.02 — Deel I: Beschrijving  
Onderdeel van de GEMeentelijke Model Architectuur (GEMMA)


# Voorwoord

Het Referentiemodel Stelsel van Gemeentelijke Basisgegevens (RSGB) heeft zijn oorsprong in het streven dat burgers en bedrijven hun gegevens maar één keer aan de overheid hoeven te verstrekken. De landelijke basisregistraties maken het mogelijk dat de overheid die gegevens daarna meervoudig gebruikt. Voor gemeenten was het daarbij van belang om vanuit gemeentelijk perspectief in beeld te brengen hoe het stelsel van basisgegevens samenhangt. Daarnaast was er behoefte om ook gemeentespecifieke gegevens die zich lenen voor hergebruik eenduidig te beschrijven. Daaruit komt het principe voort dat in het RSGB alleen gegevens worden opgenomen die geschikt zijn voor meervoudig gebruik.

Versie 1.0 van het RSGB is medio 2007 gepubliceerd door het toenmalige EGEM, als vervanging van het GFO-Basisgegevens van de VNG. In het voorjaar van 2008 is met versie 1.1 het toepassingsgebied uitgebreid met de Basisregistratie WOZ (Waardering Onroerende Zaken). Voortschrijdend inzicht, de eerste ervaringen met het RSGB, ontwikkelingen in de (catalogi van de) landelijke basisregistraties en de ontwikkeling van de berichtenstandaard StUF-BG leidden tot versie 2.0. Die versie is in mei 2009 vastgesteld door de StUF-regiegroep. Per 1 januari 2010 is het beheer van het RSGB overgegaan naar het Kwaliteitsinstituut Nederlandse Gemeenten (KING). In april 2010 bracht KING versie 2.01 uit, met aanpassingen naar aanleiding van de catalogus BAG (versie 2009) en het Logisch Ontwerp GBA (versie 3.7). Per 1 januari 2017 is KING opgegaan in VNG Realisatie, dat sindsdien verantwoordelijk is voor het beheer van het RSGB. In april 2018 is via de beheerprocedure, op verzoek van de StUF-expertgroep, een patch doorgevoerd voor de modellering van niet-natuurlijke personen. Daarmee ontstond versie 2.02, de laatst vastgestelde versie van het RSGB.

Het RSGB ondersteunt gemeenten bij het stroomlijnen van hun gegevenshuishouding en van de processen voor beheer en gebruik van basisgegevens. Het vormt bovendien de basis voor standaarden voor gegevensuitwisseling, zodat gemeenten een samenhangende informatievoorziening kunnen inrichten.

Dit document beschrijft de volgende versie van het RSGB. Eerder is een initiatief gestart om tot een nieuwe versie te komen, maar dat heeft nooit tot vaststelling geleid. Die versie werd informeel aangeduid als versie 3.02. Om verwarring te voorkomen heeft de versie die nu tot stand komt het nummer 3.1 gekregen.

## Beheer

Het beheer van het RSGB ligt bij VNG Realisatie. Commentaar op deze versie en wijzigingsverzoeken worden meegenomen in de reguliere beheerprocedure van het RSGB. Iedere belangstellende kan een wijzigingsverzoek indienen. Wijzigingsverzoeken worden beoordeeld door specialisten van VNG Realisatie en ter advisering voorgelegd aan werkgroepen met een publiek-private samenstelling. Voor vragen, suggesties of opmerkingen kunt u contact opnemen via [contactpunt / link naar de GitHub-repository].


# Leeswijzer
 
Dit document richt zich op iedereen die beroepsmatig betrokken is bij het structureren van de gemeentelijke informatievoorziening, het inrichten en beheren van basisregistraties en het tot stand brengen en beheren van gegevensuitwisseling.

Het RSGB 3.1 is opgesteld als een conceptueel informatiemodel conform het Metamodel Informatiemodellering (MIM) versie 1.2. Het model beschrijft welke objecten en gegevens voor gemeenten van belang zijn, wat ze betekenen en hoe ze samenhangen. Het model is implementatieneutraal: het schrijft geen database-, berichten- of API-ontwerp voor. Logische en technische modellen, zoals API-specificaties of datastructuren, kunnen erop worden gebaseerd.

De documentatie wordt gepubliceerd volgens de ReSpec-standaard, als één online document met doorklikbare verwijzingen tussen de onderdelen. De opdeling in een deel I (beschrijving) en een deel II (specificaties), zoals in eerdere versies, is daarmee vervallen. Het document is als volgt opgebouwd:

-   Hoofdstuk Inleiding: de achtergrond van het RSGB, de afbakening ten opzichte van de landelijke basisregistraties en de doelen van het model.
-   Hoofdstuk Uitgangspunten en modelleerprincipes: de keuzes die bij het opstellen van het model zijn gemaakt. Bijvoorbeeld dat alleen gegevens worden opgenomen die geschikt zijn voor meervoudig gebruik, hoe gegevens uit basisregistraties worden opgenomen of waarnaar wordt verwezen, en hoe wordt omgegaan met historie, afgeleide gegevens en waardelijsten.
-   Hoofdstuk Het informatiemodel op hoofdlijnen: een overzicht van het model aan de hand van diagrammen per domein, zoals personen, adressen en gebouwen, kadaster, WOZ en ondernemingen, met een toelichting op de samenhang.
-   Hoofdstuk Gegevensdefinities: de specificaties van alle modelelementen volgens MIM. Dat zijn objecttypen, attribuutsoorten, relatiesoorten, gegevensgroepen, keuzes, datatypen, enumeraties en waardelijsten. Per element zijn de MIM-metagegevens opgenomen, zoals naam, definitie, herkomst, kardinaliteit, indicatie materiële en formele historie en indicatie authentiek. Dit hoofdstuk is vooral bedoeld als naslagwerk.
-   Bijlage Wijzigingen ten opzichte van RSGB 2.02: een overzicht van de doorgevoerde wijzigingen, met verwijzing naar de bijbehorende wijzigingsverzoeken.
-   Bijlage Relatie met de landelijke basisregistraties: per basisregistratie (zoals de BRP, de BAG en de BRK) hoe de gegevens in het RSGB zijn opgenomen of waarnaar wordt verwezen.

Het UML-model waaruit deze documentatie is gegenereerd, de wijzigingsverzoeken en eerdere versies zijn te vinden op [link naar de GitHub-repository].


---

# Samenvatting
De invoering van een overheidsbreed stelsel van basisregistraties is één van de meest ingrijpende ontwikkelingen waarmee gemeenten te maken hebben. Het Referentiemodel Stelsel van Gemeentelijke Basisgegevens (RSGB) biedt gemeenten en hun leveranciers houvast bij het invoeren en het gebruiken van deze gegevens.
Dit objectenmodel voor de gemeentelijke basisgegevens presenteert de samenhang tussen basisregistraties op een logische wijze. Maar gemeenten hebben meer gegevens nodig voor hun werkprocessen dan nu in de landelijke basisregistraties beschikbaar zijn. Het binnengemeentelijk stelsel is dan ook ‘rijker’ dan het landelijke stelsel.
Dit referentiemodel is onderdeel van de GEMmeentelijke Model Architectuur (GEMMA), gepubliceerd door de VNG. De inhoud is in lijn met de Nederlandse OverheidsReferentieArchitectuur (NORA).

![#Stelsel van Gemeentelijke Basisgegevens op hoofdlijnen](Images/RSGB_op_hoofdlijnen.png)

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
Het stelsel van basisregistraties is een van de pijlers van de gegevenshuishouding van de overheid. Onder het motto “De overheid vraagt niet naar de bekende weg” is wettelijk vastgelegd dat burgers en bedrijven hun basisgegevens maar één keer aan de overheid hoeven te verstrekken, en dat overheidsorganisaties verplicht zijn deze gegevens te gebruiken.

Voor gemeenten zijn de basisregistraties extra belangrijk, omdat zij niet alleen gebruiker zijn, maar ook bronhouder van onder meer de Basisregistratie Personen en de Basisregistratie Adressen en Gebouwen. Tegelijk vormen de basisgegevens maar een klein deel van de gegevens die gemeenten nodig hebben om hun taken uit te voeren. Het RSGB brengt de samenhang tussen de basisregistraties vanuit gemeentelijk perspectief in beeld. Het vult deze aan met gemeentelijke gegevens die geschikt zijn voor meervoudig gebruik. Het voorwoord beschrijft hoe het RSGB zich sinds 2007 heeft ontwikkeld.

Sinds de laatst vastgestelde versie, RSGB 2.02, zijn zowel de landelijke basisregistraties als de manier van informatiemodelleren sterk veranderd. Het Logisch Ontwerp BRP en de BAG 2.0 zijn bijvoorbeeld vernieuwd, en met MIM is een landelijke standaard voor informatiemodellen ontstaan. RSGB 3.1 brengt het model weer in lijn met de actuele basisregistraties en legt het vast als conceptueel informatiemodel conform MIM 1.2.

## 1.2 Opzet
VNG Realisatie biedt met het RSGB een standaard die het gebruik van basisgegevens binnen gemeenten en daarmee samenwerkende organisaties bevordert. Binnen gemeenten spreken we over één samenhangend stelsel van basisgegevens en niet over een basisregistratie; die laatste term is gereserveerd voor de landelijke basisregistraties. Het landelijke stelsel vormt wel het uitgangspunt voor het gemeentelijke model.

Vertrekpunt voor deze versie is RSGB 2.02 (vng-realisatie.github.io/RSGB). Deze versie is in lijn gebracht met de volgende informatiemodellen en catalogi van de landelijke basisregistraties:

Basisregistratie Personen (BRP): Logisch Ontwerp BRP, versie 2026.Q3, Rijksdienst voor Identiteitsgegevens. Gepubliceerd op rvig.nl.
Basisregistratie Adressen en Gebouwen (BAG): Catalogus BAG 2018 met het informatiemodel IMBAG 2.0, Ministerie van BZK en Kadaster. Gepubliceerd op imbag.github.io/catalogus.
Handelsregister (HR): Gegevenscatalogus Handelsregister, versie 3.0.4, KVK. Gepubliceerd op kvk.nl.
Basisregistratie Kadaster (BRK): Catalogus Basisregistratie Kadaster, versie 2.3 (30 januari2020), Kadaster. Gepubliceerd op kadaster.nl.
Basisregistratie WOZ: Catalogus Basisregistratie WOZ, versie 1.8, Waarderingskamer. Gepubliceerd op waarderingskamer.nl.
Basisregistratie Grootschalige Topografie (BGT) en IMGeo: Gegevenscatalogus BGT versie 1.2 en Gegevenscatalogus IMGeo, versie 2.2, Geonovum. Gepubliceerd op docs.geostandaarden.nl/imgeo/catalogus/bgt en docs.geostandaarden.nl/imgeo/catalogus/imgeo.

Het model is opgesteld volgens het Metamodel Informatiemodellering (MIM), versie 1.2 (docs.geostandaarden.nl/mim/mim).

Andere basisregistraties zijn niet in het RSGB opgenomen. Het model wordt alleen uitgebreid als er een aantoonbare gemeentelijke behoefte is aan meervoudig gebruik van gegevens uit die registraties.

Het RSGB is onderdeel van de Gemeentelijke Model Architectuur (GEMMA), die wordt beheerd door VNG Realisatie (gemmaonline.nl). De inhoud is in lijn met de Nederlandse Overheid Referentie Architectuur (NORA, noraonline.nl).

**Méér dan de landelijke basisregistraties**
Het referentiemodel is een weergave en een uitbreiding van het landelijk stelsel van basisregistraties met het oog op de gemeentelijke informatiebehoefte. Op onderdelen zijn er uitbreidingen vanuit gemeentelijk pesrspectief gedaan. verschilt het dan ook van het landelijk stelsel. Wel zijn de landelijke basisregistraties bijna volledig opgenomen in het referentiemodel. KING raadt gemeenten dringend aan om bij de ontwikkeling van hun informatievoorziening uit te gaan van het referentiemodel en niet alleen van één, of meer, catalogi van landelijke basisregistraties. Op die manier sluiten zij aan bij het landelijk stelsel én kunnen zij hun eigen informatievoorziening optimaal faciliteren. Daarnaast gaat KING er van uit dat de leveranciers van gemeentelijke software niet alleen anticiperen op de landelijke basisregistraties maar ook het referentiemodel en de daarop gebaseerde versie van StUF-BG in de software verwerken.

## 1.3 Relatie met het landelijk stelsel van basisregistraties

Het RSGB vertaalt het landelijk stelsel van basisregistraties naar de gemeentelijke informatiebehoefte en breidt het daarvoor uit. Uitgangspunt is dat het RSGB de informatiemodellen van de basisregistraties volledig volgt. Het RSGB neemt geen objecttypen uit die informatiemodellen over, maar verwijst ernaar. De definities, attribuutsoorten en relatiesoorten van bijvoorbeeld een verblijfsobject of een kadastraal onroerende zaak blijven daardoor eenduidig belegd bij de basisregistratie die er de bron van is. Wijzigingen in een basisregistratie leiden zo niet langer tot afwijkingen tussen het RSGB en die basisregistratie.

Voor de aansluiting tussen het RSGB en de basisregistraties maakt het RSGB gebruik van grensobjecten,. Deze wijze van modelleren is eerde onderzocht binnen VNGRealisatie en toegepast in het POC-informatiemodel "Klantinteracties". Een grensobject is een objecttype in het RSGB dat verwijst naar een objecttype in een basisregistratie. Het is de plek waar de gemeentelijke informatiebehoefte samenkomt met het landelijk stelsel. Soms hebben gemeenten behoefte aan attribuutsoorten bij zo’n objecttype die de basisregistratie niet registreert, maar die wel relevant zijn voor gemeenten en geschikt voor hergebruik. Die attribuutsoorten worden in het grensobject opgenomen, en niet in een kopie van het objecttype uit de basisregistratie. Zo blijft altijd zichtbaar welke gegevens uit de basisregistratie afkomstig zijn en welke gegevens gemeentelijk zijn.

VNG Realisatie raadt gemeenten dringend aan om bij de ontwikkeling van hun informatievoorziening uit te gaan van het RSGB en niet alleen van één of meer informatiemodellen van landelijke basisregistraties. Zo sluiten zij aan bij het landelijk stelsel en kunnen zij tegelijk hun eigen informatievoorziening optimaal inrichten. Daarnaast gaat VNG Realisatie ervan uit dat leveranciers van gemeentelijke software niet alleen de landelijke basisregistraties ondersteunen, maar ook het RSGB en de daarop gebaseerde standaarden voor gegevensuitwisseling.

# Objectenmodel


In dit hoofdstuk bakenen we allereerst het stelsel van gemeentelijke basisgegevens af (paragraaf 2.1). We lichten het referentiemodel toe op basis van de objecttypen en hun relaties (paragraaf 2.3). We besteden ook bijzondere aandacht aan de doelen van dit stelsel (paragraaf 2.2) en aan de metagegevens (paragraaf 2.4). Het stelsel schetsen we in de nevenstaande figuur.

![#Schets van het stelsel](media/Schets_Stelsel.png)

## Afbakening

Het stelsel van gemeentelijke basisgegevens is geen basisregistratie zoals bedoeld in het (landelijke) stelsel van basisregistraties. Het is de vertaling van dit stelsel naar de gemeentelijke informatievoorziening. Hierin is nadrukkelijk behoefte aan samenhang tussen de objecten en gegevens uit die basisregistraties èn behoefte aan specifieke gemeentelijke basisgegevens. Het RSGB is dan ook meer dan de optelsom van de landelijke basisregistraties. Dit is hieronder gevisualiseerd. Ook ondersteunt de gemeentelijke informatievoorziening diverse taakgebieden en bestaan er uiteenlopende informatiebehoeften. Voor sommige taakgebieden is, of wordt dit uitgewerkt in specifieke informatiemodellen. Deze zijn gerelateerd aan het stelsel van gemeentelijke basisgegevens doordat zij, waar dat zinvol is, een deel van deze objecten en gegevens bevatten.
Het kan voorkomen dat dergelijke taakspecifieke modellen ook zijn gebaseerd op gegevensuitwisseling met niet-gemeentelijke ketenpartners, die op hun beurt weer andere sectormodellen toepassen. De specificaties daarin zouden kunnen afwijken van die in dit referentiemodel. Om dat te voorkomen, lijkt het wenselijk om objecten en gegevens waarvoor dit geldt en die uitgewisseld worden tussen sectoren, op te nemen (en te specificeren) in het landelijk stelsel van basisregistraties. Door deze (gewijzigde) specificaties over te nemen in het referentiemodel ontstaat er weer harmonie tussen de informatiemodellen op de diverse niveaus en binnen de verschillende sectoren.

![](media/RSGB_Afbakening.png)



## Doelen
De gemeentelijke gegevenshuishouding omvat een diversiteit aan objecten, gegevens daarvan en relaties daartussen. In de praktijk mondt dit uit in een groot aantal eilanden met eigen specificaties die uitwisseling, koppeling, meervoudig en ‘gemeentebreed’ gebruik van gegevens belemmeren. Eenduidigheid is daarom dringend gewenst. De kern hiervan zijn de gemeentelijke basisgegevens. Dit referentiemodel specificeert het objecten- of gegevensmodel van deze basisgegevens. Dat is in 1998 gebeurd in het GFO-Basisgegevens. Het RSGB kunt u beschouwen als een herziening daarvan op basis van hedendaagse inzichten, met name de komst van het landelijk stelsel van basisregistraties.
Het RSGB wil eraan bijdragen dat gemeenten en daarmee samenwerkende organisaties de kern van hun gegevenshuishouding, de basisgegevens, eenmalig onderhouden en meervoudig gebruiken. De achterliggende doelen zijn:
- het eenduidig onderhouden van basisgegevens door gemeenten;
- uitwisseling van basisgegevens mogelijk te maken, door leveranciers hun software daarop te laten baseren; en
- het waarborgen van het uitwisselen met, en het benutten van, het landelijk stelsel van basisregistraties.

**Houvast**
Dit gegevensmodel vormt geen grondslag voor een (relationele) database. Het staat partijen – gemeenten, leveranciers – vrij om een eigen technische realisatievorm te kiezen. Die kan bijvoorbeeld bestaan uit meerdere databases. De essentie van het referentiemodel is vooral om eenduidig aan te geven welke gegevens kunnen worden ontleend aan het Stelsel van Gemeentelijke Basisgegevens: welke informatievragen kunt u stellen die ook kunnen worden beantwoord? Denk bijvoorbeeld aan ruimtelijke relaties tussen objecten. Uit het model kunt u afleiden over welke ruimtelijke relaties u informatie kunt krijgen, ongeacht of deze relaties administratief zijn vastgelegd, of gegenereerd worden met behulp van GIS-analysetechnieken.
Veel informatievragen zullen voortkomen uit softwarecomponenten die bepaalde taken van de gemeente ondersteunen, en aan softwarecomponenten die delen van het stelsel ondersteunen. Om deze componenten te kunnen laten samenwerken, hebben we het referentiemodel uitgewerkt in een nieuwe versie van de berichtenstandaard StUF-BG, waarin we services of berichten definiëren.
Ten slotte biedt het referentiemodel gemeenten houvast als zij zelf databases en software willen ontwikkelen en helpt het hen bij het selecteren van softwarecomponenten en databases van leveranciers. Het is raadzaam om aan – potentiële – leveranciers steeds te vragen of zij hun database baseren op het referentiemodel en of zij de berichten ondersteunen die op basis van het referentiemodel zijn gespecificeerd.

## 2.3 Toelichting
In deze paragraaf lichten we het objectenmodel toe. Het model op hoofdlijnen is weergegeven in de samenvatting. Het is gebaseerd op de modellen van de diverse basisregistraties. We wijken niet af van deze modellen, maar in sommige gevallen zijn we gedetailleerder of hebben 10
we bepaalde gegevens niet overgenomen. Verder hebben we de modellen aangevuld en met elkaar verbonden, om te kunnen voldoen aan de gemeentelijke behoefte aan basisgegevens. We modelleren alleen de actuele situatie. De behoefte aan historie specificeren we met de desbetreffende metagegevens.

**Tekenwijze**
We brengen een objecttype in beeld met een rechthoek. De naam van het objecttype is in de rechthoek vermeld. In een oranje vlak staan de objecttypen die deel uitmaken van enige (catalogus van een) basisregistratie (A). KING heeft de andere objecttypen toegevoegd. Een witte rechthoek visualiseert een objecttype dat uit meerdere andere objecttypen is samengesteld. Dit is een zogenaamde generalisatie van objecttypen. Laatstgenoemde objecttypen zijn op hun beurt specialisaties van het gegeneraliseerde objecttype. Een gegeneraliseerd objecttype heeft een ‘vet’ kader (C) als één of meer van de specialisaties daarvan deel uitmaken van enige (catalogus van een) basisregistratie. In een blauw vlak staan de objecttypen die geen generalisaties zijn van andere objecttypen en geen deel uitmaken van enige (catalogus van een) basisregistratie (B).

![](media/Tekenwijze.png)

Tussen de objecttypen brengen we de drie soorten relaties als volgt in beeld: een 1:1-relatie (een lijn), een 1:N-relatie (een lijn met één ‘harkje’) en een N:M-relatie (een lijn met twee ‘harkjes’). Een relatie die deel uitmaakt van enige (catalogus van een) basisregistratie is ‘vetter’ gevisualiseerd dan relaties waarvoor dit niet geldt: de relaties die KING heeft toegevoegd. Een relatie veronderstelt dat een object van het ene objecttype altijd gerelateerd is aan dat van het andere objecttype. Wanneer dit niet het geval hoeft te zijn, dan ziet u dat aan het open rondje aan het uiteinde van de relatie(lijn). In het voorbeeld: een object van objecttype B is altijd gerelateerd aan een object van objecttype A, maar andersom hoeft dat niet het geval te zijn. Met een of-of-relatie tenslotte bedoelen we dat een object van – in dit geval – objecttype C een relatie kent met een object van één van beide gerelateerde objecttypen, hier objecttype A of B.

**Basisregistratie-objecten**
De volgende objectenmodellen vormen de kern van het objectenmodel: de Basisregistraties van Adressen en Gebouwen (de BAG: BRA en BGR), de Basisregistratie Personen (GBA en RNI), de Basisregistratie Ondernemingen en Rechtspersonen (het NHR oftewel Nieuw Handelsregister), de Basisregistratie Kadaster (de BRK), de BasisRegistratie WOZ (de BRWOZ) en de Basisregistratie Grootschalige Topografie (GBKN) cq. het Informatiemodel Geografie (IMGeo).
Het gaat om de objecttypen: WOONPLAATS, OPENBARE RUIMTE, NUMMERAANDUIDING (onderdeel van ADRESEERBAAR OBJECT AANDUIDING), VERBLIJFSOBJECT (onderdeel van GEBOUWD OBJECT), STANDPLAATS, LIGPLAATS (beide onderdeel van BENOEMD TERREIN), PAND, INGEZETENE (PERSOON in BRP-termen, hier onderdeel van NATUURLIJK PERSOON), INGESCHREVEN NIET-NATUURLIJK PERSOON (onderdeel van 11
OBJECTTYPE BOBJECTTYPE A1:N-relatieniet altijd voor-komende relatieTekensymboliekobjecttype van basisregistratieobjecttype niet in landelijke basisregistratiealtijd voorko-mende relatieOBJECTTYPE Cgeneralisatie ('groep') van meer objecttypen;1 of meer van laatstgenoemde objecttypen maakt deel uit van een basisregistratieof-of-relatieN:M-relatie
NIET-NATUURLIJK PERSOON), MAATSCHAPPELIJKE ACTIVITEIT, VESTIGING, KADASTRALE ONROERENDE ZAAK, ZAKELIJK RECHT, WOZ-OBJECT, WOZ-BELANG, WOZ-WAARDE en de geo-objecttypen: WEGDEEL, WATERDEEL, TERREINDEEL, SPOORBAANDEEL, KUNSTWERKDEEL en INRICHTINGSELEMENT.

**Adressen, gebouwen en terreinen**
KING heeft de GEMEENTE als objecttype toegevoegd, omdat zij het bestuurlijke gebied is waarbinnen de betreffende ruimtelijke objecten liggen.
Binnen een gemeente bevinden zich één of meer WOONPLAATSen, maar een woonplaats bevindt zich altijd binnen één gemeente.
Binnen elke woonplaats bevinden zich één of meer OPENBARE RUIMTEn die in de BAG zijn gedefinieerd. Aangezien een openbare ruimte, zoals een straat, zich kan uitstrekken over meerdere woonplaatsen is GEMEENTELIJKE OPENBARE RUIMTE toegevoegd. De OPENBARE RUIMTE is nu dát deel van de gemeentelijke openbare ruimte dat zich binnen één woonplaats bevindt.
De CBS-indeling in WIJKen en BUURTen hebben we eveneens toegevoegd. De geometrie is één van de te registreren gegevens. Een belangrijk voordeel hiervan is dat managementinformatie geografisch in beeld gebracht kan worden.
Aan een OPENBARE RUIMTE kunnen ADRESSEERBARE OBJECT AANDUIDINGen gerelateerd zijn. In de meeste gevallen gaat het om NUMMERAANDUIDINGen die de BAG onderscheidt. Soms is het noodzakelijk om ook andere adressen vast te stellen, bijvoorbeeld van terreinen die geen stand- en ligplaatsen zijn en eventueel van gebouwen die geen
verblijfsobjecten zijn. Een dergelijke OVERIGE ADRESSEERBAAR OBJECT AANDUIDING wordt weliswaar officieel vastgesteld, maar maakt geen deel uit van de BAG.
De BGR onderscheidt gebouwde objecten als VERBLIJFSOBJECTen en terreinen als STAND- en LIGPLAATSen. In het RSGB hebben we voor het onderscheid in gebouwen (GEBOUWD OBJECT) en terreinen (BENOEMD TERREIN) gekozen. Met de verblijfsobjecten wordt immers niet de hele gebouwde omgeving, voor zover zinvol, gemodelleerd. Vandaar dat we het OVERIG GEBOUWD OBJECT hebben toegevoegd. Dit geeft, in combinatie met de verblijfsobjecten, gemeenten de mogelijkheid om het deel van de gebouwde omgeving dat zij relevant vinden adequaat te registreren. Een OVERIG GEBOUWD OBJECT kan op één van drie manieren een adres krijgen:
- door gebruik te maken van een ‘BAG-adres’ (NUMMERAANDUIDING), aangevuld met een locatieomschrijving;
- door een officieel adres vast te stellen dat niet in de BAG wordt geregistreerd (OVERIGE ADRESSEERBAAR OBJECTAANDUIDING);
- door de ligging ten opzichte van een OPENBARE RUIMTE aan te geven met een locatieomschrijving.
Gemeenten hebben de behoefte om naast stand- en ligplaatsen ook andere afgebakende terreinen te registreren en een officieel (niet-authentiek) adres te geven. Hiervoor hebben we het OVERIG TERREIN toegevoegd. In combinatie met de stand- en ligplaatsen kunnen gemeenten dan alle terreinen registreren waaraan zij een officieel adres willen toekennen.
VERBLIJFSOBJECT, STANDPLAATS en LIGPLAATS hebben we gegeneraliseerd naar ADRESSEERBAAR OBJECT teneinde aan te sluiten bij de terminologie van de BAG. GEBOUWD OBJECT en BENOEMD TERREIN hebben we gegeneraliseerd naar BENOEMD OBJECT omdat veel relaties de groepering van al deze objecttypen betreffen.
VERBLIJFSOBJECTen maken deel uit van PANDen (gevisualiseerd met de ligt-in-relatie). Maar niet elk pand bevat verblijfsobjecten. Voor dergelijke panden hebben we een optionele relatie toegevoegd tussen PAND en BUURT om van de panden die niet aan VERBLIJFSOBJECTen worden gerelateerd, duidelijk te maken binnen welke buurt (en daarmee gemeente) zij vallen, bijvoorbeeld omdat een gemeente eigenaren van dergelijke panden wil aanschrijven. Overigens valt de relatie tussen een pand als bijgebouw van een verblijfsobject zijnde een hoofdgebouw af te leiden via de relaties van beide objecten met het WOZ-object.

![#Detaillering Adressen, Gebouwen en Terreinen](media/Detaillering_ADG.png)

**Topografie**
Een deel van de geschetste objecttypen heeft betrekking op fysieke ruimtelijke objecten of geo-objecten zoals VERBLIJFSOBJECT en PAND. De andere geo-objecten benoemen we hier onafhankelijk van elkaar, zoals hiernaast is geschetst.

![Topografie](media/Topografie.png)

Het RSGB bevat objecttypen uit BAG, BRP, NHR, BRK, WOZ en IMGeo. Gemeenten voegen aanvullende objecttypen toe voor hun eigen processen.

**Kadaster**
Het objectenmodel van het stelsel van basisregistraties kent een n:m-relatie tussen enerzijds onroerende zaken (onderdeel van de BasisRegistratie Kadaster) en anderzijds verblijfsobjecten en stand- en ligplaatsen. Een onroerende zaak is de groepering van kadastrale percelen, appartementsrechten en leidingnetwerk. Alleen de eerste twee zijn zodanig belangrijk voor de gemeentelijke informatievoorziening dat die in het referentiemodel zijn opgenomen. Het KADASTRAAL PERCEEL en het APPARTEMENTSRECHT vormen gezamenlijk de KADASTRALE ONROERENDE ZAAK. Om aan te sluiten bij de toegevoegde objecttypen (OVERIG GEBOUWD OBJECT en OVERIG TERREIN) hebben we de relatie met adresseerbare objecten vormgegeven als een verplichte relatie tussen BENOEMD OBJECT en KADASTRALE ONROERENDE ZAAK.
Verder hebben we een 1:n-relatie toegevoegd tussen kadastrale percelen onderling (‘ligt binnen’). Een geheel perceel beschikt over geometrie (de perceelgrens), voor deelpercelen is dit niet het geval. Door deze relatie is van deelpercelen vast te leggen bij welke gehele percelen zij qua ligging horen. Op analoge wijze hebben we van de BRK afgeleid de ‘liggings-relaties’ tussen appartementsrechten en kadastrale percelen (‘is ondergrond van …’) via de zgn. appartementscomplexen. Op deze wijze is van elke kadastrale onroerende zaak vast te leggen om welk deel van het gemeentelijk grondgebied het gaat. Tot slot hebben we de voornaamste zakelijk gerechtigde (een RECHTSPERSOON) van een KADASTRALE ONROERENDE ZAAK toegevoegd.
Het ZAKELIJK RECHT legt van elke kadastrale onroerende zaak vast welke RECHTSPERSOON (of RECHTSPERSOONen) daarop zakelijke rechten uitoefent.

![](media/Detaillering_KOZ.png)

**De WOZ**
Centraal in dit gedeelte van het obejctenmodel staat het WOZ-OBJECT zoals dat in de BRWOZ voorkomt. Dit heeft relaties naar de KADASTRALE ONROERENDE ZAAKen (percelen en appartementsrechten) die tot het WOZ-object behoren, naar de zgn. WOZ-BELANGen, naar de WOZ-WAARDEn en naar de WOZ-DEELOBJECTen waaruit het is samengesteld.
Het WOZ-DEELOBJECT betreft een element van een WOZ-OBJECT; meerdere WOZ-deelobjecten (bijvoorbeeld de woning, de losstaande schuur en de grond) vormen gezamenlijk een WOZ-object en/of onderbouwen de waarde ervan nader (bijvoorbeeld de waarde-invloed van bodemverontreiniging). Voor een WOZ-deelobject geldt telkens één van de volgende situaties:
het komt overeen met een benoemd object (gebouwd object, benoemd terrein) of is een gedeelte daarvan,
het komt overeen met een pand of is een gedeelte daarvan of
het is geen van beide, het WOZ-deelobject betreft geen gebouwd object, pand, benoemd terrein of gedeelte daarvan; een voorbeeld hiervan is een bouwkavel waarop nog geen bouwvergunning verleend is.
Het is bovendien zo dat een WOZ-deelobject nooit overeen kan komen met meer dan één (deel van een) benoemd object of pand. En, indien een WOZ-deelobject een relatie heeft met een pand, dan kan het alleen gaan om panden waarbinnen geen verblijfsobjecten afgebakend zijn, zoals garages en schuren bij woningen, en gedeelten van panden die niet afgebakend zijn als verblijfsobject, zoals een niet-afsluitbare parkeergarage onder een appartementencomplex.
Door middel van het objecttype WOZ-BELANG leggen we vast welk subject als belanghebbende eigenaar is aangewezen, welk subject als belanghebbende gebruiker is aangewezen en eventueel welke "derden" zich bekend maken als "medebelanghebbenden".
WOZ-objecten moeten voorzien kunnen worden van een voor de belanghebbende begrijpelijke aanduiding van de locatie waar het WOZ-object zich bevindt: de WOZ-object-aanduiding. In het gangbare spraakgebruik gaat het om een begrijpelijk adres voor het WOZ-object. Uitgangspunt van het RSGB is dat we voor de aanduiding van het WOZ-object gebruik maken van de adressen van de benoemde objecten waaraan het WOZ-object via zijn WOZ-deelobjecten is gerelateerd. Veelal is de WOZ-aanduiding eenduidig af te leiden uit deze relaties. Om ook in andere gevallen een WOZ-object van de aanduiding te kunnen voorzien, hebben we relatiesoorten toegevoegd van WOZ-OBJECT naar ADRESSEERBAAR OBJECT AANDUIDING en naar OPENBARE RUIMTE.

![]()

**Subjecten**
Het SUBJECT is de verzameling van RECHTSPERSOONen: NATUURLIJKe PERSOONen en NIET-NATUURLIJKe PERSOONen, en VESTIGINGen. Deze benamingen wijken af van de door SBG gehanteerde terminologie. Dit doen we om verwarring tussen de begrippen persoon en natuurlijke persoon in het spraakgebruik te voorkomen.
Natuurlijk persoon
Een NATUURLIJK PERSOON kan een INGESCHREVEN PERSOON zijn, of een ANDER NATUURLIJK PERSOON. En een ingeschreven persoon kan op zijn beurt weer een INGEZETENE of een NIET-INGEZETENE zijn. Een INGEZETENE is de persoon zoals de GBA die benoemd (als onderdeel van de BasisRegistratie Personen). De twee andere typen natuurlijke personen hebben we toegevoegd, omdat
ook deze personen van belang zijn voor het uitoefenen van de gemeentelijke taken. Met de niet-ingezetenen lopen we vooruit op de invoering van de Registratie Niet-Ingezetenen als onderdeel van de BasisRegistratie Personen. De combinatie met de ingezetenen omvat daarmee alle personen die woonachtig zijn in Nederland, of die in het buitenland wonen, maar zijn ingeschreven als (niet-)ingezetene. Alle andere personen die relevant zijn voor de gemeentelijke taakuitoefening wonen in het buitenland en hebben we als ANDER BUITENLANDS NATUURLIJK PERSOON gemodelleerd. We onderscheiden twee groepen relaties tussen ingeschreven personen: OUDER-KIND-RELATIE en HUWELIJK/GEREGISTREERDPARTNERSCHAP-RELATIE.
Een INGESCHREVEN PERSOON verblijft gewoonlijk in of op een ADRESSEERBAAR OBJECT (VERBLIJFSOBJECT, STAND- of LIGPLAATS). Is de verblijfsrelatie onbekend dan wordt de verblijfplaats, indien mogelijk, omschreven door een combinatie van de WOONPLAATS waarin de ingeschrevene verblijft met een zogenaamde nadere adresaanduiding. Is dit niet mogelijk dan resteert het registreren van een correspondentieadres of van een buitenlands adres, als de ingeschrevene in het buitenland verblijft. Aangezien een natuurlijk persoon zich kan inschrijven op een nevenadres wordt zijn of haar inschrijvingsadres bepaald door de relatie naar NUMMERAANDUIDING.
Het correspondentieadres hebben we toegevoegd aan NATUURLIJK PERSOON. Dit kan zijn een (relatie met een) OVERIGE ADRESSEERBAAR OBJECTAANDUIDING (een NUMMERAANDUIDING of ander officieel adres) of een postadres (postbus of antwoordnummer) dat zich in een WOONPLAATS bevindt.
Zowel correspondentie-adres als buitenlands adres gelden dus ook voor de ANDER BUITENLANDS NATUURLIJK PERSOON.
Eén of meer ingeschreven personen kunnen gezamenlijk een HUISHOUDEN vormen dat is gehuisvest in of op een ADRESSEERBAAR OBJECT. Daarin respectievelijk daarop kunnen zich meerdere HUISHOUDENs bevinden.



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
**CONCEPT !! **  
Het aspect tijd speelt een belangrijke rol in het gebruik van de informatie uit (basis)registraties. Afnemers hebben eigen rechtsprocedures en moeten kunnen herleiden wanneer attribuutwaarden als bekend mochten worden verondersteld. Als bijvoorbeeld besluiten ter discussie worden gesteld, is het juridisch van belang te achterhalen op basis van welke attribuutwaarden zo’n besluit genomen is. Als onjuiste attribuutwaarden zijn gebruikt, is het relevant te weten of de juiste attribuutwaarden tijdens de besluitvorming al bekend waren.

### Tijd lijnen
Er spelen twee tijdslijnen een rol bij het herleiden van attribuutwaarden:

-   Wanneer is iets gebeurd, in de werkelijkheid of volgens opgave (wanneer zijn de opgenomen gegevens geldig)? Dit valt binnen de tijdlijn van de aangehouden werkelijkheid (Tijdlijn Geldigheid)
-   Vanaf wanneer wist de overheid (als collectief van organisaties) dat de gegevens bekend waren? Dit valt binnen de tijdlijn van het administratieproces of de administratieve werkelijkheid (Tijdlijn Registratie).

In het MIM is bepaald dat middels indicaties wordt aangegeven of een tijdlijn al dat niet van toepassing is op een attribuutsoort of een realtiesoort. Het MIM definieert daarvoor de "indicatie tiujdlijn geldigheid" en "indicatie tijdlijn registratie". 
Bij het bepalen of er historie van toepassing is op attribuutsoorten volgen we de MIM methodiek. 

Het definieren van historie per attribuutsoort impliceert dat het gegevensmodel dat gebruikt moet worden voor de implementatie een 6NF model zou worden waarbij er per attribuutsoort waarvoor historie moet worden bijgehouden een aparte tabel wordt geïntroduceerd. Deze vorm van implementeren wordt weliswaar in innovatieve projecten beproefd, maar is niet de geadviseerde implementatievorm. 

Advies is om bij implementatie de historie bij  te houden op object-niveau of gegevens-groep niveau, voor zover dat object of die gegevensgoep attributen bevat waarvanhistorie moet worden bijgehouden. Dit betekent weliswaar dat er gegevens redundant opgeslagen worden als er een gegeven wijzigt waarvan de historie moet worden bijgehouden, maar deze benadering reduceert wel het aantal tabellen dat moet worden bijgehouden.



## 2.4.3 Afleidbare gegevens
**Samenvatting:**  


## 2.4.4 Domeinwaarden of tabel
**Samenvatting:**  
Domeinwaarden worden bij attributen opgenomen, tenzij ze dynamisch zijn (zoals LAND).

---

# Bijlage 1: Relatie tot GFO Basisgegevens
**Samenvatting:**  
Vergelijking tussen RSGB en GFO‑BG. Veel objecttypen zijn herzien, vervallen of uitgebreid. Tabellen tonen per gegevensgroep hoe deze in het RSGB zijn opgenomen.

# Bijlage 2: Design decisions bij het actualiseren.

| Datum     | Issue-nummer  |  Samenvatting beslissing    | 
| --------- | -------------- | --------------------------- | 
| 22-09-2026 | [#6](https://github.com/VNG-Realisatie/Actualisering-RSGB/issues/6) | Element  "69.10 Gemeente waar de PK zich bevindt" wordt niet opgenomen in het RSGB. |
| 27-10-2026 | [#29](https://github.com/VNG-Realisatie/Actualisering-RSGB/issues/29) | Element 88.20 "Omschrijving verdrag" wordt niet opgenomen in de het RSGB | 
| 27-10-2026 | [#30](https://github.com/VNG-Realisatie/Actualisering-RSGB/issues/30) | Indicatie Blokkering wordt uit het RSGB verwijderd en datum ingang blokkering PL wordt niet opgenomen in het RSGB.  |