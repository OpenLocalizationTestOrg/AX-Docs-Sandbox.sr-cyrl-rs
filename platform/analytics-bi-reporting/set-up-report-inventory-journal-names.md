---
title: Inventory journal reports
description: When you use configurable inventory reports based on electronic reporting, you need to set up a relationship between a specific report and a journal type.
author: ShylaThompson
manager: AnnBe
ms.date: 2016-12-22 15 - 24 - 32
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventJournalName
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 265144
ms.assetid: 0f07f62f-1053-46e9-b235-a7b38cbda409
ms.search.region: Estonia, Hungary, Latvia, Lithuania, Poland
ms.author: v-lenest
ms.dyn365.ops.intro: 01-11-2016
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: b97d17ceabfd25c52c5f0c1e96a123bae6941c5a
ms.openlocfilehash: 976d29c9fb4da450b3a34af549a00058a9cd984c
ms.lasthandoff: 02/22/2017


---

# <a name="inventory-journal-reports"></a>Inventory journal reports

When you use configurable inventory reports based on electronic reporting, you need to set up a relationship between a specific report and a journal type.

To set up a relationship between a specific report and a journal type, on the **Inventory journal names** page (**Inventory management** &gt; **Setup** &gt; **Journal names** &gt; **Inventory**), enter a name for the report. **Note:** To set up supported configurations, download the required electronic reporting configurations. For more information, see [Download Electronic reporting configurations from Lifecycle Services](download-electronic-reporting-configuration-lcs.md). Examples of inventory reports with supported configurations in Europe are listed in the following table.
|                    |                                     |                  |                                         |
|--------------------|-------------------------------------|------------------|-----------------------------------------|
| **Country**        | **Report description**              | **Journal type** | **Format mapping name**                 |
| Lithuania, Hungary | Inventory statement report          | Counting         | Inventory statement (HU, LT)            |
| Latvia, Poland     | Inventory reclassification document | Transfer         | InventoryReclassificationDocument\_PLLV |
| Estonia            | Inventory reclassification document | Transfer         | InventoryReclassificationDocument\_EE   |
| Poland             | Internal PW/RW                      | Movement         | InventJournalLinesDocPL                 |
| Latvia             | Inventory movement document         | Movement         | Movement\_LV                            |
| Latvia             | Inventory write-down document       | Adjustment       | InventJournalLines\_LV                  |
| Latvia             | Transfer delivery note              | Transfer         | InternalTransferDeliveryNote\_LV        |
| Latvia             | Counting document report            | Counting         | CountedDocument\_LV                     |
| Latvia             | Counting list report                | Counting         | Counting list                           |




