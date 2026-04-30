---
title: Create a monetary benefit plan for a project
description: Project benefit plans capture the potential benefits accrued by the project when the project is executed. Create a monetary benefit plan to specify the estimated benefit in a category spanning one or more fiscal periods.
locale: en-US
release: xanadu
product: Project Management
classification: project-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Define a project, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Create a monetary benefit plan for a project

Project benefit plans capture the potential benefits accrued by the project when the project is executed. Create a monetary benefit plan to specify the estimated benefit in a category spanning one or more fiscal periods.

## Before you begin

Role required: it\_project\_manager

## About this task

The monetary benefit plan breakdown records are automatically created when you save the benefit plan.

## Procedure

1.  Navigate to **Project** &gt; **Projects** &gt; **All**.

2.  Open the required project.

3.  In the **Monetary Benefit Plans** related list, click **New**.

    **Note:** To create a monetary benefit plan from the **Financials** tab in Project Workspace, click **Manage**.

4.  On the form, fill in the fields.

<table id="table_benefit_plan_form"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Descriptive name of the benefit plan.

</td></tr><tr><td>

Work

</td><td>

Project or demand to which the benefit plan belongs.

</td></tr><tr><td>

Sponsor

</td><td>

Sponsor for the project.

</td></tr><tr><td>

Category

</td><td>

Type of benefit:-   **Hard**: Benefits that can be measured in terms of revenue.
-   **Soft**: Benefits that are measured in terms of value.


</td></tr><tr><td>

Sub category

</td><td>

Sub-categories of hard and soft benefits.The selection in **Category** field determines the selections available in this field.

</td></tr><tr><td>

Benefit type

</td><td>

Type of benefit. Select **Monetary benefits**.

</td></tr><tr><td>

Offset type

</td><td>

Field to indicate when the benefits start realizing. Select any of the following options:-   **None**: The default value is None. When you select None, you need to manually enter the benefit plan start and end fiscal periods.
-   **Milestone**: After completion of a milestone.
-   **Start Date**: At the start of the project.
-   **End Date**: After the project ends.
 If the value in the selected offset type changes, the benefit plan start date shifts accordingly. For example, if the offset type is set to **End Date** and the end date of the project changes, the benefit plan start date shifts to align with the new end date of the project.

</td></tr><tr><td>

Milestone

</td><td>

**Note:** The field appears if you select **Milestone** in the **Offset type** field.

Project milestones to which the benefit plan belongs.

</td></tr><tr><td>

Milestone start date

</td><td>

**Note:** The field appears if you select **Milestone** in the **Offset type** field.

Start date of the selected milestone.

</td></tr><tr><td>

Work start date

</td><td>

**Note:** The field appears if you select **Start Date** in the **Offset type** field.

Start date of the project or demand.

</td></tr><tr><td>

Work end date

</td><td>

**Note:** The field appears if you select **End Date** in the **Offset type** field.

End date of the project or demand.

</td></tr><tr><td>

Offset

</td><td>

Number of periods before or after the offset type when the benefit plan starts. For example, if the offset type is selected as **End Date** and the offset is -2, the benefit plan is two periods prior to the project end date. If the project end date shifts, the benefit plan start date shifts to two periods prior to the new project due date.

</td></tr><tr><td>

Duration in periods

</td><td>

The length, in periods, of the benefit plan.

</td></tr><tr><td>

Start fiscal period

</td><td>

Starting fiscal period. Populated based on the value in the Offset field relative to the selected Milestone, Project or Demand start date, or Project or Demand end date, and Duration in period values.The field is editable if you select **None** in the **Offset type** field.

 When you change the start fiscal period, the associated benefit breakdown values also change.

</td></tr><tr><td>

End fiscal period

</td><td>

Ending fiscal period. Populated based on the value in the Offset field relative to the selected Milestone, Project or Demand start date, or Project or Demand end date, and Duration in period values.The field is editable if you select **None** in the **Offset type** field.

 When you change the end fiscal period, the associated benefit breakdown values also change.

</td></tr><tr><td>

Associated benefit

</td><td>

Non-monetary benefit that is associated to this monetary benefit plan.

</td></tr></tbody>
</table><table id="table_emz_vdg_mcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Entered benefit

</td><td>

Benefit incurred from the project or demand specified in terms of entered currency.If the selected currency is different from the functional currency, the corresponding [budget reference rate](../concept/c_BudgetReferenceRates.md) is used to calculate the **Total planned benefit** of the project.

</td></tr><tr><td>

Entered currency

</td><td>

Currency in which you want the benefit plan to be created.

</td></tr><tr><td>

Functional currency

</td><td>

Currency that is obtained from the [**glide.system.locale** property](https://www.servicenow.com/docs/access?context=currency-properties&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US). For upgraded customers, if the selected currency is different from the functional currency configured in the Financial Management application, the corresponding [budget reference rate](../concept/c_BudgetReferenceRates.md) is used to calculate the **Total planned benefit** of the project.

</td></tr><tr><td>

Total planned benefit

</td><td>

Estimated amount of potential benefit of the project or demand.

</td></tr><tr><td>

Benefit in functional currency

</td><td>

Benefit incurred from project or demand in terms of functional currency.

</td></tr><tr><td>

Actual benefit

</td><td>

Actual benefit that is incurred from the project or demand. This value is rolled up from the **Actual benefit** field of all the benefit plan breakdowns.

</td></tr><tr><td>

Recurring

</td><td>

Check box to indicate that the benefit is recurring for all the fiscal periods in the benefit plan.

</td></tr></tbody>
</table>    **Note:** When you move the project or the milestone date, the associated benefit plans also change accordingly based on whether the benefit plan is tied to the project start date, end date, or one of the project milestones. The [project property](../reference/r_InstalledWithProjectManagement.md#project_application_properties) **Change Resource Plan, Cost Plan and Benefit Plan Start Date with Demand or Project Start Date Change** controls the behavior for project date changes.

5.  Click **Submit**.


## What to do next

On the Benefit Plan form, view the benefit breakdown by fiscal period in the Monetary Benefit Plan Breakdowns related list.

-   **[Update a monetary benefit plan breakdown for a project](update-benefit-plan-breakdown.md)**  
Update a monetary benefit plan breakdown record that specifies the estimated and actual benefits, at a granular level, for specific fiscal periods.

**Parent Topic:**[Define a project](t_CreateAProject.md)

**Related topics**  


[Create and manage waterfall projects](../../project-portfolio-suite/concept/c_CreateAndManageWaterfallProjects.md)

[Copy a project](t_CopyAProject.md)

[Create baseline of a project](t_CreateAProjectBaseline.md)

[Assign a project schedule](t_UseAProjectSchedule.md)

[Create a project cost plan](t_CreateAProjectCostPlan.md)

[Create a non-monetary benefit plan for a project](create-a-non-monetary-benefit-plan-for-a-project.md)

[Associate monetary and non-monetary benefit plans](associate-monetary-and-non-monetary-benefit-plans-project.md)

[Project and portfolio funding](../../project-portfolio-suite-with-financials/concept/c_ProjectAndPortfolioFunding.md)

[Create an expense line](t_CreateAExpenseLine.md)

[Generate labor costs](gen-cost-pln-prj-wrkspc.md)

[Migrate budget of active projects to Next Experience](fin-migrate-budget-project-ppm.md)

[Migrate financial baselines of projects to Next Experience](migrate-fin-baselines-projects.md)

[Create a project status report](t_CreateAProjectStatusReport.md)

[View project status reports](project-status-report.md)

[Create a cost type definition](t_CreateAResourceTypeDefinition.md)

[Allocate budget to a project](allocate-budget-to-project.md)

[RIDAC records for a project in Project Workspace](../concept/ridac-entries-for-project.md)

