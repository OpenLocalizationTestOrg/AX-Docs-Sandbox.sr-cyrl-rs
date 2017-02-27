---
title: Low-cost fixed assets
description: This topic provides information about low-cost fixed assets for Hungary.
author: ShylaThompson
manager: AnnBe
ms.date: 2016-12-19 19 - 43 - 08
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations
ms.custom: 264684
ms.assetid: 8452cf9f-13fa-4ea0-a4e2-c35335c863b8
ms.search.region: Hungary
ms.author: epopov
ms.dyn365.ops.intro: 01-11-2016
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: b97d17ceabfd25c52c5f0c1e96a123bae6941c5a
ms.openlocfilehash: 633b537bde107a6b35a6449a412e4d6d584a05a3
ms.lasthandoff: 02/22/2017


---

# <a name="low-cost-fixed-assets"></a>Low-cost fixed assets

This topic provides information about low-cost fixed assets for Hungary.

A low-cost asset is an asset for which the acquisition cost doesn't exceed a predefined amount. Hungarian tax law defines the limit (threshold) for low-cost assets. These assets can be fully depreciated at the same time that they are acquired.

## <a name="set-up-parameters-for-lowcost-fixed-assets"></a>Set up parameters for lowcost fixed assets
### <a name="set-up-the-low-cost-asset-threshold"></a>Set up the low-cost asset threshold

To set up the limit for low-cost assets, click **Fixed assets** &gt; **Setup** &gt; **Fixed assets parameters**. Then, in the **Low-cost asset threshold** field, enter the value limit for low-cost assets.

### <a name="set-up-books"></a>Set up books

When you create an acquisition transaction for an asset that uses the book for low-cost assets, depreciation is generated automatically.

1.  Click **Fixed assets** &gt; **Setup** &gt; **Books**.
2.  Select the book for low-cost assets, and select the **Low-cost asset** check box.

**Note:** Only value models that use the "Manual" or "Straight line service life" depreciation profiles/global methods, or the Hungary-specific "Straight line (Hu)" method, are available for low-cost depreciation.

### <a name="generate-acquisition-and-depreciation-transactions-for-low-cost-fixed-assets"></a>Generate acquisition and depreciation transactions for low-cost fixed assets

When you acquire an asset, you create an acquisition transaction from the pre-acquisition transaction. When you post the acquisition transaction for a low-cost asset, the depreciation transaction is generated automatically.


