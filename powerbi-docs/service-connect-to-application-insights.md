---
title: Anslut till Application Insights Anslut till Power BI
description: Application Insights för Power BI
author: SarinaJoan
manager: kfile
ms.reviewer: maggiesMSFT
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 08/10/2018
ms.author: sarinas
LocalizationGroup: Connect to services
ms.openlocfilehash: 34e3524d561fb6f6394d69fed55c1bd29bddf4bd
ms.sourcegitcommit: 60fb46b61ac73806987847d9c606993c0e14fb30
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/25/2018
ms.locfileid: "50100598"
---
# <a name="connect-to-application-insights-with-power-bi"></a>Anslut till Application Insights med Power BI
Använd Power BI för att skapa kraftfulla anpassade instrumentpaneler från telemetrin [Application Insights](/azure/application-insights/app-insights-overview/). Förutse din apptelemetri på nya sätt. Kombinera mått för flera appar eller komponenttjänster på en instrumentpanel. Den första versionen av Power BI-innehållspaketet för Application Insights innehåller widgetar för vanliga användningsrelaterade mått såsom aktiva användare, sidvy, sessioner, webbläsare och OS-version och geografisk fördelning av användare på en karta.

Anslut till [Application Insights-innehållspaket för Power BI](https://app.powerbi.com/getdata/services/application-insights).

>[!NOTE]
>Den här integreringsmetoden är nu **inaktuell**. Mer information om den föredragna metoden för att ansluta Application Insights till Power BI finns i [exportera funktioner för analytiska frågor](https://docs.microsoft.com/azure/application-insights/app-insights-export-power-bi#export-analytics-queries).

## <a name="how-to-connect"></a>Så här ansluter du
1. Välj **Hämta data** längst ned i det vänstra navigeringsfönstret.
   
    ![Knappen Hämta data](media/service-connect-to-application-insights/pbi_getdata.png)
2. I rutan **tjänster** väljer du **Hämta**.
   
    ![Knappen Hämta tjänster](media/service-connect-to-application-insights/pbi_getservices.png)
3. Välj **Application Insights** > **Hämta**.
   
    ![Application Insights-innehållspaket](media/service-connect-to-application-insights/appinsights.png)
4. Ange information om programmet som du vill ansluta till, inklusive **resursnamnet för Application Insights**, **resursgrupp** och **prenumerations-ID**. Se [Hitta Application Insights-parametrar](#FindingAppInsightsParams) nedan för mer information.
   
    ![Dialogrutan för Application Insights-anslutning](media/service-connect-to-application-insights/pbi_contpkappinsitconnectndialog.png)    
5. Välj **Logga In** och följ anvisningarna för att ansluta.
   
    ![Inloggning för Application Insights-anslutning](media/service-connect-to-application-insights/pbi_contpkappinsitconnectn2.png)
6. Importen startar automatiskt. När du är klar visas ett meddelande och en ny instrumentpanel, rapport och datauppsättning visas i navigeringsfönstret markerade med en asterisk.  Välj instrumentpanelen för att se dina importerade data.
   
    ![Application Insights-instrumentpanel](media/service-connect-to-application-insights/pbi_contpkappinsitdash.png)

**Och sedan?**

* Prova att [ställa en fråga i rutan Frågor och svar](consumer/end-user-q-and-a.md) överst på instrumentpanelen
* [Ändra panelerna](service-dashboard-edit-tile.md) på instrumentpanelen.
* [Välj en panel](consumer/end-user-tiles.md) för att öppna den underliggande rapporten.
* Medan din datauppsättning schemaläggs att uppdateras dagligen så kan du ändra uppdateringsfrekvensen eller testa att uppdatera den på begäran med **Uppdatera nu**

## <a name="whats-included"></a>Det här ingår
Application Insights-innehållspaketet innehåller följande tabeller och mått:  

    ´´´
    - ApplicationDetails  
    - UniqueUsersLast7Days   
    - UniqueUsersLast30Days   
    - UniqueUsersDailyLast30Days  
    - UniqueUsersByCountryLast7Days  
    - UniqueUsersByCountryLast30Days   
    - PageViewsDailyLast30Days   
    - SessionsLast7Days   
    - SessionsLast30Days  
    - PageViewsByBrowserVersionDailyLast30Days   
    - UniqueUsersByOperatingSystemLast7Days   
    - UniqueUsersByOperatingSystemLast30Days    
    - SessionsDailyLast30Days   
    - SessionsByCountryLast7Days   
    - SessionsByCountryLast30Days   
    - PageViewsByCountryDailyLast30Days  
    ´´´ 

<a name="FindingAppInsightsParams"></a>

## <a name="finding-parameters"></a>Hitta parametrar
Ditt resursnamn, din resursgrupp och ditt prenumerations-ID hittar du i Azure Portal. Genom att markera namnet öppnas en detaljerad vy och du kan använda Essentials-listrutan för att hitta de värden som du behöver.

![Application Insights-parametrar](media/service-connect-to-application-insights/pbi_contpkappinsitparams.png)

Kopiera och klistra in dessa i fälten i Power BI:

![Application Insights-parametrar](media/service-connect-to-application-insights/pbi_contpkappinsitparam2.png)

## <a name="next-steps"></a>Nästa steg
[Kom igång i Power BI](service-get-started.md)

[Hämta data i Power BI](service-get-data.md)

