---
title: Create resource assignments using Project Workspace
description: Create an attribute-based resource assignment in the Project Workspace application for any project or project task.
locale: en-US
release: australia
product: Resource Management
classification: resource-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Manage resource assignments from Project Workspace, Use, Resource Management Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Create resource assignments using Project Workspace

Create an attribute-based resource assignment in the Project Workspace application for any project or project task.

## Before you begin

After a resource assignment is created, a Resource Plan is created automatically in the back-end. The resources are allocated to the project and approved by the Resource Manager. You can edit the assignment throughout the project life cycle.

Role required: it\_project\_manager

## Procedure

1.  Navigate to **Workspaces** &gt; **Project Workspace** and open a project.

2.  View the resource assignment pane by enabling the **Resource assignments** toggle button.

    **Note:** If the **sn\_pw.enable\_resource\_planning** property is set to true, then the **Resource assignment** toggle button and resource assignment pane are displayed in Project Workspace. The default value is false. You must have the pps\_admin role to enable this property.

3.  From the Planning pane, double-click the **Resource assignees** field for a project task.

    You can assign the resources from both planning and resource assignment pane.

4.  From the resource assignee list, select a user or group and press **Enter**.

    When you create a resource assignment, the user or group allocation is based on the selected effort type. For example, when you add a user and the effort type is selected as hours, the allocations are displayed in hours.

    A resource assignment record is created and auto-saved. The resource assignment form auto-populates the project or task information.

5.  From the resource assignment pane, create a resource assignment for a project or task by selecting **Add resource**.

    You can create a resource assignment for a project from the resource assignment pane only.

6.  Select the expense type of the assignment based on the work as **Opex** or **Capex**.

    A resource can use this information while capturing efforts using the time sheet portal. Once the time sheet is approved, an expense line is created for the project capturing the expense as capex or opex, based on the selected expense type.

7.  View the resource allocations in the heatmap by enabling the **Allocation heatmap** toggle button.

    You can switch from the week view to the month view based on your requirement.


## What to do next

[Update resource assignment from Project Workspace](../../pw-resource-management/task/update-resource-assignment-pw.md)

**Parent Topic:**[Manage resource assignments from Project Workspace](../concept/use-ra-rmw.md)

**Related topics**  


[Delete a resource assignment from Project Workspace](../../pw-resource-management/task/delete-resource-assignment-pw.md)

[Update the resource allocation in a heatmap](../../pw-resource-management/task/view-allocations-heatmap-prj-wksp.md)

[Realign resource assignment to project task](../../pw-resource-management/task/realign-resource-assignment-to-task.md)

