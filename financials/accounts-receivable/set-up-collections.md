---
title: Set up Credit and collections | Microsoft Docs
description: This article explains how to set up the collections functionality.
author: twheeloc
manager: AnnBe
ms.date: 2015-12-02 23:04:01
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
keywords: CustCollectionsActivitiesListPage
audience: Application User
ms.reviewer: 2231
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 14031
ms.assetid: 74851390-96e2-4876-be84-9d58fb628238
ms.region: Global
ms.author: mfalkner
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: 89f8b66426d524030ee3b4040b7ae4fa6f38ca41


---

# <a name="set-up-credit-and-collections"></a>Set up Credit and collections

This article explains how to set up the collections functionality.

<a name="set-up-aging-period-definitions"></a>Set up aging period definitions
-------------------------------

Set up an aging period definition. An aging period definition defines the columns that appear on the **Aged balances**, **Collections activities**, and **Collections cases** list pages. It also defines the periods that appear on the **Collections** page. If a customer pool is set up, the aging period definition for the pool is used. If no pools are set up, the default aging period definition that is specified on the **Accounts receivable parameters** page is used. If no default aging period definition is specified, the first aging period definition on the **Aging period definitions** page is used.

## <a name="create-an-aging-snapshot"></a>Create an aging snapshot
Create aging snapshot records for all customers or for the customers in a customer pool. Aging snapshot information appears on the **Aged balances** list page and on the **Collections** page. You must create an aging snapshot before you can use the list page. The list page shows information only for customers that an aging snapshot has been created for.

## <a name="optional-set-up-customer-pools"></a>Optional: Set up customer pools
You can set up customer pools to represent groups of customers. You can use customer pools as filters for the customer information that appears on **Collections** list pages, on the **Collections** page, or when you create aging snapshots.

## <a name="optional-create-a-collections-team"></a>Optional: Create a collections team
If multiple people in your organization do collections work, you can set up a collections team. You can select the team on the **Accounts receivable parameters** page. If you don't create a collections team, a team is created automatically when you set up collections agents on the **Collections agent** page.

## <a name="set-up-a-collections-case-category"></a>Set up a collections case category
If you will use cases to organize your collections work, set up a case category that has the **Collections** category type. This setup is required only if you want to use the case functionality on the **Collections** page.

## <a name="set-up-journal-names-settlement-writeoff-and-nsf"></a>Set up journal names (settlement, writeoff, and NSF)
Set up the journal names that are used when transactions are processed on the **Collections** page. This processing includes settlement of a transaction, write-off of a transaction, and processing of a not sufficient funds (NSF) payment.

| Description | Journal type     |
|-------------|------------------|
| Settlement  | Customer payment |
| Write-off   | Daily            |
| NSF         | Customer payment |

## <a name="set-up-a-reason-code-for-writeoff-transactions"></a>Set up a reason code for writeoff transactions
Set up the default reason code that is used when transactions are written off on the **Collections** page. You can change the code during the write-off process.

## <a name="set-up-a-folder-for-email-attachments-and-create-email-templates"></a>Set up a folder for email attachments and create email templates
If you will send email messages from the **Collections** page that have Microsoft Excel attachments, you can create optional email templates for those messages.

## <a name="set-up-accounts-receivable-parameters-for-collections"></a>Set up accounts receivable parameters for collections
Set up the accounts receivable parameters that appear on the **Collections** tab.

## <a name="optional-set-up-collections-agents"></a>Optional: Set up collections agents
If multiple people in your organization do collections work, you can set up collections agents. A collections agent is a worker who is set up as a user on the **User relations** page. You can assign customer pools (customer queries) to collections agents to help the agents organize their work. The collections agents are added to the team that is selected on the **Accounts receivable parameters** page. If a team isn't selected on that page, a new team that is named **Collections** is automatically created, and the collections agents are added to that team.

## <a name="set-up-a-writeoff-account"></a>Set up a writeoff account
Set up the write-off account that is used for the general ledger write-off entry when a transaction is written off. This account is stored on the customer posting profile.

## <a name="set-up-nsf-information-for-bank-accounts"></a>Set up NSF information for bank accounts
Update bank accounts so that they have the correct journal when NSF payments are identified on the **Collections** page. On the **Currency management** tab,  in the **NSF payment journal** field, select a payment journal.

## <a name="set-up-outlook-settings-for-users-of-the-collections-page"></a>Set up Outlook settings for users of the Collections page
Before workers can create activities or send email messages by using the **Collections** page, you must verify that the **Microsoft Outlook synchronization** configuration key is selected, and that Outlook synchronization is set up for those workers.

## <a name="set-up-email-and-address-settings-for-collections-customer-contacts"></a>Set up email and address settings for collections customer contacts
Set up email addresses for customer contacts if you want to send email messages to those contacts from the **Collections** page. The collections contact is used as the default contact on the **Collections** page. You can set up a statement address for a customer if statements should use an address other than the primary address. On the **Credit and Collections** FastTab for a customer, in the **Collections contact** field, select the person in the customer organization who works with your collections agent. This person is used as the default contact on the **Collections** page, and email messages are sent to him or her. **Note:** If a collections contact isn't specified for a customer, the primary contact for the customer is used. If a primary contact isn't specified, email messages are sent to the first address that is listed on the **Contacts** page.

## <a name="set-up-email-settings-for-salespeople"></a>Set up email settings for salespeople
Set up email addresses for salespeople if you want to send email messages to salespeople from the **Collections** page. Set up an email address for each sales representative in each commission sales group. The sales representative who has the **Contact** option selected is the default salesperson that email messages are sent to. If a sales representative isn't specified, the primary salesperson for the customer organization is used. If a primary salesperson isn't specified, email messages are sent to the first salesperson who is listed on the page.




<!--HONumber=Feb17_HO3-->

