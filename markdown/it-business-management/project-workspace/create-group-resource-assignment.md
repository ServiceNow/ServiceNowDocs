---
title: Create group resource assignment in Project Workspace
description: Use Project Workspace to create a group and associate it to your resource assignment. You can associate a set of users who share a common purpose to a group.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/it-business-management/project-workspace/create-group-resource-assignment.html
release: yokohama
product: Project Workspace
classification: project-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Create resource assignments using Project Workspace, Resource assignments in Project Workspace, Plan resources, Project Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Create group resource assignment in Project Workspace

Use Project Workspace to create a group and associate it to your resource assignment. You can associate a set of users who share a common purpose to a group.

## Before you begin

Role required: admin or it\_project\_manager

## About this task

Create group and assign roles to them. Users assigned to the group inherit the roles.

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Groups**.

2.  Create a group.

    For more information on how to create a group, see [Create a user group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/t_CreateAGroup.md).

3.  Assign the pps\_resource role to a group required for group-based resource assignment.

    For more information on how to assign a role to a group, see [Assign a role to a group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/t_AssignRoleToGroup.md).

4.  Add members to the group so that the users inherit all the roles assigned to the group.

    For more information, see [Add a user to a group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/t_CreateAGroup.md).

5.  Navigate to **Workspaces** &gt; **Project Workspace** and open a project.

6.  From the Planning pane, double-click the **Resource assignees** field for a project task.

    You can assign the resources from both planning and resource assignment pane.

7.  In the **Resource** field, select the group from step 2 and press **Enter**.


## Result

A resource assignment record for the group is created and auto-saved.

**Note:** When you select a group in the **Resource** field, the assignment is created in the Pending state. When an assignment type is set to group, an assignment is created for all the members of the group and the requested effort is distributed among them.

For the **Hours** effort type, effort is distributed in whole hours. Each member receives the same base number of hours, and any remaining hours are distributed one hour at a time until all hours are assigned. As a result, some members can receive one hour more than others. A member can receive zero hours when the total effort is less than the number of members. For example, if you request 2 hours for a group of three members, two members are each assigned 1 hour and the third member is assigned 0 hours. The total effort on the group assignment remains 2 hours.

For the **FTE** and **Person days** effort types, the effort is divided equally among the members, including fractional values.

**Parent Topic:**[Create resource assignments using Project Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-business-management/project-workspace/create-resource-assignment-prj-wksp.md)

