---
title: Skala din Power BI Embedded-kapacitet | Microsoft Docs
description: Den här artikeln beskriver hur du skalar din Power BI Embedded-kapacitet i Microsoft Azure.
services: power-bi-embedded
author: markingmyname
ms.author: maghan
manager: kfile
editor: ''
tags: ''
ms.service: power-bi-embedded
ms.topic: conceptual
ms.date: 07/31/2018
ms.openlocfilehash: 08ba4113eb4988919c249052e883e8887295a028
ms.sourcegitcommit: fecea174721d0eb4e1927c1116d2604a822e4090
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/31/2018
ms.locfileid: "39360365"
---
# <a name="scale-your-power-bi-embedded-capacity-in-the-azure-portal"></a>Skala din Power BI Embedded-kapacitet på Azure Portal

Den här artikeln beskriver hur du skalar din Power BI Embedded-kapacitet i Microsoft Azure. Genom att skala kan du öka eller minska storleken på din kapacitet.

Detta förutsätter att du har skapat en Power BI Embedded-kapacitet. Om du inte har gjort det läser du [Skapa Power BI Embedded-kapacitet på Azure Portal](azure-pbie-create-capacity.md) för att komma igång.

> [!NOTE]
> En skalningsåtgärd tar ungefär en minut. Kapaciteten är inte tillgänglig under denna tid. Inbäddat innehåll kanske inte kan läsas in.

## <a name="scale-a-capacity"></a>Skala en kapacitet

1. Logga in på [Azure Portal](https://portal.azure.com/).

2. Visa dina kapaciteter genom att välja **Alla tjänster** > **Power BI Embedded**.

    ![Alla tjänster på Azure Portal](media/azure-pbie-scale-capacity/azure-portal-more-services.png)

3. Välj den kapacitet som du vill skala.

    ![Lista över Power BI Embedded-kapaciteter på Azure Portal](media/azure-pbie-scale-capacity/azure-portal-capacity-list.png)

4. Välj **Prisnivå** under **Skala** i din kapacitet.

    ![Alternativet Prisnivå under Skala](media/azure-pbie-scale-capacity/azure-portal-scale-pricing-tier.png)

    Din aktuella prisnivå är markerat med blått.

    ![Aktuell prisnivå i blått](media/azure-pbie-scale-capacity/azure-portal-current-tier.png)

5. Om du vill skala upp eller ned väljer du den nya nivån som du vill byta till. När du väljer en ny nivå visas en streckad blå linje runt ditt val. Välj **Välj** för att skala till den nya nivån.

    ![Välj ny nivå](media/azure-pbie-scale-capacity/azure-portal-select-new-tier.png)

    Skalningen tar en eller ett par minuter.

6. Bekräfta din nivå genom att gå till fliken Översikt. Den aktuella prisnivån visas.

    ![Bekräfta aktuell nivå](media/azure-pbie-scale-capacity/azure-portal-confirm-tier.png)

## <a name="next-steps"></a>Nästa steg

Om du vill pausa eller starta din kapacitet läser du [Pausa och starta din Power BI Embedded-kapacitet på Azure Portal](azure-pbie-pause-start.md).

Om du vill börja bädda in Power BI-innehåll i ditt program läser du [Bädda in Power BI-instrumentpaneler, -rapporter och -paneler](https://powerbi.microsoft.com/documentation/powerbi-developer-embedding-content/).

Har du fler frågor? [Fråga Power BI Community](http://community.powerbi.com/)
