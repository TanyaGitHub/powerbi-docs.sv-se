---
title: Anslut till SQL Sentry med Power BI
description: "SQL Sentry för Power BI"
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
ms.openlocfilehash: e13abe206b4f46726e196a3423bd1fad21391be5
ms.sourcegitcommit: d803e85bb0569f6b357ba0586f5702c20d27dac4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/19/2018
---
# <a name="connect-to-sql-sentry-with-power-bi"></a>Anslut till SQL Sentry med Power BI
Det är enkelt att analysera dina prestandadata som samlats in av SQL Sentry med Power BI. Power BI hämtar dina data och skapar sedan en standardinstrumentpanel och relaterade rapporter baserat på dessa data.

Anslut till [SQL Sentry-innehållspaketet](https://app.powerbi.com/groups/me/getdata/services/sql-sentry) för Power BI.

>[!NOTE]
>Åtkomst till ett SQL Sentry-konto som du använder för att ansluta till http://cloud.sqlsentry.com och ett databas-ID som du övervakar krävs för att ansluta.  Instruktionerna för var du hittar databas-ID finns nedan.

## <a name="how-to-connect"></a>Så här ansluter du
1. Välj **Hämta data** längst ned i det vänstra navigeringsfönstret.
   
   ![](media/service-connect-to-sql-sentry/pbi_getdata.png)
2. I rutan **Tjänster** väljer du **Hämta**.
   
   ![](media/service-connect-to-sql-sentry/pbi_getservices.png) 
3. Välj **SQL Sentry \> Hämta**.
   
   ![](media/service-connect-to-sql-sentry/sqlsentry.png)
4. Ange **databas-ID** för den databas som du vill övervaka i Power BI. Mer information om hur du [hittar det](#FindingParams) nedan.
   
   ![](media/service-connect-to-sql-sentry/img2400.png)
5. Som autentiseringsmetod väljer du **oAuth2 \> logga in**.
   
   När du uppmanas, anger du dina autentiseringsuppgifter för cloud.sqlsentry.com och följer autentiseringsprocessen SQL Sentry.
   
   ![](media/service-connect-to-sql-sentry/img6400.png)
   
   Första gången du ansluter, uppmanas du att ge Power BI skrivskyddad åtkomst till ditt konto. Klicka på Bevilja för att starta importen.  Importen kan ta några minuter beroende på mängden data i ditt konto.
   
   ![](media/service-connect-to-sql-sentry/img7400.png)
6. När Power BI har importerat dessa data, visas en ny instrumentpanel, rapport och datauppsättning i det vänstra navigeringsfönstret. Nya objekt har markerats med en gul asterisk \*:
   
   ![](media/service-connect-to-sql-sentry/img8200.png)
7. Välj SQL Sentry-instrumentpanelen.
   
   Det här är standardinstrumentpanelen som Power BI skapar för att visa dina data. Du kan modifiera den här instrumentpanelen för att visa dina data på det sätt som du vill.
   
   ![](media/service-connect-to-sql-sentry/img9dashboard800.png)

**Och sedan?**

* Prova att [ställa en fråga i rutan Frågor och svar](power-bi-q-and-a.md) överst på instrumentpanelen
* [Ändra panelerna](service-dashboard-edit-tile.md) på instrumentpanelen.
* [Välj en panel](service-dashboard-tiles.md) för att öppna den underliggande rapporten.
* Även om din datauppsättning är schemalagd för att uppdateras dagligen, kan du ändra uppdateringsschemat eller försöka uppdatera den på begäran med **Uppdatera nu**.

## <a name="whats-included"></a>Det här ingår
Följande data finns tillgängliga från SQL Sentry i Power BI:

| Tabellnamn | Beskrivning |
| --- | --- |
| Anslutning |Den här tabellen innehåller information om dina SQL Sentry-definierade anslutningar. |
| Datum<br /> |Den här tabellen innehåller datum från idag tillbaka till det tidigaste datumet då prestandadata samlades in och sparades. |
| Driftstopp<br /> |Den här tabellen innehåller information relaterat till driftstopp och driftstid för varje server som övervakas i din miljö. |
| Minnesanvändning<br /> |Den här tabellen innehåller data om hur mycket minne som är tillgängligt eller fritt i var och en av dina servrar.<br /> |
| Server<br /> |Den här tabellen innehåller poster för varje server i din miljö. |
| Serverhälsa<br /> |Den här tabellen innehåller data för händelser som skapats av anpassade villkor i din miljö, inklusive allvarlighetsgrad och antal. |

<a name="FindingParams"></a>

## <a name="finding-parameters"></a>Hitta parametrar
Du kan hitta **databas-ID** genom att logga in på <https://cloud.sqlsentry.com> i ett nytt webbläsarfönster.  **Databas-ID** visas på huvudöversiktssidan:

    ![](media/service-connect-to-sql-sentry/database2.png)

**Databas-ID** visas också på skärmen databasinformation:

    ![](media/service-connect-to-sql-sentry/database.png)


## <a name="troubleshooting"></a>Felsökning
Om data från vissa av dina appar inte visas i Power BI, kontrollera att du använder rätt databas-ID och att du har behörighet att visa data. 

Om du inte är ägare till SQL Sentry-databas som synkroniseras till <https://cloud.sqlsentry.com>, kontakta din administratör för att kontrollera att du har behörighet att visa insamlade data.

## <a name="next-steps"></a>Nästa steg
[Kom igång med Power BI](service-get-started.md)

[Hämta data för Power BI](service-get-data.md)
