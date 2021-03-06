---
title: Power BI-administratörsportalen
description: I administratörsportalen kan Power BI-klienterna i din organisation hanteras. Den innehåller sådant som användningsstatistik för åtkomst till Office 365-administrationscenter och inställningar.
author: mgblythe
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-admin
ms.topic: conceptual
ms.date: 06/28/2017
ms.author: mblythe
LocalizationGroup: Administration
ms.openlocfilehash: 2f10ead5d08efa12cae05aeb6f2e3d3068636f77
ms.sourcegitcommit: a3ce866caba24217bcdd011e892b9ea72f3d2400
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/18/2018
ms.locfileid: "49396921"
---
# <a name="power-bi-admin-portal"></a>Power BI-administratörsportalen

I administratörsportalen kan Power BI-klienterna i din organisation hanteras. Den innehåller sådant som användningsstatistik för åtkomst till Office 365-administrationscenter och inställningar.

Klient-hantering av Power BI för ditt företag görs via Power BI-administratörsportalen. Administrationsportal är tillgänglig för alla användare som är globala administratörer i Office 365 eller som har tilldelats rollen administratör i Power BI-tjänsten. Läs mer om administratörsrollen för Power BI-tjänsten i [Förstå administratörsrollen för Power BI](service-admin-role.md).

Alla användare kan se **administrationsportalen** under kugghjulsikonen. Om de inte är en administratör kan de bara se området **Premiuminställningar** och de ser bara de kapaciteter som de har behörighet att hantera.

## <a name="how-to-get-to-the-admin-portal"></a>Navigera till administrationsportalen

Ditt konto måste vara markerat som **Global administratör** i Office 365 eller Azure Active Directory, eller ha tilldelats administratörsrollen för Power BI-tjänsten, för att ha åtkomst till Power BI-administratörsportalen. Läs mer om administratörsrollen för Power BI-tjänsten i [Förstå administratörsrollen för Power BI](service-admin-role.md). Gör följande för att gå till Power BI-administratörsportalen.

1. Välj kugghjulet längst upp till höger i Power BI-tjänsten.
2. Välj **Administratörsportalen**.

![](media/service-admin-portal/powerbi-admin-settings.png)

Det finns sex flikar i portalen. Dessa beskrivs nedan.

* [Användningsstatistik](#usage-metrics)
* [Användare](#users)
* [Granskningsloggar](#audit-logs)
* [Klientinställningar](#tenant-settings)
* [Premiuminställningar](#premium-settings)
* [Bädda in koder](#embed-codes)
* [Visuella organisationsobjekt](#Organization-visuals)

![](media/service-admin-portal/powerbi-admin-landing-page.png)

## <a name="usage-metrics"></a>Användningsstatistik
Den första fliken i administrationsportalen är **Användningsstatistik**. Användningsstatistiken ger dig möjlighet att övervaka användningen inom Power BI för din organisation. Det ger också möjlighet att se vilka användare och grupper som är mest aktiva i Power BI för din organisation.

> [!NOTE]
> Första gången du använder instrumentpanelen eller när du kommer tillbaka efter en lång tid utan att visa instrumentpanelen visas antagligen en skärm för inläsning medan vi läser in instrumentpanelen.

När instrumentpanelerna har lästs in kan du se två områden med fönster. Det första området innehåller användningsdata för enskilda användare och det andra avsnittet har liknande information för grupper i din organisation.

Här är en uppdelning av vad du kan se i varje panel:

* Räknar separat instrumentpaneler, rapporter och datauppsättningar på användararbetsytan
  
    ![](media/service-admin-portal/powerbi-admin-usage-metrics-number-tiles.png)

* Med använd instrumentpanel enligt antal användare med åtkomst till den. Till exempel, om du har en instrumentpanel som du har delat med 3 användare och du även har lagt till den i ett innehållspaket som två olika användare som är anslutna till, skulle antalet vara 6 (1 + 3 + 2)
  
    ![](media/service-admin-portal/powerbi-admin-usage-metrics-top-dashboards.png)

* Det mest populära innehåll som användare är anslutna till. Det är något användarna kan nå genom processen Hämta data, det vill säga innehållspaket från SaaS, organisationsinnehållspaket, filer eller databaser.
  
    ![](media/service-admin-portal/powerbi-admin-usage-metrics-top-connections.png)

* En vy över toppanvändarna baserat på hur många instrumentpaneler de har, såväl instrumentpaneler de skapat själva som instrumentpaneler som någon har delat med dem.
  
    ![](media/service-admin-portal/powerbi-admin-usage-metrics-top-users-dashboards.png)

* En vy över toppanvändarna baserat på hur många rapporter de har
  
    ![](media/service-admin-portal/powerbi-admin-usage-metrics-top-users-reports.png)

Det andra avsnittet visar samma typ av information, men baserat på grupper. Här kan du se vilka grupper i din organisation som är mest aktiva och vilken sorts information de använder.

Med den här informationen kommer du att kunna hämta verkliga insikter om hur personer använder Power BI inom organisationen och identifiera de användare och grupper som är mest aktiva i din organisation.

## <a name="users"></a>Användare

Den andra fliken i administrationsportalen är **Hantera användare**. Användarhantering för Power BI sker i administrationscentret för Office 365, så det här avsnittet hjälper dig att snabbt nå området för att hantera användare, administratörer och grupper i Office 365.

![](media/service-admin-portal/powerbi-admin-manage-users.png)

När du klickar på **gå till administrationscentret för O365**, går du direkt till startsidan för Office 365 Administrationscenter för att hantera användare för din klient.

![](media/service-admin-portal/powerbi-admin-o365-admin-center.png)

## <a name="audit-logs"></a>Granskningsloggar

Den tredje fliken i administrationsportalen är **granskningsloggar**. Loggarna finns i säkerhet- och efterlevnadscentrum för Office 365. Detta avsnitt ger snabbåtkomst till detta område i Office 365.

Mer information om granskningsloggarna finns i [granska Power BI i din organisation](service-admin-auditing.md)

## <a name="tenant-settings"></a>Klientinställningar

Den tredje fliken i administrationsportalen är **klientinställningar**. Klientinställningarna ger dig större kontroll över vilka funktioner som är tillgängliga för din organisation. Om du har frågor kring känsliga data, vissa av våra funktioner inte är lämpliga för din organisation eller om du bara vill att en viss funktion ska vara tillgänglig för en särskild grupp. Om så är fallet, kan du stänga av den i din klient.

![](media/service-admin-portal/powerbi-admin-tenant-settings.png)

> [!NOTE]
> Det kan ta upp till 10 minuter för att inställningen ska gälla för alla i din klient.

Inställningarna kan ha tre tillstånd:

* **Har inaktiverats för hela organisationen**: Du kan inaktivera en funktion så att användare inte kan använda den.

    ![](media/service-admin-portal/powerbi-admin-tenant-settings-disabled.png)

* **Har aktiverats för hela organisationen**: Du kan aktivera en funktion för hela organisationen så att alla användare har åtkomst till funktionen.

    ![](media/service-admin-portal/powerbi-admin-tenant-settings-enabled.png)

* **Har aktiverats för en del av organisationen**: Du kan även aktivera en funktion för en del av din organisation. Detta kan göras på ett par olika sätt. Du kan aktivera den för hela organisationen utom en viss användargrupp.

    ![](media/service-admin-portal/powerbi-admin-tenant-settings-enabled-except.png)

    Du kan också endast aktivera funktionen för en viss grupp av användare och även inaktivera den för en grupp av användare. Därmed har vissa användare inte åtkomst till funktionen även om de finns i en tillåten grupp.

    ![](media/service-admin-portal/powerbi-admin-tenant-settings-enabled-except2.png)

Följande avsnitt ger en översikt över de olika typerna av inställningar för klientorganisation.

## <a name="workspace-settings"></a>Arbetsyteinställningar

### <a name="create-workspaces-preview"></a>Skapa arbetsytor (förhandsversion)
Användare i organisationen kan skapa apparbetsytor för att samarbeta på instrumentpaneler, rapporter och annat innehåll.

Mer information finns i [Skapa nya arbetsytor](service-create-the-new-workspaces.md).

## <a name="export-and-sharing-settings"></a>Inställningar för export och delning

### <a name="share-content-to-external-users"></a>Dela innehåll för externa användare

Användare i organisationen kan dela instrumentpaneler med användare utanför organisationen.

![](media/service-admin-portal/powerbi-admin-sharing-external-02.png)

Här är meddelandet som visas när du delar med en extern användare.

![](media/service-admin-portal/powerbi-admin-sharing-external.png)

### <a name="publish-to-web"></a>Publicera på webben

Användare i organisationen kan publicera rapporter på webben. [Läs mer](service-publish-to-web.md)

![](media/service-admin-portal/powerbi-admin-publish-to-web.png)

Användarna ser olika alternativ i användargränssnittet baserat på vad inställningen för publicering på webben är.

|Visning av aktuellt objekt |Aktiverad för hela organisationen |Inaktiverad för hela organisationen |Specifika säkerhetsgrupper   |
|---------|---------|---------|---------|
|**Publicera på webben** under rapportens **Fil**meny.|Aktiverad för alla|Inte synlig för alla|Endast synlig för behöriga användare eller grupper.|
|**Hantera inbäddade koder** under **Inställningar**|Aktiverad för alla|Aktiverad för alla|Aktiverad för alla<br><br>Alternativet * **Ta bort** endast för behöriga användare eller grupper.<br>* **Hämta koder** aktiverat för alla.|
|**Inbäddade koder** i administrationsportalen|Statusen visar något av följande:<br>* Aktiv<br>* Stöds ej<br>* Blockerad|Statusen visar **Inaktiverad**|Statusen visar något av följande:<br>* Aktiv<br>* Stöds ej<br>* Blockerad<br><br>Om en användare inte har behörighet baserat på klientinställningen visas statusen **Intrång**.|
|Befintliga publicerade rapporter|Alla aktiverade|Alla inaktiverade|Rapporter fortsätta att visas för alla.|

### <a name="export-data"></a>Exportera data

Användare i organisationen kan exportera data från ett fönster eller en visualisering. [Läs mer](visuals/power-bi-visualization-export-data.md)

![](media/service-admin-portal/powerbi-admin-export-data.png)

> [!NOTE]
> När du inaktiverar **Exportera data** kan användare inte heller använda funktionen **Analysera i Excel** eller live-anslutning till Power BI-tjänsten.

### <a name="export-reports-as-powerpoint-presentations"></a>Exportera rapporter som PowerPoint-presentationer

Användare i organisationen kan exportera Power BI-rapporter som PowerPoint-filer. [Läs mer](consumer/end-user-powerpoint.md)

![](media/service-admin-portal/powerbi-admin-powerpoint.png)

### <a name="print-dashboards-and-reports"></a>Skriva ut instrumentpaneler och rapporter

Användare i organisationen kan skriva ut instrumentpaneler och rapporter. [Läs mer](consumer/end-user-print.md)

![](media/service-admin-portal/powerbi-admin-print-dashboard.png)

![](media/service-admin-portal/powerbi-admin-print-report.png)

## <a name="content-pack-settings"></a>Inställningar för innehållspaket

### <a name="publish-content-packs-to-the-entire-organization"></a>Publicera innehållspaket för hela organisationen

Användare i organisationen kan publicera innehållspaket i hela organisationen.

![](media/service-admin-portal/powerbi-admin-publish-entire-org.png)

### <a name="create-template-organizational-content-packs"></a>Skapa mall för organisationsinnehållspaket

Användare i organisationen kan skapa mallinnehållspaket som använder datauppsättningar som bygger på en datakälla i Power BI Desktop.

### <a name="push-apps-to-end-users"></a>Pusha appar till slutanvändare

Din klientadministratör aktiverar funktionen för att pusha appar i **Klientinställningar**.

   ![Aktivera funktionen för att pusha appar](media/service-create-distribute-apps/power-bi-apps-pushapps01.png)

Du kan växla inställningen till **Aktiverad** och sedan ange vilka som får den här funktionen (hela organisationen eller specifika säkerhetsgrupper).

> [!NOTE]
> Tänk på att det tar tid innan klientinställningarna verkställs.

Här kan du [läsa mer om att pusha appar](service-create-distribute-apps.md).

## <a name="integration-settings"></a>Inställningar för integrering

### <a name="ask-questions-about-data-using-cortana"></a>Ställ frågor om data med hjälp av Cortana

Användare i organisationen kan ställa frågor om sina data med hjälp av Cortana.

> [!NOTE]
> Den här inställningen gäller för hela organisationen och kan inte begränsas till specifika grupper.

### <a name="use-analyze-in-excel-with-on-premises-datasets"></a>Analysera i Excel med lokala datauppsättningar

Användare i organisationen kan använda Excel för att visa och interagera med lokala Power BI-datauppsättningar. [Läs mer](service-analyze-in-excel.md)

> [!NOTE]
> När du inaktiverar **Exportera data** kan användare inte heller använda funktionen **Analysera i Excel**.

### <a name="use-arcgis-maps-for-power-bi"></a>Använda ArcGIS Maps for Power BI

Användare i organisationen kan använda ArcGIS Maps for Power BI-visualiseringen som tillhandahålls av Esri. [Läs mer](power-bi-visualization-arcgis.md)

### <a name="use-global-search-for-power-bi-preview"></a>Använda global sökning för Power BI (förhandsversion)

Användare i organisationen kan använda externa sökfunktioner som förlitar sig på Azure Search. Användare kan till exempel använda Cortana för att hämta viktig information direkt från Power BI-instrumentpaneler och Power BI-rapporter. [Läs mer](service-cortana-intro.md)

## <a name="custom-visuals-settings"></a>Inställningar för anpassade visuella objekt

### <a name="enable-custom-visuals-for-the-entire-organization"></a>Aktivera anpassad visuell information för hela organisationen

Användare i organisationen kan interagera med och dela anpassad visuell information. [Läs mer](power-bi-custom-visuals.md)

> [!NOTE]
> Den här inställningen gäller för hela organisationen och kan inte begränsas till specifika grupper.

## <a name="r-visuals-settings"></a>Inställningar för R-visualisering

### <a name="interact-with-and-share-r-visuals"></a>Interagera med och dela visuell R-information

Användare i organisationen kan interagera med och dela visuella objekt som skapats med R-skript. [Läs mer](visuals/service-r-visuals.md)

> [!NOTE]
> Den här inställningen gäller för hela organisationen och kan inte begränsas till specifika grupper.

## <a name="audit-and-usage-settings"></a>Gransknings- och användningsinställningar

### <a name="create-audit-logs-for-internal-activity-auditing-and-compliance"></a>Skapa granskningsloggar för intern aktivitetsgranskning och efterlevnad

Användare i organisationen kan använda granskning för att övervaka åtgärder som vidtas i Power BI av andra användare i organisationen. [Läs mer](service-admin-auditing.md)

Den här inställningen måste vara aktiverad för att registrera granskningsloggposter. Det kan förekomma en fördröjning på upp till 48 timmar mellan det att granskning aktiveras och att granskningsdata kan visas. Om du inte ser data omedelbart kontrollerar du granskningsloggarna senare. Det kan förekomma en liknande fördröjning mellan hämtning av behörighet för att visa granskningsloggar och att komma åt loggarna.

> [!NOTE]
> Den här inställningen gäller för hela organisationen och kan inte begränsas till specifika grupper.

### <a name="usage-metrics-for-content-creators"></a>Användningsstatistik för skapare av innehåll
Användarna i organisationen kan se användningsstatistik för de instrumentpaneler och rapporter som de har skapat. [Läs mer](service-usage-metrics.md).

Du kan växla inställningen till **Aktiverad** och sedan ange vilka som kan se användningsstatistik (hela organisationen eller specifika säkerhetsgrupper).

> [!NOTE]
> Tänk på att det tar tid innan klientinställningarna verkställs.

### <a name="per-user-data-in-usage-metrics-for-content-creators"></a>Data per användare i användningsmått för innehållsskapare
Om du använder mått för skapare av innehåll visas visningsnamn och e-postadresser för de användare som har åtkomst till innehållet. [Läs mer](service-usage-metrics.md).

Du kan växla inställningen till **Aktiverad** och sedan ange vilka som kan se visningsnamn och e-postadresser i användningsstatistiken (hela organisationen eller specifika säkerhetsgrupper).

Data per användare är aktiverat för användningsstatistik som standard, och kontoinformation om innehållsskapare ingår i statistikrapporten. Om du inte vill inkludera den här informationen för vissa eller alla användare kan du inaktivera funktionen för specifika säkerhetsgrupper eller hela organisationen. Kontoinformation visas då i rapporten som *Namnlös*.

> [!NOTE]
> Tänk på att det tar tid innan klientinställningarna verkställs.


## <a name="dashboard-settings"></a>Inställningar för instrumentpanelen

### <a name="data-classification-for-dashboards"></a>Klassificering av instrumentpanelsdata

Användare i organisationen kan tagga instrumentpaneler med klassificeringar som anger instrumentpanelens säkerhetsnivåer. [Läs mer](service-data-classification.md)

> [!NOTE]
> Den här inställningen gäller för hela organisationen och kan inte begränsas till specifika grupper.

## <a name="developer-settings"></a>Inställningar för utvecklare

### <a name="embed-content-in-apps"></a>Bädda in innehåll i appar

Användare i organisationen kan bädda in Power BI-instrumentpaneler och rapporter i SaaS-program (programvara som en tjänst). När du inaktiverar den här inställningen kan användare inte använda REST-API: er för att bädda in Power BI-innehåll i sina program.

## <a name="capacity-settings"></a>Kapacitetsinställningar

### <a name="premium-settings"></a>Premiuminställningar

På fliken Premiuminställningar kan du hantera alla premiumfunktioner för Power BI (Em eller P SKU) som har köpts för din organisation. Alla användare inom din organisation ser fliken Premiuminställningar, men kan endast se innehåll om de har angetts som antingen **kapacitetadministratör** eller en användare som har tilldelningsbehörighet. Om en användare inte har några behörigheter visas följande meddelande.

![Administratörsinställningar till Power BI Premium](media/service-admin-portal/premium-settings-no-access.png "Ingen åtkomst till premiuminställningar")

Mer information om hur du hanterar premiuminställningar finns [Hantera Power BI Premium](service-admin-premium-manage.md).

### <a name="power-bi-embedded-settings"></a>Inställningar för Power BI Embedded

På fliken för Power BI Embedded-inställningar kan du visa de Power BI Embedded-kapaciteter (A SKU) som du har köpt för din kund. Eftersom du kan bara köpa A SKU:er från Azure kan du [hantera inbäddade kapaciteter i Azure](developer/azure-pbie-create-capacity.md) från **Azure Portal**.

![Administratörsinställningar för Power BI Embedded](media/service-admin-portal/manage-pbie-capacities-01.png)

![Information om administratörsinställningar för Power BI Embedded](media/service-admin-portal/manage-pbie-capacities-02.png)

Mer information om hur du hanterar inställningar för Power BI Embedded (A SKU) finns i [Vad är Power BI Embedded](developer/azure-pbie-what-is-power-bi-embedded.md).

## <a name="embed-codes"></a>Bädda in koder

![Bädda in koder i administrationsportalen för Power BI](media/service-admin-portal/embed-codes.png)

Som administratör kan du visa de inbäddningskoder som har genererats för din klient. Du har åtgärderna för att visa rapporten och ta bort den inbäddade koden om du vill återkalla den.

## <a name="organization-visuals"></a>Visuella organisationsobjekt

Med fliken för visuella organisationsobjekt kan du distribuera och hantera anpassade visuella objekt i din organisation, så att du lätt kan distribuera egna anpassade visuella objekt i organisationen, och så att rapportförfattare enkelt kan identifiera och importera dessa visuella objekt direkt från Power BI Desktop till sina rapporter.

Sidan visar alla de anpassade visuella objekt som för närvarande har distribuerats i organisationens databas.

![Organisera visuellt objekt som administratör](media/service-admin-portal/power-bi-custom-visuals-organizational-admin-01.png)

### <a name="add-a-new-custom-visual"></a>Lägga till ett nytt anpassat visuellt objekt

Om du vill lägga till ett nytt anpassat visuellt objekt i listan väljer du **Lägg till ett anpassat visuellt objekt**

![](media/service-admin-portal/power-bi-custom-visuals-organizational-admin-02.png)

> [!WARNING]
> Ett anpassat visuellt objekt kan innehålla kod som innebär säkerhets- eller integritetsrisker. Kontrollera att författaren och det visuella objektets källa är betrodda innan du distribuerar till organisationens databas.

Fyll i fälten:

* Välj en .pbiviz-fil (obligatoriskt): välj en fil för ett anpassat visuellt objekt att överföra. Endast versionshanterade visuella API-objekt stöds, och här kan du läsa vad det innebär.

Innan du överför ett anpassat visuellt objekt bör du granska objektet ur säkerhets- och sekretessynvinkel för att säkerställa att det uppfyller din organisations standarder. Läs mer om säkerhet och anpassade visuella objekt.

* Namnge ditt anpassade visuella objekt (obligatoriskt): ge det visuella objektet en kort rubrik så att Power BI Desktop-användare lätt kan förstå hur det fungerar

* Ikon (obligatoriskt): den ikonfil som visas i användargränssnittet för Power BI Desktop.

* Beskrivning: en kort beskrivning av det visuella objektet som ger användaren mer kontext och kunskap

Initiera överföringsförfrågan genom att välja Använd. Om detta lyckas visas det nya objektet i listan. Om det inte lyckas får du ett felmeddelande

### <a name="delete-a-custom-visual-from-the-list"></a>Ta bort ett anpassat visuellt objekt från listan

Välj papperskorgen om du vill ta bort det visuella objektet permanent från databasen.
Viktigt: Du kan inte ångra borttagningen. När det visuella objektet väl har tagits bort upphör det omedelbart att återges i befintliga rapporter. Även om du överför samma visuella objekt igen, så ersätter det inte det föregående objekt som tagits bort. Användarna kan importera det nya visuella objektet på nytt och ersätta den förekomst de har i sina rapporter.

### <a name="disable-a-custom-visual-in-the-list"></a>Inaktivera ett anpassat visuellt objekt i listan

Välj kugghjulsikonen om du vill inaktivera det visuella objektet från organisationens lager. Inaktivera det anpassade visuella objektet i avsnittet **Åtkomst**.

När du har inaktiverat det visuella objektet återges inte det visuella objektet i befintliga rapporter utan visar felmeddelandet nedan.

*Detta anpassade visuella objekt är inte längre tillgängligt. Kontakta din administratör om du vill ha mer information.*

Visuella objekt som har bokmärken fungerar dock fortfarande.

Efter uppdatering eller byte av administratör bör Power BI Desktop-användare starta om programmet eller uppdatera webbläsaren i Power BI-tjänsten för att se uppdateringarna.

### <a name="how-to-update-a-visual"></a>Så här uppdaterar du ett visuellt objekt

Om du vill uppdatera en visualisering i databasen eftersom det finns en ny version av visualiseringen (t.ex. felkorrigeringar, nya funktioner, etc.), väljer du ikonen **Uppdatera** och laddar upp den nya filen. Kontrollera att visualiserings-ID förblir oförändrat. Den nya filen ersätter den tidigare filen för alla rapporter i hela organisationen. Men om den nya versionen av visualiseringen kan skada någon användnings- eller datastruktur av den tidigare versionen av visualiseringen ska du inte ersätta den tidigare versionen. I stället bör du skapa en ny lista för den nya versionen av visualiseringen. Lägg till exempel till ett nytt versionsnummer (version X.X) till rubriken för den nya listade visualiseringen. På det här sättet är det klart att det är samma visualisering men bara med ett uppdaterat versionsnummer så att befintliga rapporter inte skadar deras funktioner. Kontrollera igen att visualiserings-ID förblir oförändrat. Nästa gång användarna använder organisationens databas från Power BI Desktop kan de importera den nya versionen, vilket tvingar dem att ersätta den aktuella version som de har i sina rapporter.

## <a name="next-steps"></a>Nästa steg

[Förstå Power BI-administratörsrollen](service-admin-role.md)  
[Granska Power BI i din organisation](service-admin-auditing.md)  
[Hantera Power BI Premium](service-admin-premium-manage.md)  
[Administrera Power BI i din organisation](service-admin-administering-power-bi-in-your-organization.md)  

Har du fler frågor? [Fråga Power BI Community](http://community.powerbi.com/)
