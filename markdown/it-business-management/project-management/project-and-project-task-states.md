---
title: Project and project task states
description: In the base system, the states in project and project task inherit the states in Task table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/project-management/project-and-project-task-states.html
release: australia
product: Project Management
classification: project-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Basics of Project Management, Exploring Project Management, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Project and project task states

In the base system, the states in project and project task inherit the states in Task table.

The states are grouped into different categories as shown below:

|State|Label|Category|
|-----|-----|--------|
|-5|Pending|Pending|
|1|Open|Open|
|2|Work in Progress|Work in Progress|
|3|Closed Complete|Closed|
|4|Closed Incomplete|Closed|
|7|Closed Skipped|Closed|

The category information for the states is declared in [dictionary override](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/c_DictionaryOverrides.md) of State column in Planned task \(`planned_task`\) table in **Attributes** field. Planned task is the parent table for project and project task tables.

The start and end dates are displayed based on the project or task status:

-   Pending/Open: Planned start date is displayed.
-   Open/Work in Progress: Actual start date is displayed.
-   Closed: Actual end date is displayed.

**Parent Topic:**[Basics of Project Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-management/c_ProjectTasks.md)

**Related topics**  


[Parent-child rollup task calculations]()

[Project tasks]()

[Schedule conflicts between project tasks]()

[Change requests and project tasks]()

[Project task checklists]()

[Task resources]()

[Composite Fields]()

[Cost plan breakdown]()

[Actual project costs]()

[Types of external dependencies]()

[Project and portfolio funding]()

[View default project and project task state categories](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-management/view-default-project-task-states.md)

[Customize a state for project or project task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-management/customize-project-task-states.md)

