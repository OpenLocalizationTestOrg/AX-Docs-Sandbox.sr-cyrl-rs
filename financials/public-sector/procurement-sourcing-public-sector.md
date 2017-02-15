---
title: Procurement and sourcing in the public sector | Microsoft Docs
description: This overview introduces you to the public sector Procurement and sourcing functionality. This includes purchase order codes, vendor certification types, purchase agreement classification functionality, and purchase order line amounts.
author: rschloma
manager: AnnBe
ms.date: 2015-12-07 16:45:24
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
keywords: AgreementClassification, BudgetParameters, ProcCategoryHierarchyManagement, PurchTableListPage, smmActivities, VendCertificationType, VendTableListPage
audience: Application User
ms.reviewer: rschloma
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 19681
ms.assetid: 8ea36df3-d116-45e7-8187-99b52af01909
ms.region: Global
ms.industry: Public sector
ms.author: brpotter
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: da2524f379c47a7425737bc57234d34ea9f571b4


---

# <a name="procurement-and-sourcing-in-the-public-sector"></a>Procurement and sourcing in the public sector

This overview introduces you to the public sector Procurement and sourcing functionality. This includes purchase order codes, vendor certification types, purchase agreement classification functionality, and purchase order line amounts.

This article describes the Procurement and sourcing functionality that is available for the public sector. []()

## <a name="what-are-the-prerequisites-for-setting-up-procurement-and-sourcing-in-the-public-sector"></a>What are the prerequisites for setting up Procurement and sourcing in the public sector?
Before you begin to adjust the settings and input your data, you should:

-   Set up vendors
-   Set up the numbering system for vendors, purchase orders, and so on
-   Specify vendor certification types

You may need to set up the following Procurement and sourcing features for public sector organizations:

-    [Public sector purchase order codes](https://docs.microsoft.com/en-us/dynamics365/operations/financials/public-sector/purchase-order-codes-in-the-public-sector) Create codes and special messages for confirming purchase orders. A confirming purchase order circumvents the typical purchasing process.

**Note** This also applies to Accounts payable.

-   [Public sector accounting in France](https://docs.microsoft.com/en-us/dynamics365/operations/financials/localizations/europe/public-sector-accounting-in-france) For French organizations, additional steps may be required for the public sector.

The following sections describe the Procurement and sourcing features that are available for the public sector.

## <a name="what-are-vendor-certification-types"></a>What are vendor certification types?
You can create and assign to vendor organizations any types of certification that the vendors hold. This includes not only professional credentials, such as a professional engineer’s license or Microsoft SQL Server Certification, but also whether they have liability insurance, minority status, or are in compliance with various environmental or consumer safety standards. You use the **Certification type** page in Accounts payable to enter the certification type and the description.

## <a name="what-do-i-need-to-know-about-purchase-or-sales-agreement-classifications"></a>What do I need to know about purchase or sales agreement classifications?
When users create a new purchase agreement or sales agreement, they must always select the type of purchase agreement or sales agreement. Additional public sector controls are available on the **Agreement classifications** pages. To create and specify agreement classifications, you use the **Purchase agreement classification** page in Procurement and sourcing or the **Sales agreement classification** page in Sales and marketing. Take the following information into account when specifying details for purchase or sales agreement classifications.

### <a name="how-do-i-enter-information-about-subcontractors-on-purchase-agreements"></a>How do I enter information about subcontractors on purchase agreements?

Select the **Subcontractors** option.

### <a name="how-do-i-enter-information-about-insurance-policies-and-bonds-on-purchase-agreements"></a>How do I enter information about insurance policies and bonds on purchase agreements?

Select the **Certifications** option. The information can be used to generate a report that you can use to monitor vendor compliance with certification requirements. (To generate the report, go to the **Purchase agreement certification compliance** page.)

### <a name="how-do-i-enter-information-about-milestones-and-tasks-on-purchase-agreements"></a>How do I enter information about milestones and tasks on purchase agreements?

Select the **Activities** option.

### <a name="how-do-i-require-direct-invoicing-and-prevent-the-use-of-release-orders-with-purchase-agreements"></a>How do I require direct invoicing and prevent the use of release orders with purchase agreements?

Select the **Require direct invoicing** option. []()

## <a name="can-i-view-purchase-order-line-amounts"></a>Can I view purchase order line amounts?
Yes. Line amounts for a purchase order can be viewed, including the current ordered amount and any amounts that have been received or invoiced. They can also view any amounts that remain to be invoiced or amounts for pending invoices.

### <a name="tip"></a>Tip

Let’s say you view a purchase order line with purchases posted to two ledger accounts. One ledger account is for office furniture ordered from a vendor. The second ledger account is for office supplies. The ordered amount is equal to the sum of the invoiced amounts, pending invoice amounts, and invoice remaining amounts. The received amount is the portion of the ordered amount that has been received from the vendor.

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Ledger account</strong></td>
<td><strong>Ordered</strong></td>
<td><strong>Received</strong></td>
<td><strong>Invoiced</strong></td>
<td><strong>Pending invoice</strong></td>
<td><strong>Invoice remaining</strong></td>
</tr>
<tr class="even">
<td>60010 (office furniture)</td>
<td><p>1,200.00</p></td>
<td>250.00</td>
<td>350.00</td>
<td>200.00</td>
<td><p>650.00</p></td>
</tr>
<tr class="odd">
<td>60020 (office supplies)</td>
<td><p>750.00</p></td>
<td>150.00</td>
<td>400.00</td>
<td></td>
<td><p>350.00</p></td>
</tr>
<tr class="even">
<td>Totals</td>
<td><p>1,950.00</p></td>
<td>400.00</td>
<td>750.00</td>
<td>200.00</td>
<td><p>1,000.00</p></td>
</tr>
</tbody>
</table>

 

<a name="see-also"></a>See also
--------

[Procurement and sourcing](https://docs.microsoft.com/en-us/dynamics365/operations/manufacturing/procurement-sourcing/procurement-and-sourcing)

[Accounts payable in the public sector](https://docs.microsoft.com/en-us/dynamics365/operations/financials/public-sector/accounts-payable-in-the-public-sector)




<!--HONumber=Feb17_HO3-->


