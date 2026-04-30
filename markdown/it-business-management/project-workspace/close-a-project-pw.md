---
title: Closing a project in Project Workspace
description: End the project when all tasks are completed. When you close a project, all project tasks, sub-projects, and resource assignments associated with the project are closed automatically.
locale: en-US
release: yokohama
product: Project Workspace
classification: project-workspace
topic_type: task
last_updated: "2025-06-20"
reading_time_minutes: 3
breadcrumb: [Manage Projects, Project Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Closing a project in Project Workspace

End the project when all tasks are completed. When you close a project, all project tasks, sub-projects, and resource assignments associated with the project are closed automatically.

## Before you begin

Role required: it\_project\_manager

## About this task

Ideally, you should not reopen a project after it is closed. Updating the project state from Closed to Work In Progress, Pending, or Open is not allowed. If you still need to reopen a closed project, reopen an existing project task or add a new task to the project. This action for a task moves the project from Closed to Work in Progress state without affecting the other closed tasks. You can cancel the associated future resource plans and complete the allocated resource plans for a closed project.

## Procedure

1.  Open a project from the planning page of Project Workspace.

    For information on how to navigate to the planning page, see [Access the new Project Workspace](access-new-project-workspace.md).

2.  Verify that your work is completed for all the tasks in the project you want to close.

3.  On the Project form, change the state field to one of the closed states:

    -   Closed complete
    -   Closed Incomplete
    -   Closed skipped

        **Note:**

        -   When you close a project, a notification is displayed, which enables you to view all resource assignments associated with the project. You can synchronize all resource assignment dates with project dates. The resource assignment ends on the exact date and time that the project ends.
        -   You can track, modify, and synchronize all resource assignments for a project from the Resource Assignment List page.
    Alternatively, close every project task first, starting with the lowest-level child tasks. The closed states roll up to parent tasks, and when all highest-level parent tasks are closed, the project state changes to closed. However, the default closed states for parent tasks and for the project is **Closed Complete**. Therefore, even if you change any or all project tasks to **Closed Incomplete** or **Closed Skipped**, the project state is changed to **Closed Complete**.

    Also, change the **Phase** value to **Closing**. The project phase is for reference only and isn’t linked to or dependent on the **State** field.

    If your project contains sub-projects, you can close the sub-project without affecting the parent project. Change the **State** of the sub-project to any closed state to close the sub-project. Closing the sub-project closes or changes the state of all the tasks associated with the sub-project. Also, changing the state of the sub-project to Work in Progress, moves all the associated tasks to Work in Progress state.

    If there are project tasks associated with the parent project that are not closed, the parent project remains in the Open, Work in Progress, or Pending state. If the tasks associated with the parent project are closed, the state of the parent project also changes to **Closed Complete**.

4.  After the project is complete, create a final baseline to see how closely the project's actual values came to the estimated values.

    **Note:** Baselines compare only planned start and end date values with actual start and end date values. Use reports to compare the effort and cost.


## Result

For projects created from an incident, problem, or change, updating the project state does not automatically update the related incident, problem, or change request record. You must update the related record manually. For example, if the completion of a project also means that a related Change can be closed, go to the Change record and modify its **State** field. It is also a good idea to update the work notes field on the related record to include any relevant information about the project.

**Parent Topic:**[Managing projects with Project Workspace](../concept/use-projects-pw.md)

**Related topics**  


[Export a project from Project Workspace](export-project-to-powerpoint-from-project-workspace.md)

[Add a RIDAC record to a project in Project Workspace](add-risk-project-project-workspace.md)

