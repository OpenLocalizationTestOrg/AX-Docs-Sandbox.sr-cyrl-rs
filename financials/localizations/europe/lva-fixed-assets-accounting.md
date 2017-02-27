---
title: Fixed assets accounting for tax purposes
description: This topic provides information about the tax Depreciation functionality for Latvia.
author: ShylaThompson
manager: AnnBe
ms.date: 2016-12-16 21 - 35 - 17
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetBookTable, AssetDepreciationProfile, AssetTable, AssetTaxDepreciation
audience: Application User
ms.search.scope: Operations
ms.custom: 264374
ms.assetid: cbf94106-2c1b-45dd-8734-18a2a56a4682
ms.search.region: Latvia
ms.author: v-elgolu
ms.dyn365.ops.intro: 01-11-2016
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: b97d17ceabfd25c52c5f0c1e96a123bae6941c5a
ms.openlocfilehash: de6f54c668b0bb23b59ea0035fd916ed753071bf
ms.lasthandoff: 02/22/2017


---

# <a name="fixed-assets-accounting-for-tax-purposes"></a>Fixed assets accounting for tax purposes

This topic provides information about the tax Depreciation functionality for Latvia. 

This topic discusses tax depreciation setup and calculation as well as printing the tax depreciation report. **Note:** Tax depreciation works with the value models. The value model and depreciation book have been merged into a single concept that is called a *book.* For more information, see [Fixed asset value model and depreciation book merge](fixed-asset-value-model-depreciation-book-merge.md).

## <a name="set-up-a-depreciation-profile"></a>Set up a depreciation profile
When you set up a depreciation profile, consider the following.

|                       |                                                                                                                                                                                                                                                                                                                    |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Depreciation year** | Select the type of year that you use to calculate the depreciation. The depreciation year and the period frequency are related. Therefore, the options **Period frequency** field depend on the **Depreciation year** field value.                                                                                 |
| **Period frequency**  | Select the frequency of ledger accruals during the calendar year or fiscal year. The options that appear in this field vary, depending on the depreciation year that you selected. If you selected **Calendar** as the depreciation year, the options are **Yearly**, **Monthly**, **Quarterly**, **Half-yearly**. |
| **Full depreciation** | Select this option to fully depreciate the fixed asset when the service life that remains is 0 (zero).                                                                                                                                                                                                             |

To set up a depreciation profile, complete the following procedure, [Set up and create depreciation profiles](http://ax.help.dynamics.com/en/wiki/set-up-and-create-depreciation-profiles/).

## <a name="set-up-books"></a>Set up books
Use the **Books** page to define a tax category. Books are also referred to as tax categories. To create a book, select the depreciation profile that has **Reducing balance** selected in the **Method** field in the **Depreciation profiles** page. The **Books** page for legal entities in Latvia contain the following fields:

-   **Posting layer** - Select **Tax** in this field.
-   **Summarize for category** - Select this option if tax depreciation should be summarized and calculated for all fixed assets that have the same book selected in the **Category** field.
-   **Tax coefficients** -** **You can set up tax coefficients for each coefficient to adjust the acquisition price for the fiscal year.

For more information about setting up books, see [Set up depreciation books](http://ax.help.dynamics.com/en/wiki/set-up-depreciation-books/).

### <a name="set-up-tax-depreciation-calculation"></a>Set up tax depreciation calculation

To set up tax depreciation calculation, on the **Fixed assets** page, select a fixed asset. Then, on the **General** FastTab, select a **Book** in the **Category** field. A fixed asset should only have one book associated in the current posting layer. **Note:** This field displays the books record with a posting layer value equal to Tax only.

## <a name="calculate-tax-depreciation"></a>Calculate tax depreciation
To calculate fixed asset tax depreciation, on the **Tax depreciation** page, create a New tax period to use for reporting.

|                   |                                                                                                                                                                |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Field name**    | **Description**                                                                                                                                                |
| **Start date**    | Select the date from which the period is valid.                                                                                                                |
| **End date**      | Select the date up to which the period is valid.                                                                                                               |
| **Period status** | Select the period status (**Open** or **Closed**). If the status is **Closed**, **Categories** on the **Category details** FastTab cannot be added or deleted. |

On the **Category details** FastTab, select the book in the **Category** field that you want to calculate tax depreciation for. Click **Calculate** to calculate tax depreciation. Tax depreciation calculates for either individual fixed assets or is based on summary information from all fixed assets that are assigned to the same fixed asset tax category. The calculation is based on the tax coefficient from the selected book, and accounting data on the books of fixed assets associated with the book selected in the **Category** field.

|                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------|
| **Calculation formulas**                                                                                         |
| Adjusted Value  = Starting Balance + Value adjustments - Disposal + Acquisition price \* Acquisition Coefficient |
| Tax Depreciation amount = Adjusted Value \* Base Depreciation \*2 /100 \* number of months in period / 12        |
| End Balance = Adjusted Value – Tax Depreciation amount                                                           |
| Starting Balance (current depreciation period) = End Balance (previous depreciation calculation period)          |

To view the tax depreciation details, click **Tax depreciation details** to open the **Tax depreciation details** page.

## <a name="print-the-tax-depreciation-report"></a>Print the Tax depreciation report
The **Tax depreciation** report provides Latvian users with tax reporting that is relevant to fixed assets in a company. To print the report, go to the **Tax depreciation calculation** page, select a specific record to summarize at the **Category** level. Click **Tax depreciation report** for categories that are not summarized using the **Tax depreciation** report.


