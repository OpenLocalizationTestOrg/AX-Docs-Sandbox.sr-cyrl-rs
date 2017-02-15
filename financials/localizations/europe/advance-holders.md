---
title: Advance holders | Microsoft Docs
description: Learn about advance holder functionality in Microsoft Dynamics 365 for Operations.
author: ShylaThompson
manager: AnnBe
ms.date: 2016-12-12 21:45:42
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: 81
ms.suite: Released- Dynamics 365 for Operations version 1611
ms.custom: 262574
ms.assetid: 8dc6583d-4ee8-4e22-931a-513301ce177f
ms.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-elgolu
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: f60c4249b2de21446663328d4c3893b8b6f4f7cb


---

# <a name="advance-holders"></a>Advance holders

Learn about advance holder functionality in Microsoft Dynamics 365 for Operations.

An *advance holder* is an employee of a company who is accountable for an expense amount that is provided by the organization. Only a company's worker can be an advance holder. When a procurement happens, an advance holder reports to the company about the expenditures that were made. The company reimburses the employee for the expense amount. A company controls a balance for each advance holder. Users in legal entities in Estonia, Latvia, Lithuania, Poland, Czech Republic, Hungary, and Russia can reflect specific transactions accompanying operations with company’s employees who are accountable for the expense amount that is provided by the organization.

## <a name="set-up-an-advance-holder"></a>Set up an advance holder
To set up an advance holder, the following tasks should be completed in order.
1.  Create advance holder groups.
2.  Set up an employee posting profile.
3.  Set up account payable parameters.
4.  Create a specific terms of payment for the advance holder.
5.  Create an advance holder.

### <a name="advance-holder-groups"></a>Advance holder groups

Use the **Advance holder groups** page to create an advance holder group. You can specify the name, description, and offset account for the advance holder group.
### <a name="employee-posting-profile"></a>Employee posting profile

Use the **Employee posting profiles** page to create a profile for advance holder transactions. You can specify the following information for the employee posting profile.
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
<td><strong>Posting profile</strong></td>
<td>Enter the posting profile identification code for the advance holder.</td>
</tr>
<tr class="odd">
<td><strong>Description</strong></td>
<td>Enter a brief description of the posting profile.</td>
</tr>
<tr class="even">
<td><strong>Valid for</strong></td>
<td>Select one of the following options for the level of grouping for setting up the posting profile:
<ul>
<li><strong>Table</strong> – This option is used to set up the posting profile for one advance holder. You must indicate the advance holder code in the <strong>Reference</strong> field.</li>
<li><strong>Group</strong> – This option is used to set up the posting profile for a group of advance holders. You must indicate the group code in the <strong>Reference</strong> field.</li>
<li><strong>All</strong> – This option is used to set up the posting profile for all advance holders.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Reference</strong></td>
<td>Select the advance holder code if <strong>Table</strong> is selected in the <strong>Valid for</strong> field, or select the advance holder group if <strong>Group</strong> is selected in the <strong>Valid for</strong> field.</td>
</tr>
<tr class="even">
<td><strong>Summary account</strong></td>
<td>Select the summary account for posting the transactions.</td>
</tr>
</tbody>
</table>

### <a name="account-payable-parameters"></a>Account payable parameters

To reflect advance holder’s transactions you must set up the following on the **Account payable parameters** page in the **Advance holders** section.
|                                                |                                                                                                                                                                                  |
|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  **Field**                                     | **Description**                                                                                                                                                                  |
| **Posting profile**                            | Select the default profile to complete transactions for advance holders.                                                                                                         |
| **Advance holder sorting**                     | If selected, advance holders will be displayed at the beginning of the list in the **Advance holders** page.                                                                     |
| **Issue when balance is open**                 | If selected, issue of a cash advance to an advance holder who has an open positive balance will be allowed.                                                                      |
| **Balance closing via cash field group: Name** | Select the cash slip journal code. This journal code is used to generate cash disbursement slips and reimbursement slips when closing an advance holder’s balances through cash. |
| **Cash**                                       | Select the cash account to determine the vouchers that are used for closing the balances for the advance holder.                                                                 |
| **Balance closing via bank field group: Name** | Select the journal code for transactions to close the balances through a bank.                                                                                                   |
| **Account type**                               | Select a bank to close the balances for an advance holder through a bank.                                                                                                        |
| **Main account**                               | Select a bank account code to close the balances for an advance holder through a bank.                                                                                           |

### <a name="terms-of-payment-for-advance-holder"></a>Terms of payment for advance holder

To correctly register and post a purchase order through an advance holder, you must use a Terms of payment that was set up with the **From advance holder** option set to **True**.
### <a name="create-an-advance-holder-creation"></a>Create an advance holder creation

Before you can create an advance holder, you must have already set up workers. For more information, see [Enter worker information.](http://ax.help.dynamics.com/en/wiki/enter-worker-information/) Use the **Advance holders** page to set up a worker as an advance holder. Select the worker to use as an advance holder, click **Edit**, and then set the **Advance holder** option to **True**. You must also complete the following fields.
|                |                                                                                             |
|----------------|---------------------------------------------------------------------------------------------|
| **Field**      | **Description**                                                                             |
| **Group**      | Select an advance holder group.                                                             |
| **Series**     | Enter the series of the document that is used to verify the identity of the advance holder. |
| **Number**     | Enter the number of the document that is used to verify the identity of the advance holder. |
| **Issue date** | Select or enter the document issue date.                                                    |
| **Issued by**  | Enter the details of the authority or person who issued the document.                       |

## <a name="advance-holder-inquiries-and-reports"></a>Advance holder inquiries and reports
### <a name="advance-holder-transactions-inquiry"></a>Advance holder transactions inquiry

For a list of transactions for an advance holder, click the **Transactions** button on the **Advance holders** page. To see transactions for all advance holders or to create a specific inquiry based on advance holders’ transactions, click **Accounts payable** &gt; **Inquiries and reports** &gt; **Advance holders inquiries and reports** &gt; Transactions. Click **Voucher** to open the **Voucher transactions** page.
### <a name="advance-holder-balance-inquiry"></a>Advance holder balance inquiry

To see balance for an Advance holder use the **Advance holders** page. To see balance for all advance holders or to create a specific inquiry based on advance holders’ accounts, click **Accounts payable** &gt; **Inquiries and reports** &gt; **Advance holders inquiries and reports** &gt; **Balance.**
### <a name="advance-holder-balance-report"></a>Advance holder balance report

To preview and print a report based on information about advance holders’ balance, click **Accounts payable** &gt; **Inquiries and reports** &gt; **Advance holders inquiries and reports** &gt; **Advance holder balance report**.
### <a name="advance-holder-transactions-report"></a>Advance holder transactions report

To preview and print a report based on advance holders’ transactions, click **Accounts payable** &gt; **Inquiries and reports** &gt; **Advance holders inquiries and reports** &gt; **Advance holder transactions report**.



<a name="see-also"></a>See also
--------

[Advance holder transactions](https://docs.microsoft.com/en-us/dynamics365/operations/financials/localizations/europe/advance-holders-transactions)




<!--HONumber=Feb17_HO3-->


