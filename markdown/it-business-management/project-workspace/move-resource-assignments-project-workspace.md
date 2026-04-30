---
title: Move a resource assignment in Project Workspace
description: Move the resource assignment to a new start and end dates to accommodate changes in task scheduling or resource allocation. Shift assignments to balance workloads across resources and avoid over-allocation.
locale: en-US
release: yokohama
product: Project Workspace
classification: project-workspace
topic_type: task
last_updated: "2025-07-01"
reading_time_minutes: 2
breadcrumb: [Resource assignments in Project Workspace, Plan resources, Project Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Move a resource assignment in Project Workspace

Move the resource assignment to a new start and end dates to accommodate changes in task scheduling or resource allocation. Shift assignments to balance workloads across resources and avoid over-allocation.

## Before you begin

Role required: resource\_user, resource\_manager

## About this task

-   When you move an assignment to a new start and end dates, the initial requested or approved efforts are retained for the latest duration.
-   When an assignment is moved, the Ready for review state is retained and the assignment remains accessible to resource managers for work allocation.
-   You cannot move a resource assignment if actuals efforts are entered for the work.
-   New assignment dates should be within the task duration dates.

## Procedure

1.  Navigate to **Workspaces** &gt; **Project Workspace** and open a project.

2.  View the resource assignment pane by enabling the **Resource assignments** toggle button.

    **Note:** If the **sn\_pw.enable\_resource\_planning** property is set to true, then the **Resource assignment** toggle button and resource assignment pane are displayed in Project Workspace. The default value is false. You must have the pps\_admin role to enable this property.

3.  Select a project task to view the assignments associated to the task.

4.  From the resource assignment pane, select the row context menu \(![Row context menu.](../../project-workspace/image/icon-row-context-menu.png)\) and then select **Move**.

5.  From Move assignment modal, select a **New start date** using the date picker modal.

6.  Change the assignment status using the **New status** list to one of the following available statuses.

    Changing the status is restricted to the resource\_manager role.

7.  Select **Confirm**.

    When you move the resource assignment for a group, the assignments are moved for all members of that group. You cannot move assignments for individual users within the group or for child resource assignments.


**Parent Topic:**[Resource assignments in Project Workspace](../concept/resource-assignments-pw.md)

**Related topics**  


[Extend a resource assignment](extend-resource-assignment-pw.md)

[Update resource assignment from Project Workspace](update-resource-assignment-pw.md)

[Delete a resource assignment from Project Workspace](delete-resource-assignment-pw.md)

[Update the resource allocation in a heatmap](view-allocations-heatmap-prj-wksp.md)

[Realign resource assignment to project task](realign-resource-assignment-to-task.md)

