---
title: Använda sammansättningar i Power BI Desktop (förhandsversion)
description: Utföra interaktiva analyser på stordata i Power BI Desktop
author: davidiseminger
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-desktop
ms.topic: conceptual
ms.date: 10/17/2018
ms.author: davidi
LocalizationGroup: Transform and shape data
ms.openlocfilehash: 3e94dc516f41d764394828309ba4b612083d4583
ms.sourcegitcommit: fbb27fb40d753b5999a95b39903070766f7293be
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2018
ms.locfileid: "49359733"
---
# <a name="aggregations-in-power-bi-desktop-preview"></a>Sammansättningar i Power BI Desktop (förhandsversion)

Med hjälp av **sammansättningar** i Power BI kan du utföra interaktiv analys på stordata på ett sätt som inte var möjligt tidigare. Med **sammansättningar** kan du drastiskt minska kostnaderna för att låsa upp stora datauppsättningar för beslutsfattande.

![sammansättningar i Microsoft Power BI Desktop](media/desktop-aggregations/aggregations_07.jpg)

Följande lista innehåller fördelar med att använda **sammansättningar**:

* **Frågeprestanda för stora datauppsättningar** – när användare interagerar med visuella objekt i Power BI-rapporter skickas DAX-frågor till datamängden. Kör frågor snabbare genom att cachelagra data på den aggregerade nivån med en bråkdel av de resurser som krävs på detaljnivån. Lås upp stordata på ett sätt som annars inte skulle vara möjligt.
* **Datauppdateringsoptimering** – Minska cachestorlekar och uppdateringshastigheter genom att cachelagra data på den aggregerade nivån. Gör data tillgängliga för användare snabbare.
* **Få balanserad arkitektur** – Gör det möjligt för den minnesinterna cachelagringen i Power BI att hantera aggregerade frågor, vilket görs på ett effektivt sätt. Begränsa frågor som skickas till datakällan i DirectQuery-läge, vilket gör det lättare att hålla sig inom samtidighetsgränserna. Frågor som passerar igenom brukar vara filtrerade frågor på transaktionsnivå som informationslager och stordatasystem vanligtvis hanterar väl.

### <a name="table-level-storage"></a>Lagring på tabellnivå
Lagring på tabellnivå används normalt med sammansättningsfunktionen. Läs artikeln [lagringsläge i Power BI Desktop (förhandsversion)](desktop-storage-mode.md) för mer information.

### <a name="data-source-types"></a>Typer av datakälla
Sammansättningar används tillsammans med datakällor som representerar dimensionsmodeller, till exempel informationslager och data mart samt Hadoop-baserade stordatakällor. Den här artikeln beskriver vanliga modelleringsskillnader i Power BI för varje typ av datakälla.

Alla Power BI Import- (icke-flerdimensionella) och DirectQuery-källor fungerar med sammansättningar.

## <a name="enabling-the-aggregations-preview-feature"></a>Aktivera förhandsgranskningsfunktionen för sammansättningar

Funktionen för **sammansättningar** är i förhandsversion och måste aktiveras i **Power BI Desktop**. Om du vill aktivera **sammansättningar** väljer du **Arkiv > Alternativ och inställningar > Alternativ > Förhandsfunktioner** och markerar sedan kryssrutorna **sammansatta modeller** och **Hantera sammansättningar**. 

![aktivera förhandsversionsfunktioner](media/desktop-aggregations/aggregations_01.jpg)

Du måste starta om **Power BI Desktop** för att funktionen ska aktiveras.

![omstart krävs för att ändringarna ska börja gälla](media/desktop-composite-models/composite-models_03.png)

## <a name="aggregations-based-on-relationships"></a>Sammansättningar som baseras på relationer

**Sammansättningar** som baseras på relationer används vanligtvis med dimensionella modeller. Power BI-datauppsättningar som använder informationslager och data mart som källor liknar star/snowflake-scheman med relationer mellan dimensionstabeller och faktatabeller.

Fundera på följande modell, som är från en enskild datakälla. Vi antar att alla tabeller till att börja med använder DirectQuery. Faktatabellen **Sales** innehåller flera miljarder rader. Att konfigurera lagringsläge för **Sales** till **Import** för cachelagring skulle förbruka mycket minne och administrationskostnader.

![tabeller i en modell](media/desktop-aggregations/aggregations_02.jpg)

Istället skapar vi tabellen **Sales Agg** som en sammansättningstabell. Den är mer detaljerad än **Sales** och innehåller därför mycket färre rader. Antalet rader ska vara lika med summan av **SalesAmount** som grupperats efter **CustomerKey**, **Datekey** och **ProductSubcategoryKey**. Istället för flera miljarder rader kan det röra sig om miljontals rader, vilket är mycket enklare att hantera.

Anta att följande dimensionstabeller är vanligast för frågor med högt affärsvärde. De är tabeller som kan filtrera **Sales Agg** med *en-till-många* (eller *många-till-en*)-relationer. Andra relationer, som *många-till-många* eller *flera källor*, används inte för sammansättningar.

* Geografi
* Kund
* Datum
* Produktunderkategori
* Produktkategori

Följande bild visar den här modellen.

![sammansättningstabell i en modell](media/desktop-aggregations/aggregations_03.jpg)

> [!NOTE]
> Tabellen **Sales Agg** är en helt vanlig tabell, så den kan läsas in på en mängd olika sätt. Till exempel kan sammansättning utföras i källdatabasen med hjälp av ETL/ELT-processer eller med [M-uttrycket](https://msdn.microsoft.com/query-bi/m/power-query-m-reference) för tabellen. Den kan använda läget Importera lagring med eller utan [Inkrementell uppdatering i Power BI Premium](service-premium-incremental-refresh.md), eller vara DirectQuery och vara optimerad för snabba frågor med hjälp av [kolumnlagringsindex](https://docs.microsoft.com/sql/relational-databases/indexes/columnstore-indexes-overview). Den här flexibiliteten gör det möjligt för balanserade arkitekturer att sprida frågebelastningen och undvika flaskhalsar.

### <a name="storage-mode"></a>Lagringsläge 
Vi fortsätter med exemplet som vi använder. Vi ställer in lagringsläget för **Sales Agg** på **Import** för att snabba på frågorna.

![konfigurera lagringsläget](media/desktop-aggregations/aggregations_04.jpg)

När vi gör det visas följande dialogruta som informerar oss om att de relaterade dimensionstabellerna anges till lagringsläget **Dubbla**. 

![dialogruta för lagringsläge](media/desktop-aggregations/aggregations_05.jpg)

Om du ställer in dem på **Dubbla** kan relaterade dimensionstabeller fungera som Import eller DirectQuery beroende på underfrågan.

* Frågor som aggregerar mätvärden från tabellen **Sales Agg**, som är Import och grupperas efter attribut från de relaterade dubbeltabellerna kan returneras från den minnesinterna cachen.
* Frågor som aggregerar mätvärden i tabellen **Sales**, som är DirectQuery och grupperas efter attribut från de relaterade dubbeltabellerna kan returneras i DirectQuery-läget. Frågans logik, inklusive gruppering efter åtgärd, skickas till källdatabasen.

Mer information om lagringsläget **Dubbla** finns i artikeln [lagringsläge](desktop-storage-mode.md).

> Obs! Tabellen **Sales Agg** är dold. Sammansättningstabeller bör döljas för datauppsättningens konsumenter. Konsumenter och frågor refererar till detaljtabellen, inte till sammansättningstabellen. De behöver inte ens veta att sammansättningstabellen finns.

### <a name="manage-aggregations-dialog"></a>Hantera dialogrutan sammansättningar
Sedan definierar vi sammansättningarna. Välj snabbmenyn **Hantera sammansättningar** för tabellen **Sales Agg** genom att högerklicka på tabellen.

![Hantera menyval för sammansättning](media/desktop-aggregations/aggregations_06.jpg)

Dialogrutan **Hantera sammansättningar** visas. Det visas en rad för varje kolumn i tabellen **Sales Agg** där vi kan ange sammansättningsbeteendet. Frågor som skickats till Power BI-datauppsättningen som refererar till tabellen **Sales** dirigeras om internt till tabellen **Sales Agg**. Datauppsättningskonsumenter behöver inte ens veta att tabellen **Sales Agg** finns.

![Hantera dialogrutan sammansättningar](media/desktop-aggregations/aggregations_07.jpg)

I följande tabell visas sammansättningar för tabellen **Sales Agg**.

![sammansättningstabell](media/desktop-aggregations/aggregations-table_01.jpg)

#### <a name="summarization-function"></a>Sammanfattningsfunktion

I listrutan för sammanfattning kan du välja mellan följande.
* Antal
* GroupBy
* Max
* Min
* Summa
* Antal tabellrader

#### <a name="validations"></a>Valideringar

Följande viktiga valideringar tillämpas av dialogrutan:

* Informationskolumnen som har valts måste ha samma datatyp som sammansättningskolumnen förutom sammanfattningsfunktioner för Antal och Antal tabellrader. Antal och Antal tabellrader erbjuds endast för heltalskolumner för sammansättning och kräver inte en matchande datatyp.
* Länkade sammansättningar som omfattar tre eller flera tabeller är inte tillåtna. Det går till exempel inte att ställa in sammansättningar i **Tabell A** som refererar till **Tabell B** som har sammansättningar som refererar till **Tabell C**.
* Duplicerade sammansättningar där två poster använder samma sammanfattningsfunktion och hänvisar till samma informationstabell/kolumn är inte tillåtna.

Följande valideringar tillämpas också för **sammansättningar** i den allmänt tillgängliga förhandsversionen. Vi har för avsikt att ta bort dessa valideringar i den allmänt tillgängliga versionen.

* Sammansättningar kan inte användas med säkerhet på radnivå (RLS). *Begränsningar i den allmänt tillgängliga förhandsversionen.*
* Informationstabellen måste vara DirectQuery, inte Import. *Begränsningar i den allmänt tillgängliga förhandsversionen.*

De flesta valideringar tillämpas genom att inaktivera listrutevärden och visa förklarande text i knappbeskrivningen, vilket visas i följande bild.

![valideringar som visas med knappbeskrivning](media/desktop-aggregations/aggregations_08.jpg)

### <a name="group-by-columns"></a>Gruppera efter kolumner

I det här exemplet är de tre GroupBy-posterna valfria. De påverkar inte sammansättningsbeteendet (förutom för exempelfrågan DISTINCTCOUNT, vilket visas på nästa bild). De ingår för att förbättra läsbarheten. Utan dessa GroupBy-poster skulle sammansättningarna fortfarande användas utifrån relationer. Det här är annorlunda jämfört med att använda sammansättningar utan relationer, vilket visas i exemplet med stordata som tas upp senare i den här artikeln.

### <a name="detecting-whether-aggregations-are-hit-or-missed-by-queries"></a>Identifiera om sammansättningar används eller missas av frågor

Mer information om hur du identifierar om frågor returneras från den minnesinterna cachen (lagringsmotor) eller DirectQuery (skickas till datakällan) med SQL Profiler finns i artikeln om [lagringsläget](desktop-storage-mode.md). Den här processen kan även användas för att identifiera om sammansättningar används.

Dessutom tillhandahålls följande utökade händelser i SQL Profiler.

    Query Processing\Aggregate Table Rewrite Query

Följande JSON-kodfragment visar ett exempel på utdata från händelsen när en sammansättning används.

* **matchingResult** visar att en sammansättning användes för underfrågan.
* **dataRequest** visar gruppera efter-kolumner och sammansatta kolumner som används av underfrågan.
* **mappning** visar kolumnerna i sammansättningstabellen som det mappats till.

![utdata från en händelse när sammansättning används](media/desktop-aggregations/aggregations-code_01.jpg)

### <a name="query-examples"></a>Frågeexempel
Följande fråga använder sammansättningen eftersom kolumner i tabellen *Date* har den kornighet som kan använda sammansättningen. Sammansättningen **Sum** används för **SalesAmount**.

![frågeexempel](media/desktop-aggregations/aggregations-code_02.jpg)

Följande fråga använder inte sammansättningen. Trots att den begär summan av **SalesAmount** utför den en gruppera efter-åtgärd på en kolumn i tabellen **Produkt**, som inte har kornigheten som kan använda sammansättningen. Om du ser relationer i modellen kan en produktunderkategori ha flera **Produkt**-rader. Frågan kan inte avgöra vilka produkter som den ska aggregera till. I det här fallet återgår frågan till DirectQuery och skickar en SQL-fråga till datakällan.

![frågeexempel](media/desktop-aggregations/aggregations-code_03.jpg)

Sammansättningar kan användas till annat än enkla beräkningar som ger en tydlig summa. Även komplexa beräkningar kan utföras. En komplex beräkning är konceptuellt uppdelad i underfrågor för varje SUM, MIN, MAX och COUNT och varje underfråga utvärderas för att avgöra om sammansättningen kan användas. Den här logiken gäller inte alltid på grund av frågeplansoptimering, men generellt sett bör den stämma. I följande exempel används sammansättningen:

![frågeexempel](media/desktop-aggregations/aggregations-code_04.jpg)

Funktionen COUNTROWS kan utnyttja sammansättningar. Följande fråga använder sammansättningen eftersom en sammansättning för tabellraderna**Antal** har definierats för tabellen **Försäljning**.

![frågeexempel](media/desktop-aggregations/aggregations-code_05.jpg)

Funktionen AVERAGE kan använda sammansättningar. Följande fråga använder sammansättningen eftersom AVERAGE internt viks till en SUM som dividerats med COUNT. Sammansättningen används eftersom kolumnen **UnitPrice** har sammansättningar som definieras för både SUM och COUNT.

![frågeexempel](media/desktop-aggregations/aggregations-code_06.jpg)

I vissa fall kan funktionen DISTINCTCOUNT använda sammansättningar. Följande fråga använder sammansättningen eftersom det finns en GroupBy-post för **CustomerKey** som behåller tydligheten i **CustomerKey** i sammansättningstabellen. Den här tekniken omfattas fortfarande av prestandatröskelvärdet där mer än två till fem miljoner distinkta värden kan påverka frågeprestandan. Men den kan vara användbar i scenarier där det finns miljarder rader i informationstabellen och två till fem miljoner distinkta värden i kolumnen. I det här fallet kan antalet distinkta värden prestera snabbare än om du söker i tabellen som innehåller flera miljarder rader, även om de har cachelagrats i minnet.

![frågeexempel](media/desktop-aggregations/aggregations-code_07.jpg)

## <a name="aggregations-based-on-group-by-columns"></a>Sammansättningar som baseras på gruppera-efter-kolumner 

Hadoop-baserade modeller för stordata har andra egenskaper än dimensionella modeller. För att undvika kopplingar mellan stora tabeller förlitar de sig ofta inte på relationer. Istället är dimensionsattribut ofta avnormaliserade till faktatabeller. Sådana modeller för stordata kan låsas upp för interaktiv analys med hjälp av **sammansättningar** som baseras på gruppera efter-kolumner.

Följande tabell innehåller den numeriska kolumnen **Rörelse** som ska aggregeras. Alla andra kolumner är attribut till Gruppera efter. Den innehåller IoT-data och ett stort antal rader. Lagringsläget är DirectQuery. Frågor på datakällan som aggregerar över hela datauppsättningen är långsamma på grund av den stora volymen.

![En IoT-tabell](media/desktop-aggregations/aggregations_09.jpg)

Om du vill aktivera interaktiv analys för den här datauppsättningen lägger vi till en sammansättningstabell som kan sorteras efter de flesta attribut, men inte attribut med hög kardinalitet som longitud och latitud. Den minskar antalet rader avsevärt och är tillräckligt liten för att passa en minnesintern cache. Lagringsläget för **Driver Activity Agg** är Import.

![Tabellen Driver Activity Agg](media/desktop-aggregations/aggregations_10.jpg)

Nu ska vi definiera sammansättningsmappningarna i dialogrutan **Hantera sammansättningar**. Den visar en rad för varje kolumn i tabellen **Driver Activity Agg** där vi kan ange sammansättningsbeteendet.

![Dialogrutan Hantera sammansättningar för tabellen Driver Activity Agg](media/desktop-aggregations/aggregations_11.jpg)

I följande tabell visas sammansättningar för tabellen **Driver Activity Agg**.

![Sammansättningstabell för Driver Activity Agg](media/desktop-aggregations/aggregations-table_02.jpg)

### <a name="group-by-columns"></a>Gruppera efter kolumner

I det här exemplet är **GroupBy**-posterna **inte valfria**. Utan dem kan sammansättningarna inte användas. Det här är inte detsamma som att använda sammansättningar som baseras på relationer, vilket visades i exemplet med den dimensionella modellen tidigare i den här artikeln.

### <a name="query-examples"></a>Frågeexempel

Följande fråga använder sammansättningen eftersom kolumnen **Aktivitetsdatum** täcks av sammansättningstabellen. Sammansättningen för tabellen Antal rader används av funktionen COUNTROWS.

![frågeexempel](media/desktop-aggregations/aggregations-code_08.jpg)

Det är en bra idé att använda sammansättningar för tabellen Antal rader för modeller som innehåller filterattribut i faktatabeller. Power BI kan skicka frågor till datauppsättningen med COUNTROWS då det inte uttryckligen krävs av användaren. Till exempel visar filterdialogrutan antal rader för varje värde.

![Filterdialogruta](media/desktop-aggregations/aggregations_12.jpg)

## <a name="aggregation-precedence"></a>Sammansättningsprioritet

Med sammansättningsprioritet kan flera sammansättningstabeller övervägas av en enda underfråga.

Se följande exempel. Det är en [sammansatt modell](desktop-composite-models.md) som innehåller flera DirectQuery-källor.

* Importtabellen **Driver Activity Agg2** har hög kornighet på grund av få gruppera-efter-attribut och låg kardinalitet. Antalet rader kan vara så lågt som tusentals, så det kan enkelt anpassas till en minnesintern cache. Dessa attribut används av en viktig instrumentpanel, så frågor som refererar till dem bör kunna utföras så snabbt som möjligt.
* Tabellen **Driver Activity Agg** är en mellanliggande sammansättningstabell i DirectQuery-läge. Den innehåller mer än en miljard rader och optimeras vid källan med hjälp av kolumnlagringsindex.
* Tabellen **Driver Activity** är DirectQuery och innehåller över en biljon rader med IoT-data som kommer från ett system för stordata. Den använder detaljerade frågor för att visa enskilda IoT-avläsningar i kontexter som kontrolleras av filter.

Fotavtrycket för minnesanvändning för den här modellen är relativt litet, men det låser upp en stor datauppsättning. Den representerar en balanserad arkitektur eftersom den sprider frågebelastningen över komponenter i arkitekturen och använder dem utifrån deras styrkor.

![tabeller för ett litet fotavtryck för minnesanvändning låser upp en stor datauppsättning](media/desktop-aggregations/aggregations_13.jpg)

Dialogrutan **Hantera sammansättningar** för **Driver Activity Agg2** visar att fältet *Prioritet* är 10, vilket är högre än **Driver Activity Agg** och innebär att den kommer att anses vara viktigast av de frågor som använder sammansättningar. Underfrågor som inte har den kornighet som kan besvaras av **Driver Activity Agg2** överväger **Driver Activity Agg** istället. Informationsfrågor som inte kan besvaras av sammansättningstabellerna dirigeras om till **Driver Activity**.

Tabellen som anges i kolumnen **Informationstabell** är **Driver Activity**, inte **Driver Activity Agg** eftersom länkade sammansättningar inte tillåts (se [ valideringar](#validations) tidigare i den här artikeln).

![Hantera dialogrutan sammansättningar](media/desktop-aggregations/aggregations_14.jpg)

I följande tabell visas sammansättningar för tabellen **Driver Activity Agg2**.

![Sammansättningstabell för Driver Activity Agg2](media/desktop-aggregations/aggregations-table_03.jpg)

## <a name="aggregations-based-on-group-by-columns-combined-with-relationships"></a>Sammansättningar som baseras på gruppera-efter-kolumner kombinerat med relationer

Du kan även kombinera de två metoderna för sammansättningar som beskrivs tidigare i den här artikeln. För **sammansättningar** som baseras på relationer kan det krävas att de avnormaliserade dimensionstabellerna delas upp i flera tabeller. Om det är dyrt eller opraktiskt för vissa dimensionstabeller kan de nödvändiga attributen replikeras i sammansättningstabellen för vissa dimensioner och relationer som används för andra.

Följande modell replikerar *Månad*, *Kvartal*, *Termin* och *År* i tabellen **Sales Agg**. Det finns ingen relation mellan tabellerna **Sales Agg** och **Datum**. Det finns relationer till **Kund** och **Produktunderkategori**. Lagringsläget för **Sales Agg** är Import.

![kombinera sammansättningstekniker](media/desktop-aggregations/aggregations_15.jpg)

I följande tabell visas posterna som konfigurerats i dialogrutan **Hantera sammansättningar** för tabellen **Sales Agg**. GroupBy-poster där **Datum** är informationstabellen är obligatoriskt för att använda sammansättningar för frågor som grupperas efter datum-attribut. Som i föregående exempel påverkar GroupBy-poster för CustomerKey och ProductSubcategoryKey inte sammansättningsträffar på grund av förekomsten av relationer (återigen med undantag för DISTINCTCOUNT).

![Sammansättningstabellen Sales Agg](media/desktop-aggregations/aggregations-table_04.jpg)

> Obs! För den här modellen krävs det att tabellen **Datum** är i DirectQuery-läget för att fylla i dialogrutan Hantera sammansättningar, eftersom det är en informationstabell. Detta är en förhandsversionsbegränsning som vi har för avsikt att ta bort när den allmänna tillgängligheten börjar gälla.

### <a name="query-examples"></a>Frågeexempel

Följande fråga använder sammansättningen eftersom CalendarMonth omfattas av sammansättningstabellen och CategoryName kan nås via en-till-många-relationer. Sammansättningen Summa används för **SalesAmount**.

![frågeexempel](media/desktop-aggregations/aggregations-code_09.jpg)

Följande fråga använder inte sammansättningen eftersom CalendarDay inte täcks av sammansättningstabellen.

![frågeexempel](media/desktop-aggregations/aggregations-code_10.jpg)

Följande fråga för tidsinformation använder inte sammansättningen eftersom funktionen DATESYTD genererar en tabell med CalendarDay-värden som inte omfattas av sammansättningstabellen.

![frågeexempel](media/desktop-aggregations/aggregations-code_11.jpg)

## <a name="caches-should-be-kept-in-sync"></a>Cacheminnen bör hållas synkroniserade

**Sammansättningar** som kombinerar DirectQuery och Import och/eller dubbelt lagringsläge kan returnera olika data om den minnesinterna cachen inte är synkroniserad med källdata. Frågekörningen försöker inte maskera dataproblem genom att t.ex. filtrera DirectQuery-resultaten så att matchar cachelagrade värden. Dessa funktioner är för prestandaoptimering och bör endast användas på sätt som inte äventyrar möjligheten att uppfylla verksamhetskraven. Det är ditt ansvar att känna till dina dataflöden, så kontrollera utformningen. Det finns etablerade tekniker för att hantera sådana problem vid källan, om så behövs.

## <a name="next-steps"></a>Nästa steg

Följande artiklar beskriver mer om sammansatta modeller och beskriver DirectQuery i detalj.

* [Sammansatta modeller i Power BI Desktop (förhandsversion)](desktop-composite-models.md)
* [Många-till-många-relationer i Power BI Desktop (förhandsversion)](desktop-many-to-many-relationships.md)
* [Lagringsläge i Power BI Desktop (förhandsversion)](desktop-storage-mode.md)

DirectQuery-artiklar:

* [Använd DirectQuery i Power BI](desktop-directquery-about.md)
* [Datakällor som stöds av DirectQuery i Power BI](desktop-directquery-data-sources.md)

