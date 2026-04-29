---
title: Create a resource assignment for a group in Project Workspace
description: Use Project Workspace to create a group and associate it to your resource assignment. You can associate a set of users who share a common purpose to a group.
locale: en-US
release: australia
product: Project Workspace
classification: project-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create resource assignments using Project Workspace, Resource assignments in Project Workspace, Resource planning with Project Workspace, Project Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Create a resource assignment for a group in Project Workspace

Use Project Workspace to create a group and associate it to your resource assignment. You can associate a set of users who share a common purpose to a group.

## Before you begin

Role required: admin or it\_project\_manager

## About this task

Create group and assign roles to them. Users assigned to the group inherit the roles.

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Groups**.

2.  Create a group.

    For more information on how to create a group, see [Create a user group](https://www.servicenow.com/docs/access?context=t_CreateAGroup&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

3.  Assign the pps\_resource role to a group required for group-based resource assignment.

    For more information on how to assign a role to a group, see [Assign a role to a group](https://www.servicenow.com/docs/access?context=t_AssignRoleToGroup&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

4.  Add members to the group so that the users inherit all the roles assigned to the group.

    For more information, see [Add a user to a group](https://www.servicenow.com/docs/access?context=t_CreateAGroup&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

5.  Navigate to **Workspaces** &gt; **Project Workspace** and open a project.

6.  From the Planning pane, double-click the **Resource assignees** field for a project task.

    You can assign the resources from both planning and resource assignment pane.

7.  In the **Resource** field, select the group from step 2 and press **Enter**.


## Result

A resource assignment record for the group is created and auto-saved.

**Note:** When you select a group in the **Resource** field, the assignment is created in the Pending state. When an assignment type is set to group, an assignment is created for all the members of the group, and the allocation hours are split evenly for all the members of that group.

**Parent Topic:**[Create resource assignments using Project Workspace](create-resource-assignment-prj-wksp.md)

