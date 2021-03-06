---
title: Använda enkel inloggning (SSO) från Power BI till lokala datakällor
description: Konfigurera din gateway för att aktivera enkel inloggning (SSO) från Power BI till lokala datakällor.
author: mgblythe
ms.author: mblythe
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-gateways
ms.topic: conceptual
ms.date: 10/15/2018
LocalizationGroup: Gateways
ms.openlocfilehash: c489ff0e1b764a6ee3dc026e8294132dc8f49025
ms.sourcegitcommit: 2c4a075fe16ccac8e25f7ca0b40d404eacb49f6d
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/20/2018
ms.locfileid: "49474760"
---
# <a name="overview-of-single-sign-on-sso-for-gateways-in-power-bi"></a>Översikt över enkel inloggning (SSO) för gatewayer i Power BI

Du kan få en sömlös enkel inloggningsanslutning, vilket medför att Power BI-rapporter och -instrumentpaneler kan uppdateras från lokala data, genom att konfigurera din lokala datagateway med antingen Kerberos eller Security Assertion Markup Language (SAML). Den lokala datagatewayen genomför enkel inloggning med hjälp av DirectQuery, som används för att ansluta till lokala datakällor.

Vi stöder för närvarande följande datakällor:

* SQL Server ([Kerberos](service-gateway-sso-kerberos.md))
* SAP HANA ([Kerberos](service-gateway-sso-kerberos.md) och [SAML](service-gateway-sso-saml.md)
* Teradata ([Kerberos](service-gateway-sso-kerberos.md))
* Spark ([Kerberos](service-gateway-sso-kerberos.md))

När en användare interagerar med en DirectQuery-rapport i Power BI-tjänsten, kan varje åtgärd relaterad till korsfiltrering, sektor, sortering och rapportredigering resultera i frågor som körs i realtid mot den underliggande lokala datakällan.  När enkel inloggning har konfigurerats för datakällan körs frågorna under identiteten för den användare som interagerar med Power BI (det vill säga via webbläsaren eller Power BI Mobile-appar). Därmed ser varje användare exakt de data som han eller hon har behörighet för i den underliggande datakällan – med enkel inloggning konfigurerad finns det ingen delad datacachelagring för olika användare.

## <a name="query-steps-when-running-sso"></a>Frågesteg vid körning av enkel inloggning

En fråga som körs med SSO (enkel inloggning) består av tre steg, vilket visas i följande diagram.

![Frågesteg med enkel inloggning](media/service-gateway-sso-overview/sso-query-steps.png)

> [!NOTE]
> SSO för Oracle har inte aktiverats ännu, men är under utveckling och kommer snart.

Här finns mer information om de här stegen:

1. För varje fråga inkluderar **Power BI-tjänsten** *användarens huvudnamn* (UPN) vid sändning av en fråga till den konfigurerade gatewayen.

2. Gatewayen måste mappa Microsoft Azure Active Directorys UPN till en lokal Active Directory-identitet.

   a.  Om Azure AD DirSync (även kallat *Azure AD Connect*) har konfigurerats fungerar mappningen automatiskt i gatewayen.

   b.  I annat fall kan gatewayen söka upp och mappa Microsoft Azure AD UPN:en till en lokal användare genom att utföra en sökning mot den lokala Active Directory-domänen.

3. Gatewaytjänstprocessen personifierar den mappade lokala användaren, öppnar anslutningen till den underliggande databasen och skickar frågan. Gatewayen måste inte vara installerad på samma dator som databasen.

## <a name="next-steps"></a>Nästa steg

Nu när du förstår grunderna för enkel inloggning kan du läsa mer detaljerad information om Kerberos och SAML:

* [Enkel inloggning (SSO) – Kerberos](service-gateway-sso-kerberos.md)
* [Enkel inloggning (SSO) – SAML](service-gateway-sso-saml.md)
