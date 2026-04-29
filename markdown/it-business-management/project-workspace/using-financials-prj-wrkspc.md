---
title: Managing financials for your projects
description: Manage budget, cost plans as forecasts, actual expenses as expense lines, generate labor costs, create financial baselines, and view, analyze, and compare the financial performance of your projects at required cadence in Project Workspace.
locale: en-US
release: australia
product: Project Workspace
classification: project-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 17
breadcrumb: [Project Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Managing financials for your projects

Manage budget, cost plans as forecasts, actual expenses as expense lines, generate labor costs, create financial baselines, and view, analyze, and compare the financial performance of your projects at required cadence in Project Workspace.

The comprehensive financials view helps you to understand planned and actual costs, Forecast \(previously EAC - Estimate At Completion\), Remaining Estimates \(previously ETC - Estimate To Completion\), Actual \(previously Actuals to date\), and so on, for the selected item. You can manage cost plans and associate the expense lines and process them to reflect the actuals for a planning item.

Export the financials data from Costs and benefits or Baseline comparison view as Microsoft Excel or a CSV file and share it with your stakeholders to review the financial performance of your projects and portfolio.

## Cost view

Forecast your planned costs, create, and manage cost plans and expense lines to track the financial performance of your projects, review the latest costs and actuals.

In the Cost screen, you can:

-   As a Project Manager, you have the enhanced visibility and ability to manage the financial data across multiple project levels. Cost view of financials shows cost plans and expense lines from sub-projects, allowing you to track the finances.
-   The parent project widgets display the consolidated values of forecasted costs and expenses.
-   Identify and manage costs using the **Project/Demand** column for any sub project or demand directly from Cost view of the parent planning item.
-   Re-forecast all the cost plan values for future fiscal periods by double-clicking to edit the value in the least time scale view, either by month or by period.
-   Manage cost plans for your projects. For more information, see [Add, edit, or delete cost plans](../task/create-cost-plan-prj-wrkspc.md).
-   Add or edit expense lines for your projects to record any planned or unplanned expenses. For more information, see [Add or edit expense lines](../task/create-expense-line-prj-wrkspc.md).
-   Generate labor costs for the fiscal period. For more information, see [Generate labor costs](../task/gen-labor-costs-prj-wrkspc.md).
-   Create and compare baselines to capture the financial snapshot of your projects. For more information, see [Create and compare financial baselines for your projects](../task/create-compare-baselines-pws.md).
-   [Configure widgets](../../spw-financials/task/configure-financial-widgets.md) to get a high-level overview of the financial data for your planning item.
-   All financial details from sub-projects will be aggregated and displayed in the parent project's cost plans and widgets.

**Tip:** Cost view gives you enhanced user experience to customize the left pane columns by using the personalize icon \(![Personalize gear icon.](../../alignment-planner-workspace/images/icon-personalize.png)\) and by saving user preferences to retain the customizations made to hide, view, or adjust columns, time scope viewing, and so on.

## Multicurrency

The multicurrency feature enables you to manage the financials of your planning items in two different currencies, Functional currency and Investment currency. Functional currency is typically defined by the admin based as the primary currency that is used for planning, budgeting, and tracking the financials of your planning items.

Financial users can now perform the following financial activities in Investment currency.

-   Ability to select the Investment currency.
-   Track the planned and actual expenses.
-   Allocate and manage the budget.
-   View simple financials data.

**Important:** New customers should install the PPM Standard Multicurrency \(com.snc.ppm\_multicurrency\) plugin to enable multicurrency feature and [Activate scheduled job to populate to multicurrency fields](../../spw-financials/task/multi-currency-scheduled-job-spw.md).

Using this feature, you can work on financial reporting at global level and see the real-time currency conversions of your financial records.

Organizations operation at global or multinational level, the work is planned and financed at one location and executed at a different location. Each might use a different currency from what was used in the planning phase, multicurrency makes it easy to manage and track your planning items using any currency.

You can monitor and track the financials in one currency, and capture the costs in a different currency.

Using multicurrency, you can see all the costs in the currency you choose for the planning item, instead of restricting to use Functional currency defined in your locale. For more information on how to choose investment currency of your planning items, see [Configure multicurrency for projects](../task/config-investment-currency-pws-fin.md).

Financial records and widgets will display the costs based on the currency selection.

**Note:** Once a cost plan, benefit plan or expense line or an investment budget gets created, you won’t be able to change investment currency. You can change the investment currency as long as there are no financial records captured against the planning item.

## Display modes

On the financials page for a planning item in Project Workspace, you have Display Mode drop-down switch between different modes to view different formats of financial information of your planning items. These views provide the relevant and focused information which helps project managers and funding users to work on the financial planning.

-   Forecast
-   Budget vs forecast
-   Planned vs actual
-   Planned

Users with financial funding role \[it\_portfolio\_manager\] will see Budget allocation option instead of the Budget vs forecast.

<table id="table_pnt_1wr_bgc"><thead><tr><th>

Mode

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Forecast

</td><td>

View Actuals, Remaining estimates, and Forecast for the entire scope of the planning items.Use the time scale to view the actuals for the past fiscal periods and planned costs for the current and future fiscal periods.

</td></tr><tr><td>

Budget vs forecast

</td><td>

View the Budget, Actuals, and Variance for the fiscal periods and Forecast values for the entire scope of the planning items.Using this mode, you can:

-   Compare the latest forecasts with the approved budget at different time scales.
-   View the budget vs actual for past fiscal periods and budget vs planned for current and future fiscal periods at fiscal period level.

</td></tr><tr><td>

Budget allocation \(funding role\)

</td><td>

View the Budget, Actuals, and Variance for the fiscal periods and Forecast values for the entire scope of the planning items. Using this mode, funding users can:

-   View the latest forecast and enter the budget that can they be approved to the work item.
-   Analyze the variance for the past fiscal periods and work on budget allocation for future fiscal periods.
-   Compare latest forecast with approved budget and revise the budget, if necessary.

</td></tr><tr><td>

Planned vs actual

</td><td>

Compare the planned costs with actual expense for the past and current fiscal periods, and view planned costs for the future fiscal periods.

</td></tr><tr><td>

Planned

</td><td>

View only planned costs for the full range and manage the planned costs using the inline editing feature.

</td></tr></tbody>
</table>**Note:**

-   If you don’t see the Budget allocation or Budget vs forecast display options, [enable the budget allocation property](../task/enable-fin-budget-pws.md) and [configure the budget attribute](../task/config-budget-allocation-attribute-pws.md) at instance level.
-   To work on budget allocation using the Next Experience, [Activate a scheduled job to migrate budget of your planning items](../../spw-financials/task/fin-migrate-budget-scheduled-job-spw.md).

The last selected view is saved as user preferences.

|User role|Default mode|Role-level access|
|---------|------------|-----------------|
|it\_portfolio\_manager|Budget Allocation|Allocate and approve budget, manage cost plans and expenses lines.|
|it\_project\_manager|Forecast|Manage cost plans and expense lines.|
|business\_stakeholder|Forecast|View financial data.|

## Baseline view

Create a financial to capture a snapshot of the financial changes for your projects. You can create on-demand baselines manually or automatically at a required cadence using a scheduler job. For more information, see [Create a baseline](../../spw-financials/task/create-compare-baselines.md#ol_tgp_v2k_2zb)

**Note:** Baselines created on the parent project include cost plans and expense lines from all of the child projects to calculate and give you a better breakdown of the financial performance of the projects and sub-projects.

[Compare baselines](../../spw-financials/task/create-compare-baselines.md#ol_lrh_3gk_2zb) to compare the difference in costs between latest status against a baseline or between any two baselines.

**Note:** Each baseline is tagged with a number based on the order that they’re created. The Current Financials baseline captures the financials details in real-time and is always represented with a flag icon \(![Flag icon to indicate current baseline.](../../spw-financials/images/fin-current-baseline-flag.png)\).

Financial baselines now capture the investment currency for customers using multicurrency.

A project baseline includes the following financial metrics in investment currency.

-   Investment currency
-   Total planned cost
-   Planned benefit
-   Planned return
-   Budget cost

At the investment baseline level, a corresponding investment baseline is automatically created. This baseline captures:

-   Planned cost
-   Actual cost
-   Planned benefit
-   Actual benefit
-   Total budget
-   Capex, Opex, and breakdown of these fields
-   Benefits, and so on

All values are populated along with their respective investment currency.

Cost plan baselines now store actual cost values in investment currency, along with the investment currency field. Benefit plan baselines capture benefit values in the investment currency, along with the associated currency. At the breakdown level \(for example, fiscal period or monthly breakdowns\), actual cost and actual benefit values are populated in investment currency where actuals exist.

**Note:** Comparison of financial baselines using multicurrency is not yet supported.

You can view the planning item and investment baseline using the list view. Access the `pm_project_baseline` list to view project baselines, and `sn_invst_pln_invst_investment_baseline` to view the investment baselines.

The baselines comparison view helps you to understand the variances between the two baselines.

![Baselines comparison view.](../../spw-financials/images/fin-baselines-comparison.png)

Use the widgets when you compare baselines to view:

-   Two dedicated widgets for each baseline displaying the EAC.
-   The third widget displays the total variance between the EAC values of the selected baselines.
-   The fourth widget displays the top three variances contributing to the overall variance by cost type.

The widgets and the header rows are color-coded to help you identify the selected baselines.

**Tip:** Switch between different baselines from the comparison view by selecting the name of a baseline from one of the widgets.

When you compare baselines, you get the list of cost plans with their associated costs types, EAC at full scope, and a breakdown view of actual expenses and planned costs.

By default, the time scale of the breakdown view is set to Month.

-   Use the **Time scale** option to view the comparison breakdown view at monthly, quarter, and yearly levels.
-   Select **Time scope** to filter fiscal periods, data in the widgets, and the comparison table.

The widgets and the header rows are color-coded to help you identify the selected baselines.

**Tip:** Select the name of a baseline from the first or second widget to compare different baselines.

Let's take an example of the comparison view of two baselines: 2023-10-01, Baseline A, and Current Financials, Baseline B.

## How actuals, planned, and EAC are compared between two baselines captured at different timestamps

For a selected baseline, based on the creation date, the table shows Actuals values for the past fiscal periods from the created date and Planned values for the current and future fiscal periods.

Consider a planning item scoped from July 2023 to June 2024. Baseline A is created on 2023-10-01. If you compare the Current Financials baseline in December 2023 to the baseline captured in October 2023:

1.  The baseline comparison view show Actuals vs Actuals columns from July 2023 to September 2023.

    ![Baseline comparison of actual vs actual costs.](../../spw-financials/images/fin-baselines-actuals-vs-actuals.png)

2.  Planned vs Actuals for October 2023 and November 2023.

    ![Baseline comparison of planned vs actual costs.](../../spw-financials/images/fin-baselines-planned-vs-actuals.png)

3.  Planned vs Planned from December 2023 to June 2024.

    ![Baseline comparison of planned vs planned costs.](../../spw-financials/images/fin-baselines-planned-vs-planned.png)


**Note:** The columns are defined to calculate EAC, which is the sum of Actual costs until the last fiscal period and Planned costs from current to future fiscal periods.

## Budget allocation

Portfolio managers can manage and approve the budget for projects. The approved budget helps project managers to plan and meet the expenses to execute work.

![Project Workspace financials view for Cost vs. Budget.](../images/fin_cost_view_pws.png)

Plan and approve the budget for a shorter planning cycle at monthly, quarterly, or yearly level using the lean budgeting and funding feasibility. Lean budgeting helps Portfolio managers to track the value in return for the approved budget and to better plan the budget for future fiscal periods.

**Note:** If the budget is allocated monthly, the total budget is rolled up to quarterly and yearly level. Similarly, if the budget is allocated at a quarterly or yearly level, the equal breakdown happens till monthly level.

For more information on how to allocate, approve, and handle budget for projects, see, [Manage budget of your planning items in Strategic Planning](../../spw-financials/task/fin-manage-budget-spw.md).

**Tip:** In the budget allocation view, Portfolio managers review the EAC to understand the financial projections made by Project managers and use the **Copy cost as budget** option to allocate the entire planned cost as budget.

Choose the cost type as the attribute to allocate and approve the budget for individual cost types such as labor, non-labor.

Project managers can view the approved budget at the required time scale by switching to the Budget vs planned display mode. As the work progresses and the actuals are captured, you can compare the budget and actual costs using Budget vs planned display mode and reforecast the planned costs where the actuals are exceeding the budget using the inline edit feature at the required time scale.

Product managers can compare the latest cost with the approved budget by Capex or Opex, cost types, and for the required time scale at monthly, quarterly, or yearly level. The comparison view provides insights to Product managers to locate any variance at expense type or cost type, and at which fiscal period. Product manager can leverage this information to request for additional budget from the Portfolio manager.

You can [migrate the budget of existing active projects](../../project-management/task/fin-migrate-budget-project-ppm.md) from the Classic UI to Next Experience. Financials in the Next Experience has new budget data model that facilitates to store the budget at a detailed level by monthly breakdowns and cost types. You can migrate the budget for active projects and demands individually or by bulk using the scheduled job.

**Note:** The migrated budget is captured in the `sn_invst_pln_invst_budget` table to enable the lean budgeting for required time scope.

Budget distribution logic

The budget allocation approach introduces data‑aware budget distribution, prioritizing actuals for completed periods and planned costs for future periods. The system uses different distribution strategies depending on whether actuals or Estimate at Completion \(EAC\) values are available, and whether the fiscal period falls in the past, present, or future.

Budget allocation logic is divided into three focus areas: past fiscal periods, current fiscal periods, and future fiscal periods.

1.  Past fiscal periods that have already ended.
    -   If actuals exist, the budget is distributed proportionally to actual spending. If the total budget amount equals the total actuals, the distribution exactly matches the actual values.
    -   If there are no actuals, the budget is distributed evenly across the past fiscal periods.
2.  The current fiscal year is like a mid‑year scenario where both past and future fiscal periods are available.
    -   For past or completed fiscal periods, the system distributes the budget proportionally matching the actual expenses. If there are no actual expenses, budget is allocated as zero \(0\).
    -   If planned costs exists for the current and future fiscal periods the remaining budget is distributed proportionally based on the planned costs.
    -   If planned costs doesn't exists for the current and future fiscal periods, budget is distributed evenly across the fiscal periods.
3.  Future fiscal periods
    -   If planned costs exists, the remaining budget is distributed proportionally based on planned costs.
    -   If planned costs doesn't exists, the remaining budget is distributed evenly across the remaining fiscal periods.

|Fiscal periods|Available financial data|Distribution method|
|--------------|------------------------|-------------------|
|Past fiscal|Actual expenses|Proportional to actuals|
|Past fiscal|No financial records|No budget allocation|
|Current year – past fiscals|Actual expenses|Allocate budget proportionate to actual values|
|Current year – remaining months|Planned costs exists|Allocate budget proportionate to planned costs|
|Current year – remaining months|No planned costs|Even distribution|
|Future fiscal periods|Planned costs exists|Allocate budget proportionate to planned costs|
|Future fiscal periods|No financial records|Even distribution|

## Benefit plans

Monetary benefit plans capture potential benefits accrued while executing a planning item. Non-monetary benefit plans capture the potential non-financial benefits accrued while executing a planning item. You can create and manage [monetary benefit plans](../../spw-financials/task/fin-manage-monetary-benefit-plans-spw.md) and [non-monetary benefit plans](../../spw-financials/task/fin-manage-non-monetary-benefit-plans-spw.md) to capture the potential benefits of your planning items.

Instead of switching to and fro from the financials record page to benefit plan tabs, you now have a seamless experience to manage all the cost plans and benefit plans from the Cost and benefits view and can leverage the new financials experience with the side panel and grids for quick forecasting and tracking of monetary benefit plans.

## Simple financials

Simple financials gives you the ability to enter the preliminary high-level planned capex, opex, benefit, and so on from the Details page without capturing the costs plans from the Cost view. You can update the simple financials values as required until you have the planned and actual costs captured.

![Simple financials view in the Details page of Project Workspace.](../images/fin_simple_financials_pws.png)

Using the baseline feature, you can capture these simple financial values in a baseline and compare them against any existing baseline. You can:

-   Reforecast simple financials and compare the by selecting the Current Financials from the list of baselines.
-   Capture the planned and actual expenses as the project progresses and compare any financial baseline with simple financials baseline to track the financial performance of the project.

-   **[Configure multicurrency for projects](../task/config-investment-currency-pws-fin.md)**  
Select investment currency as an additional currency, which can be different from your functional currency, to manage financial records of your projects.
-   **[Add, edit, or delete cost plans](../task/create-cost-plan-prj-wrkspc.md)**  
Create a cost plan for a required duration to track your planned and actual expenses. Edit cost plans to adjust your planned expenses and delete any de-scoped forecasts.
-   **[Manage budget of your projects using Project Workspace](../task/fin-manage-budget-pws.md)**  
Allocate, manage, and approve budget for your projects. Lean budgeting enables you to allocate budget for short planning cycles for different fiscal periods such as monthly, quarterly, or yearly breakdown level rather than allocating the budget to the complete duration of the planning item.
-   **[Add or edit expense lines](../task/create-expense-line-prj-wrkspc.md)**  
Create or edit expense lines to capture the actual costs. You can associate the expense lines with a cost plan or create standalone expense lines to record unplanned expenses.
-   **[Generate labor costs](../task/gen-labor-costs-prj-wrkspc.md)**  
Generate labor costs in the Financials view for attribute-based resource assignments based on the financial attributes configured in the planning attributes page.
-   **[Create and compare financial baselines for your projects](../task/create-compare-baselines-pws.md)**  
Create and compare financial baselines to get a snapshot of the project expenses and compare the planned costs with the actual expenses.
-   **[Create monetary benefit plans for your projects in Project Workspace](../task/fin-manage-monetary-benefit-plans-pws.md)**  
Create and manage monetary benefit plans to capture the potential benefits while executing your projects.
-   **[Manage non-monetary benefit plans for your planning items in Portfolio Planning](../task/fin-manage-non-monetary-benefit-plans-pws.md)**  
Create and manage monetary benefit plans to capture the potential benefits while executing your planning items.
-   **[Export financials as Excel or CSV file](../task/export-financials-pws.md)**  
Export the costs or baseline comparison data of your projects to share them with your stakeholders.

**Parent Topic:**[Project Workspace](../../project-workspace/concept/project-workspace-landing-page.md)

