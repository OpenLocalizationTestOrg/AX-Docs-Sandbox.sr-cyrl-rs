---
title: Import payment formats for Sweden
description: This topic provides information about the BankGirot MAX, BankGirot OCR import, and BankGirot return formats for Sweden.
author: ShylaThompson
manager: AnnBe
ms.date: 2016-12-12 22 - 14 - 51
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustPaymMode, CustVendPaymReconciliation, LedgerJournalTransCustPaym, VendPaymMode
audience: Application User
ms.search.scope: Operations
ms.custom: 262684
ms.assetid: 7632f01a-28b6-408f-8734-b03416c6fb81
ms.search.region: Sweden
ms.author: v-lenest
ms.dyn365.ops.intro: 01-11-2016
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: b97d17ceabfd25c52c5f0c1e96a123bae6941c5a
ms.openlocfilehash: c3f4f0f14dba962557ae2336af4a4e1fcca8549e
ms.lasthandoff: 02/22/2017


---

# <a name="import-payment-formats-for-sweden"></a>Import payment formats for Sweden

This topic provides information about the BankGirot MAX, BankGirot OCR import, and BankGirot return formats for Sweden.

<a name="bankgirot-max-bankgirot-ocr"></a>BankGirot MAX, BankGirot OCR
----------------------------

BankGirot MAX and BankGirot OCR file import lets you import customer payments in BankGirot file formats. BG MAX is a file layout that collects all payments in one file. OCR is a specific kind of reference in the BG MAX file format with a payment reference. To import payments, complete the following steps.

1.  Go to the **Payment journal** page.
2.  Click **Lines**.
3.  Click **Functions** &gt; **Import payments**.
4.  In the dialog box, select the method of payment, and then browse to the location of the file to import. **Note**: Before you can complete this step, you must have already imported the configurations from Lifecycle Services (LCS) and set up the methods of payment. For more information, see [File formats for method of payments](select-file-formats-for-the-method-of-payments.md).

After you import the payment file, payment journal lines should be created for the selected journal and marked for settlement with customer invoices.

## <a name="bankgirot-autogiro-returns"></a>Bankgirot Autogiro returns
Bankgirot Autogiro returns format for the direct debit payment format of the same name. These messages can be imported as a response to direct debit messages that were previously exported. Currently, these payments are represented in Operations as payment journal lines with a **Sent** status. To import a file, complete the following steps.

1.  Go to the **Payment transfers** page.
2.  Click **Return file-customer**.
3.  In the dialog box, select corresponding method of payment, and then browse to the location of the file to import. **Note**: Before you can complete this step, you must have already imported the configurations from Lifecycle Services (LCS) and set up the methods of payment. For more information, see [File formats for method of payments](select-file-formats-for-the-method-of-payments.md).

After you import the return file, the payments should be updated to the status **Approved**.


