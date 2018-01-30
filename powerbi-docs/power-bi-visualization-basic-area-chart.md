---
title: "Grundläggande ytdiagram (självstudie)"
description: "Självstudie: Grundläggande ytdiagram."
services: powerbi
documentationcenter: 
author: mihart
manager: kfile
backup: 
editor: 
tags: 
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 09/27/2017
ms.author: mihart
ms.openlocfilehash: 42e068b11c22c32f1a6736a6ca8f9020594fb40a
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/15/2017
---
# <a name="basic-area-chart-tutorial"></a>Grundläggande ytdiagram (självstudie)
Det grundläggande ytdiagrammet (även känt som överlappande områdesdiagram) baseras på linjediagrammet. Området mellan axel och linje fylls med färger för att illustrera volym. 

Ytdiagrammet framhäver omfattningen av förändring över tid och kan användas för att uppmärksamma totalvärdet över en trend. Data som representerar vinst över tid kan till exempel ritas i ett ytdiagram för att betona den totala vinsten.

![](media/power-bi-visualization-basic-area-chart/powerbi-area-chartnew.png)

## <a name="when-to-use-a-basic-area-chart"></a>När ska du använda ett grundläggande ytdiagram
Grundläggande ytdiagram är ett bra val:

* för att se och jämföra volymtrenden över tidsserier 
* för enskilda serier som representerar en fysiskt kvantifierbar uppsättning

## <a name="create-a-basic-area-chart"></a>Skapa ett grundläggande ytdiagram
Om du vill följa anvisningarna loggar du in till Power BI och väljer **Hämta data \> Exempel \>Exempel på detaljhandelsanalys**. 

1. Välj **Totalt antal butiker** från instrumentpanelen ”Exempel på detaljhandelsanalys” för att öppna rapporten ”Exempel på detaljhandelsanalys”.
2. Välj **Redigera rapport** för att öppna rapporten i redigeringsvyn.
3. Lägg till en ny rapportsida.
4. Skapa ett ytdiagram som visar årets försäljning och förra årets försäljning per månad.
   
   a.  Från den **Fältfönstret**, väljer du **Försäljning \> förra årets försäljning** och **försäljning detta år > värde**.
   
   b.  Konvertera diagrammet till ett grundläggande ytdiagram.    
   ![](media/power-bi-visualization-basic-area-chart/convertchart.png)
   
   c.  Välj **Tid \> Månad** för att lägga till det i **Axel**-brunnen.   
   ![](media/power-bi-visualization-basic-area-chart/powerbi-area-chartnew.png)
   
   d.  Om du vill visa diagrammet efter månad, väljer du ellipserna (övre högra hörnet av visualiseringen) och väljer **sortera efter månad**.

## <a name="highlighting-and-cross-filtering"></a>Markering och korsfiltrering
Information om hur du använder filterfönstret finns i [Lägg till ett filter i en rapport](power-bi-report-add-filter.md).

För att välja ett område, klickar du inom området eller längs topplinjen.  Grundläggande ytdiagram korsfiltrerar inte till andra visualiseringar på rapportsidan. Ytdiagram är dock ett mål för korsfiltrering som utlösts av andra visualiseringar på rapportsidan.

## <a name="considerations-and-troubleshooting"></a>Överväganden och felsökning
* Grundläggande ytdiagram är inte effektiva för att jämföra värden på grund av ocklusion av överlappande områden. Power BI använder genomskinlighet för att ange överlappande områden. Dock fungerar det bara bra med två eller tre olika områden. När du behöver jämföra trender med fler än tre mått, kan du testa att använda linjediagram. När du behöver jämföra volym med fler än tre mått, kan du testa att använda en trädkarta.

## <a name="next-steps"></a>Nästa steg
[Rapporter i Power BI](service-reports.md)  
[Visualiseringar i Power BI-rapporter](power-bi-report-visualizations.md)  
[Power BI – grundläggande begrepp](service-basic-concepts.md)  
Har du fler frågor? [Prova Power BI Community](http://community.powerbi.com/)
