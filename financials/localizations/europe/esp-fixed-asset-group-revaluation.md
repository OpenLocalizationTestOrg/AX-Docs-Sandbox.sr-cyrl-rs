---
title: Fixed asset revaluation groups | Microsoft Docs
description: This topic provides information about fixed asset revaluation groups for Spain.
author: ShylaThompson
manager: AnnBe
ms.date: 2016-12-21 01:45:01
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: 81
ms.suite: Released- Dynamics 365 for Operations version 1611
ms.custom: 264994
ms.assetid: 2bf1a59b-a74f-4e50-8aad-43f0677ed040
ms.region: Spain
ms.author: epopov
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: b2a4b0298525036f0007156b5631fcced9a5430d


---

# <a name="fixed-asset-revaluation-groups"></a>Fixed asset revaluation groups

This topic provides information about fixed asset revaluation groups for Spain.

Revaluation groups are used to set up revaluation conditions for the fixed asset. For example, the revaluation group could be a factor or revaluation date. Value from the revaluation group will be used in the fixed asset journal for revaluation proposals and for individual value adjustments of revaluation transactions. To revaluate a fixed asset, you must specify the revaluation group on the **Books** page. Value from the revaluation group will be used in the fixed asset journal for revaluation proposals and for individual value adjustments of revaluation transactions.

## <a name="revaluation-group-setup"></a>Revaluation group setup
You can set up a revaluation group in the **Revaluation groups** page. In the upper pane, create an identifier for the revaluation group. In the lower pane, enter the date of the revaluation and the factor that the value will increase or decrease by.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Field</strong></td>
<td><strong>Description</strong></td>
</tr>
<tr class="even">
<td><strong>Revaluation group</strong></td>
<td>Enter the identification of the revaluation group. For fixed assets that will be set up for revaluation, a revaluation group must be allocated to the fixed asset per value model.</td>
</tr>
<tr class="odd">
<td><strong>Description</strong></td>
<td>Enter the description of the revaluation group that describes the purpose of each group.</td>
</tr>
<tr class="even">
<td><strong>Date</strong></td>
<td>Enter the date from which the revaluation factor is valid.</td>
</tr>
<tr class="odd">
<td><strong>Factor</strong></td>
<td>Enter the factor and the acquisition price that determines the revaluation proposal for the fixed asset. For example, suppose the acquisition amount was 100,000. Using the equation <em>Acquisition amount - (Acquisition amount * factor),</em> the following table displays the result of different factors.
<table>
<tbody>
<tr class="odd">
<td><strong>Factor</strong></td>
<td><strong>Formula</strong></td>
<td><strong>Transaction</strong></td>
</tr>
<tr class="even">
<td>1</td>
<td>100,000 - (100,000 * 1)</td>
<td>No transaction</td>
</tr>
<tr class="odd">
<td>10</td>
<td>100,000 - (100,000 * 10)</td>
<td>900,000 Debit</td>
</tr>
<tr class="even">
<td>0.5</td>
<td>100,000 - (100,000 * 0.5)</td>
<td>50,000 Credit</td>
</tr>
</tbody>
</table></td>
</tr>
</tbody>
</table>






<!--HONumber=Feb17_HO3-->


