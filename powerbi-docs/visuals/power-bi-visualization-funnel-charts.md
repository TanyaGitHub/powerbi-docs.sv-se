---
title: Trattdiagram
description: Trattdiagram i Power BI
author: mihart
manager: kvivek
ms.reviewer: ''
featuredvideoid: maTzOJSRB3g
ms.service: powerbi
ms.component: powerbi-desktop
ms.topic: conceptual
ms.date: 09/24/2018
ms.author: mihart
LocalizationGroup: Visualizations
ms.openlocfilehash: 962f76666e4b139b24225daefd5af776f36b3d0d
ms.sourcegitcommit: ce8332a71d4d205a1f005b703da4a390d79c98b6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/27/2018
ms.locfileid: "47416945"
---
# <a name="funnel-charts"></a>Trattdiagram
Med ett trattdiagram kan du visualisera en linjär process med intilliggande steg. Ett trattdiagram över försäljning som följer kunderna genom stadier: \>Uppslag \> Uppslag med potential \> Kontrakt \> Sälj.  Trattens form ger en översikt över processens tillstånd.

Varje steg i trattens motsvarar en procentandel av det totala antalet. I de flesta fallen är ett trattdiagram format som en tratt, där det första stadiet är störst och varje följande steg är mindre än det föregående.  En päronformad tratt kan också vara användbar – den kan identifiera ett problem i processen.  Men vanligtvis är det första stadiet, ”intaget”, det största.

![exempel på blå tratt](media/power-bi-visualization-funnel-charts/funnelplain.png)

## <a name="when-to-use-a-funnel-chart"></a>När du ska använda ett trattdiagram
Trattdiagram är ett bra alternativ:

* När data är sekventiella och går genom minst 4 steg.
* När antalet ”objekt” i det första steget förväntas vara större än antalet i det sista steget.
* Om du vill beräkna potential (intäkter, försäljning, erbjudanden osv) i etapper.
* Om du vill beräkna och spåra konvertering och kvarhållning.
* Om du vill avslöja flaskhalsar i en linjär process.
* Om du vill spåra arbetsflödet i en kundvagn.
* Om du vill spåra förloppet och resultaten a en klickbaserad reklam-/marknadsföringskampanj.

## <a name="working-with-funnel-charts"></a>Arbeta med trattdiagram
Trattdiagram:

* Kan fästas från rapporter och frågor och svar.
* Kan sorteras.
* Stöd för multipler.
* Kan markeras och korsfiltreras mot andra visualiseringar på samma rapportsida.
* Kan användas för markera och korsfiltrera andra visualiseringar på samma rapportsida.

## <a name="create-a-basic-funnel-chart"></a>Skapa ett enkelt trattdiagram
Se hur Will skapar ett trattdiagram med exemplet på försäljning och marknadsföring i den här videon.

<iframe width="560" height="315" src="https://www.youtube.com/embed/qKRZPBnaUXM" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>


Nu kan du skapa ett eget trattdiagram som visar antalet möjligheter i varje försäljningsstadium.

Dessa anvisningar använder sig av Exempel på affärsmöjlighetsanalys. Om du vill följa med kan du [hämta exemplet](../sample-datasets.md) för Power BI-tjänsten (app.powerbi.com) eller Power BI Desktop.   

1. Starta på en [tom rapportsida ](../power-bi-report-add-page.md) och välj fältet **SalesStage** \> **Försäljningssteg**. Om du inte använder Power BI-tjänsten, se till att du öppnar rapporten i [Redigeringsvyn](../service-interact-with-a-report-in-editing-view.md).
   
    ![välj försäljningsfas](media/power-bi-visualization-funnel-charts/funnelselectfield_new.png)
2. [Konvertera diagrammet](power-bi-report-change-visualization-type.md) till en tratt. Observera att **Försäljningssteg** är i brunnen **Grupp**. 
3. Från fönstret **Fält** väljer du **Fakta** \> **Antal affärsmöjligheter**.
   
    ![skapa trattdiagram](media/power-bi-visualization-funnel-charts/power-bi-funnel.png)
4. Håll muspekaren över en stapel för att visa en mängd information.
   
   * Stegets namn
   * Antalet affärsmöjligheter som finns i det här steget just nu
   * Övergripande konverteringstakt (% av leads) 
   * Steget-till-steg (kallas även förlusttakt) som är % av det föregående steget (i det här fallet förslagssteg/lösningssteg)
     
     ![information om förslagsfält](media/power-bi-visualization-funnel-charts/funnelhover_new.png)
5. [Lägg till tratten som panel i instrumentpanelen](../service-dashboard-tiles.md). 
6. [Spara rapporten](../service-report-save.md).

## <a name="highlighting-and-cross-filtering"></a>Markering och korsfiltrering
Information om hur du använder filterfönstret finns i [Lägg till ett filter i en rapport](../power-bi-report-add-filter.md).

Om du markerar ett fält i trattdiagrammet korsfiltreras de övriga visualiseringarna på rapportsidan, och vice versa. Följ med och lägg till ytterligare några visuella objekt på rapportsidan som innehåller trattdiagrammet.

1. Välj fältet **Förslag** i trattdiagrammet. Detta korsmarkerar de övriga visualiseringarna på sidan. Använd CTRL för att välja flera.
   
   ![kort video som visar visuella interaktioner](media/power-bi-visualization-funnel-charts/funnelchartnoowl.gif)
2. För att hantera hur diagram korsmarkeras och korsfiltrerar varandra, se [Visualiseringsinteraktioner i en Power BI-rapport](../service-reports-visual-interactions.md)

## <a name="create-a-funnel-chart-using-qa"></a>Skapa ett trattdiagram med frågor och svar
Öppna instrumentpanelen exempel på analys av affärsmöjligheter eller en instrumentpanel som har minst en visualiseringen fäst från datauppsättningen för exempel på analys av affärsmöjligheter.  När du skriver en fråga i Frågor och svar söker Power BI efter svar i alla datauppsättningar som är associerade med (har fästa paneler) den valda instrumentpanelen. Mer information finns i [Power BI – grundläggande koncept](../service-basic-concepts.md).

1. I instrumentpanelen för exemplet på analys av affärsmöjligheter, skriver du in din fråga i frågerutan Frågor och svar.
   
   ![frågeruta och tratt](media/power-bi-visualization-funnel-charts/power-bi-qna.png)
   
2. Var noga med att lägga till ”som tratt” så att Power BI vet vilken typ av visuellt objekt som du föredrar.

## <a name="next-steps"></a>Nästa steg

[Mätare i Power BI](power-bi-visualization-radial-gauge-charts.md)

[Visualiseringstyper i Power BI](power-bi-visualization-types-for-reports-and-q-and-a.md)
