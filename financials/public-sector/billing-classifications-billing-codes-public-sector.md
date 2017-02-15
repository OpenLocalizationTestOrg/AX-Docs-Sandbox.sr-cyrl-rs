---
title: Billing classifications and billing codes in the public sector | Microsoft Docs
description: Public-sector organizations can use billing classifications and billing codes to help manage free text invoices.
author: rschloma
manager: AnnBe
ms.date: 2015-12-07 15:35:53
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
keywords: CustBillingClassification, CustBillingCode, CustCustomField
audience: Application User
ms.reviewer: rschloma
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 19491
ms.assetid: 03c20b2a-cbc1-48a4-8632-d1b218c19942
ms.region: Global
ms.industry: Public sector
ms.author: brpotter
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: 7b5a8bd6d1ecf4c309a92b848830b5c27c53a27c


---

# <a name="billing-classifications-and-billing-codes-in-the-public-sector"></a>Billing classifications and billing codes in the public sector

Public-sector organizations can use billing classifications and billing codes to help manage free text invoices. 

<a name="billing-classifications"></a>Billing classifications
-----------------------

Billing classifications are used to group similar free text invoices for processing and viewing. For example, a transit agency might lease space in each transit station to small coffee shops and other vendors. By creating a billing classification for leases, the agency can automatically apply the same terms of payment and use the same sequence of collection letters for all leases. The agency can also view invoices for all the leases together, even if the leases don’t share the same financial dimensions. Billing classifications include the following information:

-   Billing classification code (up to 15 alphanumeric characters)
-   Description (up to 60 characters)
-   Terms of payment
-   Interest information
-   Number sequence for invoice number
-   Number sequence for credit notes
-   Number sequence for collection letters
-   Billing codes that can be assigned to invoices that use this billing classification

You can use billing classifications to control the settlement priority of free text invoices. For details, see [Settlement priority in the public sector](https://docs.microsoft.com/en-us/dynamics365/operations/financials/public-sector/settlement-priority-in-the-public-sector). A billing classification can include many billing codes, but each billing code can be assigned to only one billing classification. When you select a billing classification on a free text invoice, only the billing codes that are listed on the billing classification are available for the invoice. Before you set up billing classifications, be sure that you have set up the terms of payment, interest codes, posting profiles, collection letter sequences, number sequences, and billing codes that you plan to use on the billing classifications.

## <a name="billing-codes"></a>Billing codes
Billing codes provide a set of default billing values and rates for a defined type of service or charge. The values that you define for each billing code are automatically entered in the free text invoice line when the billing code is selected. For example, a waste management department might bill certain customers for new containers. They would have a “New container” billing code that contains the billing information for these containers. When the department creates a free text invoice and selects the “New container” billing code on an invoice line, the default values from the billing code are entered automatically. Billing codes include the following information:

-   Billing code (up to 10 alphanumeric characters)
-   Description (up to 60 characters; this will print on the invoice)
-   Effective date and expiration date
-   Sales tax information
-   Interest information
-   Accounting distribution
-   Rate information
-   Project information (if enabled on the Accounts receivable parameters page)
-   Custom fields

Generally, the default values from the billing code can be changed on the free text invoice. However, you can set the billing code to allow or prevent changes to certain fields. For details, see Free text invoices in the public sector. Billing codes can also be associated with posting definitions. When a billing code is used on an invoice line, the posting definition that is associated with the billing code is used for posting the transaction to the ledger. To learn more about posting definitions, see [Posting definitions in the public sector](https://docs.microsoft.com/en-us/dynamics365/operations/financials/public-sector/posting-definitions-in-the-public-sector).

### <a name="custom-fields"></a>Custom fields

You can create custom fields for billing codes. These fields are used to collect data related to specific billing charges. For example, the animal control department for a city could use custom fields to record the type of animal and the date of its last rabies vaccination. Because you assign custom fields to billing codes, you should create your custom fields before you create billing codes. There are six kinds of custom fields. You can set a default value for any custom field. The default values can be changed on the free text invoice.

-   **Currency** –Currency fields accept only numbers with two decimal places. You can specify the minimum and maximum values for the field.
-   **Decimal** – Decimal fields accept only decimal numbers with four decimal places. You can set minimum and maximum values for the field.
-   **Text** – Text fields can hold any kind of text, and any input entered into them will be interpreted as text. You can set a maximum field length for the field.
-   **Integer** – Integer fields accept only whole numbers. You can set minimum and maximum values for the field.
-   **Boolean** – Boolean fields allow yes/no selections.
-   **Date** – Date fields accept only dates. The date is stored as mm/dd/yyyy.

## <a name="do-i-have-to-use-billing-classifications"></a>Do I have to use billing classifications?
Although you don’t have to enable billing classifications, we strongly recommend that you do. Many of the public-sector capabilities in the Accounts receivable app are available only when billing classifications are enabled. After you have enabled billing classifications, however, the billing classification is a required field on free text invoices. To learn more about billing classifications and billing codes on free text invoices, see [Free text invoices in the public sector](https://docs.microsoft.com/en-us/dynamics365/operations/financials/public-sector/free-text-invoices-in-the-public-sector).

## <a name="how-do-i-enable-billing-classifications"></a>How do I enable billing classifications?
Enable billing classifications on the **Accounts receivable parameters** page. In the **General** section, on the **Sales setup** FastTab, select **Use billing classifications**. The pages where you create billing classifications and billing codes are available before you enable billing classifications. You’ll want to set up all of your billing classifications and billing codes before you enable them. After you have enabled billing classifications, every free text invoice must have a billing classification. **Note**: If you plan to use billing classifications to determine the settlement priority of free text invoices, you must enable the **Billing** attribute on the **Settlement priority** page after you enable billing classifications. For details, see [Settlement priorities in the public sector](https://docs.microsoft.com/en-us/dynamics365/operations/financials/public-sector/settlement-priority-in-the-public-sector).

## <a name="do-i-have-to-create-new-billing-codes-when-billing-rates-change"></a>Do I have to create new billing codes when billing rates change?
When billing codes need to be updated, you don’t need to create new billing codes. Instead, you can create multiple versions of the billing code, with effective and expiration dates for each version. On the effective date, the system will start using the updated version automatically.

## <a name="can-i-assign-the-same-billing-code-to-more-than-one-billing-classification"></a>Can I assign the same billing code to more than one billing classification?
No, but there’s a way to get the results you need anyway. Let’s say that your organization uses a separate billing classification for each department. Three of the departments need a billing code for license agreements. You can’t assign a single “License agreement” billing code to three billing classifications, but you can create a set of three identical billing codes, and assign one to each department.

<a name="see-also"></a>See also
--------

[Accounts receivable](https://docs.microsoft.com/en-us/dynamics365/operations/financials/accounts-receivable/accounts-receivable)

[Accounts receivable in the public sector](https://ax.help.dynamics.com/en/?post_type=incsub_wiki&p=169941)




<!--HONumber=Feb17_HO3-->

