---
title: VAT statement details for Latvia
description: This topic explains how to set up the VAT statement for legal entities in Latvia.
author: ShylaThompson
manager: AnnBe
ms.date: 2017-01-11 13 - 48 - 17
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: TaxAuthority, TaxReportCollection, TaxReportVoucher, TaxTable
audience: Application User
ms.search.scope: Operations
ms.custom: 266864
ms.assetid: 40104afc-cbce-4f03-9318-7d0599bb1323
ms.search.region: Latvia
ms.author: v-elgolu
ms.dyn365.ops.intro: 01-11-2016
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: b97d17ceabfd25c52c5f0c1e96a123bae6941c5a
ms.openlocfilehash: d3f5bdabf07fc8ba791225a1999f90b88f196bc2
ms.lasthandoff: 02/22/2017


---

# <a name="vat-statement-details-for-latvia"></a>VAT statement details for Latvia

This topic explains how to set up the VAT statement for legal entities in Latvia.

This topic includes country/region-specific information about the setup of the value-added tax (VAT) statement for legal entities in Latvia only. For more information about the implementation of VAT statements, see [(EU) VAT reporting](eu-vat-reporting.md).

## <a name="set-up-sales-tax-authorities"></a>Set up sales tax authorities
To generate a VAT declaration in the required format for the appropriate tax authority, you must set up the report layout for sales tax authorities. On the **Sales tax authorities** page, set the **Report layout** field to **Default**. Select the same sales tax authority for the sales tax settlement period that will be used for the sales tax codes.

## <a name="set-up-sales-tax-reporting-codes"></a>Set up sales tax reporting codes
Here is an example that shows how you might set up sales tax reporting codes on the **Report setup** FastTab of the **Sales tax codes** page to generate a VAT statement.

| Sales tax reporting code | Description (English)                                                                    | Description                                                                              | XML tag name |
|--------------------------|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|--------------|
| 41                       | Standard rate tax amount                                                                 | Ar standartlikmi apliekamie darījumi                                                     | R41          |
| 411                      | Domestic transactions for which the recipient of the goods or services pays the tax      | Iekšzemē veiktie darījumi, par kuriem nodokli maksā preču vai pakalpojumu saņēmējs       | R411         |
| 42                       | Reduced rate tax amount                                                                  | Ar samazināto likmi apliekamie darījumi                                                  | R42          |
| 45                       | Goods that are delivered to European Union (EU) member states                            | Uz ES dalībvalstīm piegādātās preces                                                     | R45          |
| 46                       | Amount of custom sales in stock                                                          | Ārpuskopienas preču piegādes muitas noliktavās un brīvajās zonās                         | R46          |
| 47                       | New vehicles delivered to EU countries                                                   | Uz ES dalībvalstīm piegādātie jaunie transportlīdzekļi                                   | R47          |
| 48                       | Provided services                                                                        | Par sniegtajiem pakalpojumiem                                                            | R48          |
| 481                      | Export goods                                                                             | Eksportētās preces                                                                       | R48\_1       |
| 482                      | The transactions other countries                                                         | Citās valstīs veiktie darījumi                                                           | R48\_2       |
| 49                       | Not taxable transactions                                                                 | Ar PVN neapliekamie darījumi                                                             | R49          |
| 50                       | Goods and services that are received from EU member states(standard rate)                | No ES dalībvalstīm saņemtās preces un pakalpojumi (standartlikme)                        | R50          |
| 51                       | Goods and services that are received from EU member states (reduced rate)                | No ES dalībvalstīm saņemtās preces (samazinātā likme)                                    | R51          |
| 54                       | Received services                                                                        | Par saņemtajiem pakalpojumiem                                                            | R54          |
| 61                       | Imported goods for the company's economic activities                                     | Par importētajām precēm                                                                  | R61          |
| 62                       | Domestic goods and services for the company's economic activities                        | Par precēm un pakalpojumiem iekšzemē                                                     | R62          |
| 63                       | Calculated tax prepayment                                                                | Aprēķinātā PVN summa saskaņā ar likuma 92.panta pirmās daļas 4.punktu (izņemot 64.rindu) | R63          |
| 64                       | Calculated tax prepayment for goods and services that are received from EU member states | Aprēķinātā PVN summa par precēm un pakalpojumiem, kas saņemti no ES dalībvalstīm         | R64          |
| 65                       | The compensation paid to farmers                                                         | Lauksaimniekiem izmaksātā kompensācija                                                   | R65          |
| 66                       | Not payable tax prepayment                                                               | PVN summa, kas nav atskaitāma kā priekšnodoklis                                          | R66          |
| 67                       | Tax amount reduction calculated for previous tax periods                                 | Iepriekšējos taksācijas periodos samaksai valsts budžetā aprēķinātā nodokļa samazinājums | R67          |
| 57                       | Calculated prepayment tax amount reduction for previous tax periods                      | Iepriekšējos taksācijas periodos atskaitītā priekšnodokļa samazinājums                   | R57          |

## <a name="configure-the-electronic-reporting-model-and-format-for-the-report"></a>Configure the Electronic reporting model and format for the report
To review or change the VAT statement configuration, on the **Reporting configurations** page, select **VAT declaration model** in the list of models. Then click **Designer** to review or change the model. To review or change the VAT statement format, on the **Reporting configurations** page, select **VAT declaration (LV)**, and then click **Designer**.

## <a name="generate-a-vat-statement"></a>Generate a VAT statement
To generate a VAT XML file, on the **Sales tax payments** page, select one or more vouchers, and then click **Export VAT XML file**.


