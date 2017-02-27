---
title: OIOUBL standards for electronic invoicing
description: This topic explains what level of coverage we have for electronic invoicing in Microsoft Dynamics 365 for Operations in the European region.
author: ShylaThompson
manager: AnnBe
ms.date: 2015-10-19 23 - 02 - 38
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations
ms.custom: 10274
ms.assetid: 3f2a14b0-6580-40e4-a3dc-1d8a0f9201c1
ms.search.region: Austria, Denmark, Italy, Norway, Spain
ms.search.industry: Public sector
ms.author: mrolecki
ms.dyn365.ops.intro: 01-02-2016
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b97d17ceabfd25c52c5f0c1e96a123bae6941c5a
ms.openlocfilehash: 998e9dd164a39cc0b22c94d811abbe0aa464d47c
ms.lasthandoff: 02/22/2017


---

# <a name="oioubl-standards-for-electronic-invoicing"></a>OIOUBL standards for electronic invoicing

This topic explains what level of coverage we have for electronic invoicing in Microsoft Dynamics 365 for Operations in the European region. 

The [European Commission](http://ec.europa.eu/finance/payments/einvoicing/index_en.htm) describes electronic reporting network in following terms: “Electronic invoicing – e-invoicing – is electronic transfer of invoicing information (billing and payment) between business partners (supplier and buyer). It is an essential part of an efficient financial supply chain and it links the internal processes of enterprises to the payment systems." Implementation and adoption of European Union wide electronic invoicing is regulated [Council Directive 2010/45/EU](http://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2010:189:0001:0008:EN:PDF), which affects all EU member states. Companies willing to take benefit from electronic invoicing must submit sales order invoices, free text invoices, project invoices, sales order credit notes, and project invoice credit notes as .xml files to the government or other trading parties that mandate use of electronic invoicing. These .xml files must comply with certain standards. The country-specific requirements and their implementation may differ across EU member states but commonly they are using Universal Business Language ([UBL](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=ubl)) in different versions with customizations as well as [PEPPOL](http://www.peppol.eu/peppol_elements/einvoicing)specifications and access points for validation and transportation. The primary advantage of UBL is that business documents can be standardized for different purposes. Because UBL is a flexible, international standard that supports many business requirements, these business documents can be exchanged across national borders.
What electronic invoice formats are currently supported in Dynamics 365 for Operations?
---------------------------------------------------------------------------------------

Dynamics 365 for Operations (1611) offers implementation of electronic invoicing based on [electronic reporting](general-electronic-reporting-ger-2.md). There is a **Customer invoice model** data model and a number of country-specific electronic reporting format configurations created for Austria, Denmark, Italy, Norway and Spain:
-   OIOUBL Sales & Project invoice (AT, DK, NO)
-   OIOUBL Sales & Project credit note (AT, DK, NO)
-   Sales & Project invoice (ES)
-   Sales & Project invoice (IT)

The electronic invoices and credit notes that you generate include required information, such as a European Article Numbering (EAN) number, contact person, dimension account number, and address information for the customer. In Microsoft Dynamics 365 for Operations, validation rules are applied when invoices are generated so you can verify that the correct information has been entered. The set of required information may differ from country to country. As the requirements as well as supported countries and formats is subject to change, you should always go to the Shared asset library on Microsoft Dynamics Lifecycle services (LCS) and view the most up-to-date list of available files that have an asset type of **GER configuration**.



<a name="see-also"></a>See also
--------

[Set up OIOUBL electronic invoicing](http://ax.help.dynamics.com/en/wiki/set-up-oioubl-electronic-invoicing/)

[Import OIOUBL electronic invoicing configurations](http://ax.help.dynamics.com/en/wiki/import-oioubl-electronic-invoicing-configurations/)

[Set up customer accounts for OIOUBL electronic invoicing](http://ax.help.dynamics.com/en/wiki/set-up-customer-accounts-for-oioubl-electronic-invoicing/)


