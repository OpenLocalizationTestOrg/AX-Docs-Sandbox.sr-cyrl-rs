---
title: Equally divided depreciation method | Microsoft Docs
description: In Japan, lump-sum assets, low-value assets, and deferred assets are depreciated in equal amounts in each year of the service life. This article answers some frequently asked questions about equally divided depreciation.
author: ShylaThompson
manager: AnnBe
ms.date: 2015-10-19 22:58:04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
keywords: AssetDepreciationProfile
audience: Application User
ms.reviewer: ShylaThompson
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 10154
ms.assetid: 1f9b0cf6-f1c3-4c64-9d43-9a34f805f651
ms.region: Japan
ms.author: leguo
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: e0c2cb95b3a28cfa77f0c5f74d160052dc1f1a4d


---

# <a name="equally-divided-depreciation-method"></a>Equally divided depreciation method

In Japan, lump-sum assets, low-value assets, and deferred assets are depreciated in equal amounts in each year of the service life. This article answers some frequently asked questions about equally divided depreciation.

Equally divided depreciation lets you depreciate a deferred, low-value, or lump-sum fixed asset equally over one or more fiscal periods within the useful life of the fixed asset. You can set up the equally divided depreciation method on the **Depreciation profiles** page.

## <a name="what-types-of-fixed-assets-can-i-depreciate-by-using-the-equally-divided-depreciation-method"></a>What types of fixed assets can I depreciate by using the equally divided depreciation method?
You can use the equally divided depreciation method to depreciate deferred, low-value, and lump-sum fixed assets. You can then generate reports to view the depreciation expenses for the assets over one or more fiscal periods.

## <a name="how-does-microsoft-dynamics-ax-calculate-depreciation-by-using-the-equally-divided-depreciation-method"></a>How does Microsoft Dynamics AX calculate depreciation by using the equally divided depreciation method?
You can set up a depreciation profile by selecting **Equally divided** as the depreciation method in the **Method** field on the **Depreciation profiles** page. When you use the equally divided depreciation profile to depreciate a fixed asset, Microsoft Dynamics AX calculates the depreciation amounts by using the following formula: Depreciation = Remaining amount × rounding (1 ÷ Number of remaining years) × rounding (1 ÷ Number of periods in the current year) The following formula is used to calculate the remaining amount: Remaining amount = Acquisition cost – Accumulated depreciation When you use the equally divided depreciation method to calculate the depreciation amount, the value in the **Number of years to equally divide depreciation amounts** field on the **Depreciation profiles** page indicates the useful life of the fixed asset instead of the service life and the depreciation period that you specified on the **Books** page.

## <a name="does-the-depreciation-amount-that-is-calculated-by-using-the-equally-divided-depreciation-method-change-if-its-calculated-at-the-beginning-of-the-month-instead-of-in-the-middle-of-the-month"></a>Does the depreciation amount that is calculated by using the equally divided depreciation method change if it's calculated at the beginning of the month instead of in the middle of the month?
No. The depreciation amount does not change, depending upon when it's calculated during the month. For example, you acquire a lump-sum fixed asset:

-   Acquisition value of the lump-sum fixed asset = 150,000 Japanese yen (JPY)
-   Acquisition date = April 1, 2013
-   Number of years to equally divide the depreciation amount = 3 years

When the equally divided depreciation method is used, the depreciation amount for this fixed asset is JPY 4,166.67 for each month, regardless of whether you calculate it at the beginning of the month or in the middle of the month.

## <a name="how-does-microsoft-dynamics-ax-calculate-equally-divided-depreciation-for-a-lowvalue-asset-that-is-acquired-midyear"></a>How does Microsoft Dynamics AX calculate equally divided depreciation for a lowvalue asset that is acquired midyear?
If you purchase a low-value fixed asset in the middle of a fiscal year, Microsoft Dynamics AX considers the current fiscal year to be the first fiscal year for the depreciation calculation. For example, you acquire a low-value fixed asset in the middle of a fiscal year:

-   Fiscal year = April 1 to March 31
-   Acquisition value of the low-value fixed asset = JPY 100,000
-   Acquisition date = December 1, 2012
-   Number of years to equally divide the depreciation amount = 1 year

Microsoft Dynamics AX calculates the depreciation for the fiscal year from April 1, 2012, to March 31, 2013, as shown in the following table.

| Start date    | End date       | Depreciation amount for the fiscal period | Accumulated depreciation | Remaining depreciation amount | Depreciation amount for the month |
|---------------|----------------|-------------------------------------------|--------------------------|-------------------------------|-----------------------------------|
| April 1, 2012 | March 31, 2013 | JPY 100,000                               | JPY 100,000              | 0                             | JPY 100, 000                      |

## <a name="how-does-microsoft-dynamics-ax-calculate-equally-divided-depreciation-for-a-lumpsum-asset-that-is-acquired-midyear"></a>How does Microsoft Dynamics AX calculate equally divided depreciation for a lumpsum asset that is acquired midyear?
If you purchase a lump-sum fixed asset in the middle of a fiscal year, Microsoft Dynamics AX calculates the current fiscal year from the purchase date of the fixed asset. For example, you acquire a lump-sum fixed asset in the middle of a fiscal year:

-   Fiscal year = April 1 to March 31
-   Acquisition value of the lump-sum fixed asset = JPY 150,000
-   Acquisition date = December 1, 2012
-   Number of years to equally divide the depreciation amount = 3 years

Microsoft Dynamics AX calculates the depreciation for the first year from December 1, 2012, to March 31, 2013, as shown in the following table.

| Start date       | End date       | Depreciation amount for a fiscal period | Accumulated depreciation | Remaining depreciation amount | Depreciation amount for a month |
|------------------|----------------|-----------------------------------------|--------------------------|-------------------------------|---------------------------------|
| December 1, 2012 | March 31, 2013 | JPY 50,000                              | JPY 50,000               | JPY 100,000                   | JPY 12,500                      |
| April 1, 2013    | March 31, 2014 | JPY 50,000                              | JPY 100,000              | JPY 50,000                    | JPY 4,167                       |
| April 1, 2014    | March 31, 2015 | JPY 50,000                              | JPY 150,000              | 0                             | JPY 4,167                       |

## <a name="how-does-microsoft-dynamics-ax-calculate-depreciation-by-using-the-equally-divided-depreciation-method-if-the-asset-calendar-is-changed-during-the-asset-life-cycle"></a>How does Microsoft Dynamics AX calculate depreciation by using the equally divided depreciation method if the asset calendar is changed during the asset life cycle?
When Microsoft Dynamics AX calculates depreciation by using the equally divided depreciation method, the calculation is based on the fiscal calendar that is selected in the **Calendar** field on the **Books** page. If an asset calendar is changed during the asset life cycle, the number of fiscal periods, such as months or quarters, in a fiscal year is calculated based on the current calendar. For example, you acquire a lump-sum fixed asset:

-   Fiscal calendar = April 1 to March 31
-   Acquisition date of the lump-sum fixed asset = April 1, 2012
-   Number of years to equally divide the depreciation amount = 3 years

In April 2013, during the second fiscal year, if you change the fiscal calendar from April 1 through March 31 to January 1 through December 31, Microsoft Dynamics AX calculates the number of depreciation periods for the fiscal years as shown in the following table.

| Fiscal year                                | Number of depreciation periods |
|--------------------------------------------|--------------------------------|
| April 1, 2012, through March 31, 2013      | 12 periods                     |
| April 1, 2013, through December 31, 2013   | 9 periods                      |
| January 1, 2014, through December 31, 2014 | 12 periods                     |
| January 1, 2015, through March 31, 2015    | 3 periods                      |

## <a name="can-i-modify-the-equally-divided-depreciation-method-during-the-life-cycle-of-a-fixed-asset"></a>Can I modify the equally divided depreciation method during the life cycle of a fixed asset?
No. When you depreciate a fixed asset by using the equally divided depreciation method, the depreciation amount is equally divided among the fiscal periods within the useful life of the fixed asset. Therefore, you can't change the depreciation method during the life cycle of the fixed asset.

## <a name="can-i-change-the-depreciation-period-for-an-equally-divided-depreciation-profile"></a>Can I change the depreciation period for an equally divided depreciation profile?
No. If you selected an equally divided depreciation profile on the **Books** page, you can't change the value in the **Number of years to equally divide depreciation amounts** field on the **Depreciation profiles** page for the depreciation profile.

<a name="see-also"></a>See also
--------

[(JPN) Fixed asset depreciation](https://docs.microsoft.com/en-us/dynamics365/operations/financials/localizations/asia-pacific/jpn-fixed-asset-depreciation)




<!--HONumber=Feb17_HO3-->


