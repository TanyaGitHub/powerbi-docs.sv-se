---
title: Använda en alternativ e-postadress
description: Använda en alternativ e-postadress
author: mgblythe
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 03/08/2018
ms.author: mblythe
LocalizationGroup: Troubleshooting
ms.openlocfilehash: 5013c70e4d3998eb39e0de2a92f890417175fd62
ms.sourcegitcommit: 80d6b45eb84243e801b60b9038b9bff77c30d5c8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/04/2018
ms.locfileid: "34240916"
---
# <a name="using-an-alternate-email-address"></a>Använda en alternativ e-postadress
Som standard används e-postadressen som du använde för att logga in på Power BI för att skicka uppdateringar om aktiviteten i Power BI.  Om någon skickar en inbjudan skickas den till den här adressen.

Ibland kanske du vill dessa e-postmeddelanden ska skickas till en annan e-postadress än den som du ursprungligen använde för att registrera dig för Power BI.

## <a name="updating-through-office-365-personal-info-page"></a>Uppdatera via sidan personlig information i Office 365
1. Gå till [sidan personlig information i Office 365](https://portal.office.com/account/#personalinfo).  Logga in med din e-postadress och lösenord för Power BI om du uppmanas.
2. Klicka på redigeringslänken på området kontaktinformation.  
   
   > [!NOTE]
   > Om du inte ser en redigeringslänk innebär det att din e-postadress hanteras av din Office 365-administratör och du måste kontakta denna för att uppdatera din e-postadress.
   > 
   > 
   
   ![](media/service-admin-alternate-email-address-for-power-bi/contact-details.png)
3. Ange den e-postadress som du vill att Power BI-uppdateringar ska skickas till i fältet Alternativ e-postadress.

> [!NOTE]
> När du ändrar den här inställningen ändras inte vilken e-postadress som används för att skicka serviceuppdateringar, nyhetsbrev och andra erbjudanden.  De kommer alltid att skickas till e-postadressen du använde när du registrerade dig för Power BI.
> 
> 

## <a name="updating-through-azure-active-directory"></a>Uppdatera via Azure Active Directory
När du samlar in en AAD-inbäddningstoken (Azure Active Directory) för Power BI kan du använda tre olika typer av e-postadresser. De tre olika typerna är:

* den huvudsakliga e-postadressen som är kopplad till en användares AAD-konto
* UPN-e-postadressen (UserPrincipalName)
* matrisattributet för ”annan” e-postadress

Power BI väljer vilken e-postadress som ska användas baserat på följande kriterier:
1.  Om e-postattributet i AAD-klientens användarobjekt finns använder Power BI det e-postattributet för e-postadressen
2.  Om UPN-e-postadressen *inte* finns inom domänen **\*.onmicrosoft.com** (informationen efter \@-symbolen) använder Power BI det e-postattributet för e-postadressen
3.  Om matrisattributet för ”annan” e-postadress i AAD-användarobjektet finns används den första e-postadressen i den listan (eftersom det kan finnas en lista över e-postadresser i det här attributet)
4. Om inget av ovanstående villkor uppfylls används UPN-adressen

## <a name="updating-with-powershell"></a>Uppdatera med PowerShell
Alternativt kan du uppdatera den alternativa e-postadressen via PowerShell för Azure Active Directory. Detta görs med kommandot [Set-AzureADUser](https://docs.microsoft.com/powershell/module/azuread/set-azureaduser).

```
Set-AzureADUser -ObjectId john@contoso.com -OtherMails "otheremail@somedomain.com"
```

Mer information finns i [Azure Active Directory PowerShell Version 2](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2).

Har du fler frågor? [Prova Power BI Community](http://community.powerbi.com/)

