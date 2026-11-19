---
title: Create a resource assignment for a user in Project Workspace
description: Use Project Workspace to create a user-based Resource assignment. User records store information about individuals who access your instance or application. These records can be assigned to groups and roles to determine what records and actions can be accessed by individuals.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/it-business-management/project-workspace/create-user-resource-assignment.html
release: yokohama
product: Project Workspace
classification: project-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create resource assignments using Project Workspace, Resource assignments in Project Workspace, Plan resources, Project Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Create a resource assignment for a user in Project Workspace

Use Project Workspace to create a user-based Resource assignment. User records store information about individuals who access your instance or application. These records can be assigned to groups and roles to determine what records and actions can be accessed by individuals.

## Before you begin

Role required: admin or it\_project\_manager

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Users**.

2.  [Create a user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/t_CreateAUser.md).

3.  Assign the pps\_resource role to the users required for user-based resource assignment.

    For more information on how to assign a role, see [Assign a role to a user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/t_AssignARoleToAUser.md).

4.  Navigate to **Workspaces** &gt; **Project Workspace** and open a project.

5.  From the Planning pane, double-click the **Resource assignees** field for a project task.

6.  In the **Resource** field, select the user from step 2 and press **Enter**.

    The **Resource status** column helps to identify any Pending or Unapproved work items assigned to a resource.

    **Note:** The status of the assigned work is rolled up to the resource level and the resource card level. If there are any pending or unassigned work items in the top tray, the rolled up status at resource level and card level shows Pending.

    \[Omitted image "user-resource-assignments-pw.png"\] Alt text: User-based resource assignments.

    A resource assignment record for the user is created and auto-saved.


**Parent Topic:**[Create resource assignments using Project Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-business-management/project-workspace/create-resource-assignment-prj-wksp.md)

**Related topics**  


[New Resource Assignment form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-business-management/resource-management/create-ra-form-rmw.md)

[Delete a resource assignment from Project Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-business-management/project-workspace/delete-resource-assignment-pw.md)

[Update the resource allocation in a heatmap](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-business-management/project-workspace/view-allocations-heatmap-prj-wksp.md)

[Realign resource assignment to project task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-business-management/project-workspace/realign-resource-assignment-to-task.md)

