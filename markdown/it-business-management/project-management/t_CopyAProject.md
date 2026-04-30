---
title: Copy a project
description: Another option for creating a project is to copy an existing project with all its tasks and relationships. After you specify the start date for the copy, the system adjusts all task start and end dates automatically.
locale: en-US
release: zurich
product: Project Management
classification: project-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Starting a project, Use, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Copy a project

Another option for creating a project is to copy an existing project with all its tasks and relationships. After you specify the start date for the copy, the system adjusts all task start and end dates automatically.

## Before you begin

Role required: it\_project\_manager

## Procedure

1.  On the Project form, select additional actions icon \(![additional actions icon.](../../agile-development/image/additional-options.png)\) and select **Copy Project**.

2.  On Copy the selected project modal, enter the **New Project Name**.

3.  Select a **Start date** and select **OK**.

    Copy partial project, which is available from the Project Task form, provides similar functionality. It copies all task or project relationships and children from the selected project and inserts them into the current project. In this case, a new project record is not created.


## Result

Actual duration and the actual start and end dates are reset to null values. The state is set to **New** and percent complete is set to **0**.

By default only the short description, planned dates and duration fields are copied from source project to the target project. If additional columns must be copied, they should be declared in the [project property](../reference/r_InstalledWithProjectManagement.md#project_application_properties) **List of attributes that will be copied from the originating project task**.

-   **[Change default values of copied project](t_ModifyTheCopyProjectUIPage.md)**  
Reset or change the default values for copied fields in the new copied partial or complete project.

**Parent Topic:**[Starting a project](t_CreateAProject.md)

**Related topics**  


[Create a project task from a project](t_CreateATaskFromAProject.md)

[Create a parent-child relationship on the Project Task form](t_CreateParentChildRelationship.md)

[Create a monetary benefit plan for a project](create-project-benefit-plan.md)

[Create a non-monetary benefit plan for a project](create-a-non-monetary-benefit-plan-for-a-project.md)

[Associate monetary and non-monetary benefit plans](associate-monetary-and-non-monetary-benefit-plans-project.md)

[Create a project cost plan](t_CreateAProjectCostPlan.md)

[Recalculating costs of all resource plans in a project](recalculate-resource-costs-of-a-project.md)

[Create an expense line](t_CreateAExpenseLine.md)

[Create and manage waterfall projects](../../project-portfolio-suite/concept/c_CreateAndManageWaterfallProjects.md)

[Update a project](t_UpdateAProjectInProgress.md)

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

[Change default values of copied project](t_ModifyTheCopyProjectUIPage.md)

