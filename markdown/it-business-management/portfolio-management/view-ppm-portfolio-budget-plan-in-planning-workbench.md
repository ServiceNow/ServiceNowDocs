---
title: Legacy- View promoted portfolio budget plans in the planning workbench
description: Use the financial planning workbench to view the portfolio budget plan promoted by portfolio manager, which is initiated in Project Portfolio Management and converted as a budget plan in Financial Management.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/portfolio-management/view-ppm-portfolio-budget-plan-in-planning-workbench.html
release: brazil
product: Portfolio Management
classification: portfolio-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Legacy- Plan the portfolio, Legacy portfolio workbench, Portfolio Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Legacy- View promoted portfolio budget plans in the planning workbench

Use the financial planning workbench to view the portfolio budget plan promoted by portfolio manager, which is initiated in Project Portfolio Management and converted as a budget plan in Financial Management.

## Before you begin

**Note:** The content in this topic is applicable for customers upgrading from a previous release to Brazil. If you are a new customer, see [Scenario Planning for PPM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/portfolio-planning-overview.md).

Role required: itfm\_plan\_analyst

You require Project Portfolio Suite with Financials \[com.snc.financial\_planning\_pmo\] plugin to perform portfolio budgeting and forecasting.

## About this task

In Project Portfolio Management, portfolio managers use [portfolio workbench to plan and promote the portfolio annual budget plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/c_FinancialPlanningForPortfolio.md).

**Note:** The budget period or forecast period must be open to promote the portfolio plan.

A budget task with the status **Pending Approval** is created when the portfolio manager promotes the budget plan, the first time in the budgeting period. The status of the task is visible in Portfolio Workbench.

\[Omitted image "PortfolioWorkbench.png"\] Alt text: Portfolio Workbench

The finance reviews the portfolio budget plans in the Planning Workbench and approves the plan.

The planning process between the portfolio managers and the IT finance is entirely automated. The plan promoted in the Portfolio Workbench is available in the Planning Workbench. Finance approves the plan by approving the task, or sends it back to portfolio manager indicating the status as **Awaiting Input**. The portfolio managers reworks on the IT finance review recommendations and promotes the plan.

**Note:** The planning workbench replaces the budget console that was used in the Jakarta release.

## Procedure

1.  Navigate to **All** &gt; **Financial Planning** &gt; **Workbench**.

2.  From the choice list at the top-right of the workbench, select the budget period for which you are doing the planning.

    You can also create a budget period and open it to make it available for budgeting.

3.  From the choice list, select the **Portfolio Budget Planning** definition.

    **Note:** The budget tasks originating from the Portfolio Workbench are initially in the **Pending Approval** state.

    \[Omitted image "PortfolioBudgetPlanning.png"\] Alt text: Portfolio budget plans

4.  To view the promoted budget amount or last forecast amount, click **Plan View**.

5.  Open a budget task record from the budget tasks list.

    You can also do this task in the VTB View of the workbench.

    As an IT finance analyst, you approve the promoted plan details or send it back to the portfolio manager by adding a note in the **Work notes** field and update the **State** field to **Awaiting Input**.

    **Forecasting**

    The same process applies even for the forecasting period. The plan view shows the last promoted column which is the last promoted forecast plan from portfolio manager. The forecast amount contains actuals until the forecasting month and forecast for remaining period by the portfolio manager.

    **Cost plan Actuals**

    The actuals column in plan view is based on the cost plan actuals which is generated based on approved expense lines and actuals from timecards from Project Portfolio Management. If you notice a discrepancy in actuals amounts, regenerate actuals from **Generate Actuals** available at the top right corner of workbench. \[Omitted image "cost\_plan\_actuals.png"\] Alt text: Cost plan actuals


-   **[Legacy- Portfolio budget object configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/portfolio_budget_object_configuration.md)**  
The planned cost of cost plans in portfolio when promoted by portfolio managers are converted to budget plans. The base system has a seeded read-only budget definition Portfolio Budget Planning Process used for the promotion of portfolio.

**Parent Topic:**[Legacy- Plan the portfolio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/c_FinancialPlanningForPortfolio.md)

