---
title: Manual depreciation of fixed assets for Italy | Microsoft Docs
description: This topic provides information about fixed assets depreciation for legal entities in Italy.
author: ShylaThompson
manager: AnnBe
ms.date: 2016-12-16 21:20:19
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
keywords: AssetDepreciationProfile, LedgerJournalTransApprove, LedgerJournalTransAsset, LedgerJournalTransDaily, LedgerJournalTransVendInvoice, PurchTable
audience: Application User
ms.reviewer: 81
ms.suite: Released- Dynamics AX application 7.0.1
ms.custom: 264294
ms.assetid: 000b1d28-d1ec-49a7-9f23-77140cc0b105
ms.region: Italy
ms.author: v-elgolu
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: 1b37bf5e7e73b703d6e56c585075feab771ef637


---

# <a name="manual-depreciation-of-fixed-assets-for-italy"></a>Manual depreciation of fixed assets for Italy

This topic provides information about fixed assets depreciation for legal entities in Italy. 

For legal entities in Italy, the manual depreciation method has additional functionality that includes the following fields:

-   **Calculation basis** -** **This field has two options: **Days** or **Months** on the **Depreciation profiles** page. Fixed assets depreciation is calculated for the year as follows:
    -   Days depreciation = Full years depreciation \* (number of days remaining/total days in the year)
    -   Months depreciation = Full years depreciation \* (number of months remaining/12)
-   **Depreciation run date** - This field was added to the following pages:
    -   General journal
    -   Fixed asset journal
    -   Invoice approval journal
    -   Invoice journal
    -   Purchase order

The **Depreciation run date** should be set up at the time of acquisition and is set to the system date during the acquisition. The **Depreciation run date** is used to calculate depreciation for the **Number of days remaining** or **Number of Months remaining**, depending on the **Calculation basis** value. If the **Depreciation run date** is before the middle of the month (either the 15th or 14th for February), then the current month is included in number of months, otherwise the asset is considered as acquired in the next month.




<!--HONumber=Feb17_HO3-->


