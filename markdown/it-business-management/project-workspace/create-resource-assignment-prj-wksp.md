---
title: Create resource assignments using Project Workspace
description: Create an attribute-based resource assignment in the Project Workspace application for any project or project task.
locale: en-US
release: xanadu
product: Project Workspace
classification: project-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Resource assignments in Project Workspace, Plan resources, Project Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Create resource assignments using Project Workspace

Create an attribute-based resource assignment in the Project Workspace application for any project or project task.

## Before you begin

After a resource assignment is created, a Resource Plan is created automatically in the back-end. The resources are allocated to the project and approved by the Resource Manager. You can edit the assignment throughout the project life cycle.

Role required: it\_project\_manager

## Procedure

1.  Navigate to **Workspaces** &gt; **Project Workspace** and open a project.

2.  View the resource assignment pane by enabling the **Resource assignments** toggle button.

    **Note:** If the property **sn\_pw.enable\_resource\_planning** is set to true, then the **Resource plan** toggle button and resource assignment pane are displayed in Project Workspace. The default value is false. You must have the pps\_admin role to enable this property.

3.  From the Planning pane, double-click the **Resource assignees** field of a project task to add resource.

    You can assign the resources from both planning and resource assignment pane.

4.  From the resource assignee list, select a user or group and press **Enter**.

    When you create a resource assignment, the user or group allocation is based on the selected effort type. For example, when you add a user and the effort type is selected as hours, the allocations are displayed in hours.

    A resource assignment record is created and auto-saved. The resource assignment form auto-populates the project or task information.

5.  From the resource assignment pane, create a resource assignment for a project or task by selecting **Add resource**.

    You can create a resource assignment for a project from the resource assignment pane only.

    ![Resource-assignment-pane.](../image/resource-assignment-pane-pw.png)

6.  Select the expense type of the assignment based on the work as **Opex** or **Capex**.

    A resource can use this information while capturing efforts using the time sheet portal. Once the time sheet is approved, an expense line is created for the project capturing the expense as capex or opex, based on the selected expense type.

7.  View the resource allocations in the heatmap by enabling the **Allocation heatmap** toggle button.

    You can switch from the weekly view to the monthly view based on your requirement using **Monthly** list.

    Extend, edit, or delete the resource assignments using the row context menu in resource assignment pane.


## What to do next

[Update a resource assignment from Project Workspace](update-resource-assignment-pw.md)

-   **[Create a resource assignment for a user in Project Workspace](create-user-resource-assignment.md)**  
Use Project Workspace to create a user-based Resource assignment. User records store information about individuals who access your instance or application. These records can be assigned to groups and roles to determine what records and actions can be accessed by individuals.
-   **[Create a resource assignment for a group in Project Workspace](create-group-resource-assignment.md)**  
Use Project Workspace to create a group and associate it to your resource assignment. You can associate a set of users who share a common purpose to a group.
-   **[Create an attribute-based resource assignment](create-attribute-resource-assignment.md)**  
Create an attribute-based resource assignment in Project Workspace. You can pre-define attributes based on your requirement.

**Parent Topic:**[Resource assignments in Project Workspace](../concept/resource-assignments-pw.md)

**Related topics**  


[New Resource Assignment form](../../resource-management-workspace/concept/create-ra-form-rmw.md)

[Delete a resource assignment from Project Workspace](delete-resource-assignment-pw.md)

[Update the resource allocation in a heatmap](view-allocations-heatmap-prj-wksp.md)

[Realign resource assignment to project task](realign-resource-assignment-to-task.md)

