---
title: Konfigurera proxyinställningar för den lokala datagatewayen
description: Information om konfiguration av proxyinställningar för den lokala datagatewayen.
author: mgblythe
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-gateways
ms.topic: conceptual
ms.date: 11/21/2017
ms.author: mblythe
LocalizationGroup: Gateways
ms.openlocfilehash: 2a62623ff54f13ac3547f53275be6d144d90025d
ms.sourcegitcommit: cce10e14c111e8a19f282ad6c032d802ebfec943
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2018
ms.locfileid: "39658114"
---
# <a name="configuring-proxy-settings-for-the-on-premises-data-gateway"></a>Konfigurera proxyinställningar för den lokala datagatewayen
Din arbetsmiljö kan kräva att du går via en proxy för att ansluta till Internet. Detta kan förhindra att den lokala datagatewayen ansluter till tjänsten.

## <a name="does-your-network-use-a-proxy"></a>Använder ditt nätverk en proxy?
I följande inlägg på superuser.com beskrivs hur du kan se om du har en proxy i nätverket.

[Hur vet jag vilken proxyserver jag använder? (SuperUser.com)](https://superuser.com/questions/346372/how-do-i-know-what-proxy-server-im-using)

## <a name="configuration-file-location-and-default-configuration"></a>Konfigurationsfilens plats och standardkonfiguration
Proxyinformationen har konfigurerats i en konfigurationsfil för .NET. Plats och filnamn är olika beroende på vilken gateway du använder.

### <a name="on-premises-data-gateway"></a>Lokal datagateway
Det finns två huvudsakliga konfigurationsfiler som ingår i den lokala datagatewayen.

**Konfiguration**

Den första är för konfigurationsskärmarna som faktiskt konfigurerar gatewayen. Om du har problem med att konfigurera gatewayen, är detta den fil som du ska titta i.

    C:\Program Files\On-premises data gateway\enterprisegatewayconfigurator.exe.config

**Windows-tjänst**

Den andra är för den Windows-tjänst som interagerar med Power BI-tjänsten och hanterar begäranden.

    C:\Program Files\On-premises data gateway\Microsoft.PowerBI.EnterpriseGateway.exe.config

## <a name="configuring-proxy-settings"></a>Konfigurera proxyinställningar
Standardproxykonfigurationen är följande.

    <system.net>
        <defaultProxy useDefaultCredentials="true" />
    </system.net>

Standardkonfigurationen fungerar med Windows-autentisering. Om proxyn använder en annan form av autentisering, behöver du ändra inställningarna. Om du inte är säker, kontaktar du din nätverksadministratör. Grundläggande proxyautentisering rekommenderas inte. Försök att använda grundläggande proxyautentisering kan orsaka proxyautentiseringsfel som resulterar i en gateway som inte är korrekt konfigurerad. Använd en starkare proxyautentiseringsmetod i stället.

Förutom att använda standardautentiseringsuppgifter kan du lägga till ett <proxy>-element och definiera proxyserverinställningar i mer detalj. Du kan till exempel ange att din lokala datagateway alltid ska använda proxyservern även för lokala resurser genom att ange parametern bypassonlocal till false. Detta kan vara användbart i felsökningssituationer om du vill spåra alla HTTPS-förfrågningar från en lokal datagateway i proxyloggfilerna. Följande exempelkonfiguration anger att alla förfrågningar måste gå via en specifik proxyserver med IP-adressen 192.168.1.10.

    <system.net>
        <defaultProxy useDefaultCredentials="true">
            <proxy  
                autoDetect="false"  
                proxyaddress="http://192.168.1.10:3128"  
                bypassonlocal="false"  
                usesystemdefault="true"
            />  
        </defaultProxy>
    </system.net>

Mer information om konfiguration av proxyelement för .NET-konfigurationsfiler finns i [defaultProxy-element (nätverksinställningar)](https://msdn.microsoft.com/library/kd3cf2ex.aspx).

## <a name="changing-the-gateway-service-account-to-a-domain-user"></a>Ändra gatewayens tjänstkonto till en domänanvändare
När du konfigurerar proxyinställningarna till att använda standardautentiseringsuppgifter enligt beskrivningen ovan, kan det uppstå autentiseringsproblem med proxyn. Detta beror på att standardkontot är ett tjänst-SID och inte en autentiserad domänanvändare. Du kan ändra gatewayens tjänstkonto till att tillåta korrekt autentisering med proxyn.

> [!NOTE]
> Vi rekommenderar att du använder ett hanterat tjänstkonto för att undvika att behöva återställa lösenorden. Lär dig hur du skapar ett [hanterat tjänstkonto](https://technet.microsoft.com/library/dd548356.aspx) i Active Directory.
> 
> 

### <a name="change-the-on-premises-data-gateway-service-account"></a>Ändra det lokala tjänstkontot för datagatewayen
1. Ändra Windows-tjänstkontot för den **lokala datagatewaytjänsten**.

    Standardkontot för tjänsten är *NT SERVICE\PBIEgwService*. Du kan ändra det till ett domänanvändarkonto i Active Directory-domänen. Eller så kan du använda ett hanterat tjänstkonto för att undvika att behöva ändra lösenordet.

    Du kan ändra kontot på fliken **Logga in** i egenskaperna för Windows-tjänsten.
2. Starta om den **lokala datagatewaytjänsten**.

    Utfärda följande kommandon i kommandotolken som administratör.

        net stop PBIEgwService

        net start PBIEgwService
3. Starta den **lokala datagatewaykonfiguratorn**. Du kan använda startknappen i Windows och söka efter *den lokala datagatewayen*.
4. Logga in i Power BI.
5. Återställa gatewayen med återställningsnyckeln.

    Detta gör att det nya tjänstkontot kan dekryptera lagrade autentiseringsuppgifter för datakällor.

> [!NOTE]
> När du ändrar tjänstkontot direkt via kontrollpanelen Tjänster, uppdateras inte ACL:er automatiskt. Du måste kontrollera att det nya tjänstkontot har åtkomst till installationsfilerna och mappen. Du hittar gatewayens installationsmapp under C:\Program\Lokal datagateway. 
> 

## <a name="next-steps"></a>Nästa steg
[Lokal datagateway (personligt läge)](service-gateway-personal-mode.md)
[Brandväggsinformation](service-gateway-onprem-tshoot.md#firewall-or-proxy)  
Har du fler frågor? [Prova Power BI Community](http://community.powerbi.com/)

