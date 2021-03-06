---
title: Installera Power BI Desktop som har optimerats för Power BI-rapportservern
description: Lär dig att installera Power BI Desktop som har optimerats för Power BI-rapportservern
author: maggiesMSFT
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-report-server
ms.topic: conceptual
ms.date: 09/19/2018
ms.author: maggies
ms.openlocfilehash: c65b945260357b0679f8fdb83c534aac53481126
ms.sourcegitcommit: 70192daf070ede3382ac13f6001e0c8b5fb8d934
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/22/2018
ms.locfileid: "46564795"
---
# <a name="install-power-bi-desktop-optimized-for-power-bi-report-server"></a>Installera Power BI Desktop som har optimerats för Power BI-rapportservern
Lär dig att installera Power BI Desktop som har optimerats för Power BI-rapportservern.

Om du vill skapa Power BI-rapporter för Power BI-rapportservern måste du hämta och installera Power BI Desktop optimerad för Power BI-rapportserver. Den här versionen skiljer sig från Power BI Desktop som används med Power BI-tjänsten. Versionen av Power BI Desktop för Power BI-tjänsten innehåller till exempel förhandsgranskningsfunktioner som inte finns tillgängliga i Power BI-rapportserverversionen förrän efter att de ges ut. Om du använder den här versionen, se till att rapportservern kan interagera med en känd version av rapporter och modeller. 

Den goda nyheten är att du kan installera Power BI Desktop och Power BI Desktop som är optimerad för Power BI-rapportserver sida vid sida på samma dator.

## <a name="download-and-install-power-bi-desktop"></a>Ladda ner och installera Power BI Desktop

Det enklaste sättet att se till att du har den senaste versionen av Power BI Desktop optimerad för Power BI-rapportserver är att starta från webbportalen för din rapportserver.

1. I webbportalen för rapportservern väljer du pilen **Hämta** > **Power BI Desktop**.

    ![Hämta Power BI Desktop från webbportalen](media/install-powerbi-desktop/report-server-download-web-portal.png)

    Eller så du kan gå direkt till [Microsoft Power BI Desktop](https://www.microsoft.com/en-us/download/details.aspx?id=57271) (optimerad för Power BI-rapportserver – augusti 2018) i Microsoft Download Center.

2. På sidan Download Center väljer du **Hämta**.

3. Beroende på din dator, väljer du: 

    - **PBIDesktopRS.msi** (32-bitarsversionen) eller

    - **PBIDesktopRS_x64.msi** (64-bitarsversionen).

1. När du har hämtat installationsprogrammet kör du installationsguiden för Power BI Desktop (augusti 2018).

2. I slutet av installationen, markerar du **Starta Power BI Desktop nu**.
   
    Det startar automatiskt och du är redo att sätta igång.

## <a name="verify-you-are-using-the-correct-version"></a>Kontrollera att du använder rätt version
Du kan kontrollera att du använder rätt version av Power BI Desktop genom att titta på startskärmen eller namnlisten i Power BI Desktop. Namnlisten visar lanseringsmånad och år för versionen.

![Namnlist för Power BI Desktop optimerad för Power BI-rapportserver](media/install-powerbi-desktop/power-bi-report-server-desktop-august-2018.png)

Power BI Desktop-versionen för Power BI-tjänsten har inte månaden och året i namnlisten.

## <a name="file-extension-association"></a>Association för filtillägg
Om du har installerat både Power BI Desktop- och Power BI Desktop som är optimerade för Power BI-rapportservern på samma dator har den senaste installationen av Power BI Desktop en filassociation med .pbix. Det innebär att när du dubbelklickar på en pbix-fil så startas den Power BI Desktop-version som installerades senast.

Om du hade Power BI Desktop och sedan installerade Power BI Desktop som har optimerats för Power BI-rapportservern öppnas alla pbix-filer i Power BI Desktop som har optimerats för Power BI-rapportservern som standard. Om du hellre vill att Power BI Desktop ska vara standard för att öppna en pbix-fil ska du installera om Power BI Desktop från Power BI-tjänsten.

Du kan alltid öppna den version av Power BI Desktop som du vill använda först. Och sedan öppna filen i Power BI Desktop.

När du redigerar en Power BI-rapport från Power BI-rapportservern eller skapar en ny Power BI-rapport från webbportalen öppnas alltid rätt version av Power BI Desktop.

## <a name="considerations-and-limitations"></a>Överväganden och begränsningar
Power BI-rapporter i Power BI-rapportserver, i Power BI-tjänsten (http://app.powerbi.com) och i Power BI-mobilappen fungerar nästan likadant men några funktioner skiljer sig).

### <a name="in-a-browser"></a>I en webbläsare
Rapporter i Power BI-rapportservern har stöd för alla visualiseringar, inklusive:

* Anpassade visuella objekt

Rapporter i Power BI-rapportservern stöder inte:

* R-visualiseringar
* ArcGIS-mappar
* Synliga sökvägar
* Power BI Desktop-förhandsgranskningsfunktioner

### <a name="in-the-power-bi-mobile-apps"></a>I Power BI-mobilappar
Rapporter i Power BI-rapportservern stöder alla de grundläggande funktionerna i [Power BI-mobilappar](../consumer/mobile/mobile-apps-for-mobile-devices.md), inklusive:

* [Telefonrapportlayout](../desktop-create-phone-report.md): Du kan optimera en rapport för Power BI-mobilappar. Optimerade rapporter på din mobiltelefon har en särskild ikon, ![telefonrapportlayout-ikonen](media/install-powerbi-desktop/power-bi-rs-mobile-optimized-icon.png) och layout.
  
    ![Rapport optimerad för telefoner](media/install-powerbi-desktop/power-bi-rs-mobile-optimized-report.png)

Rapporter i Power BI-rapportservern stöder inte de här funktionerna i Power BI-mobilappar:

* R-visualiseringar
* ArcGIS-mappar
* Anpassade visuella objekt
* Synliga sökvägar
* Geofiltering eller streckkoder

## <a name="power-bi-desktop-for-earlier-versions-of-power-bi-report-server"></a>Power BI Desktop för tidigare versioner av Power BI-rapportserver

Om din rapportserver är en tidigare version behöver du motsvarande version av Power BI Desktop. Det här är två tidigare versioner.

- Microsoft Power BI Desktop ([Optimerad för Power BI-rapportserver – oktober 2017](https://www.microsoft.com/download/details.aspx?id=56136))
- Microsoft Power BI Desktop ([Optimerad för Power BI-rapportserver – juni 2017](https://www.microsoft.com/download/details.aspx?id=55330))

## <a name="next-steps"></a>Nästa steg
Nu när du har installerat Power BI Desktop kan du börja skapa Power BI-rapporter.

[Skapa en Power BI-rapport för Power BI-rapportservern](quickstart-create-powerbi-report.md)  
[Vad är Power BI-rapportservern?](get-started.md)

Har du fler frågor? [Fråga Power BI Community](https://community.powerbi.com/)

