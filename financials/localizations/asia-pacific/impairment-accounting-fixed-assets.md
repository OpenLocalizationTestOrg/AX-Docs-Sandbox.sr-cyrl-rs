---
title: Impairment accounting for fixed assets
description: This topic includes information about impairment accounting for fixed assets in Japan.
author: ShylaThompson
manager: AnnBe
ms.date: 2016-01-06 20 - 55 - 06
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetImpairmentAssetTransInquire_JP, AssetImpairmentIndicator_JP, AssetImpairmentManageTestResult_JP
audience: Application User
ms.search.scope: AX 7.0.0, Operations
ms.custom: 28811
ms.assetid: db96c6bb-c2b1-4e26-b711-33caa49eb29f
ms.search.region: Japan
ms.author: leguo
ms.dyn365.ops.intro: 01-02-2016
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b97d17ceabfd25c52c5f0c1e96a123bae6941c5a
ms.openlocfilehash: 9095ca23cdd4a20c3de0848cff967f9c229295b2
ms.lasthandoff: 02/22/2017


---

# <a name="impairment-accounting-for-fixed-assets"></a>Impairment accounting for fixed assets

This topic includes information about impairment accounting for fixed assets in Japan.

You can perform the following tasks to set up and calculate fixed asset impairments by using Microsoft Dynamics 365 for Operations:

-   Generate a list of fixed assets that might be impaired. You can then manually review and calculate the undiscounted cash flow, fair value, or recoverable amounts of each asset in the list to determine whether the fixed assets are impaired.
-   Update impairment indicators, such as the undiscounted cash flow of the fixed assets.
-   Run the impairment recognition test by using the impairment indicators to generate a list of impaired fixed assets.
-   Specify recoverable values that indicate the extent to which the fixed assets are impaired, and then create journal transactions for these impaired fixed assets. You can specify the details about the impairment before you post the journal.
-   View the details of the impairment transactions for fixed assets.

## <a name="how-can-i-identify-impairments-in-fixed-assets"></a>How can I identify impairments in fixed assets?
You can use impairment indicators to identify impairment in fixed assets. On the **Impairment review** page, you can generate a list of fixed assets that might be impaired. You can then manually calculate the undiscounted cash flow and update impairment indicators for the fixed assets on the **Update impairment indicators** page. When you run the impairment recognition test, you can use the impairment indicators that you updated to identify impairments in fixed assets.

## <a name="can-i-select-which-assets-to-test-for-impairment"></a>Can I select which assets to test for impairment?
Yes, you can select which assets to test for impairment. To specify the criteria, click **Query** on the **Impairment recognition test** page.

## <a name="how-often-can-i-check-fixed-assets-for-impairment"></a>How often can I check fixed assets for impairment?
By creating a batch job, you can set up Microsoft Dynamics AX to check the fixed assets for impairment according to a schedule.

## <a name="are-there-types-of-fixed-assets-that-are-excluded-from-impairment-testing-and-accounting"></a>Are there types of fixed assets that are excluded from impairment testing and accounting?
Yes, the following types of fixed assets are excluded from impairment testing and accounting:

-   Leased fixed assets
-   Shared assets
-   Goodwill fixed asset

You must use the impairment for cash generating units to account for goodwill and shared assets.

## <a name="can-i-generate-reports-that-i-can-use-to-review-impaired-assets-and-impairment-amounts"></a>Can I generate reports that I can use to review impaired assets and impairment amounts?
Yes, you can generate the following reports that contain information about impaired assets and impairment accounting:

-   Fixed asset transactions report
-   Fixed asset impairment transactions report
-   Review fixed assets for impairment report



