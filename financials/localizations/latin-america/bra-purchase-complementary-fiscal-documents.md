---
title: Purchase complementary fiscal documents for Brazil
description: This topic describes the concept of a purchase complementary invoice for the Brazilian localization.
author: ShylaThompson
manager: AnnBe
ms.date: 2017-02-03 16 - 41 - 21
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BrazilParameters, FBFiscalDocument_BR, PurchComplementaryInvoice, PurchComplementaryInvoiceCancel_BR, PurchComplementaryInvoiceListPage
audience: Application User
ms.search.scope: Operations
ms.custom: 269154
ms.assetid: efff5c06-3ad6-45df-97d9-d714614c4e95
ms.search.region: Brazil
ms.author: sndray
ms.dyn365.ops.intro: 01-11-2016
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: b97d17ceabfd25c52c5f0c1e96a123bae6941c5a
ms.openlocfilehash: 64238e0a35f8225772e192a76f81062ec7c7ca23
ms.lasthandoff: 02/22/2017


---

# <a name="purchase-complementary-fiscal-documents-for-brazil"></a>Purchase complementary fiscal documents for Brazil

This topic describes the concept of a purchase complementary invoice for the Brazilian localization.

<a name="overview"></a>Overview
--------

According to the fiscal regulations in Brazil, a specific fiscal document that is known as a complementary invoice (Nota fiscal complementar) is issued or received for correction purposes. For example, if the prices of goods or services from the original invoice were incorrectly registered, a complementary invoice is required in order to fix the error. Complementary invoices are applicable only if the difference is positive. In other words, they are applicable only if the current prices or taxes amounts are more than original prices or taxes amounts. Because fiscal invoices of this type are considered complements of the original invoices, the original invoices don’t have to be canceled. Companies are obligated to issue or receive complementary invoices for the following reasons:

-   Error in the price of the goods or services
-   Error in the quantity of goods or services
-   Error in the tax percentage
-   Error in the tax calculation

## <a name="purchase-complementary-fiscal-document"></a>Purchase complementary fiscal document
You can create a purchase complementary fiscal document to adjust a purchase fiscal document that was generated for an incorrect price, an incorrect Imposto sobre Produtos Industrializados (IPI) amount, or an incorrect Imposto sobre Circulação de Mercadorias e Serviços (ICMS) amount. A purchase complementary fiscal document is issued only to adjust a positive difference. For example, a purchase complementary fiscal document is generated if the price of an item on the original purchase fiscal document is incorrect, and if the correct price for the item is more than the price that is recorded on the original purchase fiscal document. You can create a purchase complementary fiscal document to adjust an error in the price or quantity of items or services, the tax percentage, or the tax calculation. The purchase complementary fiscal document is a purchase fiscal document that complements the original purchase fiscal document. All information, except information about charges, is updated from the original purchase fiscal document. You can't add lines to or delete lines from a purchase complementary fiscal document. The following types of purchase complementary fiscal documents are available:

-   **Price** – This type of complementary fiscal document is created to adjust an incorrect price for a fiscal document. The correct price must be more than the price that is recorded on the original fiscal document. The price difference is charged to the vendor.
-   **IPI** – This type of complementary fiscal document is created to adjust an incorrect IPI tax amount for a fiscal document. The IPI tax difference is charged to the vendor.
-   **ICMS** – This type of complementary fiscal document is created to adjust an incorrect ICMS tax amount for a fiscal document. The ICMS tax difference is received by the legal entity and paid to the tax authorities.

You can create an ICMS complementary fiscal document only if the tax groups that you select for the purchase complementary fiscal document include ICMS tax codes. Likewise, you can create an IPI complementary fiscal document only if the tax groups that you select for the purchase complementary fiscal document include IPI tax codes. For example, if you create an IPI complementary fiscal document, but the existing tax groups don't have the IPI tax type, you must select a tax group that has an IPI tax code. You can cancel and inquire about a purchase complementary fiscal document that has been posted on the **All purchase complementary fiscal documents** page.

## <a name="prerequisites"></a>Prerequisites
Before you can create and post purchase complementary fiscal document, the following parameters must be configured on the **Brazilian parameters** page:

-   **Complementary fiscal document** – Specify the default fiscal document source text.
-   **Sales tax code for COFINS** – Specify the sales tax code that is used for the COFINS tax calculation amount.
-   **Sales tax code for PIS** – Specify the sales tax code that is used for the PIS tax calculation amount.

## <a name="examples"></a>Examples
[![Example that shows an original invoice together with purchase complementary fiscal documents of each of the three types](./media/purchcomplementary-1024x349.png)](./media/purchcomplementary.png)


