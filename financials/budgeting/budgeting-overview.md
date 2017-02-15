---
title: Budgeting home page | Microsoft Docs
description: This topic provides an overview of the budgeting functionality components, budgeting tools, and reporting capabilities in Microsoft Dynamics 365 for Operations.
author: twheeloc
manager: AnnBe
ms.date: 2016-08-02 18:45:27
ms.topic: index-page
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: 101
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 106043
ms.assetid: 6fc07526-e3e1-4ac3-8a4f-c07e3b13e3c9
ms.region: Global
ms.author: twheeloc
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: 58ea372b82861cba100d04b9005d665d003d8c12


---

# <a name="budgeting-home-page"></a>Budgeting home page

This topic provides an overview of the budgeting functionality components, budgeting tools, and reporting capabilities in Microsoft Dynamics 365 for Operations.

<a name="components-of-budgeting-functionality"></a>Components of budgeting functionality
-------------------------------------

The resource planning cycle for a company typically consists of planning, budgeting, and forecasting activities. [![Budgeting functionality components](./media/budgeting-functionality-components.jpg)](./media/budgeting-functionality-components.jpg) The processes for both long-term strategic planning and annual budget planning are supported through a budget plan document. Budget plan documents are tightly integrated with Microsoft Excel. Users can configure unlimited monetary and quantitative scenarios, and can also define a budgeting organizational hierarchy to both support top-down and bottom-up budgeting methods. After a budget is established and approved in Microsoft Dynamics 365 for Operations, you convert the budget plan to a budget register entry. Budget register entries provide tools for maintaining the budget and for keeping amounts traceable through budget codes. Budget register entries let you revise original budgets, perform transfers, and carry forward budget amounts from the previous year. Based on the established budget, a company can enable budget control. The level of control depends on the organizational culture and the organization's level of maturity. Organizations that have low maturity might leave the budget “as is” and might be more reactive than proactive if a budget doesn't meet expectations. Other organizations might enable budget control policies that prevent users from purchasing if budget funds aren't available. Finally, very mature organizations might establish an organizational culture where employees are educated about organizational targets and follow those targets through policies such as “Consider online meeting instead of a travel.” Dynamics 365 for Operations includes a budget control framework that lets the company's management select either hard control (which prevents postings that would go over the budget) or soft control (where users are warned that they will exceed the available budget funds but can decide for themselves how to proceed). Finally, you can use rolling forecasts. A rolling forecast is a regular comparison of budget to actuals and is used to define how well the company operates against the budget. A rolling forecast is also used to identify trends. In Microsoft Dynamics 365 for Operations, rolling forecasts are supported, through a budget plan document, as initial planning activities. Rolling forecasts can be done in parallel with the planning for the upcoming budget cycle.

-   [Basic budgeting: Overview and configuration](https://docs.microsoft.com/en-us/dynamics365/operations/financials/budgeting/basic-budgeting-overview-and-configuration)
-   [Budget control: Overview and configuration](https://docs.microsoft.com/en-us/dynamics365/operations/financials/budgeting/budget-control-overview-and-configuration)
-   [Budget planning: Overview and configuration](https://docs.microsoft.com/en-us/dynamics365/operations/financials/budgeting/budget-planning-overview-and-configuration)
-   [Position forecasting](https://docs.microsoft.com/en-us/dynamics365/operations/financials/budgeting/position-forecasting)
-   [Budget planning justification documents](https://ax.help.dynamics.com/en/budget-planning-justification-documents)
-   [Microsoft Excel templates for budget planning](https://docs.microsoft.com/en-us/dynamics365/operations/financials/budgeting/smart-excel-templates-for-budget-planning)

## <a name="budgeting-tools-in-dynamics-365-for-operations"></a>Budgeting tools in Dynamics 365 for Operations
[![Budgeting tools](./media/budgeting-tools.jpg)](./media/budgeting-tools.jpg) Additional planning and budgeting capabilities are available across Dynamics 365 for Operations and are integrated with ledger budgets.

-   **Workforce budgets** – Workforce budgeting includes detailed budget cost component planning for positions, compensation groups, and so on.
-   **Fixed assets budgets** – Based on fixed asset information, you can calculate planned depreciation and record other planned transactions that are related to fixed assets.
-   **Project budgets** – In the projects module, you can create detailed project forecasts. The projects forecasts will include details about the planned hours, expenses, fees, and items.
-   **Demand forecasting **– Based on historical transaction data, you can estimate future inventory demand and create demand forecasts.

For information about how to bring planning data from other modules into budget plans, see [Budget planning integration with other modules](https://docs.microsoft.com/en-us/dynamics365/operations/financials/budgeting/budget-planning-integration-with-other-modules).

## <a name="user-interface-and-reporting-capabilities"></a>User interface and reporting capabilities
In Dynamics 365 for Operations, users can create budget plans either directly in the Dynamics 365 for Operations client (by using a configurable budget plan document page) or through Excel. Excel provides several additional capabilities. For example, you can use external data as a source for a budget plan, do custom calculations, and use Microsoft PivotTable and charts. Most of the variables in the budget planning process can be configured. For example, you can define who does budgeting, what is budgeted, and what the process looks like. Although you can use Excel for budget planning, Dynamics 365 for Operations is kept as a single source of truth and helps prevent budget control issues. Periodic processes can be used to bring initial data for budgeting into the budget plan. For reporting, Dynamics 365 for Operations offers a set of standard inquiry pages that let you view and analyze budgeting data. Budget plan data can be accessed through Management Reporter, and separate budget plan scenarios can be displayed as columns on the Management Reporter report.

## <a name="additional-resources"></a>Additional resources
-   Additional help is available as task guides inside Dynamics 365 for Operations. To access task guides, click the Help button on any page.
-   For information about Microsoft Dynamics 365 for Operations training, see [Microsoft eLearning](https://mbs2.microsoft.com/members/elearning/dynamicstrainingcert.aspx) (requires CustomerSource account).





<!--HONumber=Feb17_HO3-->

