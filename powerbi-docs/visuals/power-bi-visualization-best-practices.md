---
title: Metodtips för design av rapporter och visuella objekt (white paper)
description: 'White paper: Metodtips för design av rapporter i Power BI'
author: mihart
manager: kvivek
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-desktop
ms.topic: conceptual
ms.date: 06/22/2018
ms.author: mihart
LocalizationGroup: Visualizations
ms.openlocfilehash: 77802d2db59ddff94123991e209441b4c491f98b
ms.sourcegitcommit: 0ff358f1ff87e88daf837443ecd1398ca949d2b6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/21/2018
ms.locfileid: "46548613"
---
# <a name="best-design-practices-for-reports-and-visuals"></a>Metodtips för design av rapporter och visuella objekt
<!-- Shared newnav Include -->
[!INCLUDE [newnavbydefault](../includes/newnavbydefault.md)]

## <a name="introduction"></a>Introduktion
I det här dokumentet finns metodtips för att utforma rapporter i Power BI. Vi börjar med planeringen och beskriver designprinciper som du kan använda i dina rapporter och för de sidor och enskilda visuella objekt som utgör rapporten.  Många av dessa metodtips gäller även instrumentpaneldesign.

Vi hoppas dokumentet blir en startpunkt för dig, att du använder det du lärt dig i dina egna rapporter och visualiseringar, samt att du fortsätter konversationen på community.powerbi.com. BI:s rapportdesign och visualiseringsanvändning är ett ämne som engagerar just nu och det finns många tankesmedjor, bloggare och webbplatser som har fördjupat sig i ämnet (vi visar några i slutet).   

> [!NOTE]
> Rekommendationerna i detta dokument är riktlinjer som du kan använda när det känns lämpligt. För varje princip som beskrivs nedan finns det oftast ett bra skäl att ”bryta regeln”.
> 
> 

*Vi översvämmas med information – inte för att det finns för mycket, utan för att vi inte vet hur vi ska hantera den.*
– Stephen Few

## <a name="a-look-at-the-landscape-and-terminology"></a>En titt på miljö och terminologi
I Power BI kan en rapport ha en eller flera rapportsidor. Alla sidor kallas tillsammans för en rapport. Grundelementen i rapporten är visuella objekt (dvs. visualiseringar), separata bilder och textrutor. Det finns oräkneliga formateringsalternativ, från enskilda datapunkter till rapportelement och själva rapportsidan.

Vi börjar med rapportplaneringsfasen, fortsätter med grundläggande rapportdesignprinciper, diskuterar visuella designprinciper och avslutar med en diskussion om metodtips för enskilda visuella typer.

Detaljerad vägledning och anvisningar för att skapa och använda Power BI-rapporter finns tillgängliga på **powerbi.com > Läs mer**.

## <a name="before-you-build-your-first-visualizationfocus-on-requirements"></a>Innan du skapar din första visualisering bör du fokusera på kraven
Skapandet av en rapport startar innan du gör ditt första visuella objekt, eftersom en bra rapport måste planeras.  Ta reda på vilka data som du ska arbeta med och skriv ner kraven för rapporten. Fråga dig själv ”Vilka är företagets behov, hur ska dessa data användas och av vem?” En viktig fråga är ”Vilka beslut kommer läsaren vilja ta utifrån den här rapporten?”

Svaren på dessa frågor kommer att påverka din design. Varje rapport har ett budskap. Kontrollera att budskapet stämmer med företagets behov. Det kan vara nära till hands att lägga till visuella objekt som visar dramatiska insikter, men om dessa insikter inte stämmer överens med företagets behov är rapporten inte användbar – och användarna kan i själva verket störas av dessa visuella objekt. Dessutom kanske inte den information som behövs för att fatta beslutet finns i dessa data. Kan rapporten användas för att mäta vad som behövs?

Rapporter kan användas för att övervaka, upptäcka, spåra, förutsäga, mäta, hantera, testa med mera. Om företaget till exempel behöver en försäljningsrapport som mäter resultat, kan du utforma en rapport för aktuell försäljning jämfört med föregående försäljning, jämföra det med konkurrenter och med vissa KPI:er som utlöser aviseringar.  Kanske läsarna kan granska nedåt i försäljningssiffrorna för att se butikens öppettider eller leveransproblem som kan påverka försäljningen.  En annan nedbrytning kan vara möjligheten att titta på försäljning per butik, region, produkt, säsong med mera.

Tänk på vem som ska läsa rapporten och utforma en rapport som använder bekant terminologi och tillhandahåller data med en detaljnivå och komplexitet som motsvarar kundernas kunskapsnivå. Har du mer än en typ av kund? En storlek passar inte alltid alla. Utforma separata rapportsidor baserat på kunskap och se till att märka varje sida tydligt så att kunderna själva kan identifiera den. Ett annat alternativ är att använda utsnitt för att kunderna ska kunna anpassa sidan på ett sätt som passar dem. Engagera kunden i planeringsfasen och undvik att skapa vad du tror att de behöver.  Var beredd på att börja om från början igen.

När du har identifierat vilka av företagets behov, kunder eller mått som du vill inkludera, är nästa steg att välja rätt visuella objekt för budskapet och presentera dessa visuella objekt på det mest effektiva sättet. Detta omfattar en hel del, så vi börjar med några grundläggande principer för rapportdesign.

## <a name="principles-of-report-design"></a>Principer för rapportdesign
En rapportsida har begränsat utrymme och något av det svåraste är att få plats med alla element som du vill använda på den enda ytan – och fortfarande kunna presentera information som är lätt att förstå. Samt inte underskatta värdet av att det är ”snyggt”. Nyckeln är att hitta balansen mellan snyggt och användbart.

Låt oss ta en titt på layout, tydlighet och estetik.

### <a name="layout---the-report-canvas"></a>Layout – rapportarbetsytan
Rapportarbetsytan har ett begränsat utrymme.  Om du inte får plats med alla element på en enda rapportsida, kan du dela upp rapporten på flera sidor.  En rapportsida kan skräddarsys för en specifik målgrupp (t.ex. HR, IT-avdelning, försäljning, SLT), en specifik företagsfråga (t.ex. Hur påverkar felen vår stilleståndstid? eller Vilken påverkan har marknadsföringskampanjen på våra sentiment?), eller som ett progressivt budskap (t.ex. första sidan som en översikt eller ”inkastare”, på andra sidan fortsätter databeskrivningen, tredje sidan visar detaljerad information osv.).  Om hela rapporten får plats på en enda sida är det bra. Om inte kan du skapa du separata rapportsidor som logiskt delar upp innehållet.  Och glöm inte att ge sidorna beskrivande och användbara namn.

Tänk dig att du fyller ett konstgalleri. Du skulle inte placera 50 konstverk i ett litet rum, fylla det med stolar och måla varje vägg i olika färg. Som curator väljer du bara de verk som har en gemensam egenskap, placerar ut dem i rummet med tillräckligt med utrymme för att besökarna ska kunna röra sig och sedan ställer du dit informativa kort som beskriver vad de tittar på. Och det finns en anledning till att de flesta moderna gallerier har vita väggar!
I den här artikeln börjar vi med ett rapportexempel som kräver mycket arbete.  Allt eftersom att vi använder våra metodtips och designprinciper förbättras vår rapport.

![](media/power-bi-visualization-best-practices/power-bi-example1newa.png)

**Bild 1:    Den här fula rapportsidan kräver mycket arbete**

Exemplet ovan har många utrymmesrelaterade (layout) designproblem som beskrivs nedan:

* justering, ordning och användning av närhet
* bristfällig användning av utrymme och sortering
* oreda

### <a name="alignment-order-and-proximity"></a>Justering, ordning och närhet
Layouten för dina rapportelement påverkar förståelsen och vägleder läsaren genom rapportsidan. Hur du placerar och positionerar element skapar ett budskap.  Budskapet kan vara ”Börja här och titta sedan här” eller ”Dessa tre element är relaterade till varandra”.

* I de flesta kulturer läser man från vänster till höger samt uppifrån och ned. Placera det viktigaste elementet i det övre vänstra hörnet av rapporten. Och organisera sedan resten av de visuella objekten på ett sätt som innebär logisk navigering och förståelse av informationen.
* Placera element som kräver att läsaren gör ett val till vänster om de visualiseringar som valet påverkar, exempelvis utsnitt.
* Placera relaterade element nära varandra. Närheten visar att elementen är relaterade.
* Ett annat sätt att visa relationer är att lägga till en ram eller färgad bakgrund för relaterade element. Omvänt kan du lägga till en avgränsare för att skilja mellan olika delar i en rapport.
* Använd den vita ytan för att visuellt dela in avsnitt på rapportsidan.
* Fyll rapportsidan. Om du märker att du har många extra vita områden, kan du göra dina visualiseringar större eller arbetsytan mindre.
* Tänk efter innan du ändrar storlek på rapportelementen. Låt inte tillgängligt utrymme styra storleken på en visualisering.
* Gör viktiga element större än andra eller lägg till ett visuellt element som t.ex. en pil för att dra uppmärksamhet till dem.
* Justera elementen på rapportsidan, antingen symmetriskt eller avsiktligt asymmetriskt.

Låt oss ta en närmare titt på justering.

#### <a name="alignment"></a>Justering
Justering innebär inte att de olika komponenterna måste ha samma storlek eller att du måste ha samma antal komponenter på varje rad i rapporten. Det betyder bara att det finns en struktur på sidan som hjälper till med navigering och läsbarhet.

Vi kan se i den uppdaterade rapporten nedan att rapportkomponenterna nu är justerade mot vänster och höger kant, samt att varje rapportrad dessutom har justerats vågrätt och lodrätt. Våra utsnitt ligger till vänster om de visuella objekt de påverkar.

![](media/power-bi-visualization-best-practices/power-bi-example2new.png)

**Bild 2:    Vårt fula rapportexempel förbättrades med layoutredigeringarna**

Power BI innehåller verktyg som hjälper dig att justera dina visuella objekt. Om flera visuella objekt har markerats i Power BI Desktop kan du använda alternativen **Justera och fördela** på fliken **Visuella objekt** i menyfliksområdet för att matcha positionen för de visuella objekten.

![](media/power-bi-visualization-best-practices/power-bi-visualization.png)

**Bild 3:    Justera visuella objekt i Power BI Desktop**

I Power BI online och Power BI Desktop får du också exakt kontroll över storlek och placering av visuella objekt med fliken **Allmänt** i formateringsfönstret för alla visuella objekt:

![](media/power-bi-visualization-best-practices/power-bi-align-vizs.png)

**Bild 4:    Ange exakt placering för ditt visuella objekt**

I vår exempelrapportsida (bild 2) har de två korten och den breda ramen justerats till **X-positionen** 200.

#### <a name="fit-to-the-space"></a>Anpassa till utrymmet
Använd utrymmet som finns på bästa sätt.  Om du vet hur rapporten ska visas, kan du utforma med det i åtanke. Minska det tomma utrymmet genom att fylla i arbetsytan.  Gör allt du kan för att minska behovet av rullningslister i enskilda visuella objekt.  Fyll utrymmet utan att de visuella objekten verkar vara hopträngda.

##### <a name="adjust-the-page-size"></a>Ändra sidstorleken
Om du minskar sidstorleken blir enskilda element större i förhållande till sidan. Gör detta genom att avmarkera alla visuella objekt på sidan och använda fliken **Sidstorlek** i formateringsfönstret.  

Här är en rapportsida som först använder sidstorleken 4:3 och sedan 16:9. Observera att layouten passar mycket bättre i 16:9. Det finns även tillräckligt med utrymme för att ta bort rullningslisten från det andra visuella objektet.

![](media/power-bi-visualization-best-practices/power-bi-page-view-before.png)

**Bild 5a:    Rapporten med sidstorlek 4:3**

![](media/power-bi-visualization-best-practices/power-bi-page-view-after.png)

**Bild 5b:    Rapporten med sidstorlek 16:9**

Ska rapporten visas med 4:3, 16:9 eller något annat förhållande? På små skärmar eller stora skärmar? Eller på alla möjliga olika skärmproportioner och storlekar?  Designa med detta i åtanke.

Sidan med vår exempelrapport ser lite hopträngd ut. Öppna formateringsfönstret utan att något visuellt objekt är markerat genom att välja färgrollerikonen. Expandera **Sidstorlek** och ändra **Höjd** till 900.

![](media/power-bi-visualization-best-practices/power-bi-page-size.png)

**Bild 6:    Öka sidhöjden**

#### <a name="reduce-clutter"></a>Minska oreda
En stökig rapportsida är svår att förstå vid en snabb titt och kan vara så överväldigande att läsaren inte ens försöker.  Ta bort alla rapportelement som inte är nödvändiga. Lägg inte till onödiga saker som varken förbättrar förståelsen eller navigeringen. Rapportsidan måste visa informationen så tydligt, snabbt och sammanhängande som möjligt.

Edward Tufte kallar det ”data to ink ratio” i sin bok *The Visual Display of Quantitative Information*.  I princip ska du ta bort allt som inte är nödvändigt.

Det som du tar bort ökar tomrummet på rapportsidan och ger mer utrymme för att tillämpa metodtipsen som vi lärde ut ovan i avsnittet ”Justering, ordning och närhet”.

Redan nu ser vårt exempel bättre ut. Vi har tagit bort massor och lagt till figurer som grupperar elementen.  Bakgrundsbilden, den onödiga pilen och textrutan är borta, ett visuellt objekt har flyttats till en annan sida i rapporten osv. Vi har också förlängt sidstorleken för att öka det vita (gula?) området.

![](media/power-bi-visualization-best-practices/power-bi-example3newer.png)

**Bild 7:    Vårt fula rapportexempel är inte längre stökigt**

### <a name="tell-a-story-at-a-glance"></a>Berätta en historia i korthet
Ett övergripande test är att någon utan tidigare erfarenhet snabbt ska kunna förstå rapporten utan att få någon som helst förklaring. Med en snabb blick ska läsaren kunna se vad sidan handlar om och vad varje diagram/tabell innehåller.   

När läsarna tittar på rapporten ska deras ögon dras till det element som du vill att de ska se först och deras ögon ska sedan fortsätta vänster-höger-uppåt-nedåt.  Ändra detta genom att lägga till visuella tips som t.ex. etiketter i textrutor, figurer, ramar, storlek och färg.  

#### <a name="text-boxes"></a>Textrutor
Ibland räcker det inte med visualiseringarnas rubriker för att få fram budskapet.  Lägg till textrutor som kommunicerar med de som läser rapporterna.  Textrutorna kan beskriva rapportsidan, en grupp med visuella objekt, eller ett separat visuellt objekt. De kan förklara resultat eller ge en bättre definition av ett visuellt objekt, komponenter i det visuella objektet eller relationer mellan visuella objekt. Textrutorna kan användas till att dra uppmärksamhet som baseras på olika kriterier i textrutan.

Välj **Textruta** i Power BI-tjänsten på den översta menyraden. (I Power BI Desktop väljer du **Textruta** i området **Infoga** i menyfliksområdet.)

![](media/power-bi-visualization-best-practices/power-bi-text-boxes.png)

**Bild 8:    Lägga till en textruta**

Skriv i den tomma rutan och använd sedan kontrollerna längst ned för att ange teckensnitt, storlek, justering med mera. Använd handtagen för att ändra storlek på rutan.

![](media/power-bi-visualization-best-practices/power-bi-text-box-edit.png)

**Bild 9:    Formatera textrutan**

Men överdriv inte! För mycket text i en rapport är distraherande och drar uppmärksamhet från de visuella objekten. Om du upptäcker att rapportsidan kräver mängder med text för att man ska förstå den, bör du börja om från början.  Kan du välja ett annat visuellt objekt presenterar budskapet bättre på egen hand? Kan du ändra det visuella objektets rubrik så att den blir mer begriplig?   

#### <a name="text"></a>Text
Skapa en textstilguide och tillämpa den på alla sidor i rapporten. Använd bara ett fåtal teckensnitt, textstorlekar och färger.  Tillämpa inte bara stilguiden på textelementen, utan även på de teckensnittsval som du gör i dina visualiseringar (se Rubriker och etiketter som ingår i visualiseringar nedan). Ange regler för när du ska använda fetstil, kursiv stil, ökad teckenstorlek, vissa färger med mera.  Försök att undvika enbart versaler eller understrykningar.

#### <a name="shapes"></a>Figurer
Figurer kan också vara till hjälp för navigering och förståelse. Använd figurer för att gruppera relaterad information, markera viktiga data och använd pilarna för att dirigera ögat. Med figurer kan läsarna få hjälp med var de ska börja och hur de ska tolka rapporten. I designtermer kallas detta ofta för *kontrast*.

![](media/power-bi-visualization-best-practices/shapes.png)

**Bild 10a:    Figurer i Power BI-tjänsten**

![](media/power-bi-visualization-best-practices/power-bi-desktop-shapes2new.png)

**Bild 10b:    Figurer i Power BI Desktop**

Hur ser vår exempelsida ut nu?  Bild 11 visar en renare och mindre rörig sida med en konsekvent användning av textytor, teckensnitt och färger.  Sidrubriken i det övre vänstra hörnet visar vad sidan handlar om.

![](media/power-bi-visualization-best-practices/power-bi-example4new.png)

**Bild 11:    Rapportexemplet med textriktlinjerna tillämpade och en tillagd rubrik**

I vårt exempel lades en rubrik för rapportsidan till i det övre vänstra hörnet, vilket är den första plats som läsaren ser. Teckenstorleken är 28 och teckensnittet är Segoe Bold, vilket skiljer det från resten av sidan.  Vår textstilguide behöver inte någon bakgrund, svarta rubriker, förklaringar eller etiketter och detta har tillämpats för alla visuella objekt på sidan där det är möjligt (det går inte att redigera axlar och etiketter i kombinationsdiagram).  Dessutom:

* Kort: **Kategorietikett** är inställd på Av, **Rubrik** som På samt 12 pt svart centrerad.
* Visuella rubriker: Om det är inställt som På, ange 12 pt och vänsterjusterad.
* Utsnitt: **Rubrik** inställt på Av, **Rubrik** inställt som På. Lämna **Objekt** > **Text** grått och 10 punkter.
* Punkt- och kolumndiagram: Svart teckensnitt för X- och Y-axlarna samt X- och Y-axlarnas rubriker, om det används.

#### <a name="color"></a>Färg
Använd färger konsekvent.  Vi kommer att prata mer om färg i Principer för visuell design nedan. Men här menar vi att du ska fundera över valet av färg så att den inte förhindrar att läsaren förstår din rapport snabbt.  För många starka färger hindrar sinnena. Det här avsnittet handlar mer om vad du inte ska göra med färg.

#### <a name="backgrounds"></a>Bakgrunder
När du ställer in bakgrunder för rapportsidor bör du välja färger som inte överskuggar rapporten, krockar med andra färger på sidan eller minskar synvänligheten. Tänk på att vissa färger har en särskild betydelse.  I vissa länder anses t.ex. färgen röd i rapporter betyda att något är dåligt.

![](media/power-bi-visualization-best-practices/power-bi-page-background.png)

**Bild 12: Ställ in rapportens bakgrund**

Du skapar inte ett konstverk utan en funktionell rapport. Välj en färg som förbättrar läsbarhet och tydlighet för rapportelementen.  

Vid en undersökning av användningen av färg och visualiseringar på webbsidor upptäckte man att en större kontrast mellan färger påskyndar förståelsen (The effect of text and background colour on visual search of Web pages och **Determining Users’ Perception of Web Page Visual Complexity and Aesthetic Characteristics**).

Vi har använt några metodtips för färger i vårt exempelrapport (bild 20 och 21) nedan. Det mest anmärkningsvärda var att vi ändrade bakgrundsfärgen till svart.  Den gula var för ljus och tröttade våra ögon.  I diagrammet ”Antal idrottare per år och klass” försvann dessutom den gula delen av staplarna in i den gula bakgrunden.  Med hjälp av en svart (eller vit) bakgrund får vi maximal kontrast och de visuella objekten blir fokus för uppmärksamheten.

Här är ytterligare steg som vi tog för att förbättra exempelrapporten:

**Sidrubrik**

När vi ändrade bakgrunden till svart försvann vår rubrik eftersom textrutans fält bara tillåter ett svart teckensnitt.   Lös problemet genom att lägga till en rubrik i en textruta i stället.  När textrutan är markerad raderar du texten. Gå till fliken Visualiseringar, välj **Rubrik** och ställ in den som På. Välj pilen för att expandera alternativen i **Rubrik**, skriv **Sommar-OS** i fältet **Rubriktext** och välj vit **Teckenfärg**.

![](media/power-bi-visualization-best-practices/power-bi-text-box-title.png)

**Bild 13: Lägga till en sidrubrik**

**Kort**

För de visuella kortobjekten öppnar du formateringsfönstret (färgrollerikonen) och ställer in **Bakgrund** som På. Välj vit med en genomskinlighet på 0 %. Ställ in **Rubrik** som På samt välj vit **Teckenfärg** och svart **Bakgrundsfärg**.

**Utsnitt**

Fram tills nu har de två utsnitten haft en annan formatering som inte passar designen. Ändra bakgrundsfärgen till turkos för båda utsnitten.  Turkos är ett bra val eftersom det ingår i sidans färgpalett – det finns i koropletkartan, trädkartan och kolumndiagrammet.

![](media/power-bi-visualization-best-practices/power-bi-slicer-background.png)

**Bild 14: Ändra utsnittets bakgrundsfärg**

Lägg till en tunn vit kantlinje.

![](media/power-bi-visualization-best-practices/power-bi-slicer-outline.png)

**Bild 15: Lägg till en kantlinje i utsnittet**

Det grå teckensnittet är svårt att se mot turkos, så ändra färgen för **Objekt** till vit.

![](media/power-bi-visualization-best-practices/power-bi-slicer-items.png)

**Bild 16: Ändra utsnittets teckenfärg**

Och slutligen går du till **Rubrik** och ändrar **Teckenfärg** till vit samt lägger till en svart **Bakgrundsfärg**.

![](media/power-bi-visualization-best-practices/power-bi-card-formatting.png)

**Bild 17: Formatera utsnittets rubrik**

**Rektangelfigur**

Rektangeln har också försvunnit in i den svarta bakgrunden.  Lös problemet genom att markera figuren och i fönstret **Formatera figur** ställa in **Bakgrund** som På.

![](media/power-bi-visualization-best-practices/power-bi-shape-format.png)

**Bild 18: Formatera figuren**

**Stapeldiagram, bubbeldiagram, koropletkarta och trädkarta**

Lägg till en vit bakgrund i återstående visuella objekt på rapportsidan. Från formateringsfönstret expanderar du alternativet **Linje** och anger **Linjefärg** till vit och **Tjocklek** till 3.

![](media/power-bi-visualization-best-practices/power-bi-background.png)

**Bild 19: Lägg till en vit bakgrund i återstående visualiseringar**

![](media/power-bi-visualization-best-practices/power-bi-example5a.png)

**Bild 20: Rapportexempel med färgmetodtips tillämpade (svart bakgrund)**

![](media/power-bi-visualization-best-practices/power-bi-example5b.png)

**Bild 21:    Rapportexempel med färgmetodtips tillämpade (vit bakgrund)**
 

### <a name="aesthetics"></a>Estetik
Mycket av vad vi anser vara estetiskt har redan diskuterats ovan: justering, färg, alternativ för teckensnitt, oreda osv.  Men det finns några fler metodtips för rapportdesign som är värda att diskutera och dessa behandlar det övergripande utseendet i rapporten.  

Kom ihåg att funktionen för rapporten är att uppfylla företagets behov, inte att vara snygg.  Men vissa skönhetskrav finns, särskilt när det gäller första intrycket. Nashville-konsulten Tony Bodoh förklarar ”Känslor utlöses en halv sekund innan logiken kickar in”.  Läsarna kommer först att reagera på en känslomässig nivå på rapportsidan innan de tar sig tid att gå på djupet. Om sidan ser oordnad, förvirrande och oprofessionell ut kanske läsaren aldrig upptäcker vilket kraftfullt budskap den har.

TDI-bloggaren och TechTarget-branschanalytikern Wayne Eckerson har en bra liknelse.  Att utforma en rapport är som att dekorera ett rum.  Ibland köper du en vas, en soffa, ett bord eller en tavla.  Du gillar alla dessa saker var för sig. Men även om varje enskilt val är klokt, kanske de inte passar ihop eller konkurrerar med varandra om uppmärksamheten.

Koncentrera dig på att:

* Skapa ett gemensamt tema eller utseende på rapporten och tillämpa det på alla rapportsidorna
* Använd fristående bilder och annan grafik som ger stöd, i stället för att dra uppmärksamhet från det verkliga budskapet
* Och tillämpa alla metodtips som beskrivits hittills i artikeln.

## <a name="principles-of-visual-design"></a>Principer för visuell design
Vi har tittat på principerna för rapportdesign och du har lärt dig att ordna rapportelementen på ett sätt som gör det enkelt att snabbt förstå rapporten.  Nu ska vi titta på designprinciper för de visuella objekten.  Och i nästa avsnitt fortsätter vi med enskilda visuella objekt och diskuterar metodtips för vissa av vanligaste typerna.

I det här avsnittet är det dags att lämna exempelrapportsidan ett tag och titta på andra exempel.  När vi har gått igenom principerna för visuell design går vi tillbaka till sidan med vår exempelrapport och tillämpar det vi lärt oss (med hjälp av stegvisa instruktioner).  

### <a name="planning--choose-the-right-visual"></a>Planera – Välj rätt visuellt objekt
På samma sätt som det är viktigt att planera rapporten innan du börjar skapa den, kräver varje visuellt objekt också planering.  Fråga dig själv ”Vilket budskap vill jag få fram med det här visuella objektet?” Och sedan tar du reda på vilken visuell typ som kan förmedla det bäst. Du kan visa förloppet via en försäljningscykel som ett stapeldiagram, men kanske skulle ett vattenfalls- eller trattdiagram illustrera det bättre? Om du behöver hjälp med detta kan du läsa det sista avsnittet i det här dokumentet ”Visuella typer och metodtips”, som beskriver metodtipsen för vissa av de vanligaste typerna.  Bli inte förvånad om den första visuella typ som du väljer inte visar sig vara det bästa alternativet.  Testa mer än en visuell typ om du vill se vilken som är bäst för budskapet.

Förstå skillnaden mellan kategoriska och kvantitativa data och vilka visuella typer som fungerar bäst med vilken typ av data. Kvantitativa data kallas ofta för mått och är vanligtvis numeriska. Kategoriska data kallas ofta för dimensioner och kan klassificeras. Detta beskrivs mer ingående i ”Välja rätt mått” nedan.

Undvik frestelsen att använda avancerade eller mer komplexa visuella typer bara för att göra din rapport mer imponerande. Det du söker är det enklaste alternativet för att förmedla budskapet. Vågräta stapeldiagram och enkla linjediagram kan förmedla information snabbt.  De är välbekanta och bekväma och tolkas enkelt av de flesta läsare.  En annan fördel är att de flesta läser från vänster till höger och uppifrån och ned. Det går därför snabbt att läsa och förstå dessa två diagramtyper.

Kräver ditt visuella objekt att man använder en rullningslist? Undvik rullningslister om det går.  Försök att använda filter och hierarkier/nedbrytning. Om detta inte eliminerar rullningslisten bör du fundera på att välja en annan visuell typ. Om du inte kan undvika rullningslister är det bättre med vågrät rullning än med lodrät rullning.

Även om du väljer det absolut bästa visuella objektet för budskapet, kan du fortfarande behöva hjälp.  Det är där etiketter, rubriker, menyer, färg och storlek kommer in. Vi diskuterar dessa designelement senare i avsnittet ”Designelement”.

### <a name="choose-the-right-measure"></a>Välja rätt mått
Är budskapet som ditt visuella objekt förmedlar tilltalande? Spelar det någon roll?  Skapa inte visuella objekt bara för att du kan. Du kanske tycker det är datan som ger budskapet, men det är inte. Var inte rädd för att börja om från början och leta efter ett intressantare sätt att få fram budskapet. Eller så kanske budskapet finns där, men det måste mätas på ett annat sätt.

Anta exempelvis att du vill mäta hur framgångsrika dina försäljningschefer är. Vilka mått ska du använda för att göra detta?  Vill du mäta genom att titta på total försäljning eller total vinst, tillväxt under föregående år eller resultat mot ett uppsatt mål? Säljaren Lisa kanske har den största vinsten och om du visade vinst per säljare i ett stapeldiagram skulle hon framstå som en rockstjärna jämfört med de andra säljarna.  Men om Lisa har en hög försäljningskostnad (resekostnader, leveranskostnader, tillverkningskostnader etc.) räcker det inte att bara titta på försäljningen.

#### <a name="reflect-realitydont-distort-reality"></a>Återspegla verkligheten/förvräng inte verkligheten
Det går att skapa ett visuellt objekt som förvränger sanningen. Det finns en webbplats där dataentusiaster delar ”dåliga” visuella objekt. Det allmänna temat i kommentarerna är besvikelse på företaget som skapat och distribuerat det visuella objektet.  Det skickar ett budskap om att det inte går att lita på dem.

Så skapa visuella objekt som inte avsiktligt förvränger verkligheten och som inte har ändrats för att ge det budskap som du vill få fram.  Här är ett exempel:

![](media/power-bi-visualization-best-practices/corp-success-distorted.png)

**Bild 22:    Diagram med förvrängd verklighet**

Det verkar som om det är stor skillnad mellan de fyra företagen och att CorpB lyckas mycket bättre än de andra tre i det här exemplet.  Men observera att X-axeln inte börjar på noll och att skillnaderna mellan företagen sannolikt ligger inom felmarginalen.  Här är samma data med en X-axel som startar på noll.

![](media/power-bi-visualization-best-practices/corp-success.png)

**Bild 23:    Realistiskt diagram**

Läsarna förväntar sig och förutsätter ofta att X-axeln startar på noll. Om du väljer att inte börja på noll, bör du göra det på ett sätt som inte förvränger resultatet och dessutom lägga till en textruta som påpekar avvikelsen från normen.  

### <a name="design-elements"></a>Designelement
När du har valt en typ och ett mått samt skapat det visuella objektet är det dags att finjustera visningen för att få maximal effektivitet.  Det här avsnittet beskriver:

* Layout, utrymme och storlek
* Textelement: etiketter, kommentarer, menyer, rubriker
* Sortering
* Visuell interaktion
* Färg

#### <a name="tweaking-visuals-for-best-use-of-space"></a>Modifiera visuella objekt för att utnyttja utrymmet på bästa sätt
Om du försöker få plats med flera diagram i en rapport kan det hjälpa att maximera förhållandet mellan data och text för att budskapet i dina data ska nå fram. Som nämnts ovan myntade Edward Tufte uttrycket ”data-ink ratio” där målet är att ta bort så mycket som möjligt från ett diagram utan att försämra läsarens möjlighet att tolka datan.

I den första uppsättningen diagram nedan finns det överflödiga axeletiketter (Januari 2014, April 2014 etc.) och rubriker (”per Datum”). Rubrikerna för varje diagram kräver dessutom ett dedikerat vågrätt utrymme över varje diagram. Genom att ta bort diagramrubrikerna och aktivera separata axeletiketter försvinner viss text och vi kan använda det totala utrymmet på ett bättre sätt. Vi kan ta bort axeletiketterna för de två översta diagrammen för att få bort ytterligare text och få mer utrymme för datan.

Om det finns vissa tidsperioder som du vill lyfta fram, kan du rita linjer eller rektanglar bakom alla diagram för att rikta ögat uppåt och nedåt och underlätta jämförelser.

![](media/power-bi-visualization-best-practices/power-bi-multiples-before.png)

**Bild 24:    Före**

![](media/power-bi-visualization-best-practices/power-bi-multiples-after.png)

**Bild 25:    Efter**

**Att aktivera eller inaktivera axelrubriker**

Välj det visuella objektet för aktivera det och öppna formateringsfönstret. Visa alternativen för **X-axeln** eller **Y-axeln** och dra skjutreglaget för **Rubrik** på eller av.

![](media/power-bi-visualization-best-practices/power-bi-axis-titles.png)

**Bild 26:    Aktivera eller inaktivera axelrubriker**

**Aktivera eller inaktivera axeletiketter**

Välj det visuella objektet för aktivera det och öppna formateringsfönstret. Skjutreglagen finns bredvid **X-axeln** och **Y-axeln**.  Dra i skjutreglaget för att stänga på och av axelrubrikerna.

![](media/power-bi-visualization-best-practices/power-bi-axis-labels.png)

**Bild 27: Aktivera eller inaktivera axeletiketter**

> [!TIP]
> Ett scenario där du kan inaktivera Y-axelns etiketter är om du har stängt av **Dataetiketter**.
> 
> 

**Ta bort visuella rubriker**

Välj det visuella objektet för aktivera det och öppna formateringsfönstret. Ställ in skjutreglaget för **Rubrik** på Av.

![](media/power-bi-visualization-best-practices/power-bi-title-off.png)

**Bild 28:    Ta bort rubriker från visuella objekt**

Fundera på hur läsarna kommer att se rapporten och kontrollera att visuella objekt och text är tillräckligt stora och mörka för att kunna läsas. Om du har ett proportionellt större visuellt objekt på sidan kommer läsarna förutsätta att det är det viktigaste objektet. Ha tillräckligt med utrymme mellan de visuella objekten så att rapporten inte ser stökig och förvirrande ut.  Justera de visuella objekten så att läsarna vet var de ska rikta blicken.

**Ändra storlek på ett visuellt objekt**

Välj det visuella objektet för att aktivera det. Dra i ett av handtagen för att justera storleken.

![](media/power-bi-visualization-best-practices/power-bi-drag-handles.png)

**Bild 29: Ändra storlek på ett visuellt objekt**

**Flytta ett visuellt objekt**

Välj det visuella objektet för att aktivera det. Ta tag i handtagslisten överst i mitten på det visuella objektet och dra det till den nya platsen.

![](media/power-bi-visualization-best-practices/power-bi-move.png)

**Bild 30: Flytta ett visuellt objekt**

#### <a name="titles-and-labels-that-are-part-of-the-visualizations"></a>Rubriker och etiketter som ingår i visualiseringarna
Kontrollera att rubriker och etiketter är läsbara och självförklarande. Texten i rubriker och etiketter måste ha en optimal storlek med färger som står ut (till exempel svart i stället för standardgrå). Kommer du ihåg vår stilguide (se ”Text” ovan)? Begränsa antalet färger och storlekar – för många olika teckenstorlekar och färger gör utseendet stökigt och förvirrande.  Använd gärna samma teckenfärg och storlek för alla visuella objektrubriker på en rapportsida och välj samma justering för alla rubrikerna.  

**Formateringsfönstret**

Välj färgrollerikonen för att öppna formateringsfönstret vid varje formateringsjustering som visas nedan.

![](media/power-bi-visualization-best-practices/power-bi-paintbrush.png)

**Bild 31: Öppna formateringsfönstret**

Välj sedan det visuella element som ska justeras och kontrollera att det är aktiverat. Exempel på visuella element är: **X-axel**, **Y-axel**, **Rubrik**, **Dataetiketter** och **Förklaring**. Exemplet nedan visar elementet **Rubrik**.

![](media/power-bi-visualization-best-practices/power-bi-title-formatting.png)

**Bild 32: Formatera en visuell rubrik**

**Ange textstorleken**

Textstorleken kan justeras för rubriker och dataetiketter, men inte för X- eller Y-axlarna eller förklaringar.  När det gäller dataetiketter kan du testa olika alternativ i **Visningsenheter** och antal **Decimaler** tills du hittar den optimala detaljnivån för rapporten.   

**Ange textjusteringen**

Alternativen för rubrikjustering är vänster, höger och centrerad.  Välj samma inställning för alla visuella objekt på sidan.  

**Ange textplaceringen**

Textplaceringen kan justeras för vissa Y-axlar och för förklaringen.   Beroende på vilken du väljer gör du samma sak för de andra Y-axlarna och eventuella andra förklaringar på sidan.

**Ange längd för rubrik och etikett**

Justera längden på rubriker, axelrubriker, dataetiketter och förklaringar. Om du vill visa något av elementen justerar du längden (tillsammans med textstorleken) så att ingenting trunkeras. För **Rubrik** och **Förklaring** är inställningen **Rubriktext** och det är där du anger den faktiska rubrik som ska visas för det visuella objektet. För **X-axeln** och **Y-axeln** är inställningen **Stil** och du väljer alternativ i en listruta. För **Dataetiketter** är inställningarna **Visa** och **Decimal**. Använd listrutan **Visa** för att välja måttenheter: miljoner, tusen, ingen, automatisk osv. Använd fältet **Decimal** för att tala om för Power BI hur många decimaler som ska visas.

**Ange textfärgen**

Textfärgen kan justeras för rubriker, axlar och dataetiketter.  

#### <a name="titles-and-labels-that-are-not-part-of-the-visualizations"></a>Rubriker och etiketter som inte ingår i visualiseringarna
Tidigare i det här dokumentet visade vi hur man lägger till textrutor på rapportsidor. Ibland räcker det inte med visualiseringarnas rubriker för att få fram budskapet.  Lägg till textrutor för att ge ytterligare information till läsarna av dina rapporter.  
Se till att rapportsidan inte ser förvirrande eller stökig ut genom att vara konsekvent med din användning av textrutans teckensnitt, storlek, färger och justering. Om du vill göra en justering av texten i en textruta väljer du textrutan för att visa formateringsmenyn.

![](media/power-bi-visualization-best-practices/power-bi-text-box-edit.png)

**Bild 33: Formatera teckensnittet som används i en textruta**

#### <a name="sorting"></a>Sortering
Ett enkelt sätt att ge snabbare insikter är att ange sorteringen av visuella objekt. Genom att exempelvis sortera stapeldiagram i fallande eller stigande ordning baserat på värdet i staplarna, kan du snabbt visa viktig information utan att använda mer utrymme.

Om du vill sortera ett diagram trycker du på ellipserna (...) i det övre högra hörnet av diagrammet, väljer **Sortera** och sedan de fält som du vill sortera efter samt riktning. Mer information finns i [Ändra hur ett visuellt objekt sorteras](../consumer/end-user-change-sort.md).

#### <a name="chart-interaction-and-interplay"></a>Interaktion och samspel i diagram
En av de mest praktiska funktionerna i Power BI är möjligheten att ändra hur diagram interagerar med varandra.  Som standard är diagram korsmarkerade: när du markerar en datapunkt tänds relaterade data i andra diagram och orelaterade data tonas ned. Du kan åsidosätta detta beteende om du vill använda alla diagram som ett sant filter, vilket sparar utrymme på sidan. Gör detta genom att välja **Visuella interaktioner** på menyraden.

![](media/power-bi-visualization-best-practices/power-bi-visual-interactions.png)

**Bild 34: Visuella interaktioner**

För varje visuellt objekt bestämmer du sedan om du vill att det valda objektet ska filtrera, markera eller inte göra någonting. Det går inte att markera alla visuella objekt och för dem är kontrollen inte tillgänglig. Mer information finns i [Visuella interaktioner i Power BI](../consumer/end-user-interactions.md).

> [!TIP]
> Den här möjligheten att klicka på och interagera med rapporter kanske inte är omedelbart uppenbar för läsare som inte har använt Power BI förut. Lägg till textrutor som hjälper dem att förstå vad de kan klicka på för att hitta mer information.
> 
> 

#### <a name="the-use-of-color-in-visuals"></a>Användning av färg i visuella objekt
Tidigare i det här dokumentet talade vi om vikten av att ha en plan för hur du ska använda färg i en rapport. Det här avsnittet har vissa överlappningar men gäller främst för hur du använder färg i enskilda visuella objekt. Och samma principer gäller: Använd färg för att knyta ihop rapporten, lyfta fram viktiga data och förbättra läsarens förståelse av det visuella objektet. Om många olika färger används blir det svårt för läsaren att veta var man ska titta. Låt inte skönhet gå före förståelse. Lägg bara till färg om det förbättrar förståelsen.

> [!TIP]
> Tänk på vilken målgrupp du har och eventuella färgregler som finns.  I USA innebär exempelvis grönt ofta ”fungerande” och rött innebär ofta ”inte bra”.
> 
> 

Det här avsnittet är uppdelat i följande:

1. Datafärg
2. Färg på dataetikett
3. Färg för kategoriska värden
4. Färg för numeriska värden

**Lyft fram intressanta data med hjälp av färger**

Det enklaste sättet att använda färg på är genom att ändra en eller flera datapunktsfärger för att skapa uppmärksamhet. I det här exemplet ändras färgen när OS-spelen går från en 4-årscykel till en 2-årscykel för sommar- respektive vinterspelen.

![](media/power-bi-visualization-best-practices/power-bi-data-color.png)

**Bild 35:    Använd färg för att få fram ett budskap**

Du kan ändra datapunktsfärgerna på fliken **Datafärger** i formateringsfönstret. Om du vill anpassa varje datapunkt separat kontrollerar du att **Visa alla** är inställt som På.

![](media/power-bi-visualization-best-practices/power-bi-colors.png)

**Bild 36: Ange datapunktsfärger**

> [!NOTE]
> Power BI använder ett standardtema för rapportens visuella objekt.  Temafärgerna har valts för att ge variation och kontrast. Om du vill använda ett annat tema väljer du **Anpassad färg**.
> 
> 

![](media/power-bi-visualization-best-practices/power-bi-custom-color.png)

**Bild 37: Välj en anpassad färg**

I Power BI Desktop kan du även markera avvikare eller en del av en linje med hjälp av en andra serie:

![](media/power-bi-visualization-best-practices/power-bi-outliers.png)

**Bild 38:    Använd Desktop för att rita extremvärden**

I det här exemplet finns det endast värden i serien ”Extremvärden” när medeltemperaturen i augusti sjunker under 60 grader Fahrenheit. Detta gjordes genom att en DAX-beräknad kolumn skapades med följande formel:

Extremvärden = if(Editions[Temp]<60, Editions[Temp], BLANK())

I vårt exempel finns det 3 extremvärden: 1952, 1956 och 2000.

**Färger för etiketter och rubriker**

När du går igenom alla tillgängliga formateringsalternativ ser du att det finns många olika platser där du kan lägga till färg i rubriker och beskrivningar. Du kan till exempel ändra färgen på dataetiketter och axelrubriker. Tänk dig för innan du fortsätter.  I allmänhet bör du bara använda en enda färg för visuella rubriker.  Som med alla riktlinjer i det här dokumentet finns det alltid situationer och skäl till att ”bryta reglerna”, men om du bestämmer dig för att bryta reglerna, bör du ha en bra anledning till det.

**Färger för kategoriska värden**

Diagram med en serie har vanligtvis ett kategoriskt värde i förklaringen. Varje färg i förklaringen nedan motsvarar exempelvis en annan kategori för Land/region.

![](media/power-bi-visualization-best-practices/power-bi-bubble-color.png)

**Bild 39: Standardfärger som används**

De färger som används som standard i Power BI har valts för att ge en bra färgseparation mellan kategoriska värden så att de är lätta att skilja åt. Ibland händer det att företag ändrar färgerna för att matcha deras företagsprofil t.ex., men det kan ge problem.

![](media/power-bi-visualization-best-practices/power-bi-bubble-color2.png)

**Bild 40: Användning av nyanser av en enda färg**

Genom att en enda nyans med varierande intensitet av en färg används, finns det i det här visuella objektet en falsk känsla av ordning mellan kategorierna. Man tolkar det gärna som att mörkare bubblor ligger högre eller lägre på en skala än de ljusare nyanserna. Förutom alfabetiskt finns det vanligtvis ingen inbyggd ordning i den här typen av kategoriska värden.
Om du vill ändra standardfärgerna öppnar du formateringsfönstret och väljer **Datafärger**.

**Färger för numeriska värden**

För fält som har en inbyggd ordning och numeriska värden, kan du också färgsätta datapunkterna efter värdet. Detta kan vara bra för att visa spridningen av datavärden och kan även innebära att två variabler kan visas i ett enda diagram. Till exempel är det tydligt i det här diagrammet att även om Kina har det högsta medaljantalet, har Japan och Thailand deltagit i fler olympiska spel.

![](media/power-bi-visualization-best-practices/power-bi-saturation.png)

**Bild 41: Färgsätta datapunkter efter värde**

Lägg till ett värde i fältet Färgmättnad och justera sedan färgerna i formateringsfönstret för att skapa diagrammet.

![](media/power-bi-visualization-best-practices/power-bi-saturation2.png)

**Bild 42: Lägg till ett färgmättnadsfält**

![](media/power-bi-visualization-best-practices/power-bi-color-controls.png)

**Bild 43: Justera de färger som används för färgmättnaden**

Färg kan också användas för att betona avvikelser för ett centralt värde. Till exempel kan positiva värden vara gröna och negativa värden röda. Tänk på kulturella skillnader när du tilldelar färger till positiva eller negativa värden. Det är inte alla kulturer som använder rött för dåligt och grönt för bra!

![](media/power-bi-visualization-best-practices/power-bi-color.png)

**Bild 44:    Färg som lyfter fram avvikelser runt ett centralt värde**
 

### <a name="principles-of-visual-design--applied-to-example-report-page"></a>Principer för visuell design – tillämpat på en exempelrapportsida
Nu ska vi ta de visuella principer som beskrevs ovan och använda dem i vår exempelrapport.

Före

![](media/power-bi-visualization-best-practices/power-bi-example5a.png)

**Bild 45:    Vår exempelrapport (före)**

Efter

![](media/power-bi-visualization-best-practices/power-bi-example6anew.png)

**Bild 46: Vår exempelrapport (efter)**

#### <a name="what-did-we-do"></a>Vad har vi gjort?
1. Utsnitt: Tog bort tomma värden från utsnitten genom att lägga till ett sidnivåfilter och välja endast guld, silver och brons. Ändrade **Valkontroller** till Av för **Markera enstaka** och **Markera alla**.
2. Bubbeldiagram: Det finns så många objekt i förklaringen att de inte får plats på skärmen.  Tog bort förklaringen och aktiverade **Kategorietiketter** i stället. Kunderna kan hovra över bubblorna för att se informationen. Förkortade rubriken och tog bort ”per land/region” eftersom det verkar självklart. Aktiverade båda axeletiketterna för att göra det lättare att förstå diagrammet.
3. Koropletkarta: Ändrade **Datafärger** så att det framhävs bättre. Aktiverade **Divergerande** och angav **Minimum** till rosa och **Maximum** till röd.
4. Trädkarta: Tog bort filtret som endast angav USA. Ställde in **Dataetiketter** till 1 decimal. Det visuella objektet använde fältet Klass som inte är särskilt användbart eftersom det nästan alltid är 33 % (guld/silver/brons).  Valde ett annat mer intressant fält, nämligen Kön. Ändrade Vattensport till blå och Friidrott till grå i designen.
5. Övre stapeldiagram: Förkortade rubriken, tog bort dataetiketter, stängde av förklaringsrubriken. Ändrade ordföljden i rubriken för att matcha diagrammet nedan.
6. Nedre stapeldiagram: Sorterade stigande efter år för att matcha diagrammet ovan. Ändrade färger för att matcha klassen. Ändrade rubriken. Stängde av förklaringen för att få mer datautrymme. Aktiverade att dataetiketter inte ska visas i rapporten (eftersom det visuella objektet är för litet för att etiketterna ska gå att läsa), men att de visas när objektet öppnas i fokusläget. [Lär dig mer om fokusläget](../consumer/end-user-focus.md). Lade till Antal händelser (distinkta) i **Knappbeskrivningar**, så nu när du hovrar över en stående stapel får du i knappbeskrivningarna dessutom information om hur många händelser som har skett under året.
7. Visuella interaktioner: Stängde av interaktioner för båda korten eftersom jag vill att de alltid ska visa totalt antal spel och sporter.

## <a name="visual-types-and-best-practices"></a>Visuella typer och metodtips
Power BI innehåller många inbyggda visuella typer.  Förutom dessa finns det även anpassade visuella objekt hos Microsoft och i Power BI Community, vilket innebär att det finns för många visuella alternativ för att de ska gå att beskriva här. Låt oss i stället titta på några av de mest använda inbyggda visuella typerna.  

### <a name="line-charts"></a>Linjediagram
![](media/power-bi-visualization-best-practices/power-bi-line-chartb.png)

Linjediagram är ett kraftfullt sätt att visa data över tid.  När man tittar på data i tabeller går det inte lika snabbt att upptäcka toppar, dalar, cykler och mönster.  
I exemplet nedan visas trender i antalet medaljer som delats ut och antalet idrottare som vunnit dessa medaljer.  

![](media/power-bi-visualization-best-practices/power-bi-line-chart.png)

**Bild 47:    Linjediagram**

#### <a name="best-practices"></a>Metodtips
* När man ser ett linjediagram brukar man notera formen på kurvan först.  Det innebär att du måste ha en X-axel som gör kurvan meningsfull, som exempelvis tid eller fördelningskategorier.  Om du placerar kategoriska fält som produkt och geografi på X-axeln blir linjediagrammet inte intressant eftersom formen på kurvan inte visar någon användbar information.
* Om du väljer att placera flera diagram över och under varandra så här, blir det lättare att göra jämförelser mellan serierna. Använd filter för att se till att samma värdeintervall visas.  Om du till exempel ska granska datumintervall bör du kontrollera att diagrammen har samma intervall.  Till exempel 1896 till 2012 i båda diagrammen.
* Utnyttja utrymmet.  Om det passar för dina data kan du ange start- och slutpunkterna för Y-axeln så att du eliminerar det tomma utrymmet högst upp och längst ned i diagrammet och fokuserar på de faktiska datapunkterna. Välj färgrollerikonen för att öppna formateringsfönstret och göra detta. Expandera området **Y-axel** och ange **Start**- och **Slut**punkterna.
  
  ![](media/power-bi-visualization-best-practices/power-bi-start-end.png)
  
  **Bild 48: Ange start- och slutpunkter**
* Ett annat skäl till att ange start- och slutpunkter är om du ska jämföra två eller flera diagram på samma sida med samma fält för Y-axeln.  Om du till exempel tittar på kumulativa händelseantal och Storbritannien har ett antal mellan 1 och 70 och Australien har ett antal mellan 1 och 12, kommer de två linjediagrammen visa mycket olika Y-axlar (bild x). Det gör det svårt att jämföra med en snabb blick. Ange i stället att diagrammen ska använda samma Y-axelintervall (bild x).
  
  ![](media/power-bi-visualization-best-practices/power-bi-line-chart2.png)
  
  **Bild 49: Linjediagram med olika Y-axlar**
  
  ![](media/power-bi-visualization-best-practices/power-bi-line-chart3.png)
  
  **Bild 50: Linjediagram med matchande Y-axlar**

Mer information finns i:

* [Anpassa X och Y-axlarna](power-bi-visualization-customize-x-axis-and-y-axis.md)
* [Linjediagram och oregelbundna intervall](http://www.perceptualedge.com/articles/visual_business_intelligence/line_graphs_and_irregular_intervals.pdf)
* [Linjediagram 101](http://www.columnfivemedia.com/data-visualization-101-line-charts)

### <a name="barcolumn-charts"></a>Stapel-/kolumndiagram
![](media/power-bi-visualization-best-practices/power-bi-bar-chart.png)

Om linjediagram är standard för att granska data över tid, är stapeldiagram standarden för att titta på ett specifikt värde i olika kategorier.  Om du sorterar staplarna baserat på antal ser du omedelbart de högsta värdena och fördelningen.  Vågräta stapeldiagram fungerar bra med långa etiketter.  

![](media/power-bi-visualization-best-practices/power-bi-horizontal-scroll.png)

**Bild 51: Vågrätt stapeldiagram**

#### <a name="best-practices"></a>Metodtips
* Visa dataetiketter för värden.  Detta gör det enklare att identifiera specifika värden. Gör detta genom att öppna formateringsfönstret och ange **Dataetiketter** till På.
  
  ![](media/power-bi-visualization-best-practices/power-bi-data-labels.png)
  
  **Bild 52: Aktivera dataetiketter**
* Diagrammet ovan är användbart när man ska jämföra ett mått med många **vid en enskild tidpunkt**.  Medan linjediagrammet ovan visade oss en trend över tid, visar stapeldiagrammet oss trenden för en enskild kategori vid en viss tidpunkt.  Vid en snabb blick visar vårt stapeldiagram oss att Spanien har den värsta arbetslösheten i världen med 25 procent.
* När ett helt stapel-/kolumndiagram inte får plats i det tilldelade utrymmet, lägger Power BI dit rullningslister. Vid behov bör du strukturera det visuella objektet och rapporten så att hela diagrammet visas, för att läsaren ska få en översikt över hela fördelningen.  Detta är tyvärr inte möjligt i vårt exempel på grund av det stora antalet länder i världen.
  
  Ett sätt att begränsa de värden som ingår är att använda ett filter. Man kan till exempel lägga till ett visuellt nivåfilter som endast visar landet om arbetslösheten är högre än 20 %.
* Man kan både öka och minska detaljnivån i stapel-/kolumndiagram.  Detta är ett bra sätt att få in mer information i ett visuellt objekt utan att ta upp mer utrymme.  I exemplet nedan finns en hierarki för Regioner > Länder.  Om du dubbelklickar på ett regionsfält ökas detaljnivån till de länder som utgör den regionen.  Mer information om detaljnivåer finns i [Öka detaljnivån i en visualisering](../consumer/end-user-drill.md).
  
  ![](media/power-bi-visualization-best-practices/power-bi-drill.png)
  
  **Bild 53: Öka detaljnivån**

Mer information om stapel-/kolumndiagram:

* [Stapeldiagram 101](http://blog.newscred.com/article/data-visualization-101-bar-charts)
* [Datavisualiseringskatalog: Stapeldiagram](http://www.datavizcatalogue.com/methods/bar_chart.html#.VYV-hY3bLJw)
* [Datavisualiseringskatalog: Multimängd i stapeldiagram](http://www.datavizcatalogue.com/methods/multiset_barchart.html#.VYV_gI3bLJw)

### <a name="stacked-barcolumn-charts"></a>Liggande/stående stapeldiagram
![](media/power-bi-visualization-best-practices/power-bi-stacked.png)

Lägg till en annan dimension i stapel-/kolumndiagrammen genom att stapla olika kategorier i stapeln eller kolumnen.  Nu visar diagrammet information om en övergripande trend (baserat på höjd/längd), men också påverkan på kategorierna i denna trend. I diagrammet nedan visas den övergripande tillväxten för elitfotbollslagens intäkter över 6 miljarder 2014.

![](media/power-bi-visualization-best-practices/power-bi-deloite.png)

**Bild 54: Stående stapeldiagram**

I det stående stapeldiagrammet ser vi att den totala intäkten ökar med tiden och att marknadsförings- och sändningskategorierna växer stadigt över tid – vilket bidrar till ökade övergripande intäkter.  Men det här diagrammet gör inte det lättare att jämföra effekten som de tre kategorierna har på varandra. Hur ökar till exempel marknadsföringen jämfört med ökad sändning eller fler matchdagar?  Ett bättre alternativ för dessa data eller ett åtföljande visuellt objekt är ett linjediagram.  

![](media/power-bi-visualization-best-practices/power-bi-deloite2.png)

**Bild 55: Konvertera till ett linjediagram**

I det här linjediagrammet är det lättare att se hur de kommersiella intäkterna har växt mest till följd av sändning och matchdag.

#### <a name="best-practices"></a>Metodtips
* Precis som med kolumner/staplar kan du välja att visa diagrammet vågrätt eller lodrätt.   Vågrätt är bättre om du har långa etiketter och lodrätt passar bra om du har tidsseriedata.  
* Undvik liggande/stående stapeldiagram om du vill visa trender och andra mönster för förändringar över tid.  Andra diagram, som exempelvis linjediagram, är mycket bättre.
* Du kan också låta fördelningen baseras på total volym eller som en procentandel av summan.  
* Som Few visade *är det svårt att jämföra segmenten i en staplad liggande stapel. Om segmenten har ordnats sida vid sida och alla går upp från samma baslinje är det enkelt att jämföra deras höjd, men när de staplas ovanpå varandra blir det svårt. Plus att även om det är ganska enkelt att se hur intäkterna ändrats från månad till månad, är det mycket svårt att se hur intäkterna i de andra kategorierna ändrats*.  
* 100 % diagram är ett bra val när du använder procenttal som tillsammans utgör 100.  I exemplet nedan visas kategorifördelningen per lag.  Procenttalen är relativa och innebär att vi ser mönster med en snabb blick. Till exempel kommer Evertons intäkter främst från sändningar (drygt 70 %), medan PSG:s intäkter bara har 20 % av sina intäkter från sändningar.  Valet av en vågrät visning gör det enklare att få plats med lagetiketterna och se effekten av intäktstypen.
  
  ![](media/power-bi-visualization-best-practices/power-bi-deloite3.png)
  
  **Bild 56: Vågrätt stapeldiagram**

Mer information om stapeldiagram:

* [Datavisualiseringskatalog: liggande stapeldiagram](http://www.datavizcatalogue.com/methods/stacked_bar_graph.html#top)
* [När är 100 % liggande stapeldiagram användbara?](http://www.perceptualedge.com/blog/?p=2239)

### <a name="combo-barcolumn-charts"></a>Kombinerade stapel-/kolumndiagram
![](media/power-bi-visualization-best-practices/power-bi-combo.png)

I Power BI kan du kombinera kolumn- och linjediagram till ett kombinationsdiagram. Alternativen är: stående linje- och stapeldiagram samt grupperad linje- och stapeldiagram. Spara värdefull arbetsyta genom att kombinera två separata visuella objekt till ett.

De två skärmbilderna nedan visar en före- och en efterbild.  På den första sidan finns två separata visuella objekt: Ett kolumndiagram som visar befolkning över tid och ett linjediagram som visar BNP över tid. Dessa diagram skulle passa bra som kombinationsdiagram eftersom de har samma X-axel (år) och värden (2002 till 2012).  Varför inte kombinera dem och jämföra dessa två trender i ett enda visuellt objekt?  Om du kombinerar de två diagrammen kan du göra en snabbare jämförelse av datan.

Den nya rapportsidan har ett enda visuellt objekt: Ett stående linje- och stapeldiagram. Vi kunde lika enkelt skapat ett linje- och grupperat stapeldiagram.  Nu är det ännu enklare att söka efter en relation mellan de två trenderna.   Vi kan se att fram till 2008 följde befolkning och BNP ungefär samma trend. Men från och med 2009 när befolkningstillväxten planade ut, blev BNP:n rörligare.  

![](media/power-bi-visualization-best-practices/power-bi-spain-line.png)

 **Bild 57: Som två separata diagram**

![](media/power-bi-visualization-best-practices/power-bi-spain-combo.png)

 **Bild 58: Som ett enda kombinationsdiagram**

#### <a name="best-practices"></a>Metodtips
Kombinationsdiagram fungerar bäst när minst en axel är gemensam för båda visuella objekten.

Ha koll på din axlar! Är ditt kombinationsdiagram enkelt att läsa och tolka?  Eller använder det olika intervall och värden? Om till exempel skalan för kolumndiagrammets Y-axel är mycket mindre än skalan för Y-axeln i linjediagrammet kommer kombinationsdiagrammet inte vara meningsfullt.  Se exempelvis den tredje linjen (turkos) i nederkant.

   ![](media/power-bi-visualization-best-practices/power-bi-dual-line.png)

   **Bild 59: Ett misslyckat linjediagram**

Så kombinationsdiagrammet är inte meningsfullt om ditt kolumndiagram och linjediagram använder två olika mått och du inte har skapat dubbla axlar.  Till exempel dollar jämfört med procent. Se till att inkludera båda axlarna för att läsaren ska förstå diagrammet och lägg gärna till axeletiketter också.

Gör detta genom att öppna formateringsfönstret, expandera **Y-axeln** och ange **Visa sekundär** till På (om den inte redan är aktiverad). Den här inställningen är ibland svår att hitta: Expandera **Y-axeln (kolumn)** och rulla nedåt tills du ser **Visa sekundär**. Ange dessutom Y-axelns (kolumn) **Rubrik** till På och ange Y-axelns (rad) **Rubrik** till På.

![](media/power-bi-visualization-best-practices/power-bi-show-secondary-new.png)

**Bild 60: Visa sekundäraxeln**

![](media/power-bi-visualization-best-practices/power-bi-combo-chart.png)

**Bild 61: Skapa ett kombinationsdiagram i stället**

* Dra nytta av dubbla axlar. Detta är ett bra sätt för att jämföra flera mått med olika värdeintervall. Och det är ett bra sätt för att visa sambandet mellan två mått i ett visuellt objekt.

För mer information:

* [Kombinationsdiagram i Power BI](power-bi-visualization-combo-chart.md)
* [Risken med dubbelskalade axlar i visuella objekt](http://www.perceptualedge.com/articles/visual_business_intelligence/dual-scaled_axes.pdf)

### <a name="scatter-chart"></a>Punktdiagram
![](media/power-bi-visualization-best-practices/power-bi-scatter.png)

Ibland kan vi ha många variabler som vi vill se tillsammans. Då kan ett punktdiagram vara ett praktiskt sätt att få en övergripande bild.  Punktdiagram visar relationer mellan två (punkter) eller tre (bubblor) kvantitativa mått.  Ett punktdiagram har alltid två värdeaxlar som visar en uppsättning numeriska data längs en vågrät axel och en annan uppsättning numeriska värden längs en lodrät axel. Diagrammet visar punkter i skärningspunkten för ett numeriskt X- och Y-värde och kombinerar dessa värden till separata datapunkter. Dessa datapunkter kan vara jämnt eller ojämnt fördelade på den horisontala axeln, beroende på datan.

Ett bubbeldiagram ersätter datapunkterna med bubblor, med en bubbelstorlek som motsvarar en dimension av datan.

Nedanstående bubbeldiagram visar Sydamerika och jämför BNP per capita (Y-axeln), summan av BNP (X-axeln) och befolkning per sydamerikanskt land.  Storleken på bubblorna motsvarar den totala befolkningen för landet i fråga. Brasilien har den största befolkningsmängden (bubbelstorlek) och den största andelen av Sydamerikas BNP (den är längst bort på X-axeln).  Men observera att BNP per capita för Uruguay, Chile och Argentina är högre än Brasilien (längre upp på Y-axeln).

![](media/power-bi-visualization-best-practices/power-bi-bubble.png)

**Bild 62: Sydamerikas BNP och befolkning som bubbeldiagram**

Om du lägger till en uppspelningsaxel kan du låtsas att du är Hans Rosling och visa budskapet över tid (https://www.youtube.com/watch?v=PbaDBJWCeD4). Lägg till en uppspelningsaxel genom att dra ett datumtid-fält till **Uppspelningsaxel**.

#### <a name="best-practices"></a>Metodtips
* Punktdiagram och bubbeldiagram är bra när man ska få fram ett budskap. Men de är inte så användbara när man ska granska datan.  Stephen Few pekar på detta i avsnittet nedan *Styrkan i den här metoden är när den används för att få fram ett budskap. När Rosling tolkar vad som händer i diagrammet medan bubblorna flyttas runt och ändrar värden, pekar han på det han vill att vi ska se vilket gör informationen levande. Animerade bubbeldiagram är dock mycket mindre effektiva när vi vill granska datan och få en uppfattning om den. Jag tvivlar på att Rosling använde den här metoden för att identifiera budskapet, utan endast använde den för att informera om det när det var känt. Vi kan inte fokusera på mer än en bubbla i taget eftersom de flyttas runt, så vi måste köra animeringen flera gånger att få en uppfattning om vad som händer. Vi kan lägga till spår till valda bubblor för att kunna granska hela sökvägen för bubblorna, men om man använder spår för fler bubblor blir diagrammet snabbt för stökigt. I princip anser jag att detta inte är det bästa sättet för att visa information vid analys och undersökning.*
* Lägg till X- och Y-axeletiketter som stöd.  Särskilt i bubbeldiagram finns det många komponenter för uppspelning och etiketter som hjälper läsarna att förstå det visuella objektet.
* Genom att lägga till dataetiketter blir det lättare att tolka det visuella objektet.  Särskilt i bubbeldiagram med många objekt i förklaringen, kan det vara svårt att skilja mellan liknande färger.  I det visuella objektet ovan är förklaringsfärgerna för Surinam, Columbia och Ecuador mycket lika.
* Har du skapat ett punktdiagram där du bara ser en datapunkt som samlar alla värdena på X- och Y-axlarna? Eller samlar diagrammet alla värden längs en enda vågrät eller lodrät linje?  Lös problemet genom att lägga till ett fält i området **Information** som talar om för Power BI hur värdena ska grupperas. Fältet måste vara unikt för varje punkt som du vill rita. Mer hjälp finns i [Självstudie för Power BI:s punkt- och bubbeldiagram](power-bi-visualization-scatter.md).

### <a name="tree-map-charts"></a>Diagram med trädkartor
![](media/power-bi-visualization-best-practices/power-bi-treemap.png)

Trädkartor kan vara mycket användbara för att ge en bra översikt över den relativa storleken på olika komponenter som utgör en helhet, särskilt när du kan gruppera dem i kategorier.  När jag tittar på ett nytt företag är en trädkarta med huvudkomponenterna mycket användbar för att se den övergripande fördelningen.

I det första diagrammet nedan ser du direkt att Brasilien utgör cirka hälften av Sydamerikas BNP samt att Venezuela och Argentina är av ungefär samma storlek.

Om du vill se ett större sammanhang men ändå ha en uppfattning om effekten av de största bidragande länderna, kan du skapa visuella hierarkier med kategorimedlemmar (länder) inuti regioner. I den andra trädkartan kan vi först och främst se den relativa storleken på regionerna och därefter kan vi i varje region se vilka enskilda länder som bidrar mest. Vi kan se att det finns tre stora regioner (Europa, Asien och Nordamerika) och bland dem är det enkelt att se de främsta länderna/regionerna.

Den största begränsningen för trädkartor är möjligheten att jämföra olika rektanglar utöver de översta.  Det är ett bra diagram för att få en översikt, men kolumn- och stapeldiagram är förmodligen ett bättre alternativ om man vill få bättre uppfattning om den relativa storleken på olika komponenter.
 
Till exempel ger den första trädkartan en övergripande indikation på BNP-storleken, men det är svårt att se specifika skillnader mellan länderna, särskilt i de mindre omärkta rutorna. För dessa data där en enda gruppering jämförs, kan ett stapel- eller kolumndiagram vara ett bättre alternativ.

![](media/power-bi-visualization-best-practices/power-bi-treemap3.png)

**Bild 63: BNP-jämförelse för Sydamerika som en trädkarta**

Här vi har lagt till region som ytterligare en datanivå och vi kan se det övergripande bidraget till BNP per region samt den relativa påverkan som finns inom regionerna. Var försiktig om du gör detta med icke-summerade mått (till exempel medelvärden) eftersom summan av informationen kanske inte motsvarar det faktiska värdet på den sammanräknade nivån.

![](media/power-bi-visualization-best-practices/power-bi-treemap2.png)

**Bild 64: BNP per region och land som en trädkarta**

Mer information om trädkartor får du om du klickar på länkarna nedan.

* [Översikt över trädkartor](http://www.perceptualedge.com/articles/b-eye/treemaps.pdf)
* [Datavisualiseringskatalog: Trädkartor](http://www.datavizcatalogue.com/methods/treemap.html#.VYhylI3bL7Y)

### <a name="other-charts"></a>Andra diagram
#### <a name="pie-or-donut-charts"></a>Cirkel- eller ringdiagram
![](media/power-bi-visualization-best-practices/power-bi-donut.png)

Stapel-, kolumn- och linjediagram fungerar i allmänhet för de flesta ändamål. Det är välkänt att cirkel- och ringdiagram är svåra att tolka på rätt sätt och i praktiken ofta kan förvränga data. Undvik dem om möjligt. Stephen Few har en utmärkt beskrivning av historiken och farorna i [Save the Pies for Dessert] ([www.percetualedge.com/articles/08-21-07.pdf](http://www.perceptualedge.com/articles/08-21-07.pdf)

Han förklarar den enda gång när cirkeldiagram kan vara användbara, nämligen när man jämför relationer mellan delar och helheter. Men inte ens detta är bättre än exempelvis ett 100 % liggande stapeldiagram.

En annan rolig artikel (och animering) om cirkeldiagram finns på [Darkhorse Analytics webbplats](http://www.darkhorseanalytics.com/blog/salvaging-the-pie).

#### <a name="radial-gauges--kpis"></a>Radiella mätare och KPI:er
![](media/power-bi-visualization-best-practices/power-bi-gauge.png)

Radiella mätare verkar vara ett bra visuellt objekt som visar prestanda gentemot ett mål och de är mycket populära i ledningsgruppers instrumentpaneler. Men de har två brister. Precis som med cirkeldiagram är det svårt att tolka vinkeln för det skuggade området jämfört med en fullständig 180 grader båge eller mållinje. Dessutom används mycket utrymme för att visa ett enda mått.

Ett bra alternativ är en enkel visuell KPI

![](media/power-bi-visualization-best-practices/power-bi-kpi.png)

KPI:er visar värde, status, mål, målavvikelse och trend i samma mängd utrymme. Den gröna färgen blir röd om målet inte uppfylls och kan vara gul om vissa mellanliggande mål uppnås. De är mycket enklare att läsa och tolka än mätaren.

Mer information finns i:

* [Diagram med radiella mätare i Power BI](power-bi-visualization-radial-gauge-charts.md)
* [KPI:er i Power BI](power-bi-visualization-kpi.md)

## <a name="conclusion"></a>Slutsats
Nu är det dags att börja använda dessa metodtips.  Håll kontakten med oss och dela med dig av dina egna metodtips. Är du inte överens med oss om våra rekommendationer eller har du en bra anledning till att ”bryta reglerna”?  Vi vill gärna höra om det också.  

### <a name="book-recommendations"></a>Boktips
Det finns många bra böcker i dag som kan hjälpa till att förbättra den visuella designtekniken. Stephen Fews bok *Information Dashboard Design* är nästan ett måste att läsa. Han går även på djupet i två andra böcker, *Show Me the Numbers* och *Now You See It*. Både Few och andra författare har hämtat inspiration från Edward R. Tufte, vars bok *The Visual Display of Quantitative Information* betraktas som en klassiker inom detta område. Tufte har också skrivit *Visual Explanations*, *Envisioning Information* och *Beautiful Evidence*. Anders Kirks nya bok *Data Visualization: A Handbook for Data Driven Design* är ett annat bra alternativ. Andra författare som rekommenderas är: Lachlan James, William McKnight och Boris Evelson (Forrester), Darkhorse Analytics.

Har du fler frågor? [Prova Power BI Community](http://community.powerbi.com/)

