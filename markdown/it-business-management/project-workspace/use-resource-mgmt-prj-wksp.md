---
title: Resource planning with Project Workspace
description: Use the Resource Management application to allocate and manage your resources in the Project Workspace.
locale: en-US
release: zurich
product: Project Workspace
classification: project-workspace
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Project Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Resource planning with Project Workspace

Use the Resource Management application to allocate and manage your resources in the Project Workspace.

## Key benefits

Using Resource Management, you can create, plan, track, and monitor resource assignments at a project or task level in the Project Workspace. With Resource Management in Project Workspace, you can:

-   Create an attribute-based resource assignment.
-   Change the resource assignment dates, resources, efforts, and proposed allocations at any level of the project.
-   View resource allocations using new heatmap modal. The allocations are color-coded to display the availability of the resources.
-   View the primary attributes such as Group, Role, and Skill of each resource in the resource assignment pane. They are useful when you work on reassigning a task to a different user with the same primary attributes.
-   Switch between **Hours**, **FTE**, or **Person Days** effort types to view resource allocations.

## Resource assignment pane

The resource assignment pane displays a interface where you add resource assignments for your projects or project tasks.

## Resource allocations and heatmap

The Resource allocation view combines a hierarchical task structure by resource with time-based and effort-based allocation metrics, such as hours, FTE, or person-days over weekly or monthly intervals.

**Note:** Switch between different efforts such as hours, FTE, or person days to view a resource allocation heatmap based on the selected effort type.

Allocation heatmap modal gives you an overview of the resource utilization to identify the over allocated and the available resources. The allocations are color-coded to display the availability of the resources and help you to identify the availability of the resource for the filtered time frame. The new heatmap modal gives you the following insights for a resource such as the assigned tasks with their respective project owner, resource status, efforts for each task, total utilization percentage for the approved tasks, and the remaining capacity.

![Legend for resource allocation view.](../../resource-management-workspace/images/rmw-heatmap-legend.png)

## Heatmap breakdown

![Heatmap modal explaining different parameter values of resource allocation.](../../resource-management-workspace/images/rmw-allocation-modal.png "Allocation heatmap breakdown")

From the above example, you can see the breakdown of the approved work items along with the rolled up efforts, Utilization percentage, and the Remaining capacity for the month of January 2025. The approved work is within the resource capacity as the remaining capacity is 120 hours. Resource manager can use these insights to decide and allocate the pending work items to another resource with available effort.

Within the Resource Allocation view, the Approved state is prioritized and listed first, followed by other statuses based on their order in the record list. Additionally, if a user has no capacity during a given period, the corresponding cell is displayed in red color.

-   **[Resource assignments in Project Workspace](resource-assignments-pw.md)**  
Optimize project execution by assigning resources to tasks within the Project Workspace. You can create resource assignments for any project or project task, specifying the tasks to be performed and the resources to be allocated.

**Parent Topic:**[Project Workspace](../../project-workspace/concept/project-workspace-landing-page.md)

