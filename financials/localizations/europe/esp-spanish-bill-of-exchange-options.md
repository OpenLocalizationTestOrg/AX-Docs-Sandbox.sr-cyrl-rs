---
title: Spanish bill of exchange options
description: This topic describes specific options and changes in basic bill of exchange process implemented in Microsoft Dynamics 365 for Operations for legal entities in Spain.
author: ShylaThompson
manager: AnnBe
ms.date: 2016-12-19 18 - 00 - 38
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations
ms.custom: 264644
ms.assetid: 67e8f90e-5522-4631-96c5-62d193eab72f
ms.search.region: Spain
ms.author: v-elgolu
ms.dyn365.ops.intro: 01-11-2016
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: b97d17ceabfd25c52c5f0c1e96a123bae6941c5a
ms.openlocfilehash: 86f57da22b8422d47ba8d3f84099479aa5025fa4
ms.lasthandoff: 02/22/2017


---

# <a name="spanish-bill-of-exchange-options"></a>Spanish bill of exchange options

This topic describes specific options and changes in basic bill of exchange process implemented in Microsoft Dynamics 365 for Operations for legal entities in Spain.

For legal entities in Spain, the bill of exchange functionality has additional options:

-   Validation for bill of exchange journals
-   Dates in bill of exchange journals

## <a name="accounts-receivable-parameters-for-spanish-bills-of-exchange"></a>Accounts receivable parameters for Spanish bills of exchange
To set up the parameters for bills of exchange for legal entities in Spain, go to **Accounts receivable parameters** &gt; **Bill of exchange ES**.

## <a name="validation-for-bill-of-exchange-journals"></a>Validation for bill of exchange journals
If the **Validation on bill of exchange journal** parameter is set to **Yes**, a bill of exchange isn't posted when transactions have the same voucher number and different transaction dates. This parameter applies to ledger journal transactions. This parameter is used only when the journal allows one voucher number, and when the **Validation on bill of exchange journals** option is selected on the **Accounts receivable parameters** page. The **Validation on bill of exchange journal** parameter affects the following documents:

-   Draw bill of exchange journal
-   Remittance journal
-   Protest bill of exchange journal
-   Redraw bill of exchange journal
-   Settle bill of exchange journal
-   Payment journal

## <a name="dates-in-bill-of-exchange-journals"></a>Dates in bill of exchange journals
If the **Date treatment on bill of exchange journal** parameter is set to **Yes**, the transaction date on bill of exchange journals is updated to the due date when a payment proposal is used. The **Date treatment on bill of exchange journal** parameter affects the following documents:

-   Remittance journal
-   Protest bill of exchange journal
-   Redraw bill of exchange journal



