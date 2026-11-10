# Leeswijzer (Nieuw in concept)
 
Dit document richt zich op iedereen die beroepsmatig betrokken is bij het structureren van de gemeentelijke informatievoorziening, het inrichten en beheren van basisregistraties en het tot stand brengen en beheren van gegevensuitwisseling.

Het RSGB 3.1 is opgesteld als een conceptueel informatiemodel conform het Metamodel Informatiemodellering (MIM) versie 1.2. Het model beschrijft welke objecten en gegevens voor gemeenten van belang zijn, wat ze betekenen en hoe ze samenhangen. Het model is implementatieneutraal: het schrijft geen database-, berichten- of API-ontwerp voor. Logische en technische modellen, zoals API-specificaties of datastructuren, kunnen erop worden gebaseerd.

De documentatie wordt gepubliceerd volgens de ReSpec-standaard, als één online document met doorklikbare verwijzingen tussen de onderdelen. De opdeling in een deel I (beschrijving) en een deel II (specificaties), zoals in eerdere versies, is daarmee vervallen. Het document is als volgt opgebouwd:

-   Hoofdstuk Inleiding: de achtergrond van het RSGB, de afbakening ten opzichte van de landelijke basisregistraties en de doelen van het model.
-   Hoofdstuk Uitgangspunten en modelleerprincipes: de keuzes die bij het opstellen van het model zijn gemaakt. Bijvoorbeeld dat alleen gegevens worden opgenomen die geschikt zijn voor meervoudig gebruik, hoe gegevens uit basisregistraties worden opgenomen of waarnaar wordt verwezen, en hoe wordt omgegaan met historie, afgeleide gegevens en waardelijsten.
-   Hoofdstuk Het informatiemodel op hoofdlijnen: een overzicht van het model aan de hand van diagrammen per domein, zoals personen, adressen en gebouwen, kadaster, WOZ en ondernemingen, met een toelichting op de samenhang.
-   Hoofdstuk Gegevensdefinities: de specificaties van alle modelelementen volgens MIM. Dat zijn objecttypen, attribuutsoorten, relatiesoorten, gegevensgroepen, keuzes, datatypen, enumeraties en waardelijsten. Per element zijn de MIM-metagegevens opgenomen, zoals naam, definitie, herkomst, kardinaliteit, indicatie materiële en formele historie en indicatie authentiek. Dit hoofdstuk is vooral bedoeld als naslagwerk.
-   Bijlage Wijzigingen ten opzichte van RSGB 2.02: een overzicht van de doorgevoerde wijzigingen, met verwijzing naar de bijbehorende wijzigingsverzoeken.
-   Bijlage Relatie met de landelijke basisregistraties: per basisregistratie (zoals de BRP, de BAG en de BRK) hoe de gegevens in het RSGB zijn opgenomen of waarnaar wordt verwezen.

Het UML-model waaruit deze documentatie is gegenereerd, de wijzigingsverzoeken en eerdere versies zijn te vinden op de [project repository voor het actaliseren van het RSGB](https://github.com/VNG-Realisatie/Actualisering-RSGB).
