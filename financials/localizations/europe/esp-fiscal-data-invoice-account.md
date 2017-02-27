---
title: Use fiscal data from the invoice account
description: For legal entities in Spain, the Use fiscal data from invoice account functionality enables fiscal data on sales orders, free text invoices, and purchase orders to be updated automatically, based on information from the invoice account. This topic provides information about the Use fiscal data from invoice account functionality and explains how to set it up.
author: ShylaThompson
manager: AnnBe
ms.date: 2016-12-22 16 - 47 - 48
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations
ms.custom: 265224
ms.assetid: 8b46e367-0f19-46d1-8fc2-88d035c460a0
ms.search.region: Spain
ms.author: v-elgolu
ms.dyn365.ops.intro: 01-11-2016
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: b97d17ceabfd25c52c5f0c1e96a123bae6941c5a
ms.openlocfilehash: da1a90546b9505b8f6427a77ca03833e5242f6e0
ms.lasthandoff: 02/22/2017


---

# <a name="use-fiscal-data-from-the-invoice-account"></a>Use fiscal data from the invoice account

For legal entities in Spain, the Use fiscal data from invoice account functionality enables fiscal data on sales orders, free text invoices, and purchase orders to be updated automatically, based on information from the invoice account. This topic provides information about the Use fiscal data from invoice account functionality and explains how to set it up.

For legal entities in Spain, the Use fiscal data from invoice account functionality enables fiscal data on sales orders, free text invoices, and purchase orders to be updated automatically, based on information from the invoice account. The fiscal data that is updated includes the customer or vendor name, address, and tax information. The Use fiscal data from invoice account functionality affects the following modules:

-   Accounts payable'**Invoice account** change page'
-   Procurement and sourcing
-   Accounts receivable
-   Sales and marketing

## <a name="accounts-payable-and-procurement-and-sourcing"></a>Accounts payable and Procurement and sourcing
To manage the opportunity of fiscal data automatic update on Invoice account change in the Accounts payable module you need to set up a parameter Use fiscal data from invoice account on Invoice tab of the Account payable &gt; Setup &gt; Account payable &gt; parameters page. The following options are available:

-   **Never** – Information is updated from the vendor account.
-   **Always** – Information is updated from the invoice account.
-   **Ask** – The user is prompted to specify whether information should be updated from the invoice account or the vendor account.

When the **Use fiscal data from invoice account** parameter is set, three fields on a purchase order may be updated according the value of the parameter. When the **Invoice account** field is changed, the following fields are updated with information from the invoice account:

-   Name
-   Sales tax group
-   Tax exemption

## <a name="accounts-receivable-and-sales-and-marketing"></a>Accounts receivable and Sales and marketing
To manage the opportunity of fiscal data automatic update on **Invoice account** change in the **Accounts receivable** module you need to set up a parameter “**Use fiscal data from invoice account**” on the **Invoice** fasttab of the **Updates** tab of the **Account receivable** &gt; **Setup** &gt; **Account receivable** **parameters** page. The following options are available:

-   **Never** – Information is updated from the customer account.
-   **Always** – Information is updated from the invoice account.
-   **Ask** – The user is prompted to specify whether information should be updated from the invoice account or the customer account.

When the **Use fiscal data from invoice account** parameter is set, the following documents from Accounts receivable can be updated:

-   Sales orders
-   Free text invoices

When the **Invoice account** field is changed, the following fields can be updated with information from the invoice account:

-   Name
-   Sales tax group
-   Tax exemption



