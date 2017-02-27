---
title: VAT statements details for Italy
description: This topic explains how to set up a VAT statement for legal entities in Italy.
author: ShylaThompson
manager: AnnBe
ms.date: 2017-02-07 20 - 05 - 56
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations
ms.custom: 269664
ms.assetid: af07d122-5694-4de6-96bf-7bf5478b0175
ms.search.region: Italy
ms.author: sndray
ms.dyn365.ops.intro: 01-11-2016
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: b97d17ceabfd25c52c5f0c1e96a123bae6941c5a
ms.openlocfilehash: 34f68fa9daa5a9a12bd06f90fbf68842cb3e025f
ms.lasthandoff: 02/22/2017


---

# <a name="vat-statements-details-for-italy"></a>VAT statements details for Italy

This topic explains how to set up a VAT statement for legal entities in Italy. 

<a name="set-up-customervendor-tax-information-for-tax-reports"></a>Set up customer/vendor tax information for tax reports
------------------------------------------------------

To generate the sales tax report, the customer and vendor must be configured with the fiscal information for Italy. On the **Customers** page, select the fields in the following table.

#### <a name="invoice-and-delivery"></a>Invoice and delivery

| **Field**             | **Description**                                        |
|-----------------------|--------------------------------------------------------|
| **Tax exempt number** | Enter the tax exempt number for VAT declaration.       |
| **Fiscal code**       | Enter the fiscal code for this customer.               |
| **Sales tax Group**   | Select a sales tax group to be used for this customer. |

On the **Vendors** page, select the fields in the following table.

#### <a name="invoice-and-delivery"></a>Invoice and delivery

| **Field**             | **Description**                                      |
|-----------------------|------------------------------------------------------|
| **Tax exempt number** | Enter the tax exempt number for VAT declaration.     |
| **Fiscal code**       | Enter the fiscal code for this vendor.               |
| **Sales tax Group**   | Select a sales tax group to be used for this vendor. |

## <a name="set-up-a-company-fiscal-code-and-tax-registration-number"></a>Set up a company fiscal code and tax registration number
To generate reports, the company fiscal code and registration number should be set up on the **Legal entity** page. On the **Legal entity** page, select the fields in the following table.

#### <a name="registration-numbers"></a>Registration numbers

| **Field**        | **Description**                                                    |
|------------------|--------------------------------------------------------------------|
| **Fiscal Code**  | Enter the fiscal code from the legal entity registration in Italy. |
| **Legal Nature** | Enter the legal structure of the company.                          |
| **CUC**          | Enter the CUC code.                                                |

#### <a name="tax-registration"></a>Tax registration

| **Field**               | **Description**                                                 |
|-------------------------|-----------------------------------------------------------------|
| Tax registration number | Enter the tax registration number for the legal entity in Italy |

#### <a name="set-up-parameters-for-italian-sales-tax-book"></a>Set up parameters for Italian sales tax book

On the **Sales tax** page, create sales tax books to be reported to the Italian government after the settlement period is past.

| **Field**                     | **Description**                                 |
|-------------------------------|-------------------------------------------------|
| **Sales tax book type**       | Enter the movement direction. (Sales/Purchase)  |
| **Sales tax book**            | Enter the identifier of the sales tax book.     |
| **Name**                      | Enter the name of the sales tax book.           |
| **Sales tax book type**       | Enter the movement direction. (Sales/Purchase)  |
| **Settlement period**         | The period for this tax book.                   |
| **Closed to**                 | Select the transaction date.                    |
| **EU sales**                  | The amount sold to the European Union.          |
| **ATECOFIN**                  | The tax code for sales tax reporting.           |
| **Print summary and payment** | Select to print the summary and payment report. |

## <a name="yearly-tax-communication-report"></a>Yearly tax communication report
After the year end, generate the report for each settlement period. The transmission is mandatory as required by the Italian fiscal authority via a website. On the **Yearly tax communication** page, it is possible to create or view a report.

#### <a name="overview"></a>Overview

| **Field**                | **Description**                                                                               |
|--------------------------|-----------------------------------------------------------------------------------------------|
| **Tax communication ID** | Enter the identification number of the Yearly tax communication report.                       |
| **Years**                | Enter the year of the tax communication.                                                      |
| **ATECOFIN Code**        | Enter the tax code that is associated with the classification of possible company activities. |
| **Exported**             | Indicates that the .ivc file is exported.                                                     |

#### <a name="general"></a>General

| **Field**                | **Description**                                                                               |
|--------------------------|-----------------------------------------------------------------------------------------------|
| **Tax communication ID** | Enter the identification number of the Yearly tax communication report.                       |
| **Years**                | Enter the year of the tax communication.                                                      |
| **ATECOFIN Code**        | Enter the tax code that is associated with the classification of possible company activities. |
| **Exported**             | Indicates that the file was exported.                                                         |
| **Date of export**       | The date when the .ivc file was exported.                                                     |
| **Export file name**     | The name of the .ivc file.                                                                    |

## <a name="vat-summary-report"></a>VAT summary report
For VAT reporting, Italy has specific information to be reported and formatted. In the **Sales tax authorities** page, on **Tax setup**, configure the Italian authority.

| **Field**                                 | **Description**                                                                                |
|-------------------------------------------|------------------------------------------------------------------------------------------------|
| **Report layout**                         | Select the Italian report to enable Italian fields.                                            |
| **Print blank page with no transactions** | Select to print blank pages when no transactions are present.                                  |
| **Separate summary register**             | Select this check box to use a separate value added tax (VAT) book to number summary sections. |
| **Account gain**                          | Gain due to rounding.                                                                          |
| **Account loss**                          | Loss due to rounding.                                                                          |

## <a name="sales-tax-settlement-periods"></a>Sales tax settlement periods
Per Italian legislation, rules apply to settlement periods. For example, after the settlement period is closed, no change is allowed. You are required to report if the settlement refers to the last period on the fiscal year. View the settlement period status and report if it refers to a year closing. On the **Sales tax settlement period** page &gt; **Period Intervals** tab, select the following fields.

| **Field**       | **Description**                                                                                   |
|-----------------|---------------------------------------------------------------------------------------------------|
| **Closed**      | Indicates if the Italian sales tax book for the period has been updated and automatically closed. |
| **Last period** | Select this option if the period is the last period in a sales tax year.                          |




