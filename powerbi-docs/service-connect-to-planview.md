---
title: Anslut till Planview Enterprise med Power BI
description: "Planview Enterprise för Power BI"
services: powerbi
documentationcenter: 
author: joeshoukry
manager: kfile
backup: maggiesMSFT
editor: 
tags: 
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 10/16/2017
ms.author: yshoukry
ms.openlocfilehash: cef43b20a6c7fe91ef35567caa511d125c536bf5
ms.sourcegitcommit: d803e85bb0569f6b357ba0586f5702c20d27dac4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/19/2018
---
# <a name="connect-to-planview-enterprise-with-power-bi"></a>Anslut till Planview Enterprise med Power BI
Med innehållspaketet Planview Enterprise för Power BI kan du visualisera dina resurs- och arbetshanteringsdata på ett helt nytt sätt direkt i Power BI. Använd autentiseringsuppgifterna för Planview Enterprise för att se utgifter i din investeringsportfölj interaktivt, förstå var du överstiger och understiger din budget och veta hur dina projekt överensstämmer med företagets strategiska prioriteringar. Du kan också utöka den ursprungliga instrumentpanelen och rapporterna för att skaffa dig de insikter som är viktigast för dig.

[Anslut till Planview Enterprise-innehållspaketet i Power BI](https://app.powerbi.com/getdata/services/planview-enterprise)

>[!NOTE]
>Du måste vara en Planview Enterprise-användare med funktionen Reporting Portal Viewer aktiverad på din roll om du vill importera dina Planview Enterprise-data till Power BI. Se ytterligare krav nedan.

## <a name="how-to-connect"></a>Så här ansluter du
1. Välj **Hämta data** längst ned i det vänstra navigeringsfönstret.
   
    ![](media/service-connect-to-planview/get.png)
2. I rutan **Tjänster** väljer du **Hämta**.
   
    ![](media/service-connect-to-planview/services.png)
3. På Power BI-sidan väljer du **Planview Enterprise**och väljer sedan **Hämta**:  
    ![](media/service-connect-to-planview/planview.png)
4. Ange Planview Enterprise-URL:en i textrutan för den Planview Enterprise-server som du vill använda. I textrutan för Planview Enterprise-databas anger du namnet på din databas för Planview Enterprise och sedan Nästa.  
    ![](media/service-connect-to-planview/params.png)
5. I listan över autentiseringsmetoder, väljer du **Basic** om det inte redan är valt. Ange **Användarnamn** och **Lösenord** för ditt konto och välj **Logga In**.  
   ![](media/service-connect-to-planview/creds.png)
6. I den vänstra rutan, väljer du Planview Enterprise från listan över instrumentpaneler.  
     Power BI importerar Planview Enterprise-data till instrumentpanelen. Observera att data kan ta lite tid att läsa in.  
    ![](media/service-connect-to-planview/dashboard.png)

**Och sedan?**

* Prova att [ställa en fråga i rutan Frågor och svar](power-bi-q-and-a.md) överst på instrumentpanelen
* [Ändra panelerna](service-dashboard-edit-tile.md) på instrumentpanelen.
* [Välj en panel](service-dashboard-tiles.md) för att öppna den underliggande rapporten.
* Även om din datauppsättning är schemalagd för att uppdateras dagligen, kan du ändra uppdateringsschemat eller försöka uppdatera den på begäran med **Uppdatera nu**.

## <a name="system-requirements"></a>Systemkrav
Du måste vara en Planview Enterprise-användare med funktionen Reporting Portal Viewer aktiverad på din roll om du vill importera dina Planview Enterprise-data till Power BI. Se ytterligare krav nedan.

Den här proceduren förutsätter att du redan har loggat in på startsidan för Microsoft Power BI med ett Power BI-konto. Om du inte har ett Power BI-konto, skapar du ett nytt kostnadsfritt Power BI-konto på Power BI-startsidan och klickar sedan på hämta data.

## <a name="next-steps"></a>Nästa steg:

[Kom igång med Power BI](service-get-started.md)

[Hämta data för Power BI](service-get-data.md)