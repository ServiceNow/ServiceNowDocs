---
title: Create a resource assignment for a user in Project Workspace
description: Use Project Workspace to create a user-based Resource assignment. User records store information about individuals who access your instance or application. These records can be assigned to groups and roles to determine what records and actions can be accessed by individuals.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/project-workspace/create-user-resource-assignment.html
release: australia
product: Project Workspace
classification: project-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create resource assignments using Project Workspace, Resource assignments in Project Workspace, Resource planning with Project Workspace, Project Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Create a resource assignment for a user in Project Workspace

Use Project Workspace to create a user-based Resource assignment. User records store information about individuals who access your instance or application. These records can be assigned to groups and roles to determine what records and actions can be accessed by individuals.

## Before you begin

Role required: admin or it\_project\_manager

## Procedure

1.  Navigate to **Workspaces** &gt; **Project Workspace** and open a project.

2.  View the resource assignment pane by enabling the **Resource assignments** toggle button.

    **Note:** If the **sn\_pw.enable\_resource\_planning** property is set to true, then the **Resource assignment** toggle button and resource assignment pane are displayed in Project Workspace. The default value is false. You must have the pps\_admin role to enable this property.

3.  From the Planning pane, double-click the **Resource assignees** field for a project task.

    You can assign the resources from both planning and resource assignment pane.

4.  From the resource assignment pane, create a resource assignment for a project or task by selecting **Add resource**.

    You can create a resource assignment for a project from the resource assignment pane only.

5.  From the resource assignee list, select a user or group and press **Enter**.

    When you create a resource assignment, the user or group allocation is based on the selected effort type. For example, when you add a user and the effort type is selected as hours, the allocations are displayed in hours.

    A resource assignment record is created and auto-saved. The resource assignment form auto-populates the project or task information.

6.  From the resource assignment pane, create a resource assignment for a project or task by selecting **New Resource**.

    You can use this option to create a resource assignment using the resource form. On the New Resource Assignment form, fill in the fields and select **Submit**. For a description of the field names, see [New Resource Assignment form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/resource-management/create-ra-form-rmw.md).

7.  Select the expense type of the assignment based on the work as **Opex** or **Capex**.

    A resource can use this information while capturing efforts using the time sheet portal. Once the time sheet is approved, an expense line is created for the project capturing the expense as capex or opex, based on the selected expense type.


**Parent Topic:**[Create resource assignments using Project Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-workspace/create-resource-assignment-prj-wksp.md)

**Related topics**  


[Update resource assignment from Project Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-workspace/update-resource-assignment-pw.md)

[Extend a resource assignment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-workspace/extend-resource-assignment-pw.md)

