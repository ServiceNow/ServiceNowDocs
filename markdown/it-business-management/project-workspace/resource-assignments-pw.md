---
title: Resource assignments in Project Workspace
description: Optimize project execution by assigning resources to tasks within the Project Workspace. You can create resource assignments for any project or project task, specifying the tasks to be performed and the resources to be allocated.
locale: en-US
release: australia
product: Project Workspace
classification: project-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Resource planning with Project Workspace, Project Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Resource assignments in Project Workspace

Optimize project execution by assigning resources to tasks within the Project Workspace. You can create resource assignments for any project or project task, specifying the tasks to be performed and the resources to be allocated.

## Resource assignments

Resource assignment is a process of allocating a resource or group of resources to a project task. When a resource assignment is initiated, a resource plan is auto-generated in the back-end of the project management system. This resource plan details the information of how resources would be allocated throughout the project. Resource assignments are approved by the resource manager to make sure that the allocation aligns with the overall resource strategy, considering factors such as availability, skills, and project priorities. Resource assignments remain dynamic and can be edited throughout the project life cycle. Resources can be assigned based on defined attributes such as skills, expertise, or other criteria relevant to the project or task.

**Note:**

Resource efforts calculations are driven by the `com.snc.resource_management.exclude_status_from_capacity` property. Admin can configure this property to calculate efforts for certain defined resource assignments only. For more information, see [Resource Management properties](../../resource-management/reference/r_ResourceProperties.md).

Edit the child resource assignments directly using the inline editing from the resource assignment pane.

## Key features

With resource assignments, you can:

-   Determine the resource engagement timing and allocate resources for specified durations, contributing to the creation of a timeline for task completion.
-   Align task execution with the project plan, ensuring tasks are carried out in accordance with specified timelines and resource requirements.
-   Initiate an approval process that is conducted by a resource manager and make sure it aligns with project targets and resource availability.

-   **[Create resource assignments using Project Workspace](../task/create-resource-assignment-prj-wksp.md)**  
Create an attribute-based resource assignment in the Project Workspace application for any project or project task.
-   **[Update resource assignment from Project Workspace](../task/update-resource-assignment-pw.md)**  
Update a resource assignment that is associated with a project or project task.
-   **[Manage resources from resource page in Project Workspace](../task/manage-resource-assignment-pw.md)**  
View and manage all the resource assignments without navigating through individual tasks using the resource page in Project Workspace. Resources page shows all project-associated resources and their assignments to support forecasting and visualization of resource demands.
-   **[Access, assign, and approve unassigned work in Project Workspace](../task/assign-approve-unassigned-work-pw.md)**  
View, assign and authorize resources directly from Project Workspace without navigating to Resource Management Workspace.
-   **[Move a resource assignment in Project Workspace](../task/move-resource-assignments-project-workspace.md)**  
Move the resource assignment to a new start and end dates to accommodate changes in task scheduling or resource allocation. Shift assignments to balance workloads across resources and avoid over-allocation.
-   **[Extend a resource assignment](../task/extend-resource-assignment-pw.md)**  
Extend the date of an allocated resource assignment and allocate resources for the extended period.
-   **[Delete a resource assignment from Project Workspace](../task/delete-resource-assignment-pw.md)**  
Delete a resource assignment from Project Workspace. Deleting an assignment also deletes all associated resource allocations.
-   **[Update the resource allocation in a heatmap](../task/view-allocations-heatmap-prj-wksp.md)**  
Use the allocation heatmap capability in Project Workspace to view and update the resource allocation.
-   **[Realign resource assignment to project task](../task/realign-resource-assignment-to-task.md)**  
Realign or synchronize the resource assignment dates with the project task dates. This synchronization helps to schedule and align the resource assignments with the timeline of project task.

**Parent Topic:**[Resource planning with Project Workspace](use-resource-mgmt-prj-wksp.md)

**Related topics**  


[Create resource assignments using Project Workspace](../task/create-resource-assignment-prj-wksp.md)

[Update resource assignment from Project Workspace](../task/update-resource-assignment-pw.md)

[Resource plans](../../resource-management/concept/c_ResourcePlans.md)

