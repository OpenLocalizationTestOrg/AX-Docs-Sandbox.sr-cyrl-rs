---
title: Italian black list report | Microsoft Docs
description: Learn how to set up and maintain the Italian black list report.
author: ShylaThompson
manager: AnnBe
ms.date: 2016-12-02 21:05:52
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: 81
ms.suite: Released- Dynamics 365 for Operations version 1611
ms.custom: 261414
ms.assetid: 0bcb48ad-460d-4fb4-abd2-8a89685404e3
ms.region: Italy
ms.author: epopov
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: db4c1cd13e4f70bddc8886209e3c8b76f53b51f0


---

# <a name="italian-black-list-report"></a>Italian black list report

Learn how to set up and maintain the Italian black list report.

The Italian black list report provides a list of taxable transactions with companies in countries that have privileged tax structures. These countries are referred to as “black listed” by the Italian government and present a high risk from a tax perspective. This report must be submitted to Italian sales tax authorities and is typically used by accountants, collections managers, accounts receivable clerks, accounts receivable managers, sales managers, and sales clerks. You must set up a few things before you can generate the **Italian black list** report and export it in the required format.

-   Select a number sequence for the **Black list report ID** number sequence reference on the **Foreign trade parameters** page.
-   Set up the report format mapping for the **Black list** report by specifying references to electronic reporting configurations on the **Black list** on the **Foreign trade parameters** page.
-   Set up a country or region as "black listed".
-   Set up the legal nature of a legal entity.
-   Set up the country/region of residence for a foreign customer/vendor.
-   Set up the VAT type for a sales tax code.

## <a name="set-up-a-country-or-region-as-black-listed"></a>Set up a country or region as "black listed"
Use tab **Country/region properties** on the **Foreign trade parameters** page to identify a country as “black listed”:

-   In the **IT three-digit code** field, set the numeric country code as mentioned in the report instructions from the Italian government.
-   Select the **Black listed country/region** check box.

Use the **County** tab on the **Address setup** page in the Global address book to specify the **Italian county code**.

## <a name="set-up-the-legal-nature-of-a-legal-entity"></a>Set up the legal nature of a legal entity
Use the **Registration numbers** section on the **Legal entities** page to specify the fiscal code and the legal nature of a legal entity. The legal nature is the legal structure that is registered with the government, such as **Limited share partnerships**, **Limited liability companies (SRL)**, or **Public limited companies (SPA)**.

## <a name="set-up-the-countryregion-of-residence-for-a-foreign-customervendor"></a>Set up the country/region of residence for a foreign customer/vendor
Use the **Sales demographics** section on the **Customers/Vendors** pages to set up the country/region of residence for a customer in a foreign country/region and to specify information about primary contact, such as primary contact, birth place, and birth county. Only the invoice transactions with legal entities in countries that have privileged tax structures (“black listed” countries) are included in the **Italian black list** report. If the customer is also a vendor, the sales and purchase transactions are summarized as one record in the **Italian black list** report.

## <a name="set-up-the-vat-type-for-a-sales-tax-code"></a>Set up the VAT type for a sales tax code
Use the **Sales tax codes** (**Tax** &gt; **Indirect taxes** &gt; **Sales tax**) page to set up the type of tax to be calculated for the **Italian black list** report. The VAT type that is specified determines the category where the net and VAT amounts for the invoices are printed on the report and where they are located in the file. If the total net or VAT amount that is invoiced in a period is negative for a specific VAT type, it appears as credit for the previous period (or previous year, if the period starts in January). Use the following procedure to generate a report. You can also view and update the transactions before you generate the report.

## <a name="generate-the-italian-black-list-report"></a>Generate the Italian black list report
Use the **Italian black list report** page to create a new report and transfer transactions to the **Italian black list** report:

-   Specify the information in the **General** section.
-   Use **Transfer** to transfer the customer and vendor invoice transactions to the **Transactions** section based on the criteria that are specified in the **General** section. Only transactions that are associated with a sales tax code are displayed on the report. Verify the transactions and make changes, if required.
-   Use **Apply threshold** to exclude invoices from the **Italian black list** report that are below the threshold amount that is specified in the **Threshold amount** field in the **General** section.
-   Use **Report** to generate and export the report as a file.





<!--HONumber=Feb17_HO3-->


