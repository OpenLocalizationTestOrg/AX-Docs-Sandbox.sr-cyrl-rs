---
title: Packing slip date verification on invoices for Italy
description: For Italy, the invoice date is verified on packing slips and invoice proposals. This topic provides additional information about the verification that occurs.
author: ShylaThompson
manager: AnnBe
ms.date: 2016-12-14 22 - 43 - 22
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations
ms.custom: 263824
ms.assetid: 5fd63f5d-f6b1-48f2-962b-26360a7072a2
ms.search.region: Italy
ms.author: v-elgolu
ms.dyn365.ops.intro: 01-11-2016
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: b97d17ceabfd25c52c5f0c1e96a123bae6941c5a
ms.openlocfilehash: c585a3b7293082bcb1fa92d5b23dabfc20a271a0
ms.lasthandoff: 02/22/2017


---

# <a name="packing-slip-date-verification-on-invoices-for-italy"></a>Packing slip date verification on invoices for Italy

For Italy, the invoice date is verified on packing slips and invoice proposals. This topic provides additional information about the verification that occurs. 

For legal entities with primary addresses in Italy there is a packing slip date verification step for users who generate sales invoices or project invoices.

-   Packing slips that are dated later than the invoice are not be included in the suggested update quantity.
-   For project management and accounting, when you create an invoice proposal, only the customer packing slips that are dated earlier than the invoice proposal are included in the proposal. **Note**: If the user input date for the invoice proposal is empty, the system date is used.



