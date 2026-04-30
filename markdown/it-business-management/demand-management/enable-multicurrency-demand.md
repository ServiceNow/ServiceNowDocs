---
title: Enable demand currency view
description: Switch to the demand currency view to track the planned costs of a demand in the selected currency.
locale: en-US
release: yokohama
product: Demand Management
classification: demand-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Multicurrency, Configure, Demand Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Enable demand currency view

Switch to the demand currency view to track the planned costs of a demand in the selected currency.

## Before you begin

Activate the PPM Standard Multicurrency \(com.snc.ppm\_multicurrency\) plugin.

Role required: admin or it\_demand\_manager

## About this task

To manage your demands in currency different than the functional currency, the demand currency fields are added in the following tables that have the cost details and financials tab:

|Table name|Description|
|----------|-----------|
|Demand \[dmn\_demand\] table|Track a demand in a different currency. Create a demand and select another currency by navigating to the **Financial** tab and selecting a currency in the **Demand Currency** field. To create a demand, see [Create a demand](t_CreatingDemands.md).|
|Demand Task \[dmn\_demand\_task\] table|Demand tasks are used to delegate the cost, effort, risk, and benefit assessment activities. To create a demand task, see [Create a demand task](create-demand-task.md).|
|Cost Plans \[cost\_plan\] table|Cost plans capture the costs of demands. To navigate to the Cost Plan form, see [Create a demand cost plan](t_CreateADemandCostPlan.md).|
|Cost Plan Breakdown \[cost\_plan\_breakdown\] table|Cost plan breakdowns specify the estimated cost and actual cost at a granular level for a fiscal period. To navigate to the Cost Plan Breakdown form, see [Create a demand cost plan](t_CreateADemandCostPlan.md).|
|Benefit Plan \[benefit\_plan\] table|If you open the demand form in **Demand Currency** view, then by default the fields related to the demand currency appear in the Benefit Plans related list. To create a demand benefit plan, see [Create a monetary benefit plan for a demand](create-demand-benefit-plan.md).|
|Benefit Plan Breakdowns \[benefit\_plan\_breakdown\] table|Benefit plans capture the potential benefits accrued by the demand when the demand is executed. To update a benefit plan breakdown, see [Create a monetary benefit plan for a demand](create-demand-benefit-plan.md).|
|Expense Line \[fm\_expense\_line\] table|Expense lines are part of the demand cost plans and stores cost associated with a specific resource. To navigate to the Expense line form, see [Create an expense line for a demand](create_expense_line_demand.md).|
|Project Funding \[project\_funding\] table|Stores the demand target and budget expense values for both capital and operating expenses for a single fiscal period. To allocate the budget for a demand, see [Allocate budget to a demand](allocate-budget-to-demand.md).|

## Procedure

1.  Navigate to the respective form.

2.  Right-click the context menu of the form.

3.  Click **View**.

4.  Select **Demand Currency** from the list.


## What to do next

Refer to the form fields that are exclusive to the **Demand Currency** view that you have selected. All the other form tabs and fields remain the same both for the default view and the demand currency view. Continue to enter values in the fields as you would for the default view.

-   **[Multicurrency fields in demand-related forms](../reference/multicurrency-fields-demand.md)**  
When you enable the **Demand Currency** view in a Demand, Cost Plan, and Cost Plan Breakdown forms, you can observe the multicurrency fields in the Financials section of the forms.
-   **[Allocate demand budget in demand currency](allocate-budget-demand-currency.md)**  
Set the capital expense \(Capex\) and operating expense \(Opex\) budgets in demand or functional currency according to the fiscal years. The sum of the Capex and Opex budgets is calculated as the total budget in demand currency.
-   **[Cost plan updates and cost recalculation in demand currency](../concept/cost-recalculation-demand-multicurrency.md)**  
Updating the unit cost, quantity, or fiscal period of a cost plan updates all the related amount fields in the cost plan and its breakdowns. Also, the amounts in the related fields of the demand, to which the cost plan is rolling up, are recalculated and reflected in the demand currency.
-   **[Benefit plan updates and recalculation in demand currency](../concept/benefit-plan-recalculation-demand.md)**  
Updating the entered currency, entered benefit, offset type, or the fiscal period of a benefit plan also updates all related amount fields in the benefit plan and its breakdowns. Also, the amounts in the related fields of the demand, to which the benefit plan is rolling up, are recalculated and reflected in demand currency.

**Parent Topic:**[Multicurrency in Demand Management](../concept/multicurrency-demand.md)

