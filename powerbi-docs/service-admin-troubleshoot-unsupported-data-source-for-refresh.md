---
title: "Felsöka datakälla utan stöd för uppdatering"
description: "Felsöka datakälla utan stöd för uppdatering"
services: powerbi
documentationcenter: 
author: davidiseminger
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
ms.date: 12/06/2017
ms.author: davidi
ms.openlocfilehash: d95b9d7ca8cae1e4311ef679093814c51a9ba3c0
ms.sourcegitcommit: d91436de68a0e833ecff18d976de9d9431bc4121
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/06/2017
---
# <a name="troubleshooting-unsupported-data-source-for-refresh"></a>Felsöka datakälla utan stöd för uppdatering
Du kan se ett fel vid försök att konfigurera en datauppsättning för schemalagd uppdatering.

        You cannot schedule refresh for this dataset because it gets data from sources that currently don’t support refresh.

Detta händer när datakällan som du använde i Power BI Desktop inte stöds för uppdatering. Du behöver hitta datakällan som du använder och jämföra den med listan över stödda datakällor i [Refresh data in Power BI (Uppdatera data i Power BI)](refresh-data.md). 

## <a name="find-the-data-source"></a>Hitta datakällan
Om du inte är säker på vilken datakälla som användes, kan du hitta den med följande steg i Power BI Desktop.  

1. Kontrollera att du är i fönstret **Rapport** i Power BI Desktop.  
   ![](media/service-admin-troubleshoot-unsupported-data-source-for-refresh/tshoot-report-pane.png)
2. Välj **Redigera frågor** från menyfliksområdet.  
   ![](media/service-admin-troubleshoot-unsupported-data-source-for-refresh/tshoot-edit-queries.png)
3. Välj **Avancerad redigerare**.  
   ![](media/service-admin-troubleshoot-unsupported-data-source-for-refresh/tshoot-advanced-editor.png)
4. Anteckna providern som är angiven för datakällan i listan.  I det här exemplet är providern ActiveDirectory.  
   ![](media/service-admin-troubleshoot-unsupported-data-source-for-refresh/tshoot-provider.png)
5. Jämför providern med listan över stödda datakällor som finns i [Refresh data in Power BI (Uppdatera data i Power BI)](refresh-data.md).  Du kommer märka att Active Directory inte är en datakälla som stöds för uppdatering.  

## <a name="next-steps"></a>Nästa steg
[Datauppdatering](refresh-data.md)  
[Power BI Gateway – Personal](personal-gateway.md)  
[Lokal datagateway](service-gateway-onprem.md)  
[Felsökning av den lokala datagatewayen](service-gateway-onprem-tshoot.md)  
[Felsöka Power BI Gateway – Personal](service-admin-troubleshooting-power-bi-personal-gateway.md)  

Har du fler frågor? [Fråga Power BI Community](http://community.powerbi.com/)
