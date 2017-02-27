---
title: Procurement and sourcing in the public sector in France
description: "This article explains how the standard features that are related to procurement and sourcing are augmented for French entities in the public sector. These features are used to help meet the requirements of the Code des Marchés Publics."
author: rschloma
manager: AnnBe
ms.date: 2015-12-07 17 - 55 - 41
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AgreementClassification, PurchAgreement, SysPolicy
audience: Application User
ms.reviewer: rschloma
ms.search.scope: AX 7.0.0, Operations
ms.custom: 19891
ms.assetid: 3d3c89eb-5d6b-4d79-879b-ad6bf4bade35
ms.search.region: France
ms.search.industry: Public sector
ms.author: brpotter
ms.dyn365.ops.intro: 01-02-2016
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b97d17ceabfd25c52c5f0c1e96a123bae6941c5a
ms.openlocfilehash: b5d9e710de641aaf7807188146eaaf603a705eba
ms.lasthandoff: 02/22/2017


---

# <a name="procurement-and-sourcing-in-the-public-sector-in-france"></a>Procurement and sourcing in the public sector in France

This article explains how the standard features that are related to procurement and sourcing are augmented for French entities in the public sector. These features are used to help meet the requirements of the Code des Marchés Publics. 

<a name="set-spending-thresholds-by-procurement-category"></a>Set spending thresholds by procurement category
-----------------------------------------------

To set spending thresholds for purchases in the procurement categories that are defined by the Clé de Contrôle Marché, you can use the **Spending thresholds by category** purchasing policy rule . By implementing this purchasing policy rule to control spending thresholds by category, you can use the effective date attributes, predicted expenditure amounts, and threshold amounts to support your procurement practices, and to help guarantee the efficient and effective use of public funds.

## <a name="create-tranches-and-lots"></a>Create tranches and lots
To create tranches and lots, you can create a hierarchy of parent and child purchase agreements. The child purchase agreements act as the tranches and lots of the parent purchase agreement. The purchase agreement hierarchy has some specific characteristics:

-   A user can view the parent purchase agreement, and can see the total activity of the parent and all its related child agreements. This feature provides a single management view for reviewing and controlling activity on purchase agreements.
-   Some values from the parent purchase agreement are automatically transferred to the child agreements. For example, policies that are related to competitive advertising can be assigned to the parent purchase agreement. Those policies then apply to all the child agreements that are related to that parent.
-   Purchase agreements can have a prime contractor, co-contractors, and subcontractors. The prime contractor can be assigned to the parent purchase agreement, and a co-contractor or subcontractor can be assigned to specific child agreements.

**Note:** If you've added lines to a purchase agreement, that purchase agreement can't be used as a parent agreement. The **Create child agreement** button will no longer be available. Likewise, if you've created a child purchase agreement, you can't add lines to the parent purchase agreement. To see the relationships among parent and child purchase agreements, use the **Purchase agreement tree** page.

## <a name="set-up-purchase-agreement-access-and-limits"></a>Set up purchase agreement access and limits
You can set up purchase agreements so that only approved departments have access to the agreement. You can also limit the amount that each department can spend against the purchase agreement. Users who try to exceed the maximum amount that is allocated for a department receive a message, and they are prevented from confirming the release or processing the invoice. Before you can use this capability, you must set the following parameters in the **General** section of the **Accounts payable parameters** page:

-   In the **Account structure** field, select the account structure to use on the **Purchase agreement department access** page to control access to purchase agreements. The account structure must include the financial dimension segment that you use to control access to purchase agreements.
-   In the **Financial dimension** field, select the financial dimension that you use to control access to purchase agreements. Most organization use the department dimension, but some organizations might restrict access to purchase agreements to different entities within their organizations.

## <a name="manage-information-about-subcontractors-certifications-and-milestones-on-purchase-agreements"></a>Manage information about subcontractors, certifications, and milestones on purchase agreements
You can create purchase agreement classifications that add administrative fields to the purchase agreements that use the classification.

-   To add information about subcontractors to purchase agreements, select the **Subcontractors** option on the purchase agreement classification.  Purchase agreements can have a prime contractor, co-contractors, and subcontractors. The prime contractor can be assigned to the parent purchase agreement, and a co-contractor or subcontractor can be assigned to specific child agreements.
-   To add information about certifications for vendors to purchase agreements, select the **Certifications** option on the purchase agreement classification. Certification information can be used to generate a report that lets you monitor vendor compliance with certification requirements.
-   To add information about milestones and tasks to purchase agreements, select the **Activities** option on the purchase agreement classification.

 


