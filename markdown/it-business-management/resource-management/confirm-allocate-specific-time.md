---
title: Confirm or allocate resources from the Allocation Workbench
description: Confirm or allocate resources for a group, role, or user resource plan for the entire period of the resource plan or a specific period of the resource plan from the Allocation Workbench.
locale: en-US
release: xanadu
product: Resource Management
classification: resource-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Manage resources by using the allocation workbench, Allocation workbench, Resource Management classic, Project Portfolio Management, Strategic Portfolio Management]
---

# Confirm or allocate resources from the Allocation Workbench

Confirm or allocate resources for a group, role, or user resource plan for the entire period of the resource plan or a specific period of the resource plan from the Allocation Workbench.

## About this task

**Important:** Allocation workbench is being deprecated starting Xanadu release. It will be hidden and no longer available for installation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Resource Managers are encouraged to use the [Resource Management Workspace](../../resource-management-workspace/concept/rsrc-mgmt-wrkspc.md) to allocate, approve, and manage resource assignments. Resource Management Workspace is a dedicated workspace view for Resource Managers where you get the insights about unassigned tasks, heatmap view of resource bandwidth, custom view to handle priority resource assignment requests, and so on.

The allocation period must be within the resource plan duration to confirm or allocate resources for a specific time period.

You can confirm resources only for a requested or confirmed resource plan. The confirm action is not applicable for operational resource plans.

You can allocate resources only for a partially allocated or allocated resource plan.

## Before you begin

Role required: resource\_manager

## Procedure

1.  Navigate to **All** &gt; **Resource** &gt; **Resource Workbench** &gt; **Allocation Workbench**.

2.  On the Allocation Boards page, select the allocation board whose resource plans you want to manage.

3.  Select a group, role, user resource plan in the resource grid.

    The resource finder shows all the resources in that resource plan.

4.  In the resource finder section, check the availability of the resources​.

5.  Select the required resources​.​

6.  Confirm or allocate resources.

    -   For a specific period: Select the down arrow \(![Down arrow](../image/downward_arrow_resfinder.png)\) corresponding to **Confirm** or **Allocate**, and select **Confirm for specific period** or **Allocate for specific period**. ​Select the allocation period and select **Confirm** or **Allocate**.
    -   For the whole period: Select **Confirm** or **Allocate**.
    For operational resource plans, allocated hours for a resource are calculated based on the percentage capacity specified in the operational resource plan. If a new member is added to a group, you can allocate the newly added member in an already allocated operational resource plan for the same group.

    **Note:** Users already confirmed or allocated for a time period can’t be confirmed or allocated for the same time period again.


**Parent Topic:**[Manage resources by using the allocation workbench](manage-resources-allocation-workbench.md)

