---
title: "Skapa ett dynamiskt utsnitt som du kan ändra storlek på i Power BI"
description: "Lär dig hur du skapar ett dynamiskt utsnitt som du kan ändra storlek på så att det passar din rapport"
services: powerbi
documentationcenter: 
author: maggiesMSFT
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
ms.date: 12/08/2017
ms.author: maggies
ms.openlocfilehash: f95f126cc6a7c95fbe3227b712281a7d3f81e320
ms.sourcegitcommit: b780b7108fd9b52398b8377b52836f0e0fedc96e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/09/2017
---
# <a name="create-a-responsive-slicer-you-can-resize-in-power-bi-preview"></a>Skapa ett dynamiskt utsnitt som du kan ändra storlek på i Power BI (förhandsgranskning)

Dynamiska utsnitt ändrar storlek för att passa i alla olika utrymmen i rapporten. Du kan ändra storlek på de dynamiska utsnitten till olika storlekar och former, från vågräta till kvadratiska, till lodräta och värdena i utsnittet ordnar om sig själva på samma sätt som du gör. I Power BI Desktop och Power BI-tjänsten kan du göra vågräta utsnitt och datum-/intervallutsnitt dynamiska. Datum-/intervallutsnitt har också förbättrade pekområden så att det är lättare att ändra dem med ett fingertryck. Du kan göra dynamiska utsnitt så små eller stora som du vill. De ändrar också storlek automatiskt så att de passar bra för rapporter i Power BI-tjänsten och även i Power BI-appar. 

![Dynamiska utsnitt kan ha olika former](media/power-bi-slicer-filter-responsive/responsive-slicer-gif.gif)

## <a name="create-a-slicer"></a>Skapa ett utsnitt

Det första steget för att skapa ett dynamiskt utsnitt är att skapa ett grundläggande utsnitt. 

1. Välj ikonen **Utsnitt** ![Utsnittsikonen](media/power-bi-slicer-filter-responsive/power-bi-slicer-icon.png) i fönstret **Visualiseringar**.
2. Dra fältet som du vill filtrera till **Fält**.

    ![Lägg till ett fält till utsnittet](media/power-bi-slicer-filter-responsive/power-bi-slicer-field.png)

## <a name="convert-to-a-horizontal-slicer"></a>Konvertera till ett vågrätt utsnitt

1. Med det valda utsnittet väljer du fliken **Format** i fönstret **Visualiseringar**.
2. Expandera avsnittet **Allmänt** och välj sedan **Vågrätt** som **Orientering**.

    ![Ange utsnittet till vågrätt](media/power-bi-slicer-filter-responsive/power-bi-slicer-horizontal.png) 

1.  Du vill förmodligen göra det bredare för att visa fler värden.

     ![Gör utsnittet bredare](media/power-bi-slicer-filter-responsive/power-bi-slicer-wide-horizontal.png)

## <a name="make-it-responsive-and-experiment-with-it"></a>Gör det dynamiskt och experimentera med det

Det här steget är enkelt. 

1. Precis under **Orientering** i avsnittet **Allmänt** under fliken **Format** drar du **Responsiv (förhandsgranskning)** till **På**.  

    ![Utsnittet är nu dynamiskt](media/power-bi-slicer-filter-responsive/power-bi-slicer-wide-responsive.png)

1. Nu kan du experimentera med det. Dra i hörnen för att göra det kortare, längre, bredare och smalare. Om du gör det tillräckligt litet, blir det bara en filterikon.

    ![Dynamiskt utsnitt som är så litet så det är en filterikon](media/power-bi-slicer-filter-responsive/power-bi-slicer-small-filter-icon.png)

## <a name="add-it-to-a-phone-report-layout"></a>Lägg till det i en telefonrapportlayout

I Power BI Desktop kan du skapa en telefonlayout för varje sida i en rapport. Om en sida har en telefonlayout, visas den på en mobiltelefon i stående vy. I annat fall måste du visa den i liggande vy. 

1. På menyn **Visa** väljer du **Telefonlayout**.

     ![Ikon för telefonlayout, menyn Visa](media/power-bi-slicer-filter-responsive/power-bi-phone-layout-menu.png)
    
1. Dra all visuell information du vill ha i telefonrapporten till rutnätet. Dra det dynamiska utsnittet till den storlek du önskar – i det här fallet bara en filterikon.

    ![Lägg till utsnittet till telefonrapportlayouten](media/power-bi-slicer-filter-responsive/power-bi-slicer-phone-layout.png)

Läs mer om hur du skapar [rapporter som är optimerade för Power BI-appar](desktop-create-phone-report.md).

## <a name="make-a-time-or-range-slicer-responsive"></a>Gör ett tids- eller intervallutsnitt dynamiskt

Du kan följa samma steg för att göra en panel eller ett intervallutsnitt dynamiskt. När du ställer in **Dynamiskt** till **På**, upptäcker du några saker:

- Visuell information optimerar ordningen på indatarutorna beroende på arbetsytans storlek. 
- Visningen av dataelement är optimerad för att göra utsnittet så användbart som möjligt, baserat på den storleken som är tillåten på arbetsytan. 
- Nya runda handtag på reglagen optimerar pekinteraktioner. 
- När en visuell information blir för liten för att användas, blir den en ikon som representerar typen av visuell information i dess ställe. För att interagera med den dubbelklickar du bara på den för att öppna den i Fokusläge. Detta sparar värdefullt utrymme på sidan utan att förlora funktionerna.

## <a name="next-steps"></a>Nästa steg

- [Självstudier: Utsnitt i Power BI-tjänsten](power-bi-visualization-slicers.md)
- Har du fler frågor? [Fråga Power BI Community](http://community.powerbi.com/)