---
title: Anslut till Azure Search med Power BI
description: Azure Search för Power BI
author: SarinaJoan
manager: kfile
ms.reviewer: maggiesMSFT
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 10/16/2017
ms.author: sarinas
LocalizationGroup: Connect to services
ms.openlocfilehash: 5ba3c1336abc10872e58ef2ec38f076dfa120d47
ms.sourcegitcommit: 0ff358f1ff87e88daf837443ecd1398ca949d2b6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/21/2018
ms.locfileid: "46544997"
---
# <a name="connect-to-azure-search-with-power-bi"></a>Anslut till Azure Search med Power BI
Azure Search Traffic Analytics låter dig övervaka och förstå trafiken till din Azure Search-tjänst. Azure Search-innehållspaketet för Power BI innehåller detaljerad information om dina sökdata, inklusive sökning, indexering, statistik för tjänsten och svarstid från de senaste 30 dagarna. Mer information finns i [Azure-blogginlägget](https://azure.microsoft.com/blog/analyzing-your-azure-search-traffic/).

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

* Prova att [ställa en fråga i rutan Frågor och svar](consumer/end-user-q-and-a.md) överst på instrumentpanelen
* [Ändra panelerna](service-dashboard-edit-tile.md) på instrumentpanelen.
* [Välj en panel](consumer/end-user-tiles.md) för att öppna den underliggande rapporten.
* Medan din datauppsättning schemaläggs att uppdateras dagligen så kan du ändra uppdateringsfrekvensen eller testa att uppdatera den på begäran med **Uppdatera nu**

## <a name="system-requirements"></a>Systemkrav
Azure Search-innehållspaketet kräver att Azure Search Traffic Analytics är aktiverat för kontot.

## <a name="troubleshooting"></a>Felsökning
Se till att lagringskontonamnet har angetts korrekt tillsammans med den fullständiga åtkomstnyckeln. Lagringskontonamnet ska motsvara det konto som har konfigurerats med Azure Search Traffic Analytics.

## <a name="next-steps"></a>Nästa steg
[Vad är Power BI?](power-bi-overview.md)

[Power BI – grundläggande begrepp](consumer/end-user-basic-concepts.md)

