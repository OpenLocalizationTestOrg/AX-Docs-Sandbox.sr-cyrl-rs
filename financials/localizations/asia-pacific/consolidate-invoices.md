---
title: Consolidated invoices for Japan
description: In Japan, invoices are consolidated each month for payment. This article provides information about consolidated invoices, and explains how the invoice amount and due date are calculated.
author: ShylaThompson
manager: AnnBe
ms.date: 2015-10-19 23 - 03 - 02
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustConsInvoice_JP, VendConsInvoice_JP
audience: Application User
ms.reviewer: ShylaThompson
ms.search.scope: AX 7.0.0, Operations
ms.custom: 10314
ms.assetid: bd7255d9-0b0e-4372-8563-eaa559adbf24
ms.search.region: Japan
ms.author: leguo
ms.dyn365.ops.intro: 01-02-2016
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b97d17ceabfd25c52c5f0c1e96a123bae6941c5a
ms.openlocfilehash: 218b29dfdde4e5a118aca44a024a1d1c7e2a16c5
ms.lasthandoff: 02/22/2017


---

# <a name="consolidated-invoices-for-japan"></a>Consolidated invoices for Japan

In Japan, invoices are consolidated each month for payment. This article provides information about consolidated invoices, and explains how the invoice amount and due date are calculated.

You can consolidate several vendor invoices, purchase orders, purchase returns, and purchase journals into a consolidated vendor invoice for payment. You don't have to issue payments for the separate vendor transactions. You can also consolidate customer invoices, sales orders, sales returns, and sales journals into a customer consolidated invoice that you can send to the customer.

You can create two or more consolidated invoices on the same day for a customer or a vendor. After you create a consolidated invoice for a customer or a vendor, you can pay the vendor or receive payment from the customer, and settle the consolidated invoice for the amount of the payment.

The following calculations are performed for a consolidated invoice:

-   Invoice amount
-   Due date

## <a name="calculating-the-invoice-amount-for-a-consolidated-invoice"></a>Calculating the invoice amount for a consolidated invoice
After you create and confirm a consolidated invoice on the **Consolidated invoice** page, the following amounts are calculated:

-   **Previous invoice amount** – The total invoice amount for the previous consolidation period.
-   **Previously paid amount** – The total amount that was paid for the previous consolidation period.
-   **Adjustment amount** – The adjustment amount for the previous consolidation period. The adjustment amount includes cash discounts and bank charges.
-   **Outstanding amount** – The total outstanding amount for the current consolidation period. The outstanding amount is calculated by using the following formula: Previous invoice amount – Paid amount – Adjustment amount
-   **Invoice amount during consolidation period** – The total invoice amount for the current consolidated invoice. This amount includes the sales tax.
-   **Total invoice amount** – The new total invoice amount for the current invoice. This amount is calculated by using the following formula: Outstanding amount + Invoice amount during consolidation period

## <a name="calculating-the-due-date-for-a-consolidated-invoice"></a>Calculating the due date for a consolidated invoice
Invoices are consolidated each month, based on the consolidation day that you specify for each vendor or customer. The consolidation day determines the day and period that invoices are consolidated for, and the date that payment is due. If the last day of the month falls on a date that is earlier than the consolidation day that you specify, the invoices are consolidated on the last business day of the month. Therefore, if you specify 31 for the consolidation day, but the current month has fewer than 31 days, the invoices are consolidated on the last business day of that month. For example, the invoices for June 2012 are consolidated on June 29, 2012, because that is the last business day of the month. The following table shows how the payment due date is calculated for invoices that are generated on different days. The consolidation day is 10, and the payment date is the end of the month.

| Invoice number | Invoice date | Consolidation day | Due date      |
|----------------|--------------|-------------------|---------------|
| INV001         | May 4, 2012  | May 10, 2012      | June 29, 2012 |
| INV002         | May 10, 2012 | May 10, 2012      | June 29, 2012 |
| INV003         | May 18, 2012 | June 10, 2012     | July 31, 2012 |
| INV004         | June 8, 2012 | June 10, 2012     | July 31, 2012 |




