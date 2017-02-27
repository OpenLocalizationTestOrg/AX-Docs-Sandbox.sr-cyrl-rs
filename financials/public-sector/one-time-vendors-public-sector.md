---
title: One-time vendors in the public sector
description: This article provides information about how to create a one-time vendor and invoice, and how to import and create multiple one-time vendors and invoices.
author: rschloma
manager: AnnBe
ms.date: 2015-12-07 17 - 52 - 53
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerTransVoucher, SysConfiguration, Tax1099Summary, VendTableListPage
audience: Application User
ms.reviewer: rschloma
ms.search.scope: AX 7.0.0, Operations
ms.custom: 19801
ms.assetid: 403857a3-bebb-4ff7-b1b5-c88f41fc18ae
ms.search.region: Global
ms.search.industry: Public sector
ms.author: brpotter
ms.dyn365.ops.intro: 01-02-2016
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b97d17ceabfd25c52c5f0c1e96a123bae6941c5a
ms.openlocfilehash: 90ed6455c163782622b731516e636a54cec5fe8d
ms.lasthandoff: 02/22/2017


---

# <a name="one-time-vendors-in-the-public-sector"></a>One-time vendors in the public sector

This article provides information about how to create a one-time vendor and invoice, and how to import and create multiple one-time vendors and invoices. 

Occasionally, you might have to create an invoice for a new vendor that you have no regular relationship with. In Microsoft Dynamics 365 for Operations, if approval or a contract in the form of a purchase order isn't required, you can quickly create an invoice at the same time that you create a record for the vendor. For example, you have to pay referees or refunds, but a master vendor record doesn't exist. Alternatively, you might have to create multiple invoices for new vendors that you have no regular relationship with. If neither approval nor a purchase order is required, you can quickly create invoices at the same time that you create records for the vendors. For example, you want to support vendor payments for jury duty, registration payments, and customer refunds or other payments, but master vendor records don't exist. For more information, see [Planning for one-time vendors in the public-sector](plan-one-time-vendors-public-sector.md).

## <a name="how-do-i-create-a-onetime-vendor-and-invoice"></a>How do I create a onetime vendor and invoice?
The vendor record uses values from the default one-time vendor account, unless new values are entered. That account is specified in the **General** section of the **Accounts payable parameters** page. To view the account details, on the **All vendors** page, click the vendor account number of the default one-time vendor.

## <a name="how-do-i-import-and-create-multiple-onetime-vendors-and-invoices"></a>How do I import and create multiple onetime vendors and invoices?
To create multiple one-time vendors and invoices, you first create a file that contains the vendor and invoice information, and then import the file into a staging table in Microsoft Dynamics 365 for Operations. You then process the imported file and generate the invoices. For information about how to create the file, see [Planning for one-time vendors in the public sector](plan-one-time-vendors-public-sector.md).  

<a name="see-also"></a>See also
--------

[Accounts payable in the public sector](https://ax.help.dynamics.com/en/wiki/Accounts-payable-in-the-public-sector/)


