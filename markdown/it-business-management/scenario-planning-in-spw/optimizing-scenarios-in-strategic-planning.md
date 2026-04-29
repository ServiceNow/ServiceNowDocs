---
title: Optimizing planning with scenario planning in Strategic Planning Workspace
description: As a portfolio manager, optimize your portfolio planning by comparing potential outcomes, assessing their alignment with strategic goals, and approving the best scenario as your live plan.
locale: en-US
release: australia
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Optimizing planning with scenario planning in Strategic Planning Workspace

As a portfolio manager, optimize your portfolio planning by comparing potential outcomes, assessing their alignment with strategic goals, and approving the best scenario as your live plan.

## Scenario planning items in the Prioritization tab

The **Prioritization** tab of the Scenario page enables you to add and remove planning items to/from a scenario and adjust their dates.

![Prioritization tab of the Scenario screen](../image/prioritization-tab-in-strategic-planning.png)

## Scenario planning items in the Roadmap tab

The **Roadmap** tab displays a Gantt chart-like view of the planning items in the scenario, showing their planned start and end dates across the portfolio plan timeline. Using the Roadmap tab, you can drag the bars representing planning items across the timeline to adjust their dates.

![Roadmap tab of the Scenario screen](../image/roadmap-tab-in-strategic-planning.png)

## Scenario planning items in Financials tab

The **Financials** tab of the Scenario page enables you to set custom targets, budget, and compare the allocated budget against target using the outcomes panel.

![Financials tab in Scenario planning view detailing the budget and forecast values of planning items.](../image/financials-tab-in-strategic-planning.png)

Portfolio Manager can simulate multiple scenarios with different budget combinations and compare their outcomes to arrive at an informed decision to balance the resources and strategic objectives. Using the financials view in Scenario planning, you can get a simulation mode for the financial information. Using this view, the strategic planning users such as Portfolio managers, Program managers, or Portfolio user working on the portfolios, can set a portfolio budget target for a particular planning cycle, which could be a monthly, quarterly, yearly, or beyond a year up to 5 years. Using this defined budget, portfolio users can prioritize the planning items within the portfolio to analyze if the prioritized items can be executed within their portfolio budget, while reviewing the monetary benefit from the prioritized items.

**Important:** [Enable the budget allocation property](../../spw-financials/task/enable-fin-budget-spw.md) to allocate budget to your planning items at portfolio-level and [configure the budget attributes](../../spw-financials/task/config-budget-allocation-attribute-spw.md) to allocate budget by expense type or cost type.

Create multiple scenarios to compare them, and work with your stakeholders to approve an ideal plan with better monetary benefit returns. Once approved, the approved Scenario will become your new portfolio plan for the defined planning cycle. For more information to know about the changes happening in a portfolio after scenario approval, see [Approve a scenario](../task/approve-a-scenario-in-strategic-planning.md).

You can perform financial scenario planning throughout your planning or execution cycle depending on your organization needs such as at your regular planning cycles, quarterly reviews, or financial review cycles. Financials in scenario planning helps you to arrive at an informed decision and customize the portfolio planning to match with your organization needs.

**Note:**

-   Finanicals in scenario planning is supported only for Epics, Projects, and Demands type of planning items.
-   Customers using the Legacy Investment Funding should migrate to new experience to work on the financial scenario planning.

Personalize your scenario planning financials view using the Time scale and Range filters. Manage the budget of your planning items by monthly, quarterly, or yearly cadence depending on the planning cycle of your organization.

Outcomes panel in Scenario planning

The outcomes panel in the simulation indicates the financial information of the portfolio such as target and budget amounts for Capex and Opex, set budget target for this simulation, utilized and remaining budget from the target, benefit from the In-plan items, and the actual costs accounting from the out of plan items. The aggregated data is fetched based on the portfolio timeline range including the target and budget data.

Representations in outcomes panel for the identification.

|Indication|Definition|
|----------|----------|
|Red text for amount without progress bar indication for Total Simulated Budget|No defined or set target amount for this scenario.|
|Red text for amount and red progress bar for Total Simulated Budget|Total allocated budget for planning items exceeds the scenario's set target amount.|
|Red text amount for Capex Budget|Capex Budget allocations exceed the scenario's Capex target.|
|Red text amount for Opex Budget|Opex Budget allocations exceed the scenario's Opex target.|
|Green text for budget amounts and green progress bar|Budget allocation for each expense types and total budget is within the scenario's set target.|

## Scenario planning features

In scenario planning, you can perform the following actions:

|Feature|Description|
|-------|-----------|
|[Create a scenario](../task/create-a-scenario-in-strategic-planning.md)|Create a scenario from the current plan, or another scenario, in a simulated environment to compare the scenario with the live plan and other scenarios.|
|[Compare scenarios](../task/compare-scenarios-in-strategic-planning.md)|Compare scenarios and the live plan side by side to review tradeoffs and items added or removed from the plans.|
|[Approve a scenario](../task/approve-a-scenario-in-strategic-planning.md)|Approve the best scenario.|
|[Manage scenarios](../task/manage-scenarios-in-strategic-planning.md)|View list of scenarios, rename scenarios, and delete scenarios.|

## Scenario planning use cases

The following are high-level use cases for scenario planning.

-   Fiscal year planning: Megan Burke, Portfolio Manager at ACME Inc, is planning for the next fiscal year and is required to prioritize planning items and align them with the organizational strategic goals. Megan creates a scenario for the portfolio plan and then uses the Prioritization tab to align items with goals. Megan holds discussions with program managers and with the financial team, creates multiple scenarios, and compares them. Megan approves the optimal scenario as a well-aligned strategic portfolio plan for the next fiscal year.
-   Mid-cycle reprioritization; Changed priorities emerging mid-year require adjustments to the current portfolio plan. John Doe, the product manager at ACME Inc, creates a scenario and incorporates the changed priorities. John adjusts the plan based on the program manager's and financial team's feedback and finalizes the plan.

