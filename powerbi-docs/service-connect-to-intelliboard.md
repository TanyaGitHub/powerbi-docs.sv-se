---
title: Anslut till IntelliBoard med Power BI
description: "IntelliBoard för Power BI"
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
ms.openlocfilehash: e74b26c9d34b19607a0b38197c466f4eb3a06e2a
ms.sourcegitcommit: d803e85bb0569f6b357ba0586f5702c20d27dac4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/19/2018
---
# <a name="connect-to-intelliboard-with-power-bi"></a>Anslut till IntelliBoard med Power BI
IntelliBoard erbjuder en förenklad åtkomst till dina Moodle learning management system-data via Reporting Services. IntelliBoard-innehållspaketet för Power BI erbjuder ytterligare analys, inklusive mått på dina kurser, registrerade användare, övergripande prestanda och din LMS-aktivitet.

Anslut till [IntelliBoard-innehållspaketet](https://app.powerbi.com/getdata/services/intelliboard) för Power BI.

## <a name="how-to-connect"></a>Så här ansluter du
1. Välj **Hämta data** längst ned i det vänstra navigeringsfönstret.  
   
    ![](media/service-connect-to-intelliboard/getdata.png)
2. I rutan **tjänster** väljer du **Hämta**.  
   
    ![](media/service-connect-to-intelliboard/services.png)
3. Välj **IntelliBoard**och välj sedan **hämta**.  
   
    ![](media/service-connect-to-intelliboard/intelliboard.png)
4. Välj **OAuth 2** och sedan **Logga in**. När du uppmanas, anger du dina autentiseringsuppgifter för IntelliBoard.
   
    ![](media/service-connect-to-intelliboard/creds.png)
   
    ![](media/service-connect-to-intelliboard/creds2.png)
5. När du är ansluten kommer en instrumentpanel, rapport och datauppsättning automatiskt att läsas in. När du är klar, uppdateras panelerna med data från ditt IntelliBoard-konto.
   
    ![](media/service-connect-to-intelliboard/dashboard.png)

**Och sedan?**

* Prova att [ställa en fråga i rutan Frågor och svar](power-bi-q-and-a.md) överst på instrumentpanelen
* [Ändra panelerna](service-dashboard-edit-tile.md) på instrumentpanelen.
* [Välj en panel](service-dashboard-tiles.md) för att öppna den underliggande rapporten.
* Även om din datauppsättning är schemalagd för att uppdateras dagligen, kan du ändra uppdateringsschemat eller försöka uppdatera den på begäran med **Uppdatera nu**.

## <a name="whats-included"></a>Vad ingår
Innehållspaketet inkluderar data från följande tabeller:  

    - Aktivitet  
    - Agenter  
    - Författare  
    - Länder  
    - CoursesProgress  
    - Registreringar
    - Språk  
    - Plattform  
    - Summor  
    - UsersProgress    

## <a name="system-requirements"></a>Systemkrav
Ett IntelliBoard-konto med behörigheter till ovanstående tabeller krävs för att skapa en instans av det här innehållspaketet.

## <a name="next-steps"></a>Nästa steg
[Kom igång med Power BI](service-get-started.md)

[Power BI – grundläggande begrepp](service-basic-concepts.md)
