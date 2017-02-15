---
title: Mandats de paiement in the public sector in France | Microsoft Docs
description: The mandat de paiement is used by the director to notify the accountant that the organization is obligated to pay a specific amount to another entity, and to authorize the accountant to pay that amount. The mandat maintains the strict separation that is required between the operational role of the director and the accounting role of the accountant.
author: rschloma
manager: AnnBe
ms.date: 2015-12-13 05:19:51
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 27231
ms.assetid: 6427e630-4d68-46a9-a009-72e0a838a972
ms.region: France
ms.industry: Public sector
ms.author: brpotter
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: 16ebf3b9a78d4a6892b73f0d9c743ba617d3519f


---

# <a name="mandats-de-paiement-in-the-public-sector-in-france"></a>Mandats de paiement in the public sector in France

The mandat de paiement is used by the director to notify the accountant that the organization is obligated to pay a specific amount to another entity, and to authorize the accountant to pay that amount. The mandat maintains the strict separation that is required between the operational role of the director and the accounting role of the accountant.

<a name="directors-tasks"></a>Director’s tasks
----------------

From the **Maintain mandats de paiement** page, the director can complete the following tasks:

-   **Assign invoice lines to a mandat de paiement.** To find the invoice lines that haven’t yet been assigned to a mandat, you can filter the retrieved lines by the **Mandat** column.
-   **Authorize payment of invoice lines that are assigned to mandats.** This can also be done from the **Mandat de paiement** tab on the vendor invoice page or the vendor transactions page.
-   **Assign mandats to a bordereau de mandat.** To find the invoice lines that haven’t yet been assigned to a bordereau de mandat, you can filter the retrieved lines by the **Bordereau de mandat** column.
-   **Issue a requisition order.** Assign the invoice line to a new mandat before submitting it to the accountant as a requisition order.

To submit mandats to the accountant for payment, the director collects the printed mandats and their related documentation under a bordereau de mandat.

-   Print the mandats assigned to a bordereau from the **Records to include** FastTab on the **Mandat de paiement report** page.
-   Print the bordereau from the the **Records to include** FastTab on the **Bordereau de mandat report** page.

## <a name="accountants-tasks"></a>Accountant’s tasks
From the **Maintain mandats de paiement** page or from the **Mandat de paiement** tab on the pending vendor invoices or open vendor invoices page, the accountant can accept, reject, or hold mandats. When a mandat is rejected, the director status changes to **Not reviewed**, and the mandat and bordereau de mandat numbers are cleared.

## <a name="using-the-database-inquiry-page"></a>Using the database inquiry page
To open the database inquiry page on the **Maintain mandats de paiement** page, specify whether you want to work with pending or posted invoices and the range of dates you want to select invoices from. Then click **Retrieve lines**. This opens the **Database** **inquiry** page where you can specify the criteria for the invoice lines you want to retrieve. When you close the form, all invoice lines that meet the selected criteria are retrieved into the grid. Lines from invoices that are being edited will not be retrieved. **Tip**:  Use the following criteria in the database inquiry page to retrieve lines.

-   Invoice lines that have not been reviewed by the director.
    | Table  | Derived table | Field                         | Criteria       |
    |--------|---------------|-------------------------------|----------------|
    | Mandat | Mandat        | Director authorization status | "Not reviewed" |

-   Invoice lines from mandats that have been authorized for payment by the director, but not yet approved by the accountant.
    | Table  | Derived table | Field                         | Criteria       |
    |--------|---------------|-------------------------------|----------------|
    | Mandat | Mandat        | Director authorization status | "Authorized"   |
    | Mandat | Mandat        | Accountant acceptance status  | "Not reviewed" |

-   Invoice lines from mandats that were rejected by the accountant.
    | Table  | Derived table | Field                        | Criteria   |
    |--------|---------------|------------------------------|------------|
    | Mandat | Mandat        | Accountant acceptance status | "Rejected" |






<!--HONumber=Feb17_HO3-->


