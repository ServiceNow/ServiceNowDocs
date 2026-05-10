---
title: Project and project task states
description: In the base system, the states in project and project task inherit the states in Task table.
locale: en-US
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

The category information for the states is declared in [dictionary override](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/c_DictionaryOverrides.md) of State column in Planned task \(`planned_task`\) table in **Attributes** field. Planned task is the parent table for project and project task tables.

The start and end dates are displayed based on the project or task status:

-   Pending/Open: Planned start date is displayed.
-   Open/Work in Progress: Actual start date is displayed.
-   Closed: Actual end date is displayed.

**Parent Topic:**[Basics of Project Management](c_ProjectTasks.md)

**Related topics**  


[Parent-child rollup task calculations](c_ParentChildRollupTaskCalcs.md)

[Project tasks](../task/t_CreateAProjectTask.md)

[Schedule conflicts between project tasks](scheduling-conflicts.md)

[Change requests and project tasks](c_ChangeRequestsAndProjectTasks.md)

[Project task checklists](c_project-task-checklists.md)

[Task resources](c_TaskResources.md)

[Composite Fields](pm-composite-fields.md)

[Cost plan breakdown](cost-plan-breakdown.md#)

[Actual project costs](actual-project-costs.md)

[Types of external dependencies](external-dependency-types.md)

[Project and portfolio funding](../../project-portfolio-suite-with-financials/concept/c_ProjectAndPortfolioFunding.md)

[Project scheduling in Project Management](project-scheduling.md)

[Task constraints](task-constraints-project-management.md)

[View default project and project task state categories](../task/view-default-project-task-states.md)

[Customize a state for project or project task](../task/customize-project-task-states.md)

