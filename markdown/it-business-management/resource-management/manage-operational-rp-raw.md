---
title: Manage operational resource plans from the allocation workbench
description: Create and manage operational resource plans effectively from one place using the Resource Allocation Workbench without having to navigate individually to the operational resource plan's form or list.
locale: en-US
release: xanadu
product: Resource Management
classification: resource-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Allocation workbench, Resource Management classic, Project Portfolio Management, Strategic Portfolio Management]
---

# Manage operational resource plans from the allocation workbench

Create and manage operational resource plans effectively from one place using the Resource Allocation Workbench without having to navigate individually to the operational resource plan's form or list.

## About this task

**Important:** Allocation workbench is being deprecated starting Xanadu release. It will be hidden and no longer available for installation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Resource Managers are encouraged to use the [Resource Management Workspace](../../resource-management-workspace/concept/rsrc-mgmt-wrkspc.md) to allocate, approve, and manage resource assignments. Resource Management Workspace is a dedicated workspace view for Resource Managers where you get the insights about unassigned tasks, heatmap view of resource bandwidth, custom view to handle priority resource assignment requests, and so on.

## Before you begin

Enable the **Create and manage operational resource plans from the resource allocation workbench** property by navigating to **All** &gt; **Project Administration** &gt; **Properties - Resource** to create operational resource plans from the Allocation Workbench. For more information, see [Resource Management properties](../reference/r_ResourceProperties.md).

Role required: resource\_manager

## Procedure

1.  Navigate to **Resource** &gt; **Resource Workbench** &gt; **Allocation Workbench**.

2.  On the Allocation Boards page, select the allocation board whose operational resource plans you want to manage.

3.  Select the **Configuration** icon \(![Configuration](../image/configurationiconraw.png)\), and select **Operational plans**.

    The following management options are available in the resource grid, which displays the operational resource plans.

<table id="table_brk_tnm_l2b"><thead><tr><th>

Task

</th><th>

Steps

</th></tr></thead><tbody><tr><td>

Create an operational resource plan

</td><td>

Select the list icon \(![List view](../image/dropdown_raw.png)\) next to **New Plan** on the top-right corner, and select **New Operational Plan**. After the operational resource plan is created, it appears under the Operational Resource Plans header in the resource grid.

</td></tr><tr><td>

Allocate a resource plan

</td><td>

1.  Open a resource plan in the resource grid.
2.  Select the **Actions** icon \(![Actions icon](../../planning-and-policy/image/ellipsis-vertical-icon.png)\), and select **Change State &gt; Allocate**.


</td></tr><tr><td>

Extend a resource plan

</td><td>

1.  Open a resource plan in the resource grid.
2.  Select the **Actions** icon \(![Actions icon.](../../planning-and-policy/image/ellipsis-vertical-icon.png)\), and select **Extend Resource Plan**.
3.  Enter the new end date of the resource plan in the **New end date** field.
4.  Select the type of request and select **Ok**.


</td></tr><tr><td>

Allocate extension

</td><td>

Allocate resources for the extended period requested by the project manager.1.  Open a resource plan in the resource grid.
2.  Select the **Actions** icon \(![Actions icon.](../../planning-and-policy/image/ellipsis-vertical-icon.png)\), and select **Allocate Extension**.


</td></tr><tr><td>

Allocate resources for a requested group, role, or user resource plan for the whole period of the resource plan

</td><td>

Allocate users the percentage of their capacity specified in the operational resource plan. For more information, see [Confirm or allocate resources from the Allocation Workbench](confirm-allocate-specific-time.md).

</td></tr><tr><td>

Allocate resources for a group, role, or user resource plan for a specific period

</td><td>

Allocate users the percentage of their capacity specified in the operational resource plan. For more information, see [Confirm or allocate resources from the Allocation Workbench](confirm-allocate-specific-time.md).

</td></tr><tr><td>

Delete a resource plan

</td><td>

1.  Open a resource plan in the resource grid.
2.  Select the **Actions** icon \(![Actions icon.](../../planning-and-policy/image/ellipsis-vertical-icon.png)\), and select **Delete**.


</td></tr><tr><td>

Edit hours in the grid

</td><td>

Use one of the following ways:-   Enter the value for an individual cell.
    1.  Double-click a resource plan or a specific resource row.
    2.  Edit the allocated hours of the resource plan or a resource in the grid.
    3.  Move the pointer out of the cell to save.
-   Update multiple cells at once:

You can copy the existing value from a cell and update the cells to its right. For example, you want to update the planned hours of a resource for all the months of the resource plan.

    -   Right-click on the cell that you want to copy the value from and select the **Fill Right** option.

![Row-context menu option.](../image/fill-right-option.png)

    -   Fill in the details of the number of cells that you want to update and the hours.
    -   Select **Update**.
 **Note:** The Fill Right option is available only on those columns that are editable. For example, a resource plan is in the Allocated state.

</td></tr><tr><td>

Reduce the duration of an allocated resource plan

</td><td>

If no actuals are posted for the future in the resource plan, then all allocated or confirmed hours of the resources are released when you reduce the resource plan. If actuals are posted for the future, then the resource plan end date is updated to the future date on which actuals are present. All allocated or confirmed hours of all resources from the date on which actuals are present to the original end date are released.1.  Open a resource plan in the resource grid.
2.  Select the **Actions** icon \(![Actions icon.](../../planning-and-policy/image/ellipsis-vertical-icon.png)\) on a resource plan row in the resource grid.
3.  Select **Reduce Resource Plan**.
4.  Enter the new end date of the resource plan in the **End date** field, and select **Yes**.


</td></tr><tr><td>

Complete a resource plan

</td><td>

After all the associated tasks are complete or canceled, as a resource manager you can mark the resource plan complete and closed. 1.  Select the **Actions** icon \(![Actions icon.](../../planning-and-policy/image/ellipsis-vertical-icon.png)\) on a resource plan row in the resource grid.

2.  Select **Complete**.

3.  In the confirmation dialog box, select the **Completion date** option, and select **Yes**.

The state of the plan changes to Complete.

</td></tr><tr><td>

Cancel a resource plan

</td><td>

When a resource plan is no longer required, as a resource manager you can cancel it, which also cancels its past and future allocations.1.  Open a resource plan in the resource grid.
2.  Select the **Actions** icon \(![Actions icon.](../../planning-and-policy/image/ellipsis-vertical-icon.png)\) on a resource plan row in the resource grid.
3.  Select **Cancel**.


</td></tr><tr><td>

View the resource allocations at user level

</td><td>

In the resource grid section, expand a resource plan entry. The user level allocations are listed only for group and role resource plans.A negative value in a user row indicates that the user is over-allocated for that period. To see the resource over-allocation daily records of the user, select the value.

</td></tr></tbody>
</table>
**Parent Topic:**[Allocation workbench](../concept/allocation-workbench.md)

