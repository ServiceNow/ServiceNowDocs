---
title: Project scheduling in Project Management
description: Define how tasks are sequenced, timed, and connected to determine when a project starts and finishes with Project scheduling. Project scheduling calculates task start and finish dates based on the project start date, task dependencies, constraints, and task duration in forward scheduling mode.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/project-management/project-schedules-tasks.html
release: australia
product: Project Management
classification: project-management
topic_type: concept
last_updated: "2026-08-17"
reading_time_minutes: 7
keywords: [project scheduling, task constraints, forward scheduling, task dependencies, start date scheduling]
breadcrumb: [Basics of Project Management, Exploring Project Management, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Project scheduling in Project Management

Define how tasks are sequenced, timed, and connected to determine when a project starts and finishes with Project scheduling. Project scheduling calculates task start and finish dates based on the project start date, task dependencies, constraints, and task duration in forward scheduling mode.

## Project scheduling overview

Learn the relationship between the project start date, task scheduling modes, and task links helps you build accurate, flexible project plans in Project Management.

## Forward scheduling from project start date

Project Management uses forward scheduling, calculating all task dates from a defined project start date. When you create a project, the system establishes a project start date. All tasks schedule on or after this date unless you apply constraints or create dependencies to other tasks.

Forward scheduling gives maximum scheduling flexibility. The scheduling engine adjusts task start dates based on predecessor task completion, constraints you apply, resource availability, and project calendars. As you add tasks and create relationships between them, the system calculates the overall project finish date based on the longest chain of dependent tasks \(the critical path\).

**Important:** ServiceNow Project Management supports forward scheduling only. Schedule your project from a known start date to enable the system to calculate the optimal project completion date.

## Task dependencies and scheduling impact

Task dependencies establish temporal relationships between tasks. When you link tasks, the dependent task can't start until the relationship criteria are satisfied. Common task dependency types include:

-   Finish-to-start: The successor task can't start until the predecessor task completes.
-   Start-to-start: The successor task can't start until the predecessor task begins.
-   Finish-to-finish: The successor task can't finish until the predecessor task completes.
-   Start-to-finish: The successor task can't finish until the predecessor task begins.

The chain of dependent tasks determines the critical path and the project finish date. Dependencies interact with constraints: when a constraint date conflicts with a predecessor task's finish date, the constraint takes precedence, potentially delaying dependent tasks.

## Supported task constraints

Task constraints control task start and finish timing within the forward scheduling model. Constraints provide specific control while maintaining scheduling flexibility. Three constraint categories are available:

-   **Flexible constraints**

    Allow the scheduling engine to adjust task timing based on dependencies and other constraints without restricting tasks to specific dates.

-   **Semi-flexible constraints**

    Restrict tasks to a date range, accommodating external factors while retaining scheduling flexibility. These constraints require an associated date.

-   **Inflexible constraints**

    Anchor tasks to specific dates, overriding dependencies. These constraints require an associated date and are useful for external dependencies and contractual milestones.


|Category|Constraint type|Scheduling behavior|
|--------|---------------|-------------------|
|Flexible|As Soon As Possible \(ASAP\)|Schedules the task to begin at the earliest possible date. This is the default constraint for all tasks in forward scheduling. The scheduling engine has maximum flexibility to adjust the task as other tasks change. Do not enter a start or finish date with this constraint.|
|Semi-flexible|Start No Earlier Than \(SNET\)|Schedules the task to start on or after a specified date. Use this constraint to prevent tasks from starting before a required date, such as when equipment becomes available or resources become assigned.|
|Semi-flexible|Finish No Earlier Than \(FNET\)|Schedules the task to finish on or after a specified date. Use this constraint to ensure task completion occurs after a specific milestone or approval, such as after a client review.|
|Semi-flexible|Start No Later Than \(SNLT\)|Schedules the task to start on or before a specified date. Use this constraint to ensure a task begins by a deadline, such as before resource availability expires.|
|Inflexible|Must Start On \(MSO\)|Schedules the task to start on a specific date. Use this constraint when you need to anchor a task to an exact date for external dependencies or contractual milestones. This constraint overrides task dependencies.|
|Inflexible|Must Finish On \(MFO\)|Schedules the task to finish on a specific date. Use this constraint when task completion is tied to an exact date, such as a contract deadline or regulatory requirement. This constraint overrides task dependencies.|

## Constraint and dependency interaction

When you apply a constraint to a task that has dependencies, the scheduling engine evaluates both elements. If a constraint date conflicts with a predecessor task's finish date, the constraint takes precedence, and the task schedules according to the constraint date. This may delay successor tasks or create negative slack in the schedule.

Consider a task with a Start No Earlier Than \(SNET\) constraint for June 15 and a finish-to-start dependency to another task:

-   If the predecessor task finishes before June 15, the dependent task can't start until June 15.
-   If the predecessor task finishes after June 15, the dependent task starts when the predecessor finishes.

Semi-flexible constraints allow flexibility while enforcing boundaries. Inflexible constraints anchor tasks regardless of dependency timing.

## Task constraint best practices

Optimize schedule flexibility and accuracy by following these guidelines:

-   Use ASAP by default: The ASAP constraint provides the scheduling engine maximum flexibility. Apply other constraints only when necessary to enforce specific business requirements.
-   Apply semi-flexible constraints for date boundaries: SNET, FNET, and SNLT constraints allow flexibility within a date range. Use these constraints to enforce boundaries while maintaining scheduling flexibility.
-   Reserve inflexible constraints for external factors: MSO and MFO constraints anchor tasks to specific dates. Use these constraints only for external dependencies, contract milestones, regulatory deadlines, or equipment availability windows.
-   Limit overall constraint use: Excessive constraints reduce scheduling flexibility and can create negative slack. Apply constraints strategically to critical scheduling requirements only.
-   Document constraint rationale: When applying constraints beyond ASAP, document the business reason in task notes. This helps other project managers understand scheduling decisions and maintain consistency.
-   Monitor negative slack: Review schedule slack regularly. Negative slack indicates constraint dates conflict with dependencies. Adjust constraints or dependencies to resolve conflicts.

## Constraint application example

Consider a project with three tasks:

-   Task A: Design specifications \(5 days, starts project start date\)
-   Task B: Procurement \(10 days, finish-to-start dependency on Task A\)
-   Task C: Installation \(7 days, finish-to-start dependency on Task B\)

Without constraints, Task B starts on day 6 \(when Task A finishes\). However, if your vendor can't begin procurement until day 15 due to resource constraints, apply a Start No Earlier Than \(SNET\) constraint to Task B for day 15. Task B then schedules to start on day 15, even though Task A finishes on day 5. Task C adjusts to start after Task B completes on day 25.

## Related concepts

Other scheduling elements interact with constraints:

-   Task duration and task types: Determine how long a task takes to complete and how duration changes based on resource assignments.
-   Resource assignments and calendars: Affect actual task scheduling based on resource availability and working time definitions.
-   Task slack \(float\): Shows how much a task can delay without affecting the project finish date or dependent tasks.
-   Critical path: Identifies the sequence of tasks that determines the project finish date.
-   Project calendars: Define working and nonworking time for the entire project, affecting all task scheduling calculations.

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

[Types of external dependencies]()

[Project and portfolio funding]()

