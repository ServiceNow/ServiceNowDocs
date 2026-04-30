---
title: Project and project task states
description: In the base system, the states in project and project task inherit the states in Task table.
locale: en-US
release: xanadu
product: Project Management
classification: project-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Project Management, Project Portfolio Management, Strategic Portfolio Management]
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

The category information for the states is declared in [dictionary override](https://www.servicenow.com/docs/access?context=c_DictionaryOverrides&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) of State column in Planned task \(`planned_task`\) table in **Attributes** field. Planned task is the parent table for project and project task tables.

-   **[View default project and project task state categories](../task/view-default-project-task-states.md)**  
View category information for the default project and project task states. In the base system, the states in project and project task inherit the states in Task table.
-   **[Customize a state for project or project task](../task/customize-project-task-states.md)**  
Add or modify a state of project or project task using dictionary override.

**Parent Topic:**[Project Management](c_ProjectApplicationOverview.md)

