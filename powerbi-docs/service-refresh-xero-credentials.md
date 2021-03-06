---
title: Så här uppdaterar du dina innehållspaketautentiseringsuppgifter för Xero
description: Om du använder Xero Power BI-innehållspaketet kan du ha stött på ett problem med innehållspaketets dagliga uppdateringar på grund av en nyligen inträffad incident i Power BI-tjänsten.
author: SarinaJoan
manager: kfile
ms.reviewer: maggiesMSFT
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 08/10/2017
ms.author: sarinas
LocalizationGroup: Troubleshooting
ms.openlocfilehash: 5978443f05e039c34ff023f235624968b5eb8a3e
ms.sourcegitcommit: 80d6b45eb84243e801b60b9038b9bff77c30d5c8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/04/2018
ms.locfileid: "34250179"
---
# <a name="how-to-refresh-your-xero-content-pack-credentials-if-refresh-failed"></a>Så här uppdaterar du dina innehållspaketautentiseringsuppgifter för Xero om uppdateringen misslyckades
Om du använder Xero Power BI-innehållspaketet kan du ha stött på problem med innehållspaketets dagliga uppdateringar på grund av en nyligen inträffad incident i Power BI-tjänsten.

Du kan se om ditt innehållspaket har uppdaterats genom att kontrollera den senaste uppdateringsstatusen för din Xero-datauppsättning som visas på skärmbilden nedan.

![](media/service-refresh-xero-credentials/powerbi-xero-refresh-failed.png)

Om du ser att uppdateringen har misslyckats, så förnya ditt innehållspakets autentiseringsuppgifter genom att följa dessa steg.

1. Klicka på ellipsen (...) bredvid Xero-datauppsättningen, och klicka sedan på **Schemauppdatering**. Då öppnas inställningssidan för Xero-innehållspaketet.
   
    ![](media/service-refresh-xero-credentials/powerbi-xero-schedule-refresh.png)
2. Välj **Datakällans autentiseringsuppgifter** > **Redigera autentiseringsuppgifter** på sidan **Inställningar för Xero**.
   
    ![](media/service-refresh-xero-credentials/powerbi-xero-settings-page.png)
3. Ange ditt organisationsnamn > **Nästa**.
   
    ![](media/service-refresh-xero-credentials/powerbi-xero-configure.png)
4. Logga in med ditt Xero-konto.
   
    ![](media/service-refresh-xero-credentials/powerbi-xero-welcome.png)
5. Nu när dina autentiseringsuppgifter har uppdaterats, så kontrollera att uppdateringsschemat är inställt på att köras varje dag. Kontrollera detta genom att klicka på ellipsen (...) bredvid Xero-datauppsättningen, och sedan klicka på **Schemauppdatering** igen.
   
    ![](media/service-refresh-xero-credentials/powerbi-xero-refresh-schedule.png)
6. Du kan också välja att uppdatera datauppsättningen direkt. Klicka på ellipsen (...) bredvid Xero-datauppsättningen, och klicka sedan på **Uppdatera nu**.
   
    ![](media/service-refresh-xero-credentials/powerbi-xero-refresh-now.png)

Om du fortfarande har uppdateringsproblem så tveka inte att kontakta oss på [http://support.powerbi.com](http://support.powerbi.com) 

Om du vill veta mer om Xero-innehållspaketet för Power BI kan du besöka hjälpsidan för [Xero-innehållspaket](service-connect-to-xero.md).

### <a name="next-steps"></a>Nästa steg
* Har du fler frågor? [Prova Power BI Community](http://community.powerbi.com/)

