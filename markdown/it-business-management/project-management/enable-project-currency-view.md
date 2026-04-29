---
title: Enable project currency view in project-related forms
description: Switch over to the project currency view to track the planned costs of a project in the selected project currency.
locale: en-US
release: australia
product: Project Management
classification: project-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Project Management, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Enable project currency view in project-related forms

Switch over to the project currency view to track the planned costs of a project in the selected project currency.

## Before you begin

Role required: it\_project\_manager

## About this task

To manage your projects in local currency and to create a project from a demand, the project currency fields are added in the following tables that have cost details and financials tab:

<table id="table_umn_p3v_jjb"><thead><tr><th>

Table name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Demand \[dmn\_demand\] table

</td><td>

To create a project from a demand in project currency. Specify the currency that you want to use to manage your project by navigating to the **Financials** tab of the Demand form and selecting a currency in the **Project Currency** field.**Note:** You can specify the project currency only when you switch to the Demand Currency view. For more information, see [Multicurrency in Demand Management](../../planning-and-policy/concept/multicurrency-demand.md).

To create a demand, see [Create a demand](../../planning-and-policy/task/t_CreatingDemands.md).

</td></tr><tr><td>

Project \[pm\_project\] table

</td><td>

To navigate to the Project form, see [../../project-management/reference/create-a-project-form.md](../../project-management/reference/create-a-project-form.md).

</td></tr><tr><td>

Cost Plans \[cost\_plan\] table

</td><td>

To navigate to the Cost Plan form, see [Create a project cost plan](../../project-management/task/t_CreateAProjectCostPlan.md).

</td></tr><tr><td>

Cost Plan Breakdown \[cost\_plan\_breakdown\] table

</td><td>

To navigate to the Cost Plan Breakdown form, see [Update a cost plan breakdown](../../project-management/task/update-cost-plan-breakdown.md).

</td></tr><tr><td>

Benefit Plan \[benefit\_plan\] table

</td><td>

If you open the project form in Project Currency view, then by default the project currency related fields appear in the Benefit Plans related list. To create a project benefit plan, see [Create a project benefit plan](../../project-management/task/create-project-benefit-plan.md).

</td></tr><tr><td>

Benefit Plan Breakdowns \[benefit\_plan\_breakdown\] table

</td><td>

To update a benefit plan breakdown, see [Update a benefit plan breakdown](../../project-management/task/update-benefit-plan-breakdown.md).

</td></tr><tr><td>

Expense Line \[fm\_expense\_line\] table

</td><td>

Expense lines are part of project cost plans and stores cost associated with a specific resource. To navigate to the Expense line form, see [Create an expense line](../../project-management/task/t_CreateAExpenseLine.md).

</td></tr><tr><td>

Project Funding \[project\_funding\] table

</td><td>

Stores the project target and budget expense values for both capital and operating expenses for a single fiscal period.

</td></tr></tbody>
</table>## Procedure

1.  Navigate to the respective form.

2.  Right-click the context menu of the form.

3.  Click **View**.

4.  Select **Project Currency** from the list.


## What to do next

Refer to the form fields that are exclusive to the Project Currency view that you have selected. All the other form tabs and fields remain same both for the default view and the project currency view. Continue to enter values in the fields as you would for the default view.

