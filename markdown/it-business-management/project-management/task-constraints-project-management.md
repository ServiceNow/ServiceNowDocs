---
title: Task constraints
description: Task constraints define the earliest or latest dates a task can start or finish in an automatically scheduled project. Apply constraints to align the schedule with resource availability, contract milestones, and external deadlines.
locale: en-US
release: australia
product: Project Management
classification: project-management
topic_type: concept
last_updated: "2026-03-18"
reading_time_minutes: 3
breadcrumb: [Basics of Project Management, Exploring Project Management, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Task constraints

Task constraints define the earliest or latest dates a task can start or finish in an automatically scheduled project. Apply constraints to align the schedule with resource availability, contract milestones, and external deadlines.

## Types of constraints

Flexible constraints: These constraints do not require an associated date and allows the scheduling engine to place tasks as early or as late as possible within the boundaries set by dependencies and other constraints. As Soon As Possible \(ASAP\) and As Late As Possible \(ALAP\) are flexible constraints.

Semi-flexible constraints: These constraints require an associated date that defines the earliest or latest allowed start or finish date for a task. The task can complete at any time, as long as it meets the defined boundary. For example, a Start No Earlier Than \(SNET\) constraint set to May 20 helps avoid the task from starting before that date, even if its predecessor finishes earlier.

Inflexible constraints: These constraints require an associated date and anchor the task to a specific start or finish date, overriding task dependencies. For example, a Must Start On \(MSO\) constraint set to September 20 schedules the task on that date regardless of when its predecessor finishes.

## How constraints interact with dependencies

When a task has both a dependency and a constraint, the behavior depends on the constraint type:

-   Flexible constraints respect the dependency. The task starts as soon as its predecessor finishes.
-   Semi-flexible constraints enforce the date boundary. If the predecessor finishes before the constraint date, the task waits until the constraint date is reached.
-   Inflexible constraints override dependencies. The task is fixed to the specified date, regardless of when the predecessor finishes.

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

[Project scheduling in Project Management](project-scheduling.md)

[Apply or change a task constraint](../task/change-task-constraint-project-management.md)

