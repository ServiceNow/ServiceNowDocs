---
title: Managing financials for demands
description: Financials in Next Experience for Demand Management covers budget, cost plans, expense lines, labor costs, and financial baselines.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/strategic-planning/managing-financials-dw.html
release: zurich
product: Strategic Planning
classification: strategic-planning
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 10
breadcrumb: [Use, Next Experience for Demand Management in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Managing financials for demands

Financials in Next Experience for Demand Management covers budget, cost plans, expense lines, labor costs, and financial baselines.

The comprehensive financials view displays planned and actual costs for the selected item. Costs include Forecast, Remaining Estimates, and Actual. These were previously named EAC \(Estimate At Completion\), ETC \(Estimate To Completion\), and Actuals to date, respectively.

## Cost view

Forecast your planned costs, create, and manage cost plans and expense lines to track the financial performance of your demands.

In the Cost view, you can:

-   View and manage financial data for a demand.
-   Re-forecast cost plan values for future fiscal periods by selecting a value in the month or period time scale view.
-   Manage cost plans for your demands. For more information, see [Create cost plans for a demand](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/strategic-planning/add-edit-or-delete-demand-cost-plans.md).
-   Add or edit expense lines for your demands to record any expenses. For more information, see [Create expense lines for a demand](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/strategic-planning/add-or-edit-expense-lines-dw.md).
-   Generate labor costs for the fiscal period. For more information, see [Generate labor costs for a demand](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/strategic-planning/generate-labor-costs-dw.md).
-   Create and compare baselines to capture the financial snapshot of your demands. For more information, see [Create and compare financial baselines for a demand](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/strategic-planning/create-compare-financial-baselines-dw.md).

Users can filter the Financials tab grid by time scope to narrow cost plans, benefit plans, and baselines to a specific period.

**Tip:** Cost view gives you enhanced user experience to customize the left pane columns by using the personalize icon \( \[Omitted image "icon-personalize.png"\] Alt text:\). You can save user preferences to retain the customizations made to hide, view, or adjust columns, time scope viewing, and so on.

## Multicurrency

The multicurrency feature enables you to manage the financials of your demands in two different currencies, Functional currency and Demand currency. Functional currency is typically defined by the admin as the primary currency, which is used for planning, budgeting, and tracking the financials of your planning items.

You can perform the following financial activities in Demand currency.

-   Select the Demand currency.
-   Track the planned and actual expenses.
-   Allocate and manage the budget.
-   View simple financials data.

Financial reporting at a global level includes real-time currency conversions of financial records.

Organizations operate at a global or multinational level. Work is planned and financed at one location and executed at another, often using a different currency from the planning phase. Multicurrency enables management and tracking of planning items in any currency.

You can monitor and track the financials in one currency, and capture the costs in a different currency. For more information, see [Multicurrency in Next Experience for Demand Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/strategic-planning/multicurrency-in-demand-workspace.md).

**Note:** After a cost plan, benefit plan, expense line, or investment budget is created, the Demand currency cannot be changed. The Demand currency can be changed only when no financial records exist for the demand.

## Display modes

The Display mode list on the Financials page of a demand lets you switch between modes to view financial information in different formats. Each view provides focused information for financial planning. The last selected view is saved as user preferences.

The available modes are:

-   Forecast
-   Budget allocation
-   Planned vs Actuals
-   Planned

<table id="table_pnt_1wr_bgc"><thead><tr><th>

Mode

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Forecast

</td><td>

View Actuals, Remaining estimates, and Forecast for the entire scope of the demand.Use the time scale to view the actuals for the past fiscal periods and planned costs for the current and future fiscal periods.

</td></tr><tr><td>

Budget allocation

</td><td>

View the Budget, Actuals, and Variance for the fiscal periods and Forecast values for the entire scope of the demand. Using this mode, funding users can:

-   View the latest forecast and enter the budget that can be approved for the work item.
-   Analyze the variance for the past fiscal periods and work on budget allocation for future fiscal periods.
-   Compare latest forecast with approved budget and revise the budget, if necessary.

</td></tr><tr><td>

Planned vs Actuals

</td><td>

Compare the planned costs with actual expense for the past and current fiscal periods, and view planned costs for the future fiscal periods.

</td></tr><tr><td>

Planned

</td><td>

View only planned costs for the full range and manage the planned costs using the inline editing feature.

</td></tr></tbody>
</table>**Note:** If you don't see the Budget allocation mode, enable it for demands and configure the budget attribute at the instance level. For more information, see [Enable financial budget allocation for demands](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/strategic-planning/enable-financial-budget-allocation-for-demands.md) and [Configure budget attribute at instance level](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/strategic-planning/configure-budget-attribute-at-instance-level-dw.md).

## Cost plans

Cost plan breakdown records are created when you save a cost plan. The cost plan breakdowns are records that specify the estimated and actual costs and the budget at a granular level for specific fiscal periods, such as FY16: M04 and FY16: M05. The demand cost plans are added to the parent program and portfolio. To use multiple currencies, create a cost plan for another currency.

If the PPM Standard Multicurrency \(com.snc.ppm\_multicurrency\) plugin is activated and the Demand Currency view is enabled, the fields in the **Financials** section differ from the Default view. For fields available only in the Demand Currency view, see [Multicurrency in Next Experience for Demand Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/strategic-planning/multicurrency-in-dw-reference.md).

**Note:** For projects, the cost plan breakdowns specify the estimated cost and actual cost at a granular level for a fiscal period of the demand cost plan. These breakdowns are recalculated in the project currency. Similarly, the estimated breakdown amounts of the planned benefit and actual benefit of the demand benefit plans are recalculated in the project currency. The project currency amounts are then rolled up to the cost plan, benefit plan, and the project records.

## Baselines

Create a baseline to capture a snapshot of the financial changes for your demands. You can create on-demand baselines or at a cadence using a scheduler job. For more information, see [Create a baseline](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/strategic-planning/create-compare-financial-baselines-dw.md).

Compare baselines to compare the difference in costs between any two baselines.

**Note:** Each baseline is tagged with a number based on the order that they're created. The Current Financials baseline captures the financials details in real-time and is represented with a flag icon \[Omitted image "fin-current-baseline-flag.png"\] Alt text:.

The Baseline comparison view helps you to understand the variance between two baselines.

\[Omitted image "demand-baseline-comparison.png"\] Alt text: Baselines comparison view.

The following widgets are available:

-   Two dedicated widgets for each baseline displaying the EAC.
-   The Variance widget displays the total variance between the EAC values of the selected baselines.
-   The Top 3 variances by cost type widget displays the top three variances contributing to the overall variance by cost type.

The widgets and the header rows are color-coded to help you identify the selected baselines.

**Tip:** Switch between different baselines from the comparison view by selecting the name of a baseline from one of the widgets.

By default, the time scale of the breakdown view is set to Month. Use the **Time scale** option to view the comparison breakdown view at monthly, quarterly, and yearly levels.

## How planned costs are compared between two baselines captured at different timestamps

Consider a demand scoped from July 2026 to December 2026, Baseline A is created on 2026-07-24 and Baseline B is created on 2026-07-26. If you compare them in July 2026, you can see the variance between the two baselines for the planned cost.

\[Omitted image "demand-baseline-comparison-1.png"\] Alt text: Baseline comparison of planned vs planned costs.

## Budget allocation

Portfolio managers can manage and approve the budget for demands. The approved budget helps demand managers to plan and meet the expenses to execute work. For more information, see [Manage demand budgets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/strategic-planning/manage-budget-of-your-demands.md).

\[Omitted image "demand-budget-allocation.png"\] Alt text: Budget allocation view for a demand.

Plan and approve the budget for a shorter planning cycle at monthly, quarterly, or yearly level using lean budgeting and funding feasibility. Lean budgeting helps portfolio managers track the value of the approved budget and plan for future fiscal periods. When budget is allocated monthly, the system rolls it up to quarterly and yearly levels. When budget is allocated at a quarterly or yearly level, the system distributes it equally at the monthly level.

**Tip:** In the budget allocation view, portfolio managers can review the EAC to understand the financial projections made by demand managers. Use the **Copy cost as budget** option to allocate the entire planned cost as budget.

Choose the cost type as the attribute to allocate and approve the budget for individual cost types such as labor, non-labor.

Budget distribution logic

The budget allocation approach introduces data‑aware budget distribution, prioritizing actuals for completed periods and planned costs for future periods. Distribution strategies vary based on data availability. The strategy applied depends on whether actuals or Estimate at Completion \(EAC\) values exist, and whether the fiscal period is past, present, or future.

Budget allocation logic is divided into three focus areas: past fiscal periods, current fiscal periods, and future fiscal periods.

1.  Past fiscal periods that have already ended.
    -   If actuals exist, the budget is distributed proportionally to actual spending. If the total budget amount equals the total actuals, the distribution exactly matches the actual values.
    -   If there are no actuals, the budget is distributed evenly across the past fiscal periods.
2.  The current fiscal year is like a mid‑year scenario where both past and future fiscal periods are available.
    -   For past or completed fiscal periods, the system distributes the budget proportionally matching the actual expenses. If there are no actual expenses, budget is allocated as zero \(0\).
    -   If planned costs exist for the current and future fiscal periods, the remaining budget is distributed proportionally based on the planned costs.
    -   If planned costs don't exist for the current and future fiscal periods, budget is distributed evenly across the fiscal periods.
3.  Future fiscal periods
    -   If planned costs exist, the remaining budget is distributed proportionally based on planned costs.
    -   If planned costs don't exist, the remaining budget is distributed evenly across the remaining fiscal periods.

|Fiscal periods|Available financial data|Distribution method|
|--------------|------------------------|-------------------|
|Past fiscal|Actual expenses|Proportional to actuals|
|Past fiscal|No financial records|No budget allocation|
|Current year – past fiscals|Actual expenses|Allocate budget proportionate to actual values|
|Current year – remaining months|Planned costs exists|Allocate budget proportionate to planned costs|
|Current year – remaining months|No planned costs|Even distribution|
|Future fiscal periods|Planned costs exist|Allocate budget proportionate to planned costs|
|Future fiscal periods|No financial records|Even distribution|

## Benefit plans

Monetary benefit plans capture potential benefits accrued while executing a demand. Non-monetary benefit plans capture the potential non-financial benefits accrued while executing a demand. You can create and manage monetary and non-monetary benefit plans and to capture the potential benefits of your planning items. For more information, see [Create a monetary benefit plan for a demand](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/strategic-planning/create-monetary-benefit-plans-for-a-demand-dw.md) and [Create a non-monetary benefit plan for a demand](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/strategic-planning/create-non-monetary-benefit-plan-for-dw.md).

Manage cost plans and benefit plans from the **Costs and benefits** tab without switching between the financials record page and benefit plan tabs. Use the side panel and grids to forecast and track monetary benefit plans.

## Simple financials

Simple financials enables you to enter preliminary high-level planned capex, opex, and benefit values from the Details page. You can do this without capturing cost plans from the Cost view. Update the simple financials values until you have the planned and actual costs captured.

\[Omitted image "demand-simple-financials.png"\] Alt text: Simple financials in the Details page of a demand.

