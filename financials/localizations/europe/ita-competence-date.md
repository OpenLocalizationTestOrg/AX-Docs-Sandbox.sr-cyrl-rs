---
title: Competence date for transactions
description: This topic provides information about the competence date and explains how to enable the functionality for transactions in Italy.
author: ShylaThompson
manager: AnnBe
ms.date: 2016-12-19 16 - 06 - 00
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations
ms.custom: 264534
ms.assetid: d151f65a-3257-4296-8b00-d93c1dfdcf0e
ms.search.region: Italy
ms.author: epopov
ms.dyn365.ops.intro: 01-11-2016
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: b97d17ceabfd25c52c5f0c1e96a123bae6941c5a
ms.openlocfilehash: 3ce8ec844a01ec543b10ebdc76ae7ab95af3db60
ms.lasthandoff: 02/22/2017


---

# <a name="competence-date-for-transactions"></a>Competence date for transactions

This topic provides information about the competence date and explains how to enable the functionality for transactions in Italy.

In Italy, companies must use a posting date when they post transactions. The posting date is the date when the company acknowledges the transaction. Adjustment and closing transactions can be done several months after the last day of the fiscal year. (Usually, these transactions occur on the date when the balance sheet is approved by the Board of Directors.) These transactions must be reported on the Italian fiscal journal on the date when they are posted, but they must have a reference to their competence date. Therefore, two dates are required:

-   The competence date, which represents the date when the transaction affects the balance amount
-   The posting date, which is the date when the user posts the transaction

**Example:** The company's fiscal year is from January 1 through December 31. The balance sheet is approved on April 15. Therefore, adjustment and closing transactions are reported on the Italian fiscal journal in April, but they affect the balance on December 31.

## <a name="enable-the-competence-date"></a>Enable the competence date
To enable this functionality for transactions, on the **General ledger parameters** page, on the **Ledger** tab, set the **Transaction date reference to competence date** option to **Yes**. After the competence date is enabled, you can specify the competence and transactions dates for each journal that is used to post the adjustment and closing/opening transactions for the fiscal year:

-   General journal
-   Fixed assets journal
-   Bank account reconciliation
-   Closing sheet
-   Opening transaction
-   Project – Post costs
-   Project – Accrue turnover
-   Project – Estimate post
-   Project – Estimate reverse



