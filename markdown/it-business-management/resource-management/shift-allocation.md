---
title: Shift allocations of a user
description: Shift allocation of a user to a future date for a group or role resource plan to accommodate situations where planned work for a specific user of a group or role resource plan must be shifted to a future time period.
locale: en-US
release: xanadu
product: Resource Management
classification: resource-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Manage resources by using the allocation workbench, Allocation workbench, Resource Management classic, Project Portfolio Management, Strategic Portfolio Management]
---

# Shift allocations of a user

Shift allocation of a user to a future date for a group or role resource plan to accommodate situations where planned work for a specific user of a group or role resource plan must be shifted to a future time period.

## About this task

**Important:** Allocation workbench is being deprecated starting Xanadu release. It will be hidden and no longer available for installation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Resource Managers are encouraged to use the [Resource Management Workspace](../../resource-management-workspace/concept/rsrc-mgmt-wrkspc.md) to allocate, approve, and manage resource assignments. Resource Management Workspace is a dedicated workspace view for Resource Managers where you get the insights about unassigned tasks, heatmap view of resource bandwidth, custom view to handle priority resource assignment requests, and so on.

## Before you begin

Role required: resource\_manager

## Procedure

1.  Navigate to **All** &gt; **Resource** &gt; **Resource Workbench** &gt; **Allocation Workbench**.

2.  On the Allocation Boards page, select the allocation board whose resource plans you want to manage.

3.  Select a group or role resource plan in the resource grid.

4.  Select the **Actions** icon \(![Actions icon](../../planning-and-policy/image/ellipsis-vertical-icon.png)\) on the user that you want to shift allocations for, and select **Shift Allocations**.

5.  In the **From** field in the Shift allocations window, select the time period from which you want to shift the allocations.

    **Note:** The from period can’t be before the current allocation period.

6.  In the **To** field, select the time period to which you want to shift the allocations.

    If the dates of the shifted resource allocations are beyond the resource plan end date, the resource plan is extended.

7.  Select **Update**.

    The allocation cap per day is 24 hours.

    If a user is already booked for the shifted period, then the user is over-allocated for the shifted period.

    **Note:** If actuals are posted for all the periods of resource allocation, then the **Shift Allocations** option is disabled in the **Actions** menu.


**Parent Topic:**[Manage resources by using the allocation workbench](manage-resources-allocation-workbench.md)

