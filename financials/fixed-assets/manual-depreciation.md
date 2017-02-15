---
title: Manual depreciation | Microsoft Docs
description: This article gives an overview of the manual depreciation method.
author: twheeloc
manager: AnnBe
ms.date: 2015-12-02 22:55:46
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
keywords: AssetDepreciationProfile
audience: Application User
ms.reviewer: 101
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 13811
ms.assetid: 272b63c5-be73-4e0a-9a12-21b13c2b2d8c
ms.region: Global
ms.author: saraschi
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: 13961df12a4fd0be5dacd9e398ac0908651c08b4


---

# <a name="manual-depreciation"></a>Manual depreciation

This article gives an overview of the manual depreciation method.

When you set up a fixed asset depreciation profile and select **Manual** in the **Method** field on the **Depreciation profiles** page, the depreciation of fixed assets that are assigned to the depreciation profile is determined by the percentage that you enter for each interval in the calendar year. The intervals that you set up percentages for are posted according to the value that you select in the **Period frequency** field on the **General** FastTab of the **Depreciation profiles** page. Here are the values that you can select:

-   Yearly
-   Monthly
-   Quarterly
-   Half-Yearly
-   Daily

After you select the period frequency, click **Manual schedules**, and set up percentages for each posting interval. Together, the manual schedules and the posting intervals define the depreciation amount, as shown in the examples later in this article. Manual depreciation is always calculated as a percentage of the acquisition price. For manual depreciation, the percentages that you enter in the intervals of the depreciation don't have to add up to 100 percent. Manual depreciation is a flexible depreciation method that is often used to define an extraordinary depreciation profile on the **Books** page, such as a non-periodic depreciation for special purposes (for example, tax).

## <a name="examples"></a>Examples
Acquisition price: 11,000.00 Expected scrap value: 1,000.00 The following table shows the intervals and percentages that you set up on the **Fixed asset depreciation profile schedules** page.

| Interval number | Percentage |
|-----------------|------------|
| 1               | 10.00      |
| 2               | 50.00      |
| 3               | 8.00       |

The following table shows how the depreciation for each interval is calculated.

|  Interval number | Calculation of the yearly depreciation amount | Net book value at the end of the interval |
|------------------|-----------------------------------------------|-------------------------------------------|
| 1                | (11,000 – 1,000) × 10% = 1,000                | 10,000 (11,000 – 1,000)                   |
| 2                | (11,000 – 1,000) × 50% = 5,000                | 5,000 (10,000 – 5,000)                    |
| 3                | (11,000 – 1,000) × 8% = 800                   | 4,200 (5,000 – 800)                       |

If you select **Monthly** in the **Period frequency** field, you set up 12 manual schedule intervals. The following table shows the depreciation amounts for the first two intervals.

| Interval | Depreciation amount            |
|----------|--------------------------------|
| January  | (11,000 – 1,000) × 10% = 1,000 |
| February | (11,000 – 1,000) × 50% = 5,000 |

If you select **Half-Yearly** in the ****Period frequency** field**, you set up two manual schedule intervals. The following table shows the depreciation amounts for those two intervals.

| Interval    | Depreciation amount            |
|-------------|--------------------------------|
| June 30     | (11,000 – 1,000) × 10% = 1,000 |
| December 31 | (11,000 – 1,000) × 50% = 5,000 |

The total of percentages for all intervals doesn't have to be 100. However, you receive a message if the value in the **Cumulative percentage** field on the **Fixed asset depreciation profile schedules** page isn't **100**.




<!--HONumber=Feb17_HO3-->

