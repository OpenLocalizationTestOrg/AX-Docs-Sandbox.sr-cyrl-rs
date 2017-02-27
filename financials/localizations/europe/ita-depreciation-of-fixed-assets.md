---
title: Manual depreciation of fixed assets for Italy
description: This topic provides information about fixed assets depreciation for legal entities in Italy.
author: ShylaThompson
manager: AnnBe
ms.date: 2016-12-16 21 - 20 - 19
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetDepreciationProfile, LedgerJournalTransApprove, LedgerJournalTransAsset, LedgerJournalTransDaily, LedgerJournalTransVendInvoice, PurchTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations
ms.custom: 264294
ms.assetid: 89d8fca3-b653-4fc8-9186-b765c31f7544
ms.search.region: Italy
ms.author: v-elgolu
ms.dyn365.ops.intro: 01-05-2016
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: b97d17ceabfd25c52c5f0c1e96a123bae6941c5a
ms.openlocfilehash: 6304d68883069c2704eb7148276ed2531fdd287c
ms.lasthandoff: 02/22/2017


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


