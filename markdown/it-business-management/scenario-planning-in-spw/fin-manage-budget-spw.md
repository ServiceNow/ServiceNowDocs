---
title: Manage budget of your planning items in Strategic Planning
description: Allocate, manage, and approve budget for your projects. Lean budgeting allocates budget for short planning cycles across fiscal periods, such as monthly, quarterly, or yearly. This approach differs from allocating budget to the complete duration of a planning item.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/it-business-management/scenario-planning-in-spw/fin-manage-budget-spw.html
release: yokohama
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Manage financials for planning items, Portfolio Planning in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Manage budget of your planning items in Strategic Planning

Allocate, manage, and approve budget for your projects. Lean budgeting allocates budget for short planning cycles across fiscal periods, such as monthly, quarterly, or yearly. This approach differs from allocating budget to the complete duration of a planning item.

## Before you begin

-   Admins should enable the property to work on budgeting. For more information, see [Enable financial budget allocation for planning items in Strategic Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-business-management/scenario-planning-in-spw/enable-fin-budget-spw.md).
-   Admins can configure the attribute to allocate and approve budget by cost type or expense type. For more information, see [Configure budget attribute at instance-level](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-business-management/scenario-planning-in-spw/config-budget-allocation-attribute-spw.md).
-   Role required: it\_portfolio\_manager

## About this task

\[Omitted video\] Description: Manage budget for your projects

## Procedure

1.  Navigate to **Workspaces** &gt; **Strategic Planning Workspace** and select portfolio plan.

2.  Select a planning item from the Planning module.

3.  Select the **Financials** tab.

4.  Use the Display mode list and select **Budget allocation**.

5.  Manage budget using one of the following ways for the selected time scale at monthly, quarterly, or yearly level.

    -   Double-click each cell in the Budget column to manually enter the value.
    -   Select **Copy cost as budget** from the Budget column options to copy Forecast value as budget.
    **Note:** Negative budget amounts are supported. If you enter a negative **Capex Budget** or **Opex Budget** amount, or the associated cost plan has a negative total planned cost, the project budget is still distributed across the cost plan breakdowns and rolled up to the project financials.

    -   You can edit the budget values using the in-grid editing feature after copying Forecast to budget.
    -   Unapproved budget values are indicated with \[Omitted image "fin-copy-budget-icon.png"\] Alt text: Tick mark in a circle representing the unapproved budget icon.
6.  Select **Approve budget** \(\[Omitted image "fin-approve-budget-icon.png"\] Alt text: Approve budget button.\).

    Approve budget confirmation window is displayed. The **Create a financial baseline for this budget approval** option is enabled by default which captures the latest budget and financial estimates.

    **Tip:** The financial baseline created while approving the budget can be compared with the future baselines once the actual expenses are captured to track financial performance.

7.  On the confirmation window, select **Approve** \(\[Omitted image "fin-approve-icon.png"\] Alt text: Approve button.\).


## Result

Budget widget is updated to reflect the latest approved budget. Project Manager can view the approved budget and compare it with the planned costs using the **budget vs cost** view by cost type.

