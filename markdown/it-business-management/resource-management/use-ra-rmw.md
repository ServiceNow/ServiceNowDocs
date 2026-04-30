---
title: Manage resource assignments from Project Workspace
description: Optimize project execution by assigning resources to tasks within the Project Workspace. You can create resource assignments for any project or project task, specifying the tasks to be performed and the resources to be allocated. Use the Resource Management application to allocate and manage your resources in the Project Workspace.
locale: en-US
release: yokohama
product: Resource Management
classification: resource-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Use, Resource Management Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Manage resource assignments from Project Workspace

Optimize project execution by assigning resources to tasks within the Project Workspace. You can create resource assignments for any project or project task, specifying the tasks to be performed and the resources to be allocated. Use the Resource Management application to allocate and manage your resources in the Project Workspace.

## Resource assignments

Resource assignment is a process of allocating a resource or group of resources to a project task. When a resource assignment is initiated, a resource plan is auto-generated in the back-end of the project management system. This resource plan details the information of how resources would be allocated throughout the project. Resource assignments are approved by the resource manager to make sure that the allocation aligns with the overall resource strategy, considering factors such as availability, skills, and project priorities. Resource assignments remain dynamic and can be edited throughout the project life cycle. Resources can be assigned based on defined attributes such as skills, expertise, or other criteria relevant to the project or task.

**Note:**

Resource efforts calculations are driven by the `com.snc.resource_management.exclude_status_from_capacity` property. Admin can configure this property to calculate efforts for certain defined resource assignments only. For more information, see [Resource Management properties](../../resource-management/reference/r_ResourceProperties.md).

Edit the child resource assignments directly using the inline editing from the resource assignment pane.

Using Resource Management, you can create, plan, track, and monitor resource assignments at a project or task level in the Project Workspace. With Resource Management in Project Workspace, you can:

-   Create an attribute-based resource assignment.
-   Change the resource assignment dates, resources, efforts, and proposed allocations at any level of the project.
-   View resource allocations using new heatmap modal. The allocations are color-coded to display the availability of the resources.
-   View the primary attributes such as Group, Role, and Skill of each resource in the resource assignment pane. They are useful when you work on reassigning a task to a different user with the same primary attributes.
-   Switch between **Hours**, **FTE**, or **Person Days** effort types to view resource allocations.

**Important:** Resource efforts calculations are driven by the `com.snc.resource_management.exclude_status_from_capacity` property. Admin can configure this property to calculate efforts for certain defined resource assignments only. For more information, see [Resource Management properties](../../resource-management/reference/r_ResourceProperties.md).

## Key features

With resource assignments, you can:

-   Determine the resource engagement timing and allocate resources for specified durations, contributing to the creation of a timeline for task completion.
-   Align task execution with the project plan, ensuring tasks are carried out in accordance with specified timelines and resource requirements.
-   Initiate an approval process that is conducted by a resource manager and make sure it aligns with project targets and resource availability.

## Key benefits

Using Resource Management, you can create, plan, track, and monitor resource assignments at a project or task level in the Project Workspace. With Resource Management in Project Workspace, you can:

-   Create an attribute-based resource assignment.
-   Change the resource assignment dates, resources, efforts, and proposed allocations at any level of the project.
-   View resource allocations using new heatmap modal. The allocations are color-coded to display the availability of the resources.
-   View the primary attributes such as Group, Role, and Skill of each resource in the resource assignment pane. They are useful when you work on reassigning a task to a different user with the same primary attributes.
-   Switch between **Hours**, **FTE**, or **Person Days** effort types to view resource allocations.

-   **[Create resource assignments using Project Workspace](../task/create-ra-pws-rmw.md)**  
Create an attribute-based resource assignment in the Project Workspace application for any project or project task.
-   **[Update resource assignment from Project Workspace](../task/update-ra-pws-rmw.md)**  
Update a resource assignment that is associated with a project or project task.
-   **[Delete a resource assignment using Project Workspace](../task/delete-ra-pws-rmw.md)**  
Delete a resource assignment from Project Workspace. Deleting an assignment also deletes all associated resource allocations.
-   **[Update resource assignments using Project Workspace](../task/update-ra-heatmap-pws-rmw.md)**  
Use the allocation heatmap capability in Project Workspace to view and update the resource allocation.
-   **[Realign resource assignment to project task using Project Workspace](../task/realign-ra-pws-rmw.md)**  
Realign or synchronize the resource assignment dates with the project task dates. This synchronization helps to schedule and align the resource assignments with the timeline of project task.

**Parent Topic:**[Use resource assignments](use-resource-assignment.md)

