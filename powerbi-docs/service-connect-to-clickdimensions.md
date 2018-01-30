---
title: Anslut till ClickDimensions med Power BI
description: "ClickDimensions för Power BI"
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
ms.openlocfilehash: 007d4f6f5181722e23e280e1a57d305d7f069155
ms.sourcegitcommit: d803e85bb0569f6b357ba0586f5702c20d27dac4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/19/2018
---
# <a name="connect-to-clickdimensions-with-power-bi"></a>Anslut till ClickDimensions med Power BI
ClickDimensions-innehållspaketet för Power BI låter användare använda marknadsföringsdata för ClickDimensions i Power BI, vilket ger hanteringsteam ytterligare insikter om sina försäljnings- och marknadsföringsaktiviteter. Visualisera och analysera e-postinteraktioner, webbesök och inlämnade formulär i Power BI-instrumentpaneler och rapporter.

Anslut till [ClickDimensions-innehållspaketet](https://app.powerbi.com/getdata/services/click-dimensions) för Power BI.

## <a name="how-to-connect"></a>Så här ansluter du
1. Välj **Hämta data** längst ned i det vänstra navigeringsfönstret.
   
   ![](media/service-connect-to-clickdimensions/getdata.png)
2. I rutan **tjänster** väljer du **Hämta**.
   
   ![](media/service-connect-to-clickdimensions/services.png)
3. Välj **ClickDimensions** \> **hämta**.
   
   ![](media/service-connect-to-clickdimensions/clickdimensions.png)
4. Ange platsen för ditt datacenter (USA, EU, eller AU) och välj **nästa**.
   
   ![](media/service-connect-to-clickdimensions/params.png)
5. Som **autentiseringsmetod**, väljer du **grundläggande** \> **logga in**. När du uppmanas, anger du dina autentiseringsuppgifter för ClickDimensions. Se information i [sök efter de parametrarna](#FindingParams) nedan
   
    ![](media/service-connect-to-clickdimensions/creds.png)
6. Efter att du har godkänt startar importen automatiskt. När den är klar visas en ny instrumentpanel, rapport och modell i navigeringsfönstret. Välj instrumentpanelen för att visa dina importerade data.
   
     ![](media/service-connect-to-clickdimensions/dashboard.png)

**Och sedan?**

* Prova att [ställa en fråga i rutan Frågor och svar](power-bi-q-and-a.md) överst på instrumentpanelen
* [Ändra panelerna](service-dashboard-edit-tile.md) på instrumentpanelen.
* [Välj en panel](service-dashboard-tiles.md) för att öppna den underliggande rapporten.
* Även om din datauppsättning är schemalagd för att uppdateras dagligen, kan du ändra uppdateringsschemat eller försöka uppdatera den på begäran med **Uppdatera nu**.

## <a name="system-requirements"></a>Systemkrav
Om du vill ansluta till Power BI-innehållsapaketet, måste du ange det datacenter som motsvarar ditt konto och logga in med ditt ClickDimensions-konto. Om du är osäker på vilket datacenter du ska välja, kan du fråga din administratör.

<a name="FindingParams"></a>

## <a name="finding-parameters"></a>Hitta parametrar
Kontonyckeln hittar du i CRM-inställningar \> ClickDimensions-inställningar. Kopiera kontonyckeln från ClickDimensions-inställningarna och klistra in det i användarnamnsfältet.  

![](media/service-connect-to-clickdimensions/crm.png)  

Kopiera Power BI-token från ClickDimensions-inställningarna och klistra in den i lösenordsfältet. Power BI-token hittar du i CRM-inställningar \> ClickDimensions-inställningar.  

![](media/service-connect-to-clickdimensions/crm2.png)  

## <a name="next-steps"></a>Nästa steg
[Kom igång i Power BI](service-get-started.md)

[Hämta data i Power BI](service-get-data.md)
