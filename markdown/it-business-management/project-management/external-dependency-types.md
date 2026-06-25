---
title: Types of external dependencies
description: The Project management application supports two types of external dependencies - hard and soft.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/project-management/external-dependency-types.html
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

The type of external dependency can be set during [adding a dependency](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-management/create-external-dependency-planning-console.md) between two projects tasks on the planning console.

## Hard dependencies

In a hard dependency, any changes made in the predecessor project are automatically propagated to the successor project. A [notification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-management/r_PlanningConsoleTasks.md) for the changes made is triggered in the successor project. The following image shows the process flow for a hard dependency type:

\[Omitted image "ExternalHardDependency.png"\] Alt text: Process flow for a hard dependency type

## Soft dependencies

In a soft dependency, any changes made in the predecessor project trigger a notification in the successor project. As the project manager of the successor project, you can choose to accept or reject the changes in the notification. If you accept the notification changes, the changes in the predecessor project are synced to the successor project and the project is recalculated. If you reject the notification changes, the changes are not propagated to the successor project. The following image shows the process flow for a soft dependency type:

\[Omitted image "ExternalSoftDependency.png"\] Alt text: Process flow for a soft dependency type

**Parent Topic:**[Basics of Project Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-management/c_ProjectTasks.md)

**Related topics**  


[Parent-child rollup task calculations]()

[Project tasks]()

[Schedule conflicts between project tasks]()

[Change requests and project tasks]()

[Project task checklists]()

[Task resources]()

[Project and project task states]()

[Composite Fields]()

[Cost plan breakdown]()

[Actual project costs]()

[Project and portfolio funding]()

