---
title: Depreciation rounding
description: This topic explains how you can round fixed asset depreciation amounts up or down to the nearest whole number.
author: ShylaThompson
manager: AnnBe
ms.date: 2016-12-22 15 - 29 - 35
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations
ms.custom: 265204
ms.assetid: 3e535ac3-f5de-47cc-ba7b-40c9857a9460
ms.search.region: Czech Republic
ms.author: epopov
ms.dyn365.ops.intro: 01-11-2016
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: b97d17ceabfd25c52c5f0c1e96a123bae6941c5a
ms.openlocfilehash: 95a7fca3618846e2924a0fdb6cce7ac52e4d1d08
ms.lasthandoff: 02/22/2017


---

# <a name="depreciation-rounding"></a>Depreciation rounding

This topic explains how you can round fixed asset depreciation amounts up or down to the nearest whole number. 

Depreciation amounts are rounded up or down, based on the value that is entered in the **Round off depreciation** field and the rounding method that is specified in the **Rounding method** field on the **Depreciation books** page. For a depreciation amount (x) that has a **Round off depreciation** value (y), the depreciation amount (z) is calculated as x ÷ y. The rounded-up or rounded-down depreciation amount is calculated as z × y. For example, for the depreciation amount CZK 1,111.11 and a **Round off depreciation** value of **1**, the depreciation amount is calculated as CZK 1,111.11 ÷ 1, or CZK 1,111.11. The rounded-up depreciation amount is calculated as CZK 1,112 × 1, or CZK 1,112. The rounded-down depreciation amount is calculated as CZK 1,111 × 1, or CZK 1,111. The following table shows rounded-up and rounded-down depreciation amounts for various depreciation amounts and **Round off depreciation** values.
Depreciation amount (x) Round off depreciation (y) Depreciation amount (z = x ÷ y) Rounding method Normal Downward Rounding-up CZK 1,111.11 1 CZK 1,111.11 ÷ 1 = CZK 1,111.11 CZK 1,111.1 CZK 1,111.11 is rounded up to CZK 1,112. Final depreciation amount: CZK 1,112 × 1 = CZK 1,112 CZK 1,111.11 is rounded down to CZK 1,111. Final depreciation amount: CZK 1,111 × 1 = CZK 1,111 CZK 1,234.5 10 CZK 1,234.5 ÷ 10 = CZK 123.45 CZK 1,235 CZK 123.45 is rounded up to CZK 124. Final depreciation amount: CZK 124 × 10 = CZK 1,240 CZK 123.45 is rounded down to CZK 123. Final depreciation amount: CZK 123 × 10 = CZK 1,230


