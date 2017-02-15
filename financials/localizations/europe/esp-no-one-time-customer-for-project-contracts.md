---
title: One-time customers | Microsoft Docs
description: This topic provides information about one-time customers.
author: ShylaThompson
manager: AnnBe
ms.date: 2016-12-16 21:38:18
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
keywords: CustTable
audience: Application User
ms.reviewer: 81
ms.suite: Released- Dynamics 365 for Operations version 1611
ms.custom: 264394
ms.assetid: bd809211-914d-4cf9-9693-15252f568c39
ms.region: Spain
ms.author: v-elgolu
translationtype: Human Translation
ms.sourcegitcommit: d331960307ba214de4382feac7941aa5065c523d
ms.openlocfilehash: 1f4417c92f3317c9acc335dedde4cef3f00b8e2d


---

# <a name="one-time-customers"></a>One-time customers

This topic provides information about one-time customers.  

A one-time customer is a customer who does not have a long-term relationship with your company. For one-time customers, you typically don't need to save information like address, contact, or tax exempt details. To indicate that a customer is a one-time customer, complete the following steps:

1.  Open the **All customers** page.
2.  Select a customer name to open the customer's record.
3.  On the **Miscellaneous details** FastTab, set the **One-time customer** option to **Yes**.
4.  Click **Save**.

**Note:** Before you can post transactions for a one-time customer, you must specify an account to use for one-time customers in the **One-time customer account** field on the **Accounts receivable parameters** page. For Spain, you can restrict users from creating project contracts for one-time customers. To do this, complete the following steps:

1.  Open the **Project management and accounting parameters** page.
2.  Set the **No one-time customer for project contracts** parameter to **True**.
3.  Click **Save**.





<!--HONumber=Feb17_HO3-->


