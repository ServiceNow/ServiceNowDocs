---
title: Close a project
description: Closing the project involves more than just changing the project state to closed.
locale: en-US
release: xanadu
product: Project Management
classification: project-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Close a project

Closing the project involves more than just changing the project state to closed.

## Before you begin

Role required: it\_project\_manager

## About this task

Post-project activities include viewing baselines and actual values to evaluate how much the project slipped from its original estimates. They also include following up on related incidents, problems, or changes that are linked to the project through the instance.

When you close a project, all project tasks and sub-projects associated with the project are closed automatically. Normally, you should not reopen a project after it is closed. Updating the project state from Closed to Work In Progress, Pending, or Open is not allowed. If you still need to reopen a closed project, reopen an existing project task or add a new task to the project. This action for a task moves the project from Closed to Work in Progress state without affecting the other closed tasks.

You can cancel the associated future resource plans and complete the allocated resource plans for a closed project.

## Procedure

1.  Verify that the work is completed for all tasks in the project.

2.  On the Project form, change the **State** field to one of the closed states:

    -   **Closed Complete**: The project is finished and all tasks are complete.
    -   **Closed Incomplete**: The project is finished, but tasks remain unfinished.
    -   **Closed Skipped**: The project was abandoned.
    Alternatively, close every project task first, starting with the lowest-level child tasks. The closed states roll up to parent tasks, and when all highest-level parent tasks are closed, the project state changes to closed. However, the default closed states for parent tasks and for the project is **Closed Complete**. Therefore, even if you change any or all project tasks to **Closed Incomplete** or **Closed Skipped**, the project state is changed to **Closed Complete**.

    Also, change the **Phase** value to **Closing**. The project phase is for reference only and is not linked to or dependent on the **State** field.

    If your project contains sub-projects, you can close the sub-project without affecting the parent project. Change the **State** of the sub-project to any closed state to close the sub-project. Closing the sub-project closes or changes the state of all the tasks associated with the sub-project. Also, changing the state of the sub-project to Work in Progress, moves all the associated tasks to Work in Progress state.

    If there are project tasks associated with the parent project that are not closed, the parent project remains in the Open, Work in Progress, or Pending state. If the tasks associated with the parent project are closed, the state of the parent project also changes to **Closed Complete**.

3.  After the project is complete, create a final baseline to see how closely the project's actual values came to the estimated values.

    **Note:** Baselines compare only planned start and end date values with actual start and end date values. Use reports to compare the effort and cost.


## Result

For projects created from an incident, problem, or change, updating the project state does not automatically update the related incident, problem, or change request record. You must update the related record manually. For example, if the completion of a project also means that a related Change can be closed, go to the Change record and modify its **State** field. It is also a good idea to update the work notes field on the related record to include any relevant information about the project.

## What to do next

-   [Cancel the resource plans](../../resource-management/task/cancel-resource-plan-from-project-or-demand.md) associated with the project in any of the following conditions:
    -   There is a corresponding resource plan in the Confirmed, Planning, or Requested state.
    -   There is a resource plan in the Allocated state with the start date later than the project end date.
-   [Complete the resource plans](../../resource-management/task/complete-resource-plan-from-project-or-demand.md) associated with the project in the following conditions:
    -   There is a corresponding resource plan in the Allocated state.
    -   The start date of the resource plan is on or before the actual end date of the project or task.

-   **[View actual project costs](../../project-portfolio-suite-with-financials/task/t_ViewActualProjectCosts.md)**  
When you are using Project Portfolio Management with Financials, you can view actual project costs on cost plans and projects.

**Parent Topic:**[Project Management](../concept/c_ProjectApplicationOverview.md)

