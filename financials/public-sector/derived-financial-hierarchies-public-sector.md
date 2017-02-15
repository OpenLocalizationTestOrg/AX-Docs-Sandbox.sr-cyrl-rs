---
title: Derived financial hierarchies in the public sector | Microsoft Docs
description: This article describes the derived financial hierarchies functionality that is available for the public sector.
author: rschloma
manager: AnnBe
ms.date: 2015-12-08 18:59:20
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
keywords: EcoResCategory, EcoResCategoryHierarchyListPage, EcoResCategoryHierarchyRole, LedgerDerivedFinHierarchies, LedgerDerivedFinHierarchyFilterResults, LedgerDerivedFinHierarchyLegalEntities
audience: Application User
ms.reviewer: rschloma
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 20911
ms.assetid: aba2f2ae-f666-4b29-a672-b2a18f40a1ce
ms.region: Global
ms.industry: Public sector
ms.author: brpotter
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: f75860ade1efa82c154a16f8684a557f321eeb96


---

# <a name="derived-financial-hierarchies-in-the-public-sector"></a>Derived financial hierarchies in the public sector

This article describes the derived financial hierarchies functionality that is available for the public sector. 

To meet Common Government-wide Accounting Classification (CGAC) requirements, public-sector organizations can use derived financial hierarchies to collect and analyze posted transaction data for specific main account numbers, full account numbers, and financial dimension values. Typically, category hierarchies are set up to classify transactions for reporting and analysis based on the financial dimensions in an account structure at the time of posting. However, by using category hierarchies with a Derived financial hierarchy category type, you can create filter rules that create financial categories and dimension values that are not part of the account number. The financial categories and dimension values defined in the filter rules are derived from the account number dimension values that are used in the posted transactions. Derived financial hierarchies give you a more flexible approach to grouping transactions for ad hoc analytics. They allow you to categorize transactions without having to expand the account structure to include the additional categories or dimensions you want to track.

## <a name="example"></a>Example
An organization has an employee wellness program and an employee education program. These programs are not associated with financial dimensions. To collect account numbers used in the posted transactions for these programs, you could do the following:

-   **Set up the category hierarchies and the derived financial hierarchies:** Create a category hierarchy named “Employee programs” with a parent node named “Programs” and two child nodes named “Employee wellness” and “Employee education.” Assign the **Derived financial hierarchy** category type to the “Employee programs” category hierarchy. Associate the “Employee programs” derived financial hierarchy with the legal entity.
-   **Set up filter rules:** Use the **Derived financial hierarchies** page to create filter rules for the main accounts and financial dimension values associated with the “Employee wellness” and “Employee education” nodes in the “Employee programs” derived financial hierarchy. **Tip:** To enter more than one dimension value in a filter, use a comma without spaces as a separator. For example, enter 100,110 or Benefits,Insurance.
-   **Analyze posted transaction data:** In the filter results, view account numbers and their account and financial dimension details.

 

<a name="see-also"></a>See also
--------

[General ledger](https://docs.microsoft.com/en-us/dynamics365/operations/financials/general-ledger/general-ledger)

[General ledger in the public sector](https://ax.help.dynamics.com/en/?post_type=incsub_wiki&p=164121)




<!--HONumber=Feb17_HO3-->


