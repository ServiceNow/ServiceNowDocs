---
title: Create a project task from a project
description: Create tasks from the project form to break down project objectives into manageable units of work.
locale: en-US
release: yokohama
product: Project Management
classification: project-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Starting a project, Use, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Create a project task from a project

Create tasks from the project form to break down project objectives into manageable units of work.

## Before you begin

Role required: it\_project\_manager

## Procedure

1.  Navigate to **All** &gt; **Project** &gt; **Projects** &gt; **All**.

2.  Select the project from the list.

3.  In the **Project Tasks** related list, select **New**.

4.  On the form, fill in the fields.

    For more information on project task form, see [Project task form](../reference/project-task-form.md).

5.  Select **Submit**.


## Result

The new task appears in the **Project Task** related list on the Project form. If time cards are in use, the application creates a time card for the resource.

## What to do next

The value in the **Percent complete** field is related to the **State** field in the v3 application. If you change the percentage complete from **0** to any other value, the state of the task changes to **Work in progress** when you save or update the record. Likewise, if you change the state of the task to **Closed complete**, the **Percent complete** field is set to **100** and becomes read-only.

If you change the state of a project task from **Work in progress** to **Closed Skipped** or **Closed Incomplete**, the **Percent complete** field retains the current value and becomes read-only.

The **Percent complete** field appears in the Gantt chart for parent tasks as a light-colored bar \(the part of the task that is complete\). The bar overlaps the darker, underlying bar \(the full task\). For example, a Demo project is 5.41% complete as shown in a pop-up window. The **Phase 1** task is about 50% complete \(not shown in the pop-up window\).

The Project Tasks list and the Project Tasks related list on the Project form include a **Dependency** field. Any dependencies for a task, such as a parent task, are displayed in this field. Click a dependency record. See [Predecessor dependencies in the planning console](../reference/r_ProjectTaskDependencyValues.md) for a description of what you see in this column.

-   **[Create a task from an incident, problem, or change request](t_CreateTaskIntPrblmChange.md)**  
You can create a new project task from the Project Task related list on the Incident, Problem, and Change Request forms. The tasks you create from these forms makes the project task a child of the incident, problem, or change, rather than a project.
-   **[Create tasks from project task creator](t_UseTheProjectTaskCreator.md)**  
Use the project task creator to create multiple tasks at once.
-   **[Insert a row into the project tasks list](t_InsertARowIntoTheProjectTasksList.md)**  
You can create a new project task from the Project Task related list on the Project form. Administrators must enable this task-creation feature.
-   **[Copy an existing task or project](t_CopyExistingTaskorProject.md)**  
Save time when building a project by copying tasks from other projects.
-   **[Create a task from a project task template](t_UseAProjectTaskTemplate.md)**  
You can save a project task as a template and reuse it when creating a task.
-   **[View default project and project task state categories](view-default-project-task-states.md)**  
View category information for the default project and project task states. In the base system, the states in project and project task inherit the states in Task table.
-   **[Link change requests to a project task](t_LinkChangesToAProjectTask.md)**  
Link change requests to tasks on the Project Task form. You can link change requests only to project tasks that have no child tasks.
-   **[Accept or reject project task notifications](accept-project-task-notifications.md)**  
Approve or reject the changes in a notification for an external soft dependency.
-   **[Use a project task checklist](t_CreateAProjectTaskChecklist.md)**  
You can create a checklist in a project task to track items that must be completed in the task.

**Parent Topic:**[Starting a project](t_CreateAProject.md)

**Related topics**  


[Create a parent-child relationship on the Project Task form](t_CreateParentChildRelationship.md)

[Create a monetary benefit plan for a project](create-project-benefit-plan.md)

[Create a non-monetary benefit plan for a project](create-a-non-monetary-benefit-plan-for-a-project.md)

[Associate monetary and non-monetary benefit plans](associate-monetary-and-non-monetary-benefit-plans-project.md)

[Create a project cost plan](t_CreateAProjectCostPlan.md)

[Recalculating costs of all resource plans in a project](recalculate-resource-costs-of-a-project.md)

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

