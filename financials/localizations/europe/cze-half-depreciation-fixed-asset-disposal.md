---
title: Half year depreciation on fixed asset disposal for the Czech Republic | Microsoft Docs
description: This topic explains how to set up half-yearly depreciation, so that you can apply half the yearly depreciation for fixed assets that are sold or otherwise disposed of.
author: ShylaThompson
manager: AnnBe
ms.date: 2016-12-19 16:25:43
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: 81
ms.suite: Released- Dynamics 365 for Operations version 1611
ms.custom: 264554
ms.assetid: e4cfa522-1ebb-4ac9-b8af-d05c92b47afb
ms.region: Czech Republic
ms.author: epopov
translationtype: Human Translation
ms.sourcegitcommit: d331960307ba214de4382feac7941aa5065c523d
ms.openlocfilehash: 37e54e252fb3de713d5cba20a5f6400414054e75


---

# <a name="half-year-depreciation-on-fixed-asset-disposal-for-the-czech-republic"></a>Half year depreciation on fixed asset disposal for the Czech Republic

This topic explains how to set up half-yearly depreciation, so that you can apply half the yearly depreciation for fixed assets that are sold or otherwise disposed of.

When a fixed asset is sold or otherwise disposed of, you can apply half the yearly depreciation for the asset, for tax purposes. This half-yearly depreciation can be applied regardless of the disposal date.

## <a name="set-up-depreciation-methods-for-the-depreciation-profile"></a>Set up depreciation methods for the depreciation profile
Use the Regular CZ and Accelerated CZ depreciation methods to apply half-yearly depreciation for a fixed asset.

1.  Click **Fixed assets** &gt; **Setup** &gt; **Depreciation** &gt; **Depreciation profiles**.
2.  Click **New** to create a depreciation profile.
3.  In the **Method** field, select **Regular CZ** or **Accelerated CZ**.
4.  In the **Depreciation year** field, select **Calendar** as the basis for the calculation of depreciation.
5.  In the **Period frequency** field, select **Yearly**.

## <a name="apply-the-halfyearly-depreciation-method"></a>Apply the halfyearly depreciation method
After you set up the depreciation methods, you can apply half the yearly depreciation for assets that were disposed of.

1.  Click **Fixed assets** &gt; **Journals** &gt; **Fixed assets**.
2.  On the **Overview** tab, click **New** to create a journal, and then enter the required details.
3.  Click **Lines** to open the **Journal voucher** page.
4.  Create a journal line for the fixed asset that was sold or otherwise disposed of.
5.  Click **Proposals** &gt; **Depreciation proposal** to open the **Depreciation proposal** page.
6.  In the **To date** field, enter the journal date.
7.  Select the **Calculate half-year depreciation amount** check box to calculate half-yearly depreciation. When this check box is selected, the yearly depreciation amount is divided by two and rounded according to the rounding setup for the depreciation book.
8.  Optional: Select the **Summarize depreciation** check box to summarize the calculated depreciation for each fixed asset or for each value model.
9.  Click **OK** to close the **Depreciation proposal** page.
10. Post the journal.





<!--HONumber=Feb17_HO3-->


