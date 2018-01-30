---
title: Anslut till Azure Search med Power BI
description: "Azure Search för Power BI"
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
ms.openlocfilehash: 692fdaa4861ed4ae692698439b6c86a30d60c790
ms.sourcegitcommit: d803e85bb0569f6b357ba0586f5702c20d27dac4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/19/2018
---
# <a name="connect-to-azure-search-with-power-bi"></a>Anslut till Azure Search med Power BI
Azure Search Traffic Analytics låter dig övervaka och förstå trafiken till din Azure Search-tjänst. Azure Search-innehållspaketet för Power BI innehåller detaljerad information om dina sökdata, inklusive sökning, indexering, statistik för tjänsten och svarstid från de senaste 30 dagarna. Mer information finns i [Azure-blogginlägget](https://azure.microsoft.com/en-us/blog/analyzing-your-azure-search-traffic/).

Anslut till [Azure Search-innehållspaketet](https://app.powerbi.com/getdata/services/azure-search) för Power BI.

## <a name="how-to-connect"></a>Så här ansluter du
1. Välj **Hämta data** längst ned i det vänstra navigeringsfönstret.
   
   ![](media/service-connect-to-azure-search/pbi_getdata.png) 
2. I rutan **tjänster** väljer du **Hämta**.
   
   ![](media/service-connect-to-azure-search/pbi_getservices.png) 
3. Välj **Azure Search** \> **hämta**.
   
   ![](media/service-connect-to-azure-search/azuresearch.png)
4. Ange namnet på tabellagringskontot där din Azure Search-analys lagras.
   
   ![](media/service-connect-to-azure-search/params.png)
5. Välj **nyckel** som autentiseringsmetod och ange din lagringskontonyckel. Klicka på **logga In** för att starta inläsningen.
   
   ![](media/service-connect-to-azure-search/creds.png)
6. När den är klar, visas en ny instrumentpanel, en rapport och en modell i navigeringsfönstret. Välj instrumentpanelen för att se dina importerade data.
   
    ![](media/service-connect-to-azure-search/dashboard2.png)

**Och sedan?**

* Prova att [ställa en fråga i rutan Frågor och svar](power-bi-q-and-a.md) överst på instrumentpanelen
* [Ändra panelerna](service-dashboard-edit-tile.md) på instrumentpanelen.
* [Välj en panel](service-dashboard-tiles.md) för att öppna den underliggande rapporten.
* Även om din datauppsättning är schemalagd för att uppdateras dagligen, kan du ändra uppdateringsschemat eller försöka uppdatera den på begäran med **Uppdatera nu**.

## <a name="system-requirements"></a>Systemkrav
Azure Search-innehållspaketet kräver att Azure Search Traffic Analytics är aktiverat för kontot.

## <a name="troubleshooting"></a>Felsökning
Se till att lagringskontonamnet har angetts korrekt tillsammans med den fullständiga åtkomstnyckeln. Lagringskontonamnet ska motsvara det konto som har konfigurerats med Azure Search Traffic Analytics.

## <a name="next-steps"></a>Nästa steg
[Kom igång med Power BI](service-get-started.md)

[Power BI – grundläggande begrepp](service-basic-concepts.md)
