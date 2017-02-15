---
title: Fixed asset depreciation for Japan FAQ | Microsoft Docs
description: This article answers some frequently asked questions about fixed asset depreciation for Japan.
author: ShylaThompson
manager: AnnBe
ms.date: 2015-10-19 23:02:51
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: ShylaThompson
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 10294
ms.assetid: 22fde28b-0bc9-4bd9-b008-d9ef7e1954f1
ms.region: Japan
ms.author: leguo
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: 437ff014f6d9d5271d879f877de3e6c2272227a0


---

# <a name="fixed-asset-depreciation-for-japan-faq"></a>Fixed asset depreciation for Japan FAQ

This article answers some frequently asked questions about fixed asset depreciation for Japan.

A fixed asset depreciates over the course of its useful life. Therefore, the acquisition value of the asset decreases. To regulate the depreciation of a fixed asset, you must assign one of the following depreciation methods to the asset, based on the date when the asset was put into service:

-   **Old straight line** – Depreciate assets that were put into service before April 1, 2007.
-   **New straight line** – Depreciate assets that were put into service on or after April 1, 2007.
-   **Old declining balance** – Depreciate assets that were put into service before April 1, 2007.
-   **250% new declining balance** – Depreciate assets that were put into service before April 1, 2012.
-   **200% new declining balance** – Depreciate assets that were put into service on or after to April 1, 2012.

## <a name="what-are-special-depreciation-and-additional-depreciation"></a>What are special depreciation and additional depreciation?
Special depreciation and additional depreciation are depreciation types that are applied to the following special types of fixed assets:

-   Fixed assets that are used in accordance with specific industrial policies that promote the supply and development of green energy or new energy, such as wave energy
-   Fixed assets that are purchased for the purpose of safety and sustainability
-   Fixed assets that are used to help an employee who has a disability
-   Fixed assets that are built to help people who are elderly or sick

When you use special depreciation, the extra depreciation amount is calculated by multiplying the acquisition cost and the special depreciation rate. When you use additional depreciation, the extra depreciation amount is calculated by multiplying the ordinary depreciation and the additional depreciation rate. **Note:** If a fixed asset is eligible for both special depreciation and additional depreciation, you can apply only one of them to the asset for a given depreciation period.

## <a name="what-is-the-allowable-limit-for-depreciation"></a>What is the allowable limit for depreciation?
The allowable limit for depreciation is the maximum amount of the total depreciation expense that is permitted as a deductible expense per tax book per depreciation period. The allowable limit for depreciation for a fixed asset corresponds to the depreciation types that are used to depreciate your company’s fixed assets.

| Depreciation type        | Allowable limit for depreciation             |
|--------------------------|----------------------------------------------|
| Ordinary depreciation    | Allowable limit for ordinary depreciation    |
| Accelerated depreciation | Allowable limit for accelerated depreciation |
| Special depreciation     | Allowable limit for special depreciation     |
| Additional depreciation  | Allowable limit for additional depreciation  |

The allowable limit for depreciation per period for your company’s fixed assets is calculated by using the following formula: Allowable limit for depreciation = Allowable limit for ordinary depreciation + Allowable limit for accelerated depreciation + Allowable limit for special depreciation or Allowable limit for additional depreciation

## <a name="what-is-the-allowable-limit-for-accumulated-depreciation"></a>What is the allowable limit for accumulated depreciation?
The allowable limit for accumulated depreciation is the maximum amount of accumulated depreciation that can be deducted from the acquisition value of a fixed asset for its useful life. You can choose the value of the allowable limit for accumulated depreciation. Your choice depends on the depreciation method that you apply to the fixed asset, and whether the fixed asset is tangible or intangible. There are two kinds of allowable limit for accumulated depreciation:

-   **95% allowable limit for accumulated depreciation** – This limit is applied only to tangible assets that are depreciated by using the old straight line method or the old declining balance method. This limit is restricted to 95 percent of the acquisition cost of the fixed asset.
-   **Maximum allowable limit for accumulated depreciation** – This limit is applied to both tangible assets and intangible assets that are depreciated by using a deprecation method other than the old straight line method or the old declining balance method. For a tangible asset, the maximum allowable limit for accumulated depreciation is the acquisition cost of the asset. The maximum allowable limit for accumulated depreciation of an intangible asset is the acquisition cost of the asset minus 1 Japanese yen (JPY).

## <a name="can-i-calculate-depreciation-for-a-fixed-asset-for-a-fiscal-year-that-has-fewer-than-12-months"></a>Can I calculate depreciation for a fixed asset for a fiscal year that has fewer than 12 months?
Yes. Microsoft Dynamics AX supports depreciation calculation if a fiscal year has fewer than 12 months. You can set up multiple depreciation calendars and change between them. If the current fiscal year has fewer than 12 months after you change depreciation calendars, Microsoft Dynamics AX proportionally adjusts the depreciation ratio, based on the number of months in the current fiscal year and a fiscal year that has 12 months. The following example shows how depreciation is calculated for a fiscal year that has fewer than 12 months. The original fiscal year is from April 1, 2010, to March 31, 2011, and the depreciation is calculated for the whole fiscal year. After you change the depreciation calendar, the fiscal year is from January 1, 2011, to December 31, 2011. In this scenario, the months of January, February, and March become part of the previous fiscal calendar, and the current fiscal year consists of only nine months. The depreciation for the remaining nine months (from April 1, 2011, to December 31, 2011) is calculated by using a prorated method that uses the depreciation rates from the previous fiscal year.

## <a name="what-is-the-catchup-rule-for-depreciation-and-how-does-it-work"></a>What is the catchup rule for depreciation and how does it work?
The catch-up rule for depreciation provides an effective way to allocate annual depreciation expenses to the depreciation expenses for each period. You can enable the catch-up rule in Microsoft Dynamics AX by selecting the **Allow catch-up rule for depreciation** check box on the **Fixed assets parameters** page. You can also specify whether the catch-up is applied at the end of a fiscal period or at the end of a fiscal year.

## <a name="how-do-i-calculate-a-depreciation-expense-by-using-the-catchup-rule"></a>How do I calculate a depreciation expense by using the catchup rule?
The depreciation expense for each month is calculated and posted in the next month. The following factors are used to calculate the monthly depreciation expense:

-   The total depreciation expense that has been incurred since the beginning of the year: Annual depreciation expense × (Position of the current month in the fiscal year ÷ 12) = 100,000 JPY
-   Total depreciation expense that has been posted from January through the current month
-   Depreciation expense that is posted for the current month: Total depreciation expense that has been incurred since the beginning of the year – Total depreciation expense that has been posted from January through the current month = 100,000 JPY

The following formula is used to calculate the monthly depreciation: Annual depreciation expense × (Position of the current month in the fiscal year ÷ Total number of months in the calendar year) – Total depreciation expense that has been posted from January through the current month This calculation method helps guarantee that the total monthly depreciation expense equals the annual depreciation expense of the asset.

## <a name="can-i-change-the-depreciation-profile-of-a-fixed-asset-after-the-depreciation-for-the-asset-has-been-posted"></a>Can I change the depreciation profile of a fixed asset after the depreciation for the asset has been posted?
Yes. You can change the depreciation profile of a fixed asset even after you've posted the depreciation for the asset. The following table shows the depreciation method changes that are allowed.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Starting depreciation method</th>
<th>Allowed depreciation method change</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Old straight line</td>
<td>Old declining balance</td>
</tr>
<tr class="even">
<td>Old declining balance</td>
<td>Old straight line</td>
</tr>
<tr class="odd">
<td>New straight line</td>
<td><ul>
<li>250% declining balance</li>
<li>200% declining balance</li>
</ul></td>
</tr>
<tr class="even">
<td>250% declining balance</td>
<td><ul>
<li>200% declining balance</li>
<li>New straight line</li>
</ul></td>
</tr>
<tr class="odd">
<td>200% declining balance</td>
<td><ul>
<li>250% declining balance</li>
<li>New straight line</li>
</ul></td>
</tr>
</tbody>
</table>

You can use Microsoft Dynamics AX to track the history of the change. Microsoft Dynamics AX can also automatically calculate the new useful life of the asset, based on undepreciated balance schedules and years passed schedules.

## <a name="what-types-of-schedules-can-i-import-for-depreciation-purposes"></a>What types of schedules can I import for depreciation purposes?
You can import the following schedules to recalculate the depreciation and service life of a fixed asset:

-   Undepreciated balance schedule
-   Years passed schedule

The depreciation rate schedule that you import depends on the type of depreciation method that you use for a fixed asset.




<!--HONumber=Feb17_HO3-->


