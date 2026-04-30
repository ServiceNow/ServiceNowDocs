---
title: Review capacity of the resources
description: Use the capacity planning page to review the capacity and utilization trends of the resources associated with the requested resource plans.
locale: en-US
release: xanadu
product: Resource Management
classification: resource-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Capacity planning overview, Resource Management classic, Project Portfolio Management, Strategic Portfolio Management]
---

# Review capacity of the resources

Use the capacity planning page to review the capacity and utilization trends of the resources associated with the requested resource plans.

## About this task

**Important:** Capacity planning is being deprecated starting Xanadu release. It will be hidden and no longer available for installation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Resource Managers are encouraged to use the [Planning user capacity in Strategic Planning Workspace](../../spw-capacity-planning/concept/using-cap-plan-spw.md) to view and manage the capacity, allocations, and utilization of resources.

## Before you begin

Role required: resource\_manager

## Procedure

1.  Navigate to **All** &gt; **Resource** &gt; **Resource Workbench** &gt; **Capacity Planning**.

2.  To filter the list of displayed resource plans, select the filter icon \(![filter](../../project-management/image/filter_icon.png)\) in the **Resource Plans** section.

    The filtered resource plans are displayed as cards.

3.  To view its resource forecast, select a resource plan in the **Resource Plans** section.

    You can select more than one resource plan. To select all the plans in the list, select the **Select All** check box.

    **Note:** When you select multiple plans, the requested hours are added for the selected plans in the bar graph. You can continue adding plans until the team capacity \(shown as red dotted line\) is shown fully utilized.

4.  In the **Resource Forecast** section, review the resource capacity and utilization for the selected resource plans.

    The section shows the information in the following tabs.

    -   **Overview** tab: Displays the following information in a stacked bar chart. Point to any of the sections on the bar chart to show its details.
        -   **Requested**: Number of hours that the resource has been requested for the selected resource plans only.
        -   **Confirmed**: Number of hours confirmed. The value considers all resource plans and the hours across all projects and demands for the group or user requested for selected resource plans.
        -   **Allocated**: Number of hours that the resource is already committed. The value considers all resource plans and the hours on the user calendar. For example, hours allocated for operational work or meetings across all projects and demands for group or user requested for selected resource plans.
        -   **Capacity**: Total capacity trend for the resources, which is derived from the user or group schedule. The group capacity is rolled up from the schedules of all the members.

            **Note:** Capacity isn’t derived from FTE, but from schedules. Both FTE and schedules must be in synchronization with each other.

    -   **% Utilization** tab: Displays the heat map for the percentage of utilization of resources including both hard and soft allocations and requested hours for the selected resource plans.
5.  To show or hide the respective bar or line in the graph, select an item in the legend below the graph.

6.  To open and modify the display settings for the graph and heat map, select the Settings icon ![settings](../image/PersonalizeIcon.png) in the **Resource Forecast** section.

7.  In the **Resource Forecast** section, use the following options to take an action on a resource plan.

<table id="choicetable_swx_rmw_kx"><tbody><tr><td id="d64870e221">

**__Confirm__**

</td><td>

Confirms the resources to the selected plan.The selected resource plan moves to the Confirmed state. [Soft allocations](../reference/r_AllocatingResources.md) are created when the resource plan moves to the Confirmed state.

</td></tr><tr><td id="d64870e243">

**__Confirm and Allocate__**

</td><td>

Allocates the resources to the selected plan directly without first confirming them.The selected resource plan moves to the Allocated state. [Hard allocations](../reference/r_AllocatingResources.md) are created when the resource plan moves to the Allocated state.

</td></tr><tr><td id="d64870e265">

**__Reject__**

</td><td>

Rejects the selected plan.

</td></tr></tbody>
</table>    **Note:** You can select more than one resource plan to Confirm, Confirm and Allocate, or Reject.


**Parent Topic:**[Capacity planning overview](../concept/c_ResourceWorkbench.md)

