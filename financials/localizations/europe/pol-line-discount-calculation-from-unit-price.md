---
title: Line discount calculation from the unit price for Poland
description: For legal entities in Poland, the line discount can be calculated from the unit price of an invoice line instead of from a line amount. This topic provides information about the Line discount calculation from unit price method and explains how to set it up.
author: ShylaThompson
manager: AnnBe
ms.date: 2016-12-14 15 - 46 - 37
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations
ms.custom: 263424
ms.assetid: d0645f8d-05a4-4212-b6de-975a625b1fe0
ms.search.region: Poland
ms.author: v-elgolu
ms.dyn365.ops.intro: 01-11-2016
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: b97d17ceabfd25c52c5f0c1e96a123bae6941c5a
ms.openlocfilehash: 492269980589b4e6e54aa51e683bc0b7c4656d22
ms.lasthandoff: 02/22/2017


---

# <a name="line-discount-calculation-from-the-unit-price-for-poland"></a>Line discount calculation from the unit price for Poland

For legal entities in Poland, the line discount can be calculated from the unit price of an invoice line instead of from a line amount. This topic provides information about the Line discount calculation from unit price method and explains how to set it up.

For legal entities in Poland, the line discount doesn't have to be calculated from a line amount. Instead, it can be calculated from the unit price of an invoice line. When the Line discount calculation from unit price method is used, the discounted unit price is rounded before the line amount is calculated. The following table shows how the line discount is calculated by both the standard method and the Line discount calculation from unit price method.

Quantity

Price

Discount percentage

Net amount

Standard method

Line discount calculation from unit price method

100

6.75

5

641.25 (6.75 × 100 = 675.00; 675 × 0.95 = 641.25)

641.00 (6.75 × 0.95 = 6.4125; 6.41 × 100 = 641.00)

**Note:** The 0.95 that is used in the calculations equals 1.00 – 0.05, where 0.05 is the discount amount if the unit price is 1.00.

## <a name="set-up-the-calculation-of-line-discount-parameter"></a>Set up the Calculation of line discount parameter
The Line discount calculation from unit price method affects both Accounts receivable and Accounts payable, and is set up on the **Accounts receivable parameters** page and the **Procurement and sourcing parameters** page. The **Calculation of line discount** parameter has the following options:

-   **From line value** – Use the standard method to calculate the line discount.
-   **From unit price** – Use the Line discount calculation from unit price method to calculate the line discount.

The **Calculation of line discount** parameter affects the following documents:

-   Sales orders
-   Purchase orders
-   Vendor invoices



