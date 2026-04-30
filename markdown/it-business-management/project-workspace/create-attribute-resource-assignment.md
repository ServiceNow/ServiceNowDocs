---
title: Create an attribute-based resource assignment
description: Create an attribute-based resource assignment in Project Workspace. You can pre-define attributes based on your requirement.
locale: en-US
release: yokohama
product: Project Workspace
classification: project-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create resource assignments using Project Workspace, Resource assignments in Project Workspace, Plan resources, Project Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Create an attribute-based resource assignment

Create an attribute-based resource assignment in Project Workspace. You can pre-define attributes based on your requirement.

## Before you begin

Role required: pps\_admin or it\_project\_manager

## Procedure

1.  [Create a planning attribute](../../project-management/task/configure-planning-attributes.md#).

    **Note:** If the assignment is attribute-based, then the assignment is created in the Unassigned state. You should have the pps\_admin role to configure the planning attributes.

2.  Navigate to **All** &gt; **Employee Profile** &gt; **Employee Profiles**.

3.  Create an employee profile.

    For more information, see [Activate Employee Profile](https://www.servicenow.com/docs/access?context=activate-employee-profile&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US).

4.  Navigate to **Workspaces** &gt; **Project Workspace** and open a project.

5.  From the Planning pane, double-click the **Resource assignees** field for a project task.

    You can assign the resources from both planning and resource assignment pane.

6.  From the resource assignee list, select a user or group and press **Enter**.

    You can create new custom attributes, such as location, in addition to group, skill, and role, and can also leverage these custom attributes to create resource assignments.

    A resource assignment record for an attribute is created and auto-saved.

    **Note:** The **Primary group**, **Primary skill**, and **Primary role** attributes can be enabled for the Resource Management. You can create more attributes based on your requirement.


**Parent Topic:**[Create resource assignments using Project Workspace](create-resource-assignment-prj-wksp.md)

**Related topics**  


[New Resource Assignment form](../../resource-management-workspace/concept/create-ra-form-rmw.md)

[Delete a resource assignment from Project Workspace](delete-resource-assignment-pw.md)

[Update the resource allocation in a heatmap](view-allocations-heatmap-prj-wksp.md)

[Realign resource assignment to project task](realign-resource-assignment-to-task.md)

