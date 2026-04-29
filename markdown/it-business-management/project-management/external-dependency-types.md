---
title: Types of external dependencies
description: The Project management application supports two types of external dependencies - hard and soft.
locale: en-US
release: australia
product: Project Management
classification: project-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Basics of Project Management, Exploring Project Management, Project Management, Project Portfolio Management, Strategic Portfolio Management]
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

**Parent Topic:**[Basics of Project Management](c_ProjectTasks.md)

**Related topics**  


[Parent-child rollup task calculations](c_ParentChildRollupTaskCalcs.md)

[Project tasks](../task/t_CreateAProjectTask.md)

[Schedule conflicts between project tasks](scheduling-conflicts.md)

[Change requests and project tasks](c_ChangeRequestsAndProjectTasks.md)

[Project task checklists](c_project-task-checklists.md)

[Task resources](c_TaskResources.md)

[Project and project task states](project-and-project-task-states.md)

[Composite Fields](pm-composite-fields.md)

[Cost plan breakdown](cost-plan-breakdown.md#)

[Actual project costs](actual-project-costs.md)

[Project and portfolio funding](../../project-portfolio-suite-with-financials/concept/c_ProjectAndPortfolioFunding.md)

[Project scheduling in Project Management](project-scheduling.md)

[Task constraints](task-constraints-project-management.md)

