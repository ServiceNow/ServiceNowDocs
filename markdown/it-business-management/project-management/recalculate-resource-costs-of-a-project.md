---
title: Recalculating costs of all resource plans in a project
description: Recalculate the resource costs of all resource plans in a project whenever the hourly rates change in the associated rate model so that the plan costs are up to date.
locale: en-US
release: yokohama
product: Project Management
classification: project-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Starting a project, Use, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Recalculating costs of all resource plans in a project

Recalculate the resource costs of all resource plans in a project whenever the hourly rates change in the associated rate model so that the plan costs are up to date.

## Before you begin

Ensure the following setup:

-   The project must be active.
-   The project must have an active rate model assigned.
-   The resource plans must be in the Planned, Requested, Confirmed, or Allocated state.

Role required: project\_manager

## About this task

This option recalculates the costs of all resource plans of the project at once. You can also open a resource plan from the **Resource Plans** related list to [recalculate the resource costs of an individual resource plan](../../resource-management/task/recalculate-resource-costs.md).

## Procedure

1.  Navigate to **All** &gt; **Project** &gt; **Projects** &gt; **All**.

2.  Open a project.

3.  On the Project form, right-click on the header bar and select the **Recalculate Resource Costs** option.

4.  In the Recalculate Resource Cost dialog box, fill in the fields.

<table id="table_recalculate_resource_costs_project"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Start date

</td><td>

Start date of the time period for which the costs are recalculated.By default, the field shows the current date.

</td></tr><tr><td>

End date

</td><td>

End date of the time period for which the costs are recalculated.By default, the field shows the end date of the project.

</td></tr><tr><td>

Planned costs for Requested Resource plans

</td><td>

Option for recalculating the planned cost of Requested resource plans.

</td></tr><tr><td>

Confirmed/Allocated costs for Confirmed/Allocated resource plans

</td><td>

Option for recalculating the confirmed or allocated cost of Requested resource plans.

</td></tr><tr><td>

Planned costs for Confirmed/Allocated resource plans

</td><td>

Option for including the planned cost of a Confirmed or Allocated plan.The option is enabled if the **Confirmed/Allocated costs for Confirmed/Allocated resource plans** option is selected.

 By default, the option is not selected.

</td></tr></tbody>
</table>5.  Select **OK**.


## Result

-   Recalculates the selected resource costs of all the applicable resource plans in the project based on the latest hourly rates. The hourly rates are derived from the rate model associated with the project.
-   Updates the recalculated resource costs on the respective cost fields on the resource plan form and the Resource Plans related list.
-   Reflects the revised values on the respective cost fields of the project.

**Parent Topic:**[Starting a project](t_CreateAProject.md)

**Related topics**  


[Create a project task from a project](t_CreateATaskFromAProject.md)

[Create a parent-child relationship on the Project Task form](t_CreateParentChildRelationship.md)

[Create a monetary benefit plan for a project](create-project-benefit-plan.md)

[Create a non-monetary benefit plan for a project](create-a-non-monetary-benefit-plan-for-a-project.md)

[Associate monetary and non-monetary benefit plans](associate-monetary-and-non-monetary-benefit-plans-project.md)

[Create a project cost plan](t_CreateAProjectCostPlan.md)

[Create an expense line](t_CreateAExpenseLine.md)

[Create and manage waterfall projects](../../project-portfolio-suite/concept/c_CreateAndManageWaterfallProjects.md)

[Update a project](t_UpdateAProjectInProgress.md)

[Copy a project](t_CopyAProject.md)

[Assign a project schedule](t_UseAProjectSchedule.md)

[Create baseline of a project](t_CreateAProjectBaseline.md)

[Create a milestone](t_CreateMilestones.md)

[Activate project task email notifications](t_ActivateProjTaskEmailNot.md)

[Change the planned start date of a project](change-planned-start-date-of-project.md)

[Create a cost type definition](t_CreateAResourceTypeDefinition.md)

[Costing add-on in Project Management](../concept/c_ProjectManagementCostingAddOn.md)

[Generate labor costs](gen-cost-pln-prj-wrkspc.md)

[Create a project status report](t_CreateAProjectStatusReport.md)

[Allocate budget to a project](allocate-budget-to-project.md)

[Migrate budget of active projects to Next Experience](fin-migrate-budget-project-ppm.md)

[Migrate financial baselines of projects to Next Experience](migrate-fin-baselines-projects.md)

