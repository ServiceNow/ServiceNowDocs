---
title: Using Resource Management Workspace
description: Create custom resource board views of persistent portfolios to view the current resource allocation and resource requests for all of your resources and work.
locale: en-US
release: yokohama
product: Resource Management
classification: resource-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 13
keywords: [resource assignments, resource management, resource allocation]
breadcrumb: [Use, Resource Management Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Using Resource Management Workspace

Create custom resource board views of persistent portfolios to view the current resource allocation and resource requests for all of your resources and work.

Resource assignments from different planning workspaces are pulled into this dedicated view for Resource Managers to give you an overall work view. Resource Managers can access the dashboard to view the assignment details at high level and [create resource cards](../task/rmw-create-rsrc-card.md) to build persistent portfolios and view the resource allocations.

Quickly create multiple portfolios using resource cards and navigate between these cards to work on the resource requests. Use the advanced condition builder to customize these portfolios based on the teams, attributes, groups, and so on, to view the resource allocation.

**Tip:** Save the filter query and the conditions that you build to revisit and work on the resource allocations.

## Overview dashboard

Resource Management Workspace overview dashboard provides a high-level interactive resource assignment details that help Resource managers to focus on where to prioritize the efforts, identify conflicts, and review the upcoming or pending assignments. Using this dashboard, Resource managers can view the data around their resources and work for efficient resource forecast planning.

The Overview dashboard is crafted to reduce the effort of navigate between different resource boards to view the unassigned work, pend activities, and prioritize day-today tasks.

**Note:** When you navigate to Resource Management Workspace, the Overview dashboard is the landing page. You can navigate to resource cards using the side navigation menu.

You can edit the dashboard based on:

-   Primary attributes and date range selection.
-   Add and edit widgets to the dashboard.

![Dashboard view of Resource Management Workspace displaying the resource assignments stats.](../images/rmw-dashboard.png)

The interactive dashboard creates a resource board for any selected data helping you to directly access the customized board view from the dashboard. For example, if you select the Unassigned tasks widget, this creates and navigates you to a resource board view with the list of unassigned tasks from the widget.

On the board view, you can get the drill down view of all the assigned assignments to the users. The timeline range in the board view matches with the date range of the dashboard.

By accessing these custom boards, Resource managers can assign and approve the assignments in reduced turn-around time, and enhancing productivity.

![GIF showing the interactive dashboard selection navigating to resource board view.](../images/rmw-interactive-dashboard-gif.gif)

<table id="table_am1_hdr_1fc"><thead><tr><th>

Widget title

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Resources over allocated

</td><td>

Number of over-allocated users.

</td></tr><tr><td>

Resources under utilized

</td><td>

Number of users with available bandwidth.

</td></tr><tr><td>

Unassigned assignment requests

</td><td>

Number of unassigned tasks.

</td></tr><tr><td>

Pending resource requests

</td><td>

Total number of requests in Pending state.

</td></tr><tr><td>

Upcoming pending assignments

</td><td>

Number of assignments starting by next month.There are two views for this widget. A pie chart and a list view.

Selecting Pie chart navigates you to the resource board view.

Selecting the table values.

-   Start date - opens resource assignment record view.
-   Resource - opens to resource details page.
-   Task - opens project task details in record view.
-   Top task - opens the top task details in record view.

Select **View all** to see the simple list view of assignments.

</td></tr><tr><td>

Assignments ending soon

</td><td>

Number of assignments ending from current date to next month.

</td></tr><tr><td>

Ready for review

</td><td>

Number of assignments that are in ready for review state.

</td></tr><tr><td>

Overdue assignments

</td><td>

Number of assignments with past end dates.

</td></tr><tr><td>

Unapproved assignments

</td><td>

Number of unapproved assignments.

</td></tr><tr><td>

Utilization percentage

</td><td>

Average of the utilization % of the users based on the selected primary attributes.Example: You can select a primary group to view the average utilization % of the entire group. This helps Project Managers to better plan the resource requests. Resource Managers can use this data while approving the assignments.

</td></tr><tr><td>

Assignments status

</td><td>

Breakdown view of the resource assignments based on the status.

</td></tr><tr><td>

Total efforts

</td><td>

Bar chart displaying the monthly breakdown view of allocated hours vs capacity. Select the chart to get the drill down view of the resource allocations in the resource board.

</td></tr><tr><td>

Total resource work by type

</td><td>

Displays the allocated hours based on the task type.Example: Operation work, Project Task, and so on.

</td></tr><tr><td>

Role allocation

</td><td>

Bar chart displaying monthly breakdown view of the total number of allocated hours based on the user roles. Select the chart to get the drill down view of the resource allocations in the resource board.

</td></tr></tbody>
</table>## Resource board

Using this intuitive workspace, Resource Managers can:

-   View the number of tasks assigned to a resource.
-   Understand the type or state of the assignment, and track the changes made to assignments.

<table id="table_pcl_xhq_bcc"><thead><tr><th>

Indicator

</th><th>

Description

</th></tr></thead><tbody><tr><td>

![Green tick mark within a green circle indicating the resource allocation is within the available bandwidth.](../images/rmw-green-tick.png)

</td><td>

Indicates that the resource allocation is within the available bandwidth.

</td></tr><tr><td>

![Red exclamation mark within a red triangle indication the resource is over-allocated.](../images/rmw-red-warning.png)

</td><td>

Indicates that the resource is over allocated for the available bandwidth.

</td></tr><tr><td>

![Alphabet i in a circle representing group assignments.](../images/rmw-group-asgnmnt-icon.png)

</td><td>

Indicates the work assignment is made for a group.

</td></tr><tr><td>

![Bell icon indicating changes to the approved resource assignment.](../images/rmw-bell-indicator.png)

</td><td>

Indicates changes to start or end date, allocated hours, and so on, to the approved resource assignments.**Note:** When these changes are made, the status of the assignment is moved to pending, indicating resource manager about the review required for the changes made. Once the changes are reviewed and the assignment is either approved or unapproved, this icon is no longer displayed.

</td></tr></tbody>
</table>-   Understand of the status of the assigned tasks rolled up to resource level using the Resource status column.
-   View the primary attributes such as Group, Role, and Skill of each resource in the top tray. These come in handy while working on reassigning a task to different user with the same primary attributes.
-   View the priority and state of the project, demand, or epic in the Priority and State columns in the resource board and allocate resources to priority or high-risk planning items.
-   View the actual hours vs allocated hours for a task.

    Enable the **Show actuals** toggle \(![Toggle button to view actual hours in Resource Management Workspace](../images/rmw-show-actuals-toggle.png)\) from the settings side panel \(![Gear icon to view or hide settings side panel.](../images/rmw-settings-panel-icon.png)\) to view the efforts captured for a task via time cards. Approved time cards are reflected in the resource board view as actual hours.

-   Get insights about the resource allocations using the new heatmap modal.
-   View or hide requested work in the lower tray using **Unassigned tasks** toggle.
-   Filter unassigned work to view the custom requests.
-   Edit the task effort for any group allocations and approve it in the top-tray using the inline editing feature.

    **Note:** If you edit the allocations for any approved group assignment, a confirmation window appears. Once approved, the state is changed to Pending.

-   [Assign the unassigned](../task/allocate-resources-rmw.md) tasks.
-   [Approve or unapprove](../task/allocate-resources-rmw.md) the assigned tasks.
-   [Split a resource assignment](../task/split-resource-assignment-rmw.md) into two for one resource at the required date.

Once you access these resource cards, you get a similar view as the following example with extensive insights.![Resource Portfolio view depicting resource allocation and unassigned tasks.](../images/rmw-rsrc-portfolio-view.png)

**Tip:** You can filter out or add required columns in the top and bottom tray of the resource board view using **Column config** \(![Column configuration settings.](../../alignment-planner-workspace/images/icon-column-config.png)\) settings.

## Personalize your resource board view

You can customize the resource board to personalize your view. These user preferences are saved to give you the same view every time.

-   View or hide unassigned tasks

    Use the **Unassigned tasks** \(![Unassigned tasks toggle.](../images/rmw-unassigned-tasks-toggle.png)\) toggle to view or hide the unassigned tasks in the bottom tray.

    The Unassigned tasks view, in the bottom tray, facilitates you to build a custom filter condition to view unassigned requests with details such as duration, breakdown view of requested efforts, requested work item and its parent item, owner or requester of the task. Use the filter condition builder to get a custom or focused view of the unassigned tasks.

    ![Filter condition to view the current quarter's unassigned work for a specific resource.](../images/rmw-unassigned-work-filter-condition.png)

-   Change effort type

    Switch between **Hours**, **FTE**, or **Person Days** effort types to view resource allocations based on the required effort type.

-   Group By

    Customize the view of your resource boards using the **Group By** feature to regroup the resources depending on your organization needs. You can group by **Primary Group**, **Primary Role**, **Primary Skill**, **Owner**, or **Project**.

-   View or hide columns

    Use the column config option \(![Column configuration settings.](../../alignment-planner-workspace/images/icon-column-config.png)\) to view or hide any columns on the top tray or bottom tray of the resource board.


## Data grid filtering

Quick filters help you filter and build a personalized view to narrow down datasets instantly without refreshing the page or running complex queries on your resource board. You can filter lists, reference fields, strings, dates, and boolean values.

## Resource allocations and heatmap view

The resource allocation view in the top tray provides you with a nested view of the assigned work items rolling up to resource level and the resource allocation breakdown view based on the time-frame \(weekly or monthly\) and by work efforts \(hours, FTE, or person days\).

Select the arrow \(![Right pointed arrow head to expand resource details icon.](../images/icon-expand-arrow.png)\) icon to get details at the individual task level \(epics, demands, and so on\) assigned to the resources. This helps you to get a breakdown view to understand:

-   Work assigned to a specific resource.
-   The amount of time a resource is allocated to an individual task.

**Tip:** Switch between different efforts such as hours, FTE, or person days to view a resource allocation heatmap based on the selected effort type.

You can edit the resource assignments using the inline editing feature in the top-tray.

The **Resource status** column helps you to easily identify any Pending \(![Yellow rectangular pending state icon.](../images/rmw-pending-state.png)\) or Unapproved \(![Pink rectangular unapproved state icon.](../images/rmw-unapproved-state.png)\) work items assigned to a resource.

**Note:** The status of the assigned work is rolled up to the resource level and the resource card level. If there are any pending or unassigned work items in the top tray, the rolled up status at resource level and card level shows Pending.

Define custom statuses to calculate and view resource capacity in the allocation heatmap modal.

Allocation heatmap modal gives you an overview of the resource utilization to identify the over allocated and the available resources. The allocations are color-coded to display the availability of the resources and help you to identify the availability of the resource for the filtered time frame.

The new heatmap modal gives you the following insights for a resource such as the assigned tasks with their respective project owner, resource status, efforts for each task, total utilization percentage for the approved tasks, and the remaining capacity.

![Legend for resource allocation view.](../images/rmw-heatmap-legend.png)

![Heatmap modal explaining different parameter values of resource allocation.](../images/rmw-allocation-modal.png "Allocation heatmap breakdown")

From the preceding example, you can see the breakdown of the approved work items along with the rolled up efforts, Utilization percentage, and the Remaining capacity for the month of January 2025. The approved work is within the resource capacity as the remaining capacity is 120 hours. A Resource manager can use these insights to decide and allocate the pending work items to another resource with available effort.

**Important:** Resource efforts calculations are driven by the `com.snc.resource_management.exclude_status_from_capacity` property. Admin can configure this property to calculate efforts for certain defined resource assignments only. For more information, see [Resource Management properties](../../resource-management/reference/r_ResourceProperties.md).

Using the `com.snc.resource_management.exclude_status_from_capacity` property, Resources managers can customize to view the resource assignments with a specific state in their workspace and what to view in the total allocation modal. For example, you can view resource assignments in either Approved, Unapproved, and Pending resource assignments, or the ones in Approved and Pending states only.

Once the property is set up, work items in a specific states to show up in the full capacity and full allocation rollup of a resource. The new allocation modal displays the allocation breakdown and the rollup values of the work items for the configured states.

When you group a resource board using the Group by option, the heatmap allocation modal for a group gives the following insights.

![Allocation modal displaying utilization and remaining capacity for a resource group.](../images/rmw-grouped-allocation-modal.png)

For example, when you group a resource board by Primary Group to view the allocation heatmap modal of a group for January 2025, the following modal is displayed. This modal gives insights into the total overall allocation of different types of Resource statuses.

**Note:** The efforts in the allocation modal are displayed in Hours.

## Group resources on resource board

The resource board provides a comprehensive list of resources, which are fetched depending on various resource attribute types, projects, and work items. You can group these resources to gain an accurate perspective on specific attributes, owner, or the parent items associated with the projects. You can group the resources by **Primary Group**, **Primary Role**, **Primary Skill**, **Owner** of the task, or **Parent Item** of the work.

If you group the resource board by **Primary Group**, you see the list of primary groups that the resources are associated with and a drop-down of the list of resources in that group and the work item they're working on. In this view, you also get the rolled up values of the efforts at resource level and group level. The rolled up values can be viewed at a monthly or weekly breakdown.

Resource Managers can use this information to plan the resources and manage assignments.

**Tip:** Grouping the resources based on the primary attributes helps Resource Managers to easily reassign the work as the primary attributes should match to reassign work. For more information on how to reassign a work, see [Reassign or unassign work using Resource Management Workspace](../task/rmw-reassign-unassign-work.md).

![Resource board grouped by Primary Group attribute.](../images/rmw-board-groupby-primary-group.png)

-   **[Create a resource card](../task/rmw-create-rsrc-card.md)**  
Create a custom resource card to view resources and unassigned tasks, and work on resource mapping for your persistent and focused portfolios.
-   **[Create resource assignments and operation resource assignments in Resource Management Workspace](../task/create-ra-rmw.md)**  
Create and assign resource assignments and operation resource assignments from Resource Management Workspace.
-   **[View, assign, and approve unassigned work using Resource Management Workspace](../task/allocate-resources-rmw.md)**  
Filter the unassigned work to view priority requests and assign them to resources. Quickly connect with the requester via Microsoft Teams to get additional insights and approve the assigned work using the inline editing feature.
-   **[Move a resource assignment](../task/move-ra-rmw.md)**  
Move a resource assignment to a different start and end dates depending on the availability of the resource.
-   **[Reassign or unassign work using Resource Management Workspace](../task/rmw-reassign-unassign-work.md)**  
Reassign or unassign any assigned work from the Resource Management Workspace. You can group the resource board by primary attributes to identify the resources with same primary attributes.
-   **[Split resource assignments using Resource Management Workspace](../task/split-resource-assignment-rmw.md)**  
Splitting a resource assignment at a specific date creates a resource assignment for the same user.
-   **[Manage resource allocations in Resource Management Workspace](../task/manage-resource-allocations-rmw.md)**  
Manage resource allocations to change efforts, start and end dates, extend and so on to adjust resources based on their availability and the priority of the tasks.
-   **[Export resource portfolio view to Excel or CSV format](../task/export-rmw-card-view.md)**  
Export your resource portfolio view in Resource Management Workspace as Microsoft Excel or CSV format to review or share the resource status with stakeholders, even if they don't have access to your instance.

**Parent Topic:**[Use resource assignments](use-resource-assignment.md)

