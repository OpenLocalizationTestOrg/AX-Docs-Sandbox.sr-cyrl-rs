---
title: Budget analysis in the public sector
description: This topic describes how to use the Budget analysis page to view revenues and expenditures by financial dimension, and it answers frequently asked questions, including differences between the Budget analysis page and the Budget control statistics page.
author: rschloma
manager: AnnBe
ms.date: 2015-12-07 16 - 23 - 04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BudgetAnalysisInquiry_PSN, BudgetControlStatistics, DimensionDetails, LedgerPeriodCode, LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: rschloma
ms.search.scope: AX 7.0.0, Operations
ms.custom: 19641
ms.assetid: a1055712-0a20-425d-939d-de8564c358b8
ms.search.region: Global
ms.search.industry: Public sector
ms.author: brpotter
ms.dyn365.ops.intro: 01-02-2016
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b97d17ceabfd25c52c5f0c1e96a123bae6941c5a
ms.openlocfilehash: 62995086f66c3fce451f6b6a7a848b10fcafcac9
ms.lasthandoff: 02/22/2017


---

# <a name="budget-analysis-in-the-public-sector"></a>Budget analysis in the public sector

This topic describes how to use the Budget analysis page to view revenues and expenditures by financial dimension, and it answers frequently asked questions, including differences between the Budget analysis page and the Budget control statistics page. 

This topic describes the budget analysis functionality available for the public sector. Before you read this topic, you should also read [Budgeting in the public sector.](budgeting-public-sector.md) You may be required to set up the following Budgeting features for the public sector. Use the **Budget analysis** page to view revenues and expenditures by financial dimension, using a combination of general ledger and budget control data. You can view summarized amounts and transaction details for revised budgets, actual expenditures, encumbrances, and pre-encumbrances. The revenues and expenditures can be summarized by the different levels of the financial dimensions. For example, if the budget dimensions are fund, organization, and main account, you can select **Fund**, **Organization**, or **Main account** to see the financial activity summarized at that level. You also use the **Budget analysis** page to select a financial dimension set and a column set. Select or specify the following, and then click **Update totals:**

-   Parameters
-   Date information
-   Financial dimensions

**Note** You create financial dimensions on the **Financial dimensions** page. You specify the date interval for included transactions on the **Date intervals** page in General ledger.

## <a name="what-transaction-details-are-available-on-the-budget-analysis-page"></a>What transaction details are available on the Budget analysis page?
You can select an item in the grid and drill down to see the following transaction details:

-   **Revised budget** amounts (the sum of original budget, revision, transfer, and carry-forward amounts)
-   **Actual expenditures** (the sum of the debits and credits that were posted for the financial dimension values)
-   **Encumbrances** and **Pre-encumbrances** (including original and relieving transactions)

### <a name="tips"></a>Tips

-   You can view the revised budget register entries for the budget analysis inquiry by clicking **Revised budget** on the Action pane. The budget types for the revised budget register entries include original budget, carry-forward, transfer, and revision. These amounts come from the budget register entry tables.
-   To view the actual expenditures for the budget analysis inquiry, click **Actual**. The page affects the originating document page, such as an advanced ledger entry. These amounts come from the general ledger account entry tables.
-   To view the encumbrances and the referenced transactions for the budget analysis inquiry, click **Encumbrance**. The page affects the purchase order for the selected transaction. These amounts come from the budget source tracking tables.
-   To view the pre-encumbrances and the referenced transactions for the budget analysis inquiry, click **Pre-encumbrance**. The page affects the purchase requisition for the selected transaction. These amounts come from the budget source tracking tables.

## <a name="should-i-use-the-budget-control-statistics-page-or-the-budget-analysis-page"></a>Should I use the Budget control statistics page or the Budget analysis page?
The **Budget control statistics** page is the tool to use when you want to analyze a single budget account, or a combination or group of accounts by period and budget control dimension. The **Budget analysis** page is more flexible. You can use it to query in any dimension order across the chart of accounts or to query a subset of an account. For example, you could view a list of year-to-date fund totals, drill down to a specific fund to view department totals, and then drill down to a specific department to view account totals. The following table explains the differences between these pages.

|                                                                                                                         |                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| **Budget control statistics page**                                                                                      | **Budget analysis page**                                                                    |
| Shows the budget balances for a budget cycle and a budget model for a single financial dimension value or budget group. | Shows the combined budget amounts for multiple financial dimension values at the same time. |
| Includes data from both confirmed and unconfirmed encumbrances.                                                         | Includes data from confirmed encumbrances only.                                             |
| Includes data from expense accounts only.                                                                               | Includes data from both revenue and expense accounts.                                       |

**Note** If you want the available or remaining budget amounts to include draft transactions, use the **Budget control statistics** page. The **Budget analysis** page displays only posted transactions.

## <a name="can-i-export-the-budget-analysis-results-to-microsoft-excel"></a>Can I export the budget analysis results to Microsoft Excel?
Yes, you can export budget analysis results. On the **Budget analysis** page, press Ctrl+Shift+E.

## <a name="how-do-i-display-information-for-a-specific-closing-period"></a>How do I display information for a specific closing period?
To view balances and information for a specific closing period, use the **Trial balance** page. The **Budget analysis** page does not distinguish between operating periods and closing periods.

## <a name="can-i-analyze-the-budget-in-a-dimension-order-thats-different-from-the-expense-account-structure"></a>Can I analyze the budget in a dimension order that’s different from the expense account structure?
Yes. For example, you might want to view certain Main accounts across programs or other dimensions. You can create financial dimension sets that reflect the way that you want to analyze your data. To do this, use the **Financial dimension sets** page in General ledger. To view Main accounts across programs, for example, create a Programs dimension set, and then add dimensions by using **MainAccount**. When you return to the **Budget analysis** page and select that dimension set, the budget appears as a list of Main accounts. You can then drill down in any Main account to include the program level of the dimension set, which breaks down all the totals by program within that Main account.

## <a name="what-if-the-financial-dimension-set-that-i-want-to-use-isnt-included-on-the-page"></a>What if the financial dimension set that I want to use isn’t included on the page?
All existing financial dimensions sets are displayed on the **Budget analysis** page. If you don’t see the one that you want, you can create it in General ledger.

## <a name="what-is-the-carry-forwards-column-set-used-for"></a>What is the Carry forwards column set used for?
Use the **Expense budget with carry-forwards** column set if you carry forward the budget for purchase orders that are open at year-end. This column set shows separate totals both for transactions that use active prior-year budget and for transactions that use the new year’s budget. This makes it easy for you to monitor the budgeted, encumbered, and expended amounts that are related to transactions from the prior year.

## <a name="what-should-i-do-if-the-grids-are-empty-even-when-ive-selected-all-the-values"></a>What should I do if the grids are empty even when I’ve selected all the values?
If the grids are empty in the **Budget analysis** page, try the following actions to resolve the issue:

-   Click **Update totals** after you set the values at the top of the page.
-   Verify that the selected dimension set includes the dimension value that you’re looking for.
-   Verify that the posting layer and the dates are correct for the values that you’re looking for.
-   Verify that the transaction document that you’re looking for has been posted or confirmed. Only posted transactions are displayed in the **Budget analysis** page.

## <a name="how-do-i-see-updated-numbers-in-the-columns-when-i-change-the-dimension-set-dates-posting-layers-and-other-settings"></a>How do I see updated numbers in the columns when I change the dimension set, dates, posting layers, and other settings?
After you change the settings at the top of the page, click **Update totals** to see the results of your query.

<a name="see-also"></a>See also
--------

[Budgeting in the public sector](https://ax.help.dynamics.com/en/wiki/Budgeting-in-the-public-sector/)


