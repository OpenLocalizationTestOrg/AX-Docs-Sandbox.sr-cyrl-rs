---
title: Allocation rules for fixed assets
description: In Japan, a fixed asset is registered under an administrative department, and the depreciation amount must be allocated among the usage departments. You can set up an allocation rule to allocate depreciation amounts to multiple financial dimensions by percentage. This article answers some frequently asked questions about the allocation rules for fixed assets.
author: ShylaThompson
manager: AnnBe
ms.date: 2015-10-19 23 - 00 - 03
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetAllocationRuleSetup_CN
audience: Application User
ms.reviewer: ShylaThompson
ms.search.scope: AX 7.0.0, Operations
ms.custom: 10194
ms.assetid: ba1302f1-5b7d-44c4-af00-ec629f388e19
ms.search.region: Japan
ms.author: leguo
ms.dyn365.ops.intro: 01-02-2016
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b97d17ceabfd25c52c5f0c1e96a123bae6941c5a
ms.openlocfilehash: 778414417ae2912d6881fa2d22f47109eabd2630
ms.lasthandoff: 02/22/2017


---

# <a name="allocation-rules-for-fixed-assets"></a>Allocation rules for fixed assets

In Japan, a fixed asset is registered under an administrative department, and the depreciation amount must be allocated among the usage departments. You can set up an allocation rule to allocate depreciation amounts to multiple financial dimensions by percentage. This article answers some frequently asked questions about the allocation rules for fixed assets.

You can set up an allocation rule to allocate depreciation costs for a fixed asset to a dimension of your legal entity. Fixed assets can be put into service for multiple dimensions, such as departments or cost centers. When you depreciate a fixed asset, the depreciation cost is posted to an offset account. By setting up an allocation rule, you can share the depreciation cost of the fixed asset between multiple dimensions of your legal entity.

## <a name="when-depreciation-costs-are-allocated-can-the-dimensions-that-are-based-on-the-allocation-rule-of-the-fixed-asset-model-override-the-default-dimensions-in-the-journal-header"></a>When depreciation costs are allocated, can the dimensions that are based on the allocation rule of the fixed asset model override the default dimensions in the journal header?
Yes. The dimensions that you specify in the allocation rule override the default dimensions that are usually displayed in the journal header.

## <a name="what-happens-if-i-delete-a-dimension-that-is-part-of-an-allocation-rule"></a>What happens if I delete a dimension that is part of an allocation rule?
If you delete a financial dimension that is assigned to an allocation rule, you receive a message that states that the depreciation proposal can't be run. You must select another financial dimension for the allocation rule and run the depreciation proposal again.

## <a name="how-does-rounding-the-currency-up-or-down-affect-the-allocation-rule"></a>How does rounding the currency up or down affect the allocation rule?
After an allocation rule is applied to a fixed asset, the deprecation cost that is allocated to a legal entity dimension can be a whole amount or a fractional amount. If you've set up rounding rules for your currency, the resulting allocated depreciation costs can be more than or less than the depreciation cost, in accordance with the allocation rule. Here are some examples that show how currency rounding can affect the allocation rule.

### <a name="rounded-up-currency"></a>Rounded-up currency

For this example, the depreciation cost amount of a fixed asset is 170 currency units. You've set up an allocation rule to allocate 1 percent of the depreciation cost to each of the 100 dimensions of your legal entity. You've also set up a rounding rule that indicates that fractional currency units that are more than halfway between two whole currency units are rounded up to the nearest whole currency unit. Here is how the depreciation cost per dimension is calculated in this scenario:

-   Original depreciation cost per dimension = 1.70 currency units
-   Rounded-up depreciation cost per dimension = 2.00 currency units
-   Total rounded-up depreciation cost of the fixed asset = 2.00 × 100 = 200 currency units

### <a name="rounded-down-currency"></a>Rounded-down currency

For this example, the depreciation cost amount of a fixed asset is 120 currency units. You've set up an allocation rule to allocate 1 percent of the depreciation cost to each of the 100 dimensions of your legal entity. You've also set up a rounding rule that indicates that fractional currency units that are less than halfway between two whole currency units are rounded down to the nearest whole currency unit. Here is how the depreciation cost per dimension is calculated in this scenario:

-   Original depreciation cost per dimension = 1.20 currency units
-   Rounded-down depreciation cost per dimension = 1.00 currency units
-   Total rounded-down depreciation cost of the fixed asset = 1.00 × 100 = 100 currency units

If the total rounded-down depreciation cost that must be allocated across each dimension is less than the rounding amount, the allocation rule isn't applied to the depreciation. Instead, the depreciation amount is either posted to the main account or offset by using the posting profile rules that you set up on the **Fixed asset posting profiles** page. To avoid these and similar scenarios, you can manually adjust the rounding rule for fixed asset depreciation on the **Currencies** page.

<a name="see-also"></a>See also
--------

[(CHN, JPN) Create allocation rules and allocate depreciation costs](https://ax.help.dynamics.com/en/wiki/chn-jpn-create-allocation-rules-and-allocate-depreciation-costs/)

[About round-off depreciation](https://ax.help.dynamics.com/en/wiki/about-round-off-depreciation/)


