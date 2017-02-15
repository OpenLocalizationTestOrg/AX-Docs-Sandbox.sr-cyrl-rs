---
title: Free text invoices in the public sector | Microsoft Docs
description: This topic describes the free text invoice functionality that is available for public sector as well as answers common questions about using billing classifications and billing codes with free text invoices.
author: rschloma
manager: AnnBe
ms.date: 2015-12-12 23:25:50
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
keywords: CustBillingClassification, CustBillingCode, CustFreeInvoice
audience: Application User
ms.reviewer: rschloma
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 25821
ms.assetid: 059aa726-78e0-4c88-9540-ed74cb8f9351
ms.region: Global
ms.industry: Public sector
ms.author: brpotter
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: a6e9c786a261405c5964df9e253d6f9cc1162da7


---

# <a name="free-text-invoices-in-the-public-sector"></a>Free text invoices in the public sector

This topic describes the free text invoice functionality that is available for public sector as well as answers common questions about using billing classifications and billing codes with free text invoices.

<a name="do-i-have-to-select-a-billing-classification-for-every-free-text-invoice"></a>Do I have to select a billing classification for every free text invoice?
-------------------------------------------------------------------------

Yes, when billing classifications are enabled, you have to enter a billing classification for every free text invoice. The billing classification controls which billing codes that you can enter on the invoice. It also governs payment terms and conditions, number sequences, and the processing of the invoice. To learn more about billing classifications, see [Billing classifications and billing codes in the public sector](https://docs.microsoft.com/en-us/dynamics365/operations/financials/public-sector/billing-classifications-and-billing-codes-in-the-public-sector).

## <a name="what-happens-if-ive-already-created-free-text-invoices-when-i-enable-billing-classifications"></a>What happens if I’ve already created free text invoices when I enable billing classifications?
If an invoice was not yet posted when you enabled billing classifications, you have to assign a billing classification to the invoice before you can post it. When you open the page to view the invoice, you'll get a message telling you that the billing classification is required.

## <a name="why-should-i-use-billing-codes-when-i-create-free-text-invoices"></a>Why should I use billing codes when I create free text invoices?
When you select a billing code, default values are automatically entered in many fields on the invoice line. This makes data entry faster and more accurate. Billing codes are also used with posting definitions to control how Accounts receivable transactions are posted to the ledger.

## <a name="im-creating-a-free-text-invoice-and-the-billing-code-that-i-want-to-use-isnt-available-what-should-i-do"></a>I’m creating a free text invoice, and the billing code that I want to use isn’t available. What should I do?
First make sure that the invoice is using the right billing classification. Only certain billing codes can be used with each billing classification. If the billing classification is correct, then you should select one of the billing codes that are available for the free text invoice that you are creating.

## <a name="i-can-change-some-of-the-fields-on-my-free-text-invoices-all-of-the-time-and-i-can-change-all-of-the-fields-some-of-the-time-but-some-of-the-fields-i-can-only-change-some-of-the-time-whats-up-with-that"></a>I can change some of the fields on my free text invoices all of the time, and I can change all of the fields some of the time. But some of the fields I can only change some of the time. What’s up with that?
Settings on the billing code control whether you can change certain fields.

-   If the billing code on a free text invoice line doesn’t allow rate changes on the invoice, you can’t change the amount, the unit price, or the amount details on the line. **Tip**: If the **Billing code determines** field is set to unit price, you can’t change the unit price, but you can change the amount indirectly by changing the quantity.
-   If the billing code on a free text invoice line doesn’t allow changes to the ledger accounts, you can’t change the accounting distributions on the line. You can change the main account that displays on the free text invoice line, but that change affects only what is displayed. Changing the main account does not affect the distributions.
-   When there’s a project associated with the invoice line, the billing code controls whether you can change the project ID, category, and ledger account. **Tip**: To change the ledger account for invoice lines related to projects, changes have to be allowed both on the billing code itself and on the Projects section of the Accounts receivable parameters page.

To learn more about billing codes, see [Billing classifications and billing codes in the public sector](https://docs.microsoft.com/en-us/dynamics365/operations/financials/public-sector/billing-classifications-and-billing-codes-in-the-public-sector).

## <a name="where-does-the-interest-code-on-a-free-text-invoice-come-from"></a>Where does the interest code on a free text invoice come from?
The interest code can be set on the billing code, the billing classification, or the posting profile.

<a name="see-also"></a>See also
--------

[Accounts receivable](https://docs.microsoft.com/en-us/dynamics365/operations/financials/accounts-receivable/accounts-receivable)

[Accounts receivable in the public sector](https://ax.help.dynamics.com/en/?post_type=incsub_wiki&p=169941)

[Accounting distributions and subledger journal entries for free text invoices](https://docs.microsoft.com/en-us/dynamics365/operations/financials/accounts-receivable/accounting-distributions-and-subledger-journal-entries-for-free-text-invoices)




<!--HONumber=Feb17_HO3-->


