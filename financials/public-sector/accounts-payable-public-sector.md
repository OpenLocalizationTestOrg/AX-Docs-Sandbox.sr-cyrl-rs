---
title: Accounts payable in the public sector | Microsoft Docs
description: This article introduces you to the public sector Accounts payable functionality that is integrated with Microsoft Dynamics AX. This functionality includes PO codes, posting definitions, one-time vendor invoicing, 1099 tax forms, cash discounts, vendor certification types, Project Accounting activity summary, electronic payments, cover and signature pages for reports, PO line amounts, and vendor invoice journal pages.
author: rschloma
manager: AnnBe
ms.date: 2015-12-07 16:32:05
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
keywords: BudgetParameters, CustParameters, LedgerJournalTable, OMLegalEntity, PurchAgreementListPage, PurchTableListPage, SrmParameters, VendCertificationType, VendCoverPageLayout, VendOpenInvoicesListPage, VendParametersVendParameters, VendTableListPage
audience: Application User
ms.reviewer: rschloma
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 19661
ms.assetid: 8af90393-cac5-455f-9b91-2fc6d0d975f1
ms.region: Global
ms.industry: Public sector
ms.author: brpotter
translationtype: Human Translation
ms.sourcegitcommit: b53ef103bfeca05effac07a4b7c434547dcbb230
ms.openlocfilehash: fd6bbb59e131dc34c7cff0b6dd45f45f15d899b4


---

# <a name="accounts-payable-in-the-public-sector"></a>Accounts payable in the public sector

This article introduces you to the public sector Accounts payable functionality that is integrated with Microsoft Dynamics AX. This functionality includes PO codes, posting definitions, one-time vendor invoicing, 1099 tax forms, cash discounts, vendor certification types, Project Accounting activity summary, electronic payments, cover and signature pages for reports, PO line amounts, and vendor invoice journal pages. 

<a name="what-are-the-prerequisites-for-setting-up-accounts-payable-in-the-public-sector"></a>What are the prerequisites for setting up Accounts payable in the public sector?
--------------------------------------------------------------------------------

Before you begin to adjust the settings and enter your data, you should complete the following tasks:

-   Set up vendors.
-   Set up numbering systems for vendors, purchase orders, and so on.
-   Decide what purchase order (PO) codes and messages will be used.

After you’ve set up the prerequisites,  you might have to set up the following Accounts payable features:

-   [Purchase order codes in the public sector](https://docs.microsoft.com/en-us/dynamics365/operations/financials/public-sector/purchase-order-codes-in-the-public-sector) –  You can create codes and special messages for confirming purchase orders. A confirming purchase order bypasses the typical purchasing process. For example, you authorize an unplanned order by using a purchase order number at the time of a purchase, instead of by using a document that is provided before the item is required. **Note:** This also applies to Procurement and sourcing.
-   [Posting definitions in the public sector](https://docs.microsoft.com/en-us/dynamics365/operations/financials/public-sector/posting-definitions-in-the-public-sector) – You can use posting definitions to create subledger journal lines for originating transactions that meet selected criteria. For example, you can use positing definitions to generate multiple balanced ledger entries, based on attributes such as transaction types and accounts. **Note:** This also applies to General ledger, Budgeting, and Accounts receivable.
-   [One-time vendors in the public sector](https://docs.microsoft.com/en-us/dynamics365/operations/financials/public-sector/one-time-vendors-in-the-public-sector) – When approval or a contract in the form of a purchase order isn't required, you can quickly create one or more invoices at the same time that you create a record for the vendor. For more information, see [Planning for one-time vendors in the public sector](https://docs.microsoft.com/en-us/dynamics365/operations/financials/public-sector/planning-for-one-time-vendors-in-the-public-sector).
-   [1099 form overview in the public sector](https://docs.microsoft.com/en-us/dynamics365/operations/financials/localizations/north-america/form-1099-in-the-public-sector) – If you do business with vendors that are subject to United States 1099 tax, you must track the amount that you pay to each vendor and report that information at the end of the calendar year. Public sector organizations use forms 1099-G and 1099-S. **Note:** This also applies to Procurement and sourcing.

## <a name="additional-public-sector-functionality"></a>Additional public sector functionality
The remaining sections in this article describe the Accounts payable functionality that is available for the public sector.

-   **Cash discounts** – Select the account to offset when cash discounts are applied to invoices.
-   **Vendor certification types** – Define a certification type for any vendor requirement that you want to track.
-   **Purchase agreement activity summary** – Enter summary details for activities that are related to a purchase agreement.
-   **Electronic payments** – Specify electronic payments to vendors. **Note:** This also applies to Procurement and sourcing.
-   **Cover and signature pages for payments reports** – Specify what information should appear on cover and signature pages for a payment report.
-   **Purchase order line amounts** – View line amounts for a purchase order and any amounts that must still be invoiced, or for invoices that are pending.

### <a name="how-can-i-apply-cash-discounts-to-vendor-invoices"></a>How can I apply cash discounts to vendor invoices?

You use the **Cash discounts** page in Accounts payable or Accounts receivable to select the account to offset when cash discounts are applied to invoices. You can do this for either an existing invoice or a new invoice that you create. Cash discount codes are linked to customer and vendor accounts, and are applied to sales orders and purchase orders. On the **Setup** FastTab, the **Discount offset accounts** field lets you offset either the specified main account for vendor discounts account or accounts that are specified on the invoice line.

### <a name="how-do-i-specify-and-assign-certification-types-for-vendors"></a>How do I specify and assign certification types for vendors?

You can create and assign vendor organizations any type of certification that those vendors have. This certification includes professional credentials, such as a professional engineer’s license or Microsoft SQL Server Certification. However, the certification can also specify that the vendors have liability insurance or minority status, or that they are in compliance with various environmental or consumer safety standards. You use the **Certification type** page to create certification types and descriptions.

### <a name="how-do-i-view-or-enter-summary-information-for-purchase-agreement-activity"></a>How do I view or enter summary information for purchase agreement activity?

You use the **Purchase agreements** page in Accounts payable or Procurement and sourcing to enter summary details for activities that are related to a purchase agreement. You can do this for either an existing purchase agreement or a new purchase agreement that you create. Examples include project milestones, planned dates for payments to a vendor, or the dates when items that are listed in a vendor contract are due for review.

##### <a name="tips"></a>Tips

-   You can set up a unique number for the activity on the **Legal entities** page in Organization administration or General ledger. When you select the activity in the purchase agreement, the number is assigned automatically.
-   You can also set up a unique identifier for the purchase agreement, in the **Number sequences** section on the **Procurement and sourcing parameters** page. When you create a purchase agreement, the number is assigned automatically.

### <a name="how-do-i-specify-electronic-payments-to-vendors"></a>How do I specify electronic payments to vendors?

You can distribute the payment of an invoice to bank accounts for multiple vendors. You can select multiple bank accounts and allocate a percentage to each account. Based on the accounts that are selected, single or multiple open transactions are created against the invoice. You can create payments for each journal line without creating a partial payment for each vendor bank account.

##### <a name="tip"></a>Tip

For example, there’s an existing purchase order for $100, and Bank A is the default vendor bank account. In the payment disbursement table, Bank A has 100-percent allocation. (If there is no default vendor bank account, the table is blank.) You can change the allocation for Bank A to 30 percent and then add a new row. On the new row, you can select another vendor bank, such as Bank B, and the allocation for the new row is automatically updated to 70 percent.

### <a name="how-can-i-create-and-print-cover-and-signature-pages-for-payments-reports"></a>How can I create and print cover and signature pages for payments reports?

When you create cover and signature pages for a payment report, you can specify the information that should appear. This information includes the names and titles of the people who should approve the proposed payments.

### <a name="how-do-i-view-purchase-order-line-amounts"></a>How do I view purchase order line amounts?

You can view line amounts for a purchase order. These amounts include the current ordered amount, and any amounts that have been received or invoiced. You can also view any amounts that must still be invoiced or amounts for invoices that are pending. Tip For example, you view a purchase order line that has purchases that are posted to two ledger accounts. One ledger account is for items that are ordered from a vendor for office furniture. The second ledger account is for office supplies. The ordered amount is equal to the sum of the invoiced, pending invoice, and invoice remaining amounts. The received amount is the part of the ordered amount that has been received from the vendor.

<a name="see-also"></a>See also
--------

[Accounts payable](https://ax.help.dynamics.com/en/wiki/Accounts-payable/)

[Accounts receivable in the public sector](https://docs.microsoft.com/en-us/dynamics365/operations/financials/public-sector/accounts-receivable-in-the-public-sector)

[Budgeting in the public sector](https://docs.microsoft.com/en-us/dynamics365/operations/financials/public-sector/budgeting-in-the-public-sector)

[General ledger in the public sector](https://ax.help.dynamics.com/en/wiki/general-ledger-in-the-public- sector/)

[Procurement and sourcing in the public sector](https://ax.help.dynamics.com/en/wiki/procurement-and-courcing-in-the-public- sector/)




<!--HONumber=Feb17_HO3-->


