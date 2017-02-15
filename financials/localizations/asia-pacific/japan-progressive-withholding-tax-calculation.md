---
title: Progressive withholding tax | Microsoft Docs
description: This topic provides information about progressive withholding tax in Japan. Per the legal requirement in Japan, the tax percentage changes, depending on the interval in proportion to the invoice amount. The tax ratio also changes, based on the payment amount.
author: ShylaThompson
manager: AnnBe
ms.date: 2016-12-22 15:29:17
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: 81
ms.suite: Released- Dynamics 365 for Operations version 1611
ms.custom: 265164
ms.assetid: 120c149a-9968-4ab7-8cab-eddaa0964554
ms.region: Japan
ms.author: leguo
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: 1f8afa25327a0b35dcd8cb0d4a312d32f5036d09


---

# <a name="progressive-withholding-tax"></a>Progressive withholding tax

This topic provides information about progressive withholding tax in Japan. Per the legal requirement in Japan, the tax percentage changes, depending on the interval in proportion to the invoice amount. The tax ratio also changes, based on the payment amount.

<a name="tax-calculation"></a>Tax calculation
---------------

-   **Percentage of net amount** – The **Percentage of net amount** method is the default value in the **Origin** field. The withholding tax is calculated as a percentage of the purchase amount, excluding any other sales taxes.
-   **Percentage of gross amount** – The withholding tax is calculated as a percentage of the gross purchase amount, including any other sales taxes.

You can set up a withholding tax code so that it's calculated based on a whole amount or an interval amount. Use the **Calculation method** field on the **Calculation** FastTab of the **Withholding tax codes** page to select how a withholding tax code is calculated.

-   **Whole amount** – The tax rate is applied to the whole taxable amount.
-   **Interval** – The taxable amount is divided into parts, each of which falls in a range that has a specific withholding tax rate. The part of the amount that falls in a given interval is taxed according to the tax rate for that interval. The withholding tax is the sum of the tax amounts that are calculated for each amount interval.

**Note:** Withholding tax codes of different calculation methods can't be attached in a single withholding tax group.

## <a name="configuration-to-use-this-feature"></a>Configuration to use this feature
| Task                                                                                  | Considerations | More information                                                                      |
|---------------------------------------------------------------------------------------|----------------|---------------------------------------------------------------------------------------|
| Set up withholding tax codes and withholding tax groups.                              |                | [Set up withholding tax](http://ax.help.dynamics.com/en/wiki/set-up-withholding-tax/) |
| Create a new payment journal, settle open transactions, and post the payment journal. |                |                                                                                       |

1.  On the **Withholding tax codes** page, create withholding tax codes that have the following information:
    -   Origin and calculation method on the **Calculation** FastTab
    -   Limits (taxable amount interval) and values on the **Values** page

2.  On the **Withholding tax groups** page, create withholding tax groups, and add the relevant withholding tax codes on the **Setup** FastTab. You can calculate and post withholding tax on either the **Payment journal** page in Accounts payable or the **General journal** page in General ledger. The default withholding tax group for the vendor is shown in the **Withholding tax group** field.
3.  On the **Payment journal** page, select a journal or click **New** to create a journal, and then click **Lines**.
4.  Enter a payment date, and select the vendor account that is set up to calculate withholding tax. By default, the **Withholding tax group** field shows the withholding tax group for the vendor. You can select a different group. If no withholding tax should be calculated for the line, you can delete the field value.
5.  Click **Functions**, and then click **Settlement**. Select the **Mark** option for the open invoices to pay.
6.  Verify the Infolog information about the calculated withholding tax, and then close the Infolog.
7.  Optional: Click the **Withholding tax** tab for each selected line to change or delete the calculated withholding tax. You can also create lines and enter the information.
8.  Close the **Settle open transactions** page. The payment amount on the journal line is reduced by the withholding tax amount.
9.  Validate and post the payment journal.

## <a name="example-of-gross-amount"></a>Example of Gross amount
In this example, withholding tax is calculated by using an **Origin of percentage** value of **Gross amount** and a **Calculation method** value of **Interval**. Tax rates are set up as follows.

| Minimum and maximum limit (Taxable amount interval) | Value (Tax rate) |
|-----------------------------------------------------|------------------|
| 0.00 to 1,000.00                                    | 10 percent       |
| 1,001.00 to 2,000.00                                | 15 percent       |
| 2,001.00 to 0.00                                    | 20 percent       |

Payment amount: 11,000.00, which includes 10-percent sales tax (that is, 1,000) **Full payment – 11,000.00** Calculation:

| Taxable amount interval | Tax rate   | Payment amount split, based on the tax interval | Withholding tax |
|-------------------------|------------|-------------------------------------------------|-----------------|
| 0–1,000                 | 10 percent | 1,000.00                                        | 100.00          |
| 1,001–2,000             | 15 percent | 1,000.00                                        | 150.00          |
| 2,001–0                 | 20 percent | 9,000.00                                        | 1,800.00        |
|                         |            | **Total WHT amount**                            | **2,050.00**    |

**Partial payment – 6,000.00** Calculation:

| Taxable amount interval | Tax rate   | Payment amount split, based on the tax interval | Withholding tax |
|-------------------------|------------|-------------------------------------------------|-----------------|
| 0–1,000                 | 10 percent | 1,000.00                                        | 100.00          |
| 1,001–2,000             | 15 percent | 1,000.00                                        | 150.00          |
| 2,001–0                 | 20 percent | 4,000.00                                        | 800.00          |
|                         |            | **Total WHT amount**                            | **1,050.00**    |

**Balance payment – 5,000.00** Calculation:

| Taxable amount interval | Tax rate   | Payment amount split, based on the tax interval | Withholding tax |
|-------------------------|------------|-------------------------------------------------|-----------------|
| 0–1,000                 | 10 percent | 1,000.00                                        | 100.00          |
| 1,001–2,000             | 15 percent | 1,000.00                                        | 150.00          |
| 2,001–0                 | 20 percent | 3,000.00                                        | 600.00          |
|                         |            | **Total WHT amount**                            | **850.00**      |

## <a name="example-of-net-amount"></a>Example of Net amount
In this example, withholding tax is calculated by using an **Origin of percentage** value of **Net amount** and a **Calculation method** value of **Interval**. Payment amount: 11,000.00, which includes 10-percent sales tax (that is, 1,000) **Full payment – 11,000.00** Base for withholding tax calculation, excluding tax = 10,000.00 Calculation:

| Taxable amount interval | Tax rate   | Payment amount split based on the tax interval | Withholding tax |
|-------------------------|------------|------------------------------------------------|-----------------|
| 0–1,000                 | 10 percent | 1,000.00                                       | 100.00          |
| 1,001–2,000             | 15 percent | 1,000.00                                       | 150.00          |
| 2,001–0                 | 20 percent | 8,000.00                                       | 1,600.00        |
|                         |            | **Total WHT amount**                           | **1,850.00**    |

**Partial payment – 6,000.00** Base for withholding tax calculation, excluding tax = 5,455.00 Calculation:

| Taxable amount interval | Tax rate   | Payment amount split, based on the tax interval | Withholding tax |
|-------------------------|------------|-------------------------------------------------|-----------------|
| 0–1,000                 | 10 percent | 1,000.00                                        | 100.00          |
| 1,001–2,000             | 15 percent | 1,000.00                                        | 150.00          |
| 2,001–0                 | 20 percent | 3,455.00                                        | 691.00          |
|                         |            | **Total WHT amount**                            | **941.00**      |

**Balance payment – 5,000.00** Base for withholding tax calculation excluding tax = 4,545.00 Calculation:

| Taxable amount interval | Tax rate   | Payment amount split, based on the tax interval | Withholding tax |
|-------------------------|------------|-------------------------------------------------|-----------------|
| 0–1,000                 | 10 percent | 1,000.00                                        | 100.00          |
| 1,001–2,000             | 15 percent | 1,000.00                                        | 150.00          |
| 2,001–0                 | 20 percent | 2,545.00                                        | 509.00          |
|                         |            | **Total WHT amount**                            | **759.00**      |






<!--HONumber=Feb17_HO3-->


