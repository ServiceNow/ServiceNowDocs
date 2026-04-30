---
title: Replace a user in a resource plan
description: Replace a user with another user for a group, role, or user resource plan to accommodate situations like a user taking leave during a project.
locale: en-US
release: xanadu
product: Resource Management
classification: resource-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Manage resources by using the allocation workbench, Allocation workbench, Resource Management classic, Project Portfolio Management, Strategic Portfolio Management]
---

# Replace a user in a resource plan

Replace a user with another user for a group, role, or user resource plan to accommodate situations like a user taking leave during a project.

## About this task

**Important:** Allocation workbench is being deprecated starting Xanadu release. It will be hidden and no longer available for installation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Resource Managers are encouraged to use the [Resource Management Workspace](../../resource-management-workspace/concept/rsrc-mgmt-wrkspc.md) to allocate, approve, and manage resource assignments. Resource Management Workspace is a dedicated workspace view for Resource Managers where you get the insights about unassigned tasks, heatmap view of resource bandwidth, custom view to handle priority resource assignment requests, and so on.

This option is available only for a confirmed or allocated resource plan.

A user can be replaced only if no actuals are present in that period for the existing user.

## Before you begin

Role required: resource\_manager

## Procedure

1.  Navigate to **All** &gt; **Resource** &gt; **Resource Workbench** &gt; **Allocation Workbench**.

2.  On the Allocation Boards page, select the allocation board whose resource plans you want to manage.

3.  Select a group, role, or user resource plan in the resource grid.

4.  Select the **Actions** icon \(![Actions icon](../../planning-and-policy/image/ellipsis-vertical-icon.png)\) on the user that you want to replace, and select **Replace User**.

5.  In the **User** field of the Replace Users window in the **To** section, select the new user to whom allocations must be transferred.

6.  Select the replace period.

    By default, the replace period starts from the current allocation week or month.

    The replace end period can’t be later than the resource allocation's end date, and the replace start period can’t be before the resource's allocation start period.

7.  Select the **Delete the original allocation in case of complete transfer** check box to delete the original user allocations if a complete transfer happens.

    If the new user is available for all the time periods and all the hours in the replace period, a complete transfer happens.

8.  Select **Allocate** or **Confirm**.


## Result

When a user is replaced in a user resource plan, a new resource plan is created for the new user.

When the new user isn’t available for complete allocation, the maximum available allocations are transferred to the new user, and the remaining allocations remain with the existing user.

**Parent Topic:**[Manage resources by using the allocation workbench](manage-resources-allocation-workbench.md)

