---
title: Allocation workbench
description: Use the allocation workbench to allocate your resources effectively to the requesting investments by evaluating resource capacity and availability.
locale: en-US
release: yokohama
product: Resource Management
classification: resource-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Resource Management classic, Project Portfolio Management, Strategic Portfolio Management]
---

# Allocation workbench

Use the allocation workbench to allocate your resources effectively to the requesting investments by evaluating resource capacity and availability.

**Important:** Allocation workbench is being deprecated starting Xanadu release. It will be hidden and no longer available for installation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Resource Managers are encouraged to use the [Resource Management Workspace](../../resource-management-workspace/concept/rsrc-mgmt-wrkspc.md) to allocate, approve, and manage resource assignments. Resource Management Workspace is a dedicated workspace view for Resource Managers where you get the insights about unassigned tasks, heatmap view of resource bandwidth, custom view to handle priority resource assignment requests, and so on.

## Allocation boards

Allocation boards group resources based on filters so that you can view and manage specific resources for investments. For example, you can create an allocation board by filtering on a specific program to group your resources requested or allocated to projects and demands of the program.

The Allocation Boards page shows all your allocation boards. You can [create a personalized allocation board](../task/create-allocation-board.md) through a filter definition. Selecting a board name opens the allocation workbench with a list of projects, demands, and operational work types that match the allocation board filter type.

When you select a resource plan in the resource grid section, the availability details of the associated resources are displayed in the resource finder section. For example, if you select a group resource plan, the availability details of the group and its members are displayed in the resource finder section. You can expand and view other columns by selecting the **Detailed View** icon, and selecting columns from the **Configurations** list. When you change the selection, the results are automatically updated.

Watch this video to learn about the purpose and usage of the Resource Allocation Workbench.Resource Allocation Workbench and its usage

Use various options on the workbench header to do the following actions.

<table id="table_k5k_5sv_4hb"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Date range selector

 ![Date range selector](../image/DateRangeSelector.png)

</td><td>

Shows resource plans for the selected time range.

 For a new allocation board, the default period is set as the current date to six months. If you change these dates, the new range is saved as the board default for future board use.

 From the Yokohama release onwards, the following enhancements are available on the board:

-   Resource grid view starts from the month or week as per the value that you set in the **From** field. Previous and future months are visible with horizontal scroll on the grid view.

However, If there are no resource plans starting in the selected month or week, the resource grid view starts with the earliest date among all the resource plans.

-   When switching between resource plans, the timeline on the grid view does not change so that your focus remains on the selected date range. However, you can easily set the view to the plan's start date by selecting **Go to Start Date** from the **Actions** menu \(![Actions icon](../../planning-and-policy/image/ellipsis-vertical-icon.png)\).

</td></tr><tr><td>

Resource filter

 ![Resource filter options](../image/filter-options-allocation-workbench.png)

</td><td>

Enable the **Create and manage operational resource plans from the resource allocation workbench** property by navigating to **Project Administration &gt; Properties - Resource** to search for operational resource plans from the allocation workbench.

 Filters projects and demands in the resource grid by group, role, user, or task for the selected period.

 Filter operational resource plans in the resource grid by the operational work type.

</td></tr><tr><td>

State filter

 ![State filter](../image/StateFilter.png)

</td><td>

Filters resource plans in the resource grid using the \(P\) Planning, \(R\) Requested, \(C\) Confirmed, \(A\) Allocated, and \(E\) Extension Requested options.

 **Note:** The \(P\) Planning and \(C\) Confirmed filters are not applicable for operational resource plans.

</td></tr><tr><td>

Week or Month view

 ![Week and month toggle](../image/WeekMonthToggle.png)

</td><td>

Shows allocations in weekly or monthly format in both the resource grid and resource finder sections.

</td></tr><tr><td>

Hours, FTE, or Person days view

 ![Hours, FTE, Person days view list](../image/HoursFTESwitch.png)

</td><td>

Shows allocations in hours, FTE, or person days format in both the resource grid and resource finder sections.

</td></tr><tr><td>

Resource Finder

 ![Resource finder icon](../../planning-and-policy/image/ResourceFinderIcon.png)

</td><td>

Displays the resource finder section at the bottom of the workbench. Use the resource finder section to [search resources and create a resource plan for them](../task/create-resource-plan-with-finder.md).

</td></tr><tr><td>

Configuration

 ![Configuration](../image/ConfigurationIcon.png)

</td><td>

Shows or hides the selected columns on the grid.

 Selecting the **Planned Cost**, **Actual Cost**, **Conf/Alloc Cost**, or **Resource Type** columns pins them on the grid before the **Details** column group. Other columns are added in the **Details** column group in the collapsed state. To view the collapsed columns, click the expand icon \(![Expand icon](../image/expand-icon.png)\) on the **Details** column group.

</td></tr><tr><td>

Legend

 ![Legend](../image/resource_workbench_legend.png)

</td><td>

Specifies the state of the resource plan using the **Partial Allocated** legend.

</td></tr></tbody>
</table>## Resource grid

The resource grid lists all investments and the resources requested or allocated to them. In the grid view, you can perform the following tasks:

-   Edit the planned, confirmed, and allocated hours inline without opening the record in a form.
-   Request changes to submitted resource plans, or request an extension of an allocated resource plan.
-   Confirm or allocate resource plans to a project or demand.
-   Allocate resources for an operational resource plan.
-   Replace one user's allocation with another user
-   Shift allocations of a user to a future date
-   Move a resource plan and its allocations to a future date
-   Complete, delete, or cancel resource plans.
-   Group, hide, or show columns.
-   Identify the resource plans created with specific members preference by viewing the **Resource plan created with specific members** icon \(![Icon for resource plans created with specific members](../../project-management/image/specificmember_allocation_wb_grid.png)\) next to the resource plans.

    **Note:** The confirm, replace, shift, and move actions can’t be performed for an operational resource plan.


## Resource finder

The bottom resource finder section of the allocation workbench is hidden by default. To make it visible, select the resource finder icon \(![Resource finder icon](../../planning-and-policy/image/ResourceFinderIcon.png)\) at the top right. In the Resource finder, you can perform the following actions:

-   Search for resources and view their availability and utilization. You can search resources by group, role, or user.
-   Add or confirm resource plans for the current resources.
-   Configure the **Actuals** column using **Detailed View**.
-   Filter resources in the **Resource Finder** by available, overallocated, or all resources.
-   Identify resources that are created as specific members for a resource plan by viewing the **Member specified in the resource plan** icon \(![Icon for resources created as specific members](../../project-management/image/specificmember_allocation_wb_grid.png)\) next to the resources.
-   View the Resource Availability and Resource Capacity grids by selecting a capacity or availability column.

    View the user and resource allocation details in a pop-up window by selecting the **User** and **Allocated Hours** columns respectively in the **Resource Availability** grid.

    **Note:** The allocated values are displayed in the Hours, FTE, or Person Days fields based on the selection made in the Allocation Workbench.


-   **[Create or update an allocation board](../task/create-allocation-board.md)**  
Create a personalized allocation board to manage your filtered resources in terms of their capacity, availability, and utilization.
-   **[Manage resources by using the allocation workbench](../task/manage-resources-allocation-workbench.md)**  
Use the allocation workbench to manage your resources effectively. You can review all resource requests in one place for your team. You can also see the available hours for requested users and efficiently allocate resources.
-   **[Manage operational resource plans from the allocation workbench](../task/manage-operational-rp-raw.md)**  
Create and manage operational resource plans effectively from one place using the Resource Allocation Workbench without having to navigate individually to the operational resource plan's form or list.

**Parent Topic:**[Resource Management classic](c_ResourceManagement.md)

