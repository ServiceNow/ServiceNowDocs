---
title: Manage resources for demands
description: Plan resources for a demand from the Resources tab in Next Experience for Demand Management to confirm resource availability before converting the demand to a project.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-business-management/strategic-planning/resource-planning-for-demands-dw.html
release: australia
product: Strategic Planning
classification: strategic-planning
topic_type: concept
last_updated: "2026-09-29"
reading_time_minutes: 9
keywords: [demand resources, resource planning for demands, demand resource grid]
breadcrumb: [Use, Next Experience for Demand Management in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Manage resources for demands

Plan resources for a demand from the **Resources** tab in Next Experience for Demand Management to confirm resource availability before converting the demand to a project.

## Resources board

The Resources board shows the resource assignments of a demand in a single grid, along with their allocations and the capacity of the assigned resources. Assigned and unassigned resource assignments appear together in this grid. Unassigned assignments are listed under a resource row named **Empty**. Use it to check whether the resources a demand needs are available before you commit to the work. Set planned dates for the demand. If the planned dates aren't set, the resource grid isn't displayed. You must have the it\_demand\_manager role to view the Resources board.

\[Omitted image "demand-resource-board.png"\] Alt text: Resources grid for a demand.

The top of the tab shows the demand name and its **Timeline**, which is the date range that the grid covers. The grid covers the period spanning the planned dates of a demand.

Using this intuitive board, demand managers can:

-   View the number of tasks assigned to a resource.
-   Understand the type or state of the assignment, and track the changes made to assignments.

<table id="table_pcl_xhq_bcc"><thead><tr><th>

Indicator

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\[Omitted image "rmw-green-tick.png"\] Alt text: Green tick mark within a green circle indicating the resource allocation is within the available bandwidth.

</td><td>

Indicates that the resource allocation is within the available bandwidth.

</td></tr><tr><td>

\[Omitted image "rmw-red-warning.png"\] Alt text: Red exclamation mark within a red triangle indication the resource is over-allocated.

</td><td>

Indicates that the resource is over allocated for the available bandwidth.

</td></tr><tr><td>

\[Omitted image "rmw-group-asgnmnt-icon.png"\] Alt text: Alphabet i in a circle representing group assignments.

</td><td>

Indicates the work assignment is made for a group.

</td></tr><tr><td>

\[Omitted image "rmw-bell-indicator.png"\] Alt text: Bell icon indicating changes to the approved resource assignment.

</td><td>

Indicates changes to start or end date, allocated hours, and so on, to the approved resource assignments.**Note:** When these changes are made, the status of the assignment is moved to pending, indicating resource manager about the review required for the changes made. Once the changes are reviewed and the assignment is either approved or unapproved, this icon is no longer displayed.

</td></tr></tbody>
</table>-   Understand of the status of the assigned tasks rolled up to resource level using the Resource status column.
-   View the primary attributes such as Group, Role, and Skill of each resource in the grid. These are useful when reassigning a task to a different user with the same primary attributes.
-   View the actual hours vs allocated hours for a task.

    Enable the **Show actuals** toggle \(\[Omitted image "rmw-show-actuals-toggle.png"\] Alt text:\) from the settings side panel \(\[Omitted image "rmw-settings-panel-icon.png"\] Alt text:\) to view the efforts captured for a task via time cards. Approved time cards are reflected in the resource board view as actual hours.

-   Get insights about the resource allocations using the new heatmap modal.
-   Edit the task effort for any group allocations and approve it using the inline editing feature.

    **Note:** If you edit the allocations for any approved group assignment, a confirmation window appears. After approval, the state is changed to Pending.

-   Assign the unassigned tasks.
-   Approve the assigned tasks.
-   Split a resource assignment into two for a single resource at the required date.

## Personalize your resource board view

You can customize the resource board to personalize your view. These user preferences are saved to give you the same view every time.

-   Change effort type: Switch between **Hours**, **FTE**, or **Person Days** effort types to view resource allocations based on the required effort type.
-   Group By: Customize the view of your resource boards using the **Group By** feature to regroup the resources depending on your organization needs. You can group by **Primary Group**, **Primary Role**, **Primary Skill**, or **None**. By default, the grid is grouped by **Primary Group** because this grouping enables demand managers to view resources for a group and manage them efficiently.

    When the grid is grouped by **Primary Group**, an assignment for a named resource is grouped by the primary group in that resource's employee profile. The assignment is not grouped by the group on the assignment. If the resource doesn't have a primary group in their profile, the assignment is listed under the **Empty** group, even if the assignment has a group.

    You can't edit the **Empty** row itself or open a context menu on it. Expand it to work with the assignments listed under it.

    For example, an assignment is created for a user with the Database group. If this user doesn't have a primary group in the user profile, the assignment appears under the **Empty** group instead of Database.

    Assignments that don't have a named resource are grouped by the group, role, or skill on the assignment itself. For example, an unassigned assignment with the Database group appears under Database, in its **Empty** row.

-   Time scale list: Shows one column per month with **Monthly**, or one column per week with **Weekly**.
-   View or hide columns: Use the column config option \(\[Omitted image "icon-column-config.png"\] Alt text: Column configuration settings.\) to view or hide any columns on the resource board.

    To show the assignment **Name** column in the grid, an administrator can add it to the view of the resource assignment list.


## Data grid filtering

Quick filters help you filter and build a personalized view to narrow down datasets instantly without refreshing the page or running complex queries on your resource board. You can filter lists, reference fields, strings, dates, and boolean values.

## Resource allocations and heatmap view

The resource allocation view provides you with a nested view of the assigned work items rolling up to resource level. It also provides a resource allocation breakdown view based on the time-frame \(weekly or monthly\) and by work efforts \(hours, FTE, or person days\).

Select the arrow \(\[Omitted image "icon-expand-arrow.png"\] Alt text: Right pointed arrow head to expand resource details icon.\) icon to get details at the individual demand level assigned to the resources. This provides a breakdown view to understand:

-   Work assigned to a specific resource.
-   The amount of time a resource is allocated to an individual task.

**Tip:** Switch between different efforts such as hours, FTE, or person days to view a resource allocation heatmap based on the selected effort type.

You can edit the resource assignments using the inline editing feature.

The Resource status column displays any Pending \(\[Omitted image "rmw-pending-state.png"\] Alt text: Yellow rectangular pending state icon.\) or Unapproved \(\[Omitted image "rmw-unapproved-state.png"\] Alt text: Pink rectangular unapproved state icon.\) work items assigned to a resource.

**Note:** The status of the assigned work is rolled up to the resource level and the resource card level. If there are any pending or unassigned work items, the rolled up status at resource level and card level shows Pending.

Define custom statuses to calculate and view resource capacity in the allocation heatmap modal.

Allocation heatmap modal gives you an overview of the resource utilization to identify the over allocated and the available resources. The allocations are color-coded to display the availability of the resources and indicate the availability of the resource for the filtered time frame.

\[Omitted image "rmw-heatmap-legend.png"\] Alt text: Legend for resource allocation view.

**Empty** rows aren't color-coded and appear gray, because the assignments under them aren't tied to one resource's capacity. Selecting a cell in an **Empty** row doesn't open the allocation details.

\[Omitted image "demand-resource-allocation-breakdown.png"\] Alt text: Allocation heatmap showing breakdown of approved work items with utilization percentage and remaining capacity.

From the preceding example, you can see the breakdown of the approved work items. This includes the rolled up efforts, Utilization percentage, and the Remaining capacity. A demand manager can use these insights to decide and allocate the pending work items to another resource with available effort.

**Important:** Resource efforts calculations are driven by the `com.snc.resource_management.exclude_status_from_capacity` property. Admin can configure this property to calculate efforts for certain defined resource assignments only. For more information, see [Resource Management properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/resource-management/r_ResourceProperties.md).

Using the `com.snc.resource_management.exclude_status_from_capacity` property, demand managers can customize to view the resource assignments with a specific state in their workspace and what to view in the total allocation modal. For example, you can view resource assignments in either Approved, Unapproved, and Pending resource assignments, or the ones in Approved and Pending states only.

After the property is set up, work items in a specific states to show up in the full capacity and full allocation rollup of a resource. The new allocation modal displays the allocation breakdown and the rollup values of the work items for the configured states.

When you group a resource board using the Group by option, the heatmap allocation modal for a group gives the following insights.

\[Omitted image "demand-resource-allocation-bygroup.png"\] Alt text: Allocation modal displaying utilization and remaining capacity for a resource group.

## Resource finder

-   **AI-powered resource matching**

    Resource Finder is a ServiceNow Otto for SPM skill that evaluates resources against the requirements of an unassigned assignment. The skill considers multiple dimensions simultaneously. These include whether a resource's planning attributes \(role, skills, or group\) align with the requirement of assignment, how much capacity the resource has during the assignment period. They also include the resource's historical allocation patterns compared to the requested effort.

-   **Fit scoring**

    The fit score is a percentage representing how closely a candidate resource matches the requirements of an unassigned assignment. Fit score blends attribute alignment, temporal availability, and workload balance into one number so that you can compare candidates at a glance.

-   **AI-generated rationale**

    Every recommended resource comes with a rationale which is a short and simple explanation of why the skill considers a resource as a good fit. The rationale references specific factors like availability windows and attribute matches.

-   **Two operating modes**

    The AI Resource Finder adapts its behavior based on whether the skill is enabled on your instance.

    With AI enabled, the experience is recommendation-driven. Candidates are ranked by fit score with rationale, and detailed availability data. You can view this using a toggle so the initial view stays focused on the AI insights. You can reveal period-by-period capacity whenever you want to cross-check the AI's recommendations against raw numbers.

    Without AI enabled, the experience is data-driven. You see candidates listed with their availability data up front and a requested effort row appears immediately for side-by-side comparison. This mode functions as a streamlined staffing search tool without the scoring and reasoning layer.

-   **Availability and effort comparison**

    Resource Finder lists each candidate's available capacity against the effort the assignment requires, giving you a quick comparison view. Effort values honors the user preferences configured in your workspace such as hours, FTE, or person days on a weekly or monthly basis.

    The availability heatmap uses color coding to make this comparison instant. A green cell means the resource has enough capacity to meet the requested effort for that period. A red cell means they fall short. For example, if the requested effort is 1 FTE per month and a candidate shows 1 for April and 0 for May. April appears green and May appears red, giving you the availability instantly without doing any mental math.


## Resource efforts termination

Capacity is generated only for the date range between employment start date and employment end date specified in the employee profile. This information is available when the Employee Profile plugin is installed. If the start and end date are unavailable for an employee, manually specify these dates.

Availability for terminated resources is automatically updated to 0 when you run the [resource termination handler job](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/resource-management/resource-termination-scheduled-job.md). This update occurs when the termination date is after the date on which the job is run. If resources are booked for a time period beyond the user's termination dates, those bookings are also updated to 0 in the resource assignments.

