---
title: Additional acquisition depreciation
description: This article explains how depreciation is calculated for additional acquisitions in Germany and provides an example. Acquisition adjustments for fixed assets must always be calculated as if the adjustments were made on the first day of the business year.
author: ShylaThompson
manager: AnnBe
ms.date: 2015-11-16 21 - 15 - 37
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations
ms.custom: 12791
ms.assetid: b8e17c7a-917c-4016-87a5-27c34ccde941
ms.search.region: Germany
ms.author: mrolecki
ms.dyn365.ops.intro: 01-02-2016
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b97d17ceabfd25c52c5f0c1e96a123bae6941c5a
ms.openlocfilehash: 7af91c12f03ec5a96e1e2880888eaf24c296bb8f
ms.lasthandoff: 02/22/2017


---

# <a name="additional-acquisition-depreciation"></a>Additional acquisition depreciation

This article explains how depreciation is calculated for additional acquisitions in Germany and provides an example. Acquisition adjustments for fixed assets must always be calculated as if the adjustments were made on the first day of the business year.

Acquisition adjustments for fixed assets must be calculated as if the adjustments were made on the first day of the business year, regardless of when the adjustment transactions were actually created. The following formula is used to calculate the base amount of the fixed asset for depreciation: Net book value of the fixed asset on the last day of the previous business year + All acquisition adjustments for the fixed asset in the current year.

## <a name="example"></a>Example
In 2015, your organization acquired a fixed asset for 60,000. Your organization uses the straight-line life remaining depreciation method over five years. In 2015, when you process the depreciation proposal each month, 1,000 is calculated as the monthly depreciation amount (60,000 ÷ \[5 × 12\]). In March 2016, you post an additional acquisition for the fixed asset. The amount of the additional acquisition is 12,000. You must treat the additional acquisition as if it was posted on January 1, 2016. Therefore, here is how the monthly depreciation of 12,000 must be calculated for the remaining four years: 12,000 ÷ (4 × 12) = 250 The actual depreciation of the additional acquisition can start only in the month when the additional acquisition occurred (March). Therefore, the depreciation amounts for January and February must be added to the depreciation amount for March. The following table shows the monthly depreciation amounts for both the original acquisition and the acquisition adjustment for the first five months of the year.

| Month         | Monthly depreciation amount for the original 60,000 acquisition | Monthly depreciation amount for the 12,000 acquisition adjustment | Total depreciation amount |
|---------------|-----------------------------------------------------------------|-------------------------------------------------------------------|---------------------------|
| January 2016  | 1,000                                                           | 0                                                                 | 1,000                     |
| February 2016 | 1,000                                                           | 0                                                                 | 1,000                     |
| March 2016    | 1,000                                                           | 250 for January, 250 for February, and 250 for March              | 1,750                     |
| April 2016    | 1,000                                                           | 250                                                               | 1,250                     |
| May 2016      | 1,000                                                           | 250                                                               | 1,250                     |




