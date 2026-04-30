---
title: Types of external dependencies
description: The Project management application supports two types of external dependencies - hard and soft.
locale: en-US
release: xanadu
product: Project Management
classification: project-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [External dependencies, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Types of external dependencies

The Project management application supports two types of external dependencies - hard and soft.

The type of external dependency can be set during [adding a dependency](../task/create-external-dependency-planning-console.md) between two projects tasks on the planning console.

## Hard dependencies

In a hard dependency, any changes made in the predecessor project are automatically propagated to the successor project. A [notification](../reference/r_PlanningConsoleTasks.md#table_ukw_ftd_2s) for the changes made is triggered in the successor project. The following image shows the process flow for a hard dependency type:

![Process flow for a hard dependency type](../image/ExternalHardDependency.png "External hard dependency")

## Soft dependencies

In a soft dependency, any changes made in the predecessor project trigger a notification in the successor project. As the project manager of the successor project, you can choose to accept or reject the changes in the notification. If you accept the notification changes, the changes in the predecessor project are synced to the successor project and the project is recalculated. If you reject the notification changes, the changes are not propagated to the successor project. The following image shows the process flow for a soft dependency type:

![Process flow for a soft dependency type](../image/ExternalSoftDependency.png "External soft dependency")

**Parent Topic:**[External dependencies](external-dependencies.md)

**Related topics**  


[Add an external dependency on planning console](../task/create-external-dependency-planning-console.md)

