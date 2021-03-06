---
title: Ringdiagram i Power BI
description: Ringdiagram i Power BI
author: mihart
manager: kvivek
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-desktop
ms.topic: conceptual
ms.date: 09/24/2018
ms.author: mihart
LocalizationGroup: Visualizations
ms.openlocfilehash: ab292964bb1b6b1f4218d41c46eb2c28c82a034c
ms.sourcegitcommit: ce8332a71d4d205a1f005b703da4a390d79c98b6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/27/2018
ms.locfileid: "47416761"
---
# <a name="doughnut-charts-in-power-bi"></a>Ringdiagram i Power BI
Ett ringdiagram liknar ett cirkeldiagram såtillvida att det visar förhållandet mellan delarna och helheten. Den enda skillnaden är att mitten är tom och har utrymme för en etikett eller ikon.

## <a name="create-a-doughnut-chart"></a>Skapa ett ringdiagram
De här anvisningarna använder exemplet på detaljhandelsanalys för att skapa ett cirkeldiagram som visar försäljning detta år efter kategori. Om du vill följa med kan du [hämta exemplet](../sample-datasets.md) för Power BI-tjänsten eller Power BI Desktop.

1. Börja med en [tom rapportsida](../power-bi-report-add-page.md). Om du inte använder Power BI-tjänsten, se till att du öppnar rapporten i [Redigeringsvyn](../service-interact-with-a-report-in-editing-view.md).

2. I Fält-panelen, väljer du **Försäljning** \> **Senaste årets försäljning**.  
   
3. I fönstret visualiseringar, väljer du ikonen för cirkeldiagrammet ![cirkeldiagramsikonen](media/power-bi-visualization-doughnut-charts/power-bi-icon.png) för att konvertera ditt stapeldiagram till ett cirkeldiagram. Om **Fjolårets försäljning** inte är i **Värden**-området, drar du det dit.
     
   ![Visualiseringsfönstret med ringdiagram har valts](media/power-bi-visualization-doughnut-charts/power-bi-doughnut-chart.png)

4. Välj **Objekt** \> **Kategori** för att lägga till den i området **Förklaring**. 
     
    ![ringdiagram bredvid fönstret Fält](media/power-bi-visualization-doughnut-charts/power-bi-doughnut-done.png)

5. Du kan också [justera storlek och färg för diagramtexten](power-bi-visualization-customize-title-background-and-legend.md). 

## <a name="considerations-and-troubleshooting"></a>Överväganden och felsökning
* Summan av ringdiagrammets värden måste uppgå till 100 %.
* För många kategorier gör det svårt att läsa och tolka översikten.
* Ringdiagram är bättre för att jämföra en särskild sektion med helheten än för att jämföra enskilda sektioner med varandra. 

## <a name="next-steps"></a>Nästa steg
[Trattdiagram i Power BI](power-bi-visualization-funnel-charts.md)

[Visualiseringstyper i Power BI](power-bi-visualization-types-for-reports-and-q-and-a.md)


