---
title: Ansluta till SendGrid med Power BI
description: SendGrid för Power BI
author: SarinaJoan
manager: kfile
ms.reviewer: maggiesMSFT
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 10/16/2017
ms.author: sarinas
LocalizationGroup: Connect to services
ms.openlocfilehash: b077c34506462ed030f3ebf1365f3524dbf11131
ms.sourcegitcommit: 0ff358f1ff87e88daf837443ecd1398ca949d2b6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/21/2018
ms.locfileid: "46549786"
---
# <a name="connect-to-sendgrid-with-power-bi"></a>Ansluta till SendGrid med Power BI
Med Power BI-innehållspaketet för SendGrid kan du extrahera insikter och statistik från ditt SendGrid-konto. Med SendGrid-innehållspaketet kan du visualisera din SendGrid-statistik på en instrumentpanel.

Ansluta till [SendGrid-innehållspaketet](https://app.powerbi.com/getdata/services/sendgrid) för Power BI.

## <a name="how-to-connect"></a>Så här ansluter du
1. Välj **Hämta data** längst ned i det vänstra navigeringsfönstret.
   
   ![](media/service-connect-to-sendgrid/pbi_getdata.png) 
2. I rutan **Tjänster** väljer du **Hämta**.
   
   ![](media/service-connect-to-sendgrid/pbi_getservices.png) 
3. Välj **SendGrid**-innehållspaketet och klicka på **Hämta**.
   
   ![](media/service-connect-to-sendgrid/sendgrid.png) 
4. När du uppmanas till det anger du ditt SendGrid-användarnamn och lösenord. Välj **Logga in**.
   
   ![](media/service-connect-to-sendgrid/pbi_sendgridsignin.png)
5. När Power BI har importerat datan visas en ny instrumentpanel, rapport och datauppsättning i det vänstra navigeringsfönstret, ifyllt med din e-poststatistik för de senaste 90 dagarna. Nya objekt markeras med en gul asterisk \*.
   
   ![](media/service-connect-to-sendgrid/pbi_sendgriddash.png)

**Och sedan?**

* Prova att [ställa en fråga i rutan Frågor och svar](consumer/end-user-q-and-a.md) överst på instrumentpanelen
* [Ändra panelerna](service-dashboard-edit-tile.md) på instrumentpanelen.
* [Välj en panel](consumer/end-user-tiles.md) för att öppna den underliggande rapporten.
* Medan din datauppsättning schemaläggs att uppdateras dagligen så kan du ändra uppdateringsfrekvensen eller testa att uppdatera den på begäran med **Uppdatera nu**

## <a name="whats-included"></a>Det här ingår
I SendGrid-instrumentpanelen finns följande mått:

* Övergripande e-poststatistik – förfrågningar, levererade, studsade, blockerad skräppost, skräppostrapport etc.
* E-poststatistik efter kategori
* E-poststatistik efter geografi
* E-poststatistik efter Internetleverantör
* E-poststatistik efter enhet, klient, webbläsare

## <a name="next-steps"></a>Nästa steg
[Vad är Power BI?](power-bi-overview.md)

[Hämta data](service-get-data.md)

