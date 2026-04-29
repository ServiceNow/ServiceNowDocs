---
title: Parent-child rollup task calculations
description: Date changes, stage changes, and value calculations roll up from child tasks to parent tasks.
locale: en-US
release: australia
product: Project Management
classification: project-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Basics of Project Management, Exploring Project Management, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Parent-child rollup task calculations

Date changes, stage changes, and value calculations roll up from child tasks to parent tasks.

-   Date changes involve modifying the planned start or end date of a parent task based on those values in child tasks.
-   State changes involve modifying the state of the project record or parent task records when all child records are set to a certain state.
-   Calculations involve summing the values of child tasks and then automatically updating the parent to reflect a new total.

The following fields change on rollup tasks:

-   **Planned Start date**: Set to read only for parent tasks. Remains editable for the project record \(also considered the top-level task\).
-   **Planned End Date**: Becomes read only.
-   **Planned Duration**: Becomes read only.
-   **Actual Start Date**: Becomes read only.
-   **Actual end date**: Becomes read only.
-   **State**: Becomes read only.

## Duration Rollups

Rollups are calculated for the following items:

-   **Planned duration and planned effort**: the sum of all planned duration and planned effort values for all child tasks.
-   **Actual duration and actual effort**: the sum of all actual duration and actual effort values. Actual duration and actual effort values are calculated when all child tasks are in the **Closed Complete** state. Actual effort values can include rollups from time cards.

**Note:** Verify that the time card property **com.snc.time\_card.update.effort** is enabled. Navigate to **System Properties** &gt; **All Properties** to enable this property.

## Cost Rollups

Cost calculations roll up when the costing add-on is active.

-   **Estimated cost**: The sum of all cost estimates at the beginning of a project. Estimated costs of child tasks roll up to parent tasks and to the project.
-   **Actual cost**: By default for the project, the sum of all costs of all the expense lines, and are typically associated with a time card and a labor rate. To track costs, you can derive rates using any of the following options:

    -   Associate a [rate model](../../project-portfolio-suite-with-financials/concept/rate-model.md) to the project.
    -   Define rate cards for the task and labor expenses.
    -   Associate rate at the resource plan level.
    These rates automatically generate expense lines showing actual expenditures, which are associated with the projects. If rate cards are defined, the task expense lines are generated as each project task closes, and labor expense lines are generated when time cards are approved. Expense lines are visible in the **Expense Lines** related list, which requires the **Advanced view** on both Project and Project Task forms.


To ensure actual costs of child tasks correctly roll up to the project and added to project expense lines, the following must be true:

-   The `com.snc.project.rollup.cost` property must be set to **true**. To enable this property, navigate to **Project Administration** &gt; **Settings** &gt; **Preferences - Project** and select the **Enable project cost rollup** check box.
-   The `glide.cost_mgmt.process_task_top_task` property must be set to false. Go to the costing properties in the Cost Management application. Check the **When creating a task expense line should the system also create expense lines for the task's top task box** is not checked.
-   The `glide.cost_mgmt.calc_actual_cost` property must be set to true. Go to the costing properties in the Cost Management application. Check the **For planned tasks types, calculate the actual cost field using the total of expense lines for the task** box.

## Project State Rollups and Roll Downs

Project task states roll up. The state of parent tasks becomes read only, and changes automatically when you change the states of child tasks.

Project task states can roll up if:

-   The state of the child task is manually changed and there are no other conditions on the parent task.
-   The state of the child task is changed to **Work in Progress** or **Closed**. These states roll up to the parent. **Pending** and **Open** do not roll up to the parent task.

Project states can also roll down. If you change the state of a project to closed, all tasks under it change to the default closed value \(**Closed Complete**\). If a closed project or closed task is reopened, all tasks under it change as follows:

-   Project or parent changed from closed to **Pending** or **Open**: Child tasks change to **Open**.
-   Project or parent changed from closed to **Work in Progress**:
    -   Child tasks with a **Start on** date that has passed are changed to start **ASAP** and the state is changed to **Work in Progress**.
    -   Child tasks with a **Start on** date that has not yet passed retain the same start on date but the state is changed to **Open**.

**Parent Topic:**[Basics of Project Management](c_ProjectTasks.md)

**Related topics**  


[Project tasks](../task/t_CreateAProjectTask.md)

[Schedule conflicts between project tasks](scheduling-conflicts.md)

[Change requests and project tasks](c_ChangeRequestsAndProjectTasks.md)

[Project task checklists](c_project-task-checklists.md)

[Task resources](c_TaskResources.md)

[Project and project task states](project-and-project-task-states.md)

[Composite Fields](pm-composite-fields.md)

[Cost plan breakdown](cost-plan-breakdown.md#)

[Actual project costs](actual-project-costs.md)

[Types of external dependencies](external-dependency-types.md)

[Project and portfolio funding](../../project-portfolio-suite-with-financials/concept/c_ProjectAndPortfolioFunding.md)

[Project scheduling in Project Management](project-scheduling.md)

[Task constraints](task-constraints-project-management.md)

[Create a parent-child relationship on the Project Task form](../task/t_CreateParentChildRelationship.md)

