---
title: Manage demand budgets
description: Allocate, manage, and approve budget for your demands. Lean budgeting allocates budget for short planning cycles across fiscal periods, such as monthly, quarterly, or yearly. This approach differs from allocating budget to the complete duration of a demand.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/strategic-planning/manage-budget-of-your-demands.html
release: zurich
product: Strategic Planning
classification: strategic-planning
topic_type: task
last_updated: "2026-07-25"
reading_time_minutes: 1
breadcrumb: [Manage financials for demands, Use, Next Experience for Demand Management in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Manage demand budgets

Allocate, manage, and approve budget for your demands. Lean budgeting allocates budget for short planning cycles across fiscal periods, such as monthly, quarterly, or yearly. This approach differs from allocating budget to the complete duration of a demand.

## Before you begin

-   Enable the property to work on budgeting. For more information, see [Enable financial budget allocation for demands](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/strategic-planning/enable-financial-budget-allocation-for-demands.md).
-   Configure the attribute to allocate and approve budget by cost type or expense type. For more information, see [Configure budget attribute at instance level](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/strategic-planning/configure-budget-attribute-at-instance-level-dw.md).
-   Role required: it\_demand\_manager

## Procedure

1.  Navigate to **Workspaces** &gt; **Strategic Planning Workspace**.

2.  Select the Demands icon \[Omitted image "demands-icon.png"\].

3.  Open a demand from the **List** page.

4.  Select **Financials** from the navigation menu.

5.  Select **Budget allocation** from the Display mode list.

6.  Manage the budget for the selected time scale at the monthly, quarterly, or yearly level using one of the following methods.

    -   Double-click each cell in the Budget column and enter the value.
    -   Select **Copy cost as budget** from the Budget column options to copy Forecast value as budget.
    -   Edit the budget values using the in-grid editing feature after copying Forecast to budget.
    -   Unapproved budget values are marked with the \[Omitted image "fin-copy-budget-icon.png"\] Alt text: icon.
    **Note:** Negative budget amounts are supported. If you enter a negative **Capex Budget** or **Opex Budget** amount, or the associated cost plan has a negative total planned cost, the demand budget is still distributed across the cost plan breakdowns and rolled up to the demand financials.

7.  Select **Approve budget**.

    The Approve budget confirmation dialog opens. The **Create a financial baseline for this budget approval** option is selected by default. This option captures the latest budget and financial estimates.

    **Tip:** The financial baseline created while approving the budget can be compared with the future baselines once the actual expenses are captured to track financial performance.

8.  In the confirmation dialog, select **Approve**.


