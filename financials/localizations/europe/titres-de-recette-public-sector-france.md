---
title: Titres de recette in the public sector in France | Microsoft Docs
description: The titre de recette is used by the director to notify the accountant that the organization is entitled to collect a specific amount from another entity, and to authorize the accountant to deposit that amount. The director or the accountant may delegate a representative to perform the task, but the responsibility for each task remains with the director or the accountant. The titre maintains the strict separation that is required between the operational role of the director and the accounting role of the accountant.
author: rschloma
manager: AnnBe
ms.date: 2015-12-07 17:56:01
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
keywords: CustFreeInvoice
audience: Application User
ms.reviewer: rschloma
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 19931
ms.assetid: ea94f78a-84d5-46e3-b451-0d1106913828
ms.region: France
ms.industry: Public sector
ms.author: brpotter
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: be27b3083a89b4303a9935edcb4e0dea9da3a7f4


---

# <a name="titres-de-recette-in-the-public-sector-in-france"></a>Titres de recette in the public sector in France

The titre de recette is used by the director to notify the accountant that the organization is entitled to collect a specific amount from another entity, and to authorize the accountant to deposit that amount. The director or the accountant may delegate a representative to perform the task, but the responsibility for each task remains with the director or the accountant. The titre maintains the strict separation that is required between the operational role of the director and the accounting role of the accountant.

In Microsoft Dynamics 365 for Operations, each titre is assigned a single free text invoice line. This guarantees that each titre concerns only one debtor and includes only one budgetary account. A group of related titres, together with all supporting documentation, are assigned to a bordereau de titre for submittal to the accountant.

## <a name="directors-tasks"></a>Director’s tasks
From the **Maintain titres de recette** page, the director can complete the following tasks:

-   **Assign invoice lines to a titre de recette.** To find the invoice lines that haven’t yet been assigned to a titre, you can filter the retrieved lines by the **Titre** column.
-   **Authorize collection of invoice lines that are assigned to titres.** This can also be done from the **Titre de recette** tab on the free text invoice page.
-   **Assign titres to a bordereau de titre.** To find the invoice lines that haven’t yet been assigned to a bordereau de titre, you can filter the retrieved lines by the **Bordereau de titre** column.

To submit titres to the accountant for deposit, the director collects the printed titres and their related documentation under a borderau de titre.

-   Print the titres assigned to a bordereau from the **Records to include** FastTab on the **Titre de recette report** page.
-   Print the bordereau from the the **Records to include** FastTab on the **Bordereau de titre report** page.

## <a name="accountants-tasks"></a>Accountant’s tasks
From the **Maintain titres de recette** page or from the **Titre de recette** tab on the free text invoice page, the accountant can accept, reject, or hold titres. When a titre is rejected, the director status changes to Not reviewed, and the titre and bordereau de titre numbers are cleared.

## <a name="using-the-database-inquiry-page"></a>Using the database inquiry page
To open the database inquiry page on the **Maintain titres de recette** page, specify the range of dates you want to select invoices from. Then click **Retrieve lines**. This opens the database inquiry page where you can specify the criteria for the invoice lines you want to retrieve. When you close the form, all the invoice lines that meet the selected criteria are retrieved into the grid. Lines from the invoices that are being edited will not be retrieved. **Tip**: Use the following criteria in the database inquiry page to retrieve lines.

-   Invoice lines that have not been reviewed by the director.
    | Table | Derived table | Field                         | Criteria       |
    |-------|---------------|-------------------------------|----------------|
    | Titre | Titre         | Director authorization status | "Not reviewed" |

-   Invoice lines from titres that have been authorized for collection by the director, but not yet approved by the accountant.
    | Table | Derived table | Field                         | Criteria       |
    |-------|---------------|-------------------------------|----------------|
    | Titre | Titre         | Director authorization status | "Authorized"   |
    | Titre | Titre         | Accountant acceptance status  | "Not reviewed" |

-   Invoice lines from titres that were rejected by the accountant.
    | Table | Derived table | Field                        | Criteria   |
    |-------|---------------|------------------------------|------------|
    | Titre | Titre         | Accountant acceptance status | "Rejected" |






<!--HONumber=Feb17_HO3-->

