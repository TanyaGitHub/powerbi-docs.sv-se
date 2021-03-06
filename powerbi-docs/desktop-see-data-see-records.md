---
title: Se data och poster i Power BI Desktop-visualiseringar
description: Använd funktionerna Se data och Se poster för Power BI Desktop för att gå in på detaljnivå
author: davidiseminger
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-desktop
ms.topic: conceptual
ms.date: 07/27/2018
ms.author: davidi
LocalizationGroup: Learn more
ms.openlocfilehash: b635f464126addaf952adf5d8af1d0407899c0b9
ms.sourcegitcommit: f01a88e583889bd77b712f11da4a379c88a22b76
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/27/2018
ms.locfileid: "39328071"
---
# <a name="use-see-data-and-see-records-in-power-bi-desktop"></a>Använd se Data och se poster i Power BI Desktop
I **Power BI Desktop** kan du visa detaljer om en visualisering och se textrepresentationer av underliggande data eller enskilda dataelement för den valda visualiseringen. De här funktionerna kallas ibland för *klicka igenom*, *detaljerad information* eller *gå in på detaljnivå*.

Du kan använda **Se data** för att visa en textversion av de värden som används av den valda visualiseringen eller använda **Se poster** för att visa alla data för en markerad post eller datapunkt. 

![Se data och Se poster](media/desktop-see-data-see-records/see-data-record.png)

>[!IMPORTANT]
>**Se data** och **Se poster** har endast stöd för följande visualiseringstyper:
>  - Stapeldiagram
>  - Kolumndiagram
>  - Ringdiagram
>  - Ifylld karta
>  - Tratt
>  - Karta
>  - Cirkeldiagram
>  - Trädkarta

## <a name="use-see-data-in-power-bi-desktop"></a>Använd Se data i Power BI Desktop

**Se data** visar data som är underliggande en visualisering. **Se data** visas i fliken **Data/detaljgranska** i avsnittet **Visuella verktyg** i menyfliksområdet när en visualisering väljs.

![Se data i menyfliksområdet](media/desktop-see-data-see-records/see-data1.png)

Du kan också visa data genom att högerklicka på en visualisering och sedan välja **Visa data** från menyn som visas, eller genom att välja ellipsen (...) **Fler alternativ** i det övre högra hörnet av en visualisering och sedan välja **Visa data**.

![Högerklicka på Visa data](media/desktop-see-data-see-records/see-data2.png)&nbsp;&nbsp;![Fler alternativ för Visa data](media/desktop-see-data-see-records/see-data3.png)

> [!NOTE]
> Du måste hovra över en datapunkt i visualiseringen för att snabbmenyn ska vara tillgänglig.

När du väljer **Se data** eller **Visa data**, visar Power BI Desktop-arbetsytan både visuella och textrepresentation av data. I *vågrät vy* visas visualiseringen på den övre delen av arbetsytan och data visas på den nedre halvan. 

![vågrät vy](media/desktop-see-data-see-records/see-data4a.png)

Du kan växla mellan vågrät vy och *lodrät vy* genom att välja ikonen i det övre högra hörnet av arbetsytan.

![växla till lodrät vy](media/desktop-see-data-see-records/see-data4.png)

Gå tillbaka till rapporten genom att markera **< Tillbaka till rapporten** i det övre vänstra hörnet på arbetsytan.

![Tillbaka till rapporten](media/desktop-see-data-see-records/see-data5.png)

## <a name="use-see-records-in-power-bi-desktop"></a>Använd Se poster i Power BI Desktop

Du kan också fokusera på en datapost i en visualisering och gå in på detaljnivå på bakomliggande data. För att använda **Se poster**, välj en visualisering och sedan **Se poster** i fliken **Data/detaljgranska** i avsnittet **Visuella verktyg** i menyfliksområdet och välj sedan en datapunkt eller raden på visualiseringen. 

![Se poster i menyfliksområdet](media/desktop-see-data-see-records/see-record1.png)

> [!NOTE]
> Om knappen **Se poster** i menyfliksområdet är inaktiverad och nedtonad, betyder det att den valda visualiseringen inte stöder **Se poster**.

Du kan också högerklicka på ett dataelement och välja **Se poster** från menyn som visas.

![Se poster genom att högerklicka](media/desktop-see-data-see-records/see-record2.png)

När du väljer **Se poster** för ett dataelement visar Power BI Desktop-arbetsytan alla data som är associerade med det valda elementet. 

![](media/desktop-see-data-see-records/see-record3.png)

Gå tillbaka till rapporten genom att markera **< Tillbaka till rapporten** i det övre vänstra hörnet på arbetsytan.

![](media/desktop-see-data-see-records/see-record4.png)

> [!NOTE]
>**Se poster** har följande begränsningar:
> - Du kan inte ändra data i vyn **Se poster** och spara tillbaka dem till rapporten.
> - Du kan inte använda **Se poster** när din visualisering använder ett beräknat mått.
> - Du kan inte använda **Se poster** när du är ansluten till en flerdimensionell livemodell (MD).

## <a name="next-steps"></a>Nästa steg
Det finns en massa sorters rapportformatering och funktioner för datahantering i **Power BI Desktop**. Kolla in följande resurser för några exempel:

* [Använd gruppering och diskretisering i Power BI Desktop](desktop-grouping-and-binning.md)
* [Använd stödlinjer, fäst till rutnät, z-ordning, justering och distribution i Power BI Desktop-rapporter](desktop-gridlines-snap-to-grid.md)

