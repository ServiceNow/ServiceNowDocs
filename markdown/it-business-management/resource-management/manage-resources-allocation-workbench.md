---
title: Manage resources by using the allocation workbench
description: Use the allocation workbench to manage your resources effectively. You can review all resource requests in one place for your team. You can also see the available hours for requested users and efficiently allocate resources.
locale: en-US
release: yokohama
product: Resource Management
classification: resource-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 9
breadcrumb: [Allocation workbench, Resource Management classic, Project Portfolio Management, Strategic Portfolio Management]
---

# Manage resources by using the allocation workbench

Use the allocation workbench to manage your resources effectively. You can review all resource requests in one place for your team. You can also see the available hours for requested users and efficiently allocate resources.

## About this task

**Important:** Allocation workbench is being deprecated starting Xanadu release. It will be hidden and no longer available for installation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Resource Managers are encouraged to use the [Resource Management Workspace](../../resource-management-workspace/concept/rsrc-mgmt-wrkspc.md) to allocate, approve, and manage resource assignments. Resource Management Workspace is a dedicated workspace view for Resource Managers where you get the insights about unassigned tasks, heatmap view of resource bandwidth, custom view to handle priority resource assignment requests, and so on.

The allocation workbench resource grid provides a detailed breakdown of resource data. You can change the view and filter data.

If you confirm or allocate hours from the **Actions** menu, the per day capacity for a resource is 24 hours.

You can view and manage resource availability and utilization using the resource finder. To enable the resource finder, click the resource finder icon \(![Resource finder](../../planning-and-policy/image/ResourceFinderIcon.png)\). If you confirm or allocate hours from the resource finder section, the per day capacity for a resource is based on the resource's schedule.

If a warning is displayed while performing a task from the Allocation Workbench, you can navigate to detailed logs for that action on a new tab by clicking the hyperlink on the message. For example, while requesting extension of a resource plan, if a resource plan can’t be extended for all the requested hours, a warning is displayed that specifies that some hours can’t be extended.

If the **Do not allow resource plan dates to be outside the Project/Demand dates** property is enabled, the resource plan start and end dates must be within the project or demand dates when you create, extend, shift, move, or change the state of a resource plan from requested to confirm or allocate.

## Before you begin

Role required: resource\_manager

## Procedure

1.  Navigate to **All** &gt; **Resource** &gt; **Resource Workbench** &gt; **Allocation Workbench**.

2.  On the Allocation Boards page, select the allocation board whose resource plans you want to manage.

3.  Perform the following tasks in the resource grid.

    The available options change depending on the state of the resource plan.

<table id="table_brk_tnm_l2b"><thead><tr><th>

Task

</th><th>

Steps

</th></tr></thead><tbody><tr><td>

Create a resource plan for a project or demand

</td><td>

1.  Click a project or demand in the resource grid.
2.  Click the **New Plan** button located in the top-right corner.​


</td></tr><tr><td>

Create a resource plan for a project or demand from selected resources

</td><td>

1.  Click a project or demand in the resource grid.
2.  In the resource finder section, search for and select the desired available resources​.​
3.  Click the **Add New Plan** button.​


</td></tr><tr><td>

Request a resource plan

</td><td>

1.  Click a resource plan in the resource grid.
2.  Click the **Actions** icon \(![Actions icon](../../planning-and-policy/image/ellipsis-vertical-icon.png)\), and select **Change State &gt; Request**.


</td></tr><tr><td>

Confirm or allocate a resource plan

</td><td>

1.  Click a resource plan in the resource grid.
2.  Click the **Actions** icon \(![Actions icon](../../planning-and-policy/image/ellipsis-vertical-icon.png)\), and select **Change State &gt; Confirm** or **Change State &gt; Allocate**.


</td></tr><tr><td>

Extend a resource plan

</td><td>

1.  Open a resource plan in the resource grid.
2.  Click the **Actions** icon \(![Actions icon.](../../planning-and-policy/image/ellipsis-vertical-icon.png)\), and select **Extend Resource Plan**.
3.  Enter the new end date of the resource plan in the **New end date** field.
4.  Select the type of request and click **Ok**.


</td></tr><tr><td>

Allocate extension

</td><td>

Allocate resources for the extended period requested by the project manager.1.  Click a resource plan in the resource grid.
2.  Click the **Actions** icon \(![Actions icon](../../planning-and-policy/image/ellipsis-vertical-icon.png)\), and select **Allocate Extension**.


</td></tr><tr><td>

Confirm or allocate resources for a requested group, role, or user resource plan for the whole period of the resource plan

</td><td>

See the [Confirm or allocate resources from the Allocation Workbench](confirm-allocate-specific-time.md) topic.

</td></tr><tr><td>

Confirm or allocate resources for a group, role, or user resource plan for a specific period

</td><td>

See the [Confirm or allocate resources from the Allocation Workbench](confirm-allocate-specific-time.md) topic.

</td></tr><tr><td>

Partially allocate a resource plan for specific periods

</td><td>

This option is available only for a Confirmed resource plan.

 You can allocate a resource plan for a specific period instead of allocating the resource plan for the full duration. For a group and role resource plan, you can partially allocate a plan at the user level.

 You can allocate resources in one of the following ways:

 -   To allocate a resource for all the periods updated in a row, click the **Actions** icon \(![Actions icon](../../planning-and-policy/image/ellipsis-vertical-icon.png)\) and select the **Allocate** option.
-   To allocate a resource for a specific period:
    1.  In the resource grid section, right-click in the **Conf/Alloc** cell for the required period.
    2.  Select **Allocate**.
 The resource plan is partially allocated and the partially allocated icon \(![Partially allocated icon](../image/PartialAllocationIcon.png)\) is displayed in the **State** cell in the resource grid.

</td></tr><tr><td>

Delete a resource plan

</td><td>

1.  Click a resource plan in the resource grid.
2.  Click the **Actions** icon \(![Actions icon](../../planning-and-policy/image/ellipsis-vertical-icon.png)\), and select **Delete**.


</td></tr><tr><td>

Edit hours in the grid

</td><td>

Use one of the following ways:-   Enter the value for an individual cell.
    1.  Double-click a resource plan or a specific resource row.
    2.  Edit the allocated hours of the resource plan or a resource in the grid.
    3.  Move the pointer out of the cell to save.
-   Update multiple cells at once:

You can copy the existing value from a cell and update the cells to its right. For example, you want to update the planned hours of a resource for all the months of the resource plan.

    -   Right-click on the cell that you want to copy the value from and select **Fill Right**.

![Row context menu options.](../image/fill-right-option.png)

    -   Fill in the details of the number of cells that you want to update and the hours.
    -   Select **Update**.
 **Note:** The Fill Right option is available only on those columns that are editable. For example, a resource plan is in the Allocated state.

</td></tr><tr><td>

Replace a user with another user for a group, role, or user resource plan.

</td><td>

See the [Replace user in a resource plan](replace-user.md) topic.

</td></tr><tr><td>

Move a resource plan and its allocations to a future date for a group, role, or user resource plan

</td><td>

See the [Move a resource plan](move-res-plan.md) topic.

</td></tr><tr><td>

Shift allocation of a user to a future date for a group or role resource plan

</td><td>

See the [Shift allocations of a user](shift-allocation.md) topic.

</td></tr><tr><td>

Request all the resource plans for a project or demand

</td><td>

The **Request All** option is available when at least one of the listed resource plans under the project or demand is in the Planning state.

 1.  Click the **Actions** icon \(![Actions icon](../../planning-and-policy/image/ellipsis-vertical-icon.png)\) on a project or demand row in the resource grid.
2.  Select **Request All**.


</td></tr><tr><td>

Request a change to a submitted resource plan

</td><td>

The **Request change** option is available for a resource plan in the Requested or Confirmed state.

 1.  Click the **Actions** icon \(![Actions icon](../../planning-and-policy/image/ellipsis-vertical-icon.png)\) on a resource plan row in the resource grid.
2.  Select **Request Change**.


</td></tr><tr><td>

Request extension of an allocated resource plan

</td><td>

See the [Request extension of an allocated resource plan](request-extension-allocated-resource-plan.md) topic.

</td></tr><tr><td>

Reduce the duration of an allocated or confirmed resource plan

</td><td>

If there are no actuals posted for future in the resource plan, then all the allocated or confirmed hours of all the resources will be released when you reduce the resource plan. If actuals are posted for future, then the resource plan end date will be updated to the future date on which actuals are present, and all the allocated or confirmed hours of all the resources from the date on which actuals are present to the original end date will be released.1.  Click the **Actions** icon \(![Actions icon](../../planning-and-policy/image/ellipsis-vertical-icon.png)\) on a resource plan row in the resource grid.
2.  Select **Reduce Resource Plan**.
3.  Enter the new end date of the resource plan in the **End date** field, and click **Yes**.


</td></tr><tr><td>

Complete a resource plan

</td><td>

After all the associated tasks and projects are complete or canceled, as a resource manager you can mark the resource plan complete and closed. The state of the plan changes to Complete.1.  Click the **Actions** icon \(![Actions icon](../../planning-and-policy/image/ellipsis-vertical-icon.png)\) on a resource plan row in the resource grid.
2.  Select **Complete**.
3.  In the Confirm dialog box, select the **Completion date** option, and click **Yes**.


</td></tr><tr><td>

Cancel a resource plan

</td><td>

When a resource plan is no longer required, as a resource manager you can cancel it, which also cancels its past and future allocations.1.  Click the **Actions** icon \(![Actions icon](../../planning-and-policy/image/ellipsis-vertical-icon.png)\) on a resource plan row in the resource grid.
2.  Select **Cancel**.


</td></tr><tr><td>

View the resource allocations at user level

</td><td>

In the resource grid section, expand a resource plan entry. The user level allocations are listed only for group and role resource plans. If an entry doesn’t have an associated resource plan, the expand option won’t be available.A negative value in a user row indicates that the user is over-allocated for that period. Click the value to see the resource over-allocation daily records of the user to see the specific over-allocated days.

</td></tr><tr><td>

View the details of a project or a demand

</td><td>

1.  Click the **Actions** icon \(![Actions icon](../../planning-and-policy/image/ellipsis-vertical-icon.png)\) on a project or demand row in the resource grid.
2.  Select **View Project** for a project or select **View demand** for a demand.


</td></tr></tbody>
</table>
-   **[Confirm or allocate resources from the Allocation Workbench](confirm-allocate-specific-time.md)**  
Confirm or allocate resources for a group, role, or user resource plan for the entire period of the resource plan or a specific period of the resource plan from the Allocation Workbench.
-   **[Replace a user in a resource plan](replace-user.md)**  
Replace a user with another user for a group, role, or user resource plan to accommodate situations like a user taking leave during a project.
-   **[Move a resource plan](move-res-plan.md)**  
Move a resource plan and its allocations to a future date for a group, role, or user resource plan.
-   **[Shift allocations of a user](shift-allocation.md)**  
Shift allocation of a user to a future date for a group or role resource plan to accommodate situations where planned work for a specific user of a group or role resource plan must be shifted to a future time period.

**Parent Topic:**[Allocation workbench](../concept/allocation-workbench.md)

