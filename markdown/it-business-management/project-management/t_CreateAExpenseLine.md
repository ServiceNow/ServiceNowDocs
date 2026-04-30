---
title: Create an expense line
description: A project expense line is cost associated with a specific source, such as a user, fixed asset, or a CI. Expense lines are part of project cost plans.
locale: en-US
release: xanadu
product: Project Management
classification: project-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Define a project, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Create an expense line

A project expense line is cost associated with a specific source, such as a user, fixed asset, or a CI. Expense lines are part of project cost plans.

## Before you begin

Role required: it\_project\_manager

Application required: Project Portfolio Management with Financials

## About this task

Only processed expense lines are considered for projects, project tasks, and demands. You can create multiple expense lines for a project or demand.

## Procedure

1.  Open the project form.

2.  In the related lists, click **Cost Plans**.

3.  Right-click on a cost plan.

4.  Click **Create Expense Line**.

5.  Fill out the expense line form \(see table\).

6.  Click **Submit**.

<table id="table_mb3_rfw_1r"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Auto generated number.

</td></tr><tr><td>

Amount

</td><td>

Select a currency type and enter the expense cost.

</td></tr><tr><td>

Date

</td><td>

Date of the expense generated.

</td></tr><tr><td>

Process date

</td><td>

Date on which the expense line was processed.

</td></tr><tr><td>

Source ID

</td><td>

Record that generated the associated cost.

</td></tr><tr><td>

State

</td><td>

State of the expense line. The state can be Pending or Processed. The cost roll-up happens only if the expense line is processed.

</td></tr><tr><td>

Cost plan

</td><td>

Name of the cost plan against which you want to create the expense line.

</td></tr><tr><td>

Summary type

</td><td>

Select the category you want to group the expense under.

</td></tr><tr><td>

Cost type

</td><td>

Select the [cost type](t_CreateAResourceTypeDefinition.md).

</td></tr><tr><td>

Expense type

</td><td>

Select **Capex** for a capital expense or **Opex** for an operating expense.

</td></tr><tr><td>

Short description

</td><td>

Enter a short description of the expense type.

</td></tr><tr><td>

Sources

</td><td>

Select the records for the sources of the expense line. These sources include:-   **Assets**
-   **Fixed assets**
-   **Contracts**
-   **Users**
-   **Configuration items**
-   **Tasks**
-   **Cost centers**


</td></tr></tbody>
</table>    **Note:**

    -   Imported processed expense lines are not rolled up to the Total actual cost field in Cost Plans.
    -   If you change the **Amount** of a Pending expense line and change the state to Processed, the latest value is captured in expense line and the same is rolled up to Total actual costs in Cost Plans.

## Result

Once the expense line is processed, the actual amount incurred becomes part of the cost plan.

The actual amount spent is recorded against the project cost plan under the appropriate expense type: **Capex** or **Opex**. Not providing a cost plan reference when creating an expense line, the actual cost is recorded at the project level in the cost plan related list.

If you create an expense line without populating the **Cost Plan** field, a [system-generated cost plans](../concept/system-generated-costplan.md) is created.

**Parent Topic:**[Define a project](t_CreateAProject.md)

**Related topics**  


[Create and manage waterfall projects](../../project-portfolio-suite/concept/c_CreateAndManageWaterfallProjects.md)

[Copy a project](t_CopyAProject.md)

[Create baseline of a project](t_CreateAProjectBaseline.md)

[Assign a project schedule](t_UseAProjectSchedule.md)

[Create a project cost plan](t_CreateAProjectCostPlan.md)

[Create a monetary benefit plan for a project](create-project-benefit-plan.md)

[Create a non-monetary benefit plan for a project](create-a-non-monetary-benefit-plan-for-a-project.md)

[Associate monetary and non-monetary benefit plans](associate-monetary-and-non-monetary-benefit-plans-project.md)

[Project and portfolio funding](../../project-portfolio-suite-with-financials/concept/c_ProjectAndPortfolioFunding.md)

[Generate labor costs](gen-cost-pln-prj-wrkspc.md)

[Migrate budget of active projects to Next Experience](fin-migrate-budget-project-ppm.md)

[Migrate financial baselines of projects to Next Experience](migrate-fin-baselines-projects.md)

[Create a project status report](t_CreateAProjectStatusReport.md)

[View project status reports](project-status-report.md)

[Create a cost type definition](t_CreateAResourceTypeDefinition.md)

[Allocate budget to a project](allocate-budget-to-project.md)

[RIDAC records for a project in Project Workspace](../concept/ridac-entries-for-project.md)

