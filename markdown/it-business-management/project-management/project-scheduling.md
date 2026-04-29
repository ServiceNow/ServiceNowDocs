---
title: Project scheduling in Project Management
description: Define how tasks are sequenced, timed, and connected to determine when a project starts and finishes with Project scheduling.
locale: en-US
release: australia
product: Project Management
classification: project-management
topic_type: concept
last_updated: "2026-03-11"
reading_time_minutes: 3
breadcrumb: [Basics of Project Management, Exploring Project Management, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Project scheduling in Project Management

Define how tasks are sequenced, timed, and connected to determine when a project starts and finishes with Project scheduling.

## Project scheduling overview

Learn the relationship between the project start date, task scheduling modes, and task links helps you build accurate, flexible project plans in Project Management.

## Project start date and finish date

When you create a project, the start date determines the schedule. By default, all tasks begin on the project start date. As you add tasks and connect them to one another, individual task start times adjust, and the last task to finish determines the project finish date.

For both manually scheduled and automatically scheduled tasks with no dependencies or constraints, the project duration equals the duration of the longest task.

## Comparing Scheduling Approaches: Start Date and Finish Date

Most projects are scheduled from a known start date, which provides maximum scheduling flexibility. You can schedule from a finish date in the following situations:

-   You should determine when the project must start to meet a required completion date.
-   The project start date is uncertain, such as when work depends on an external source.
-   Your project management method requires finish-date scheduling.

When you schedule from a finish date, Project applies the As Late As Possible \(ALAP\) constraint to automatically scheduled tasks.

-   Dragging a Gantt bar to change a task's finish date automatically applies a Finish No Later Than \(FNLT\) constraint.
-   Switching from start-date to finish-date scheduling removes leveling delays and splits from automatically scheduled tasks. Manually scheduled tasks are not affected.
-   Automatic leveling adds delays after tasks rather than before them.

## Task scheduling modes

Project supports two task scheduling modes:

-   Automatically scheduled tasks: Project calculates start and finish dates based on dependencies, constraints, and the project calendar.
-   Manually scheduled tasks: You control the start and finish dates. Manually scheduled tasks do not move automatically when linked tasks change.

## Critical path

When tasks are linked, Project sets a critical path, the longest sequence of dependent tasks that determines the project's completion date. Delays on this path can directly delay the project finish.

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

[Types of external dependencies](external-dependency-types.md)

[Project and portfolio funding](../../project-portfolio-suite-with-financials/concept/c_ProjectAndPortfolioFunding.md)

[Task constraints](task-constraints-project-management.md)

[Schedule a project from a start date](../task/schedule-a-project-pm.md)

[Task link types](../reference/task-link-types-project-management.md)

