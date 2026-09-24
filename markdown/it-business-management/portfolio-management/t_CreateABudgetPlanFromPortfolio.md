---
title: Legacy- Create and promote a budget plan
description: As part of the PPM Standard \(Project Portfolio Management\) integration, you can create and promote a budget plan for a portfolio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/portfolio-management/t\_CreateABudgetPlanFromPortfolio.html
release: brazil
product: Portfolio Management
classification: portfolio-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Legacy- Plan the portfolio, Legacy portfolio workbench, Portfolio Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Legacy- Create and promote a budget plan

As part of the PPM Standard \(Project Portfolio Management\) integration, you can create and promote a budget plan for a portfolio.

## Before you begin

-   Role required: it\_portfolio\_manager
-   The **Portfolio Planning** field for portfolio must be set to **Advanced** on the [Portfolio form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/t_CreateAPortfolio.md).
-   The name of the portfolio manager must be set in **Portfolio Manager** field on Portfolio form.
-   The [budget period](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/create-a-budget-period.md) for the selected fiscal period must be open to create and promote a budget plan for a portfolio.

    **Note:** PPS admin can also open and close the budget period for a fiscal period from **Project Administration** &gt; **Open/Close Budget Periods**.


## About this task

The budget plan includes costs from all selected projects and demands. The budget plan summary is displayed on portfolio workbench and the details can be seen in Financial Planning. In the advanced planning mode, the creation of a budget plan is mandatory to be able to track the portfolio.

## Procedure

1.  Navigate to portfolio workbench and open the portfolio that you want to track.

2.  Click **Promote Budget Plan** under **Step 3: Budgeting**.


## Result

-   The budget plan for the portfolio for the selected fiscal year is created and promoted. You can [re-promote the budget plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/repromote-budget-plan.md), if required.
-   A budget task with the status **Pending Approval** is created when the portfolio manager promotes the budget plan, the first time in the budgeting period. The status of the task is visible in Portfolio Workbench.

## What to do next

-   View the status of the budget plan below the budget plan name under **Step 3: Budgeting** in portfolio workbench. Click the **Status** link to view the budget task for the budget plan in [financial planning workbench](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/view-ppm-portfolio-budget-plan-in-planning-workbench.md). The finance reviews the portfolio budget plans in the [Planning Workbench](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/financial-planning-workbench.md) and approves the plan.
-   [Legacy- Track the portfolio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/t_ReviewFinancialPlanning.md).
-   [Legacy- Create and promote a forecast plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/create-forecast-plan.md).
-   If the budget plan is finalized and no more changes are expected, the budget period must be closed.

**Parent Topic:**[Legacy- Plan the portfolio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/c_FinancialPlanningForPortfolio.md)

**Related topics**  


[Legacy portfolio workbench](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/c_PortfolioWorkbench.md)

