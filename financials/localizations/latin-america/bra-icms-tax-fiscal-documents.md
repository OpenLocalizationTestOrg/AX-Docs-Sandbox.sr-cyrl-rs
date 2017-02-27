---
title: ICMS tax fiscal documents for Brazil
description: This topic explains the concept of tax fiscal documents and describes the requirements for generating them.
author: ShylaThompson
manager: AnnBe
ms.date: 2017-02-07 19 - 16 - 36
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: TaxFiscalDocument_BR, TaxFiscalDocumentCancel_BR, TaxFiscalDocumentListPage_BR, TaxFiscalDocumentPost_BR
audience: Application User
ms.search.scope: Operations
ms.custom: 269524
ms.assetid: 6960c023-1e50-42b7-82a5-4603dd35fa6d
ms.search.region: Brazil
ms.author: sndray
ms.dyn365.ops.intro: 01-11-2016
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: b97d17ceabfd25c52c5f0c1e96a123bae6941c5a
ms.openlocfilehash: 4c066886a3cd3da2950b85629841da7629cacda5
ms.lasthandoff: 02/22/2017


---

# <a name="icms-tax-fiscal-documents-for-brazil"></a>ICMS tax fiscal documents for Brazil

This topic explains the concept of tax fiscal documents and describes the requirements for generating them.

In Brazil, some types of fiscal documents have no effect on vendors, customers, or inventory balances. In general, the purpose of these fiscal documents is to enable legal entities to enter tax adjustments, transfer between other subsidiaries, or recover taxes (sales tax receivables) in installments for a period. To register these operations in the legal entity, specific fiscal documents must be generated that affect the General ledger and fiscal books reporting.

## <a name="imposto-sobre-circulao-de-mercadorias-e-servios-icms-tax-transfers-between-subsidiaries"></a>Imposto sobre Circulação de Mercadorias e Serviços (ICMS) tax transfers between subsidiaries
This type of tax is considered a recoverable tax and corporate income tax regulations don't allow ICMS tax to be deducted. Therefore, accumulated ICMS tax credits can't be used to decrease the taxable amount for the assessment of corporate income taxes (IRPJ and CSSL). Ways to accumulate ICMS tax credits include:

-   Exportation – ICMS tax–free
-   Deferrals
-   Reduced rate
-   Presumed credits

There are several options for managing how accumulated ICMS tax credits are used when the resulting balance due is greater than the debt accumulated credit. The accumulated ICMS tax credit can be transferred in the following situations:

-   Transfer the ICMS tax credit to other subsidiaries that have a higher volume of transactions where the ICMS is due. This only applies to subsidiaries located in the same state.
-   Transfer the ICMS tax credit to pay vendor accounts in purchase operations for raw and secondary material, equipment packages, and industrial equipment.
-   Transfer the ICMS tax credit to other subsidiaries. Up to the 30 percent of each fixed asset operation that is intended for permanent fixed assets can be transferred.
-   Payment of truck chassis acquisition with new engine, or fuel, made by the establishment of road transport.
-   Transfer the ICMS tax credit from a company that manufactures ethanol to the cooperative company that centralizes sales. Up to 30 percent of the tax that is charged in the shipment of that product can be transferred.
-   Transfer the ICMS tax credit for the industrial establishment of crude oil.

In these situations, the amount that a company that can take from the accumulated ICMS tax depends on specific rules that are established by the government. The amount isn't always applicable to 100 percent of the accumulated ICMS tax amount. ICMS tax credits are transferred by the issuing a fiscal document that is known as a tax fiscal document. This document must include specific information that reflects the operation. The taxpayer can also issue an electronic invoice nota fiscal elêtronica (NF-e) to transfer the accumulated ICMS tax credit to another subsidiary.

## <a name="recovering-icms-tax-in-installments"></a>Recovering ICMS tax in installments
In accordance with Brazilian law No 102/2000, starting January 1, 2001, ICMS tax credits that arise from the purchase of fixed assets that are used specifically in activity that is related to taxation of ICMS can be appropriated 1/48 per month. Therefore, the ICMS tax credit can't be completely recovered when the user records the purchase. Instead, the ICMS tax credit must be recovered in 48 installments over time. Here is an example:

-   Asset acquisition amount : R$ 100.000,00
-   ICMS tax amount: R$ 12.000,00
-   VAT recoverable calculation for the purpose of distribution in the accounts of current assets and long-term receivables:
    -   Current asset:
        1.  R$ 12.000,00 ÷ 48 months = R$ 250,00
        2.  R$ 250,00 × 12 months (1 year) = R$ 3.000,00
    -   Long-term asset:
        1.  R$ 12.000,00 ÷ 48 months = R$ 250,00
        2.  R$ 250,00 × 36 months (1 year) = R$ 9.000,00

In Microsoft Dynamics 365 for Operations, the entries are as follows:

**Purchase of Fixed Asset** **Dynamics 365 for Operations: Receipt Asset Purchase invoice**

**ICMS Tax adjustment of year** **Dynamics 365 for Operations: Manual Journal voucher** **(R$ 12.000,00 / 48 installments) \* 12 (months)**

Recoverable ICMS **long term** (deferred account)

*R$ 12.000,00 D*

Recoverable ICMS **short term** (deferred account)

R$ 3.000,00 D

Fixed Asset

R$ 88.000,00 C

Recoverable ICMS long term (deferred account)

*R$ 3.000,00 C*

**Long term asset** (deferred account) balance: R$ 9.000,00

**ICMS Tax adjustment of month** **Dynamics 365 for Operations: Issue an Incoming Tax fiscal document**

Recoverable ICMS tax account

R$ 250,00 D

Recoverable ICMS short term (deferred account)

*R$ 250,00 C*

On the **All tax fiscal documents** page, you can do the following:

-   Create and post an ICMS tax fiscal document to transfer the ICMS tax amount to a customer or vendor, or to recover the ICMS tax amount in installments for the purchase of fixed assets by a legal entity.
-   Add fiscal document text to an ICMS tax fiscal document.
-   View the voucher transactions that are related to an ICMS tax fiscal document on the **Voucher transactions** page.
-   Cancel a posted ICMS tax fiscal document and generate a canceled voucher transaction. The invoice amount of the canceled voucher transaction is the same as the amount of the original invoice, but the invoice amount is negative.
-   Post the canceled invoice, and view the original and canceled voucher transactions on the **Voucher transactions** page.
-   Print an ICMS tax fiscal document from General ledger. The footer text that is set up on the **Print management setup** page is not printed on ICMS tax fiscal documents.

When a new tax fiscal document is created, the following options are available:

-   ICMS tax transfer
-   ICMS installment to appropriate the credit of fixes assets (CIAP)

## <a name="prerequisites"></a>Prerequisites
The following prerequisites must be set up before you can create and post tax fiscal documents. The parameters determine how the data will be shown on the fiscal documents, and all of them are required. Missing parameters can cause inconsistencies or incorrect validations during the posting process.

-   **Brazilian parameters:** Define the item, and the **PIS** and **COFINS** sales tax codes that are used for these types of fiscal documents.
-   **Ledger posting groups in General ledger**: Define the **Sales tax receivable short terms** ledger account.

## <a name="example"></a>Example
**Outgoing fiscal documents**

-   Outgoing fiscal document to transfer the ICMS tax credit for other legal entities, subsidiary/branch of same company/organization destined for compensation of the debt balance of the ICMS (CFOP: 5.601 and 5.602)

**Incoming fiscal documents**

-   Incoming fiscal documents to transfer the ICMS tax credit from other legal entities, subsidiaries/branches of same company/organization destined for compensation of the debt balance of the ICMS (CFOP:1.601 and 1.602)
-   Incoming fiscal documents to appropriate 1/48 of the ICMS credit (CFOP:1.604) (CIAP)



