---
title: Bundling work order tasks
description: Logically grouping similar tasks into a bundle enables agents to track, start, and complete related tasks at once instead of individually with Field Service Task Bundling.
locale: en-US
release: zurich
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Assigning WOTs from Dispatcher Workspace, Scheduling and dispatching, Use, Field Service Management]
---

# Bundling work order tasks

Logically grouping similar tasks into a bundle enables agents to track, start, and complete related tasks at once instead of individually with Field Service Task Bundling.

An administrator must activate the Field Service Task Bundling plugin to bundle work order tasks. Work order task bundling is then added to the instance, and dispatchers are able to bundle work order tasks into logical groups.

For information about configuring the Field Service Task Bundling plugin, see [Configuring Task Bundling](configuring-fsm-task-bundling.md).

With work order task bundling, dispatchers can do the following:

-   Create a bundle.
-   Assign a bundle.
-   Add or remove tasks from a bundle.
-   Change a bundle.
-   Change the order of subtasks in an unassigned bundle.
-   Unbundle a bundle.

Work order task bundles are groups of work order tasks created manually by a dispatcher or automatically through dynamic bundling. Tasks bundles have the following attributes:

-   Inherit the state, assigned to, and schedule lock values from the parent bundle.
-   Inherit the actual travel and work start values from the actual travel and work start values of the earliest subtask.
-   Inherit the actual work end value from the end value of the last subtask.
-   Synchronize the estimated work duration with the estimated start and end times of bundled tasks.

## Creating bundles

Dispatchers create task bundles in Dispatcher Workspace. You can combine any number of work-order tasks into a bundle. You can group tasks by various criteria, such as a territory or an agent’s route.

When a bundle is created, a work order task and work order number are assigned. Bundles must be assigned to an agent after they’re created.

If any task in a bundle enables overtime, then the entire bundle is set to enable overtime.

Administrators can configure dynamic bundling policies and rules to bundle tasks automatically. For more information, see [Dynamic task bundling](dynamic-task-bundling.md).

## Assigning bundles

Dispatchers assign bundles in Dispatcher Workspace. Assigned and unassigned bundles follow the same rules as normal work order tasks. Subtasks in a bundle inherit the state, assigned to, and schedule lock values of their parent bundle.

Administrators can use dynamic scheduling or route optimization to assign bundles automatically.

## Accepting or rejecting tasks in the bundle

After a bundle is assigned, a field service agent can accept or reject the tasks in the bundle. Agents can reject tasks in a bundle after they’ve started to work on the bundle itself.

When an agent rejects a subtask in a bundle, the bundle is moved back to the Pending Dispatch state. If the bundle was schedule locked, the bundle is also unlocked to enable reassignment of the bundle.

For more information, see [Accept or reject a work order task](../../planning-and-policy/task/t_AcceptOrRejectAWorkOrderTask.md).

## Changing a bundle

You can change a bundle after you create it. If you want to change a subtask in a bundle, you must remove the subtask from the bundle before making changes. Dispatchers can only add tasks in the Pending Dispatch state to bundles. Tasks in the Accepted, Work in Progress, Cancelled, Closed Complete, or Closed Incomplete states can't be removed from bundles. When a task is removed from a bundle or an agent rejects a task that's in a bundle, then the task returns to the Pending Dispatch state. You can also unbundle a bundle.

## Subtasks in bundles

The location of the subtask in the first order position determines the bundle's location. If you want to update the location of a bundle, change the order location of the subtask in the first order position rather than the order location of the bundle.

If you want to change the work duration or scheduled start time for a subtask in a bundle, remove the subtask from the bundle and make the changes. Then add the subtask back to the bundle.

When a subtask is added to a bundle, validation occurs and pushes any work duration or schedule changes to the bundle. If you don't remove a subtask before changing it and adding it back, then the changes don't reflect in the bundle.

## Interactions with other features

Like work order tasks, work order task bundles can be optimized by route, scheduled dynamically, recommended through task recommendation, and altered in Dispatcher Workspace.

-   **Route Optimization**

    Dispatchers can use Route Optimization to optimize bundles on an agent's schedule using the same methods that are used for optimizing work order tasks.

    When you use Route Optimization, the bundles are considered their own tasks and are optimized as a whole alongside individual tasks. To enable optimization of subtasks within bundles, admins can toggle the \(**work.management.travel.calculation.bundle\_route\_optimization**\) property.

-   **Dynamic scheduling**

    Dynamic scheduling automatically schedules work order tasks and work order tasks bundles to agents. For more information, see [Dynamic scheduling](dynamic-scheduling.md).

    To ensure dynamic bundling runs before dynamic scheduling, admins can enable the **Dynamic Bundling before Dynamic Scheduling**\(**com.snc.dynamic.scheduling.bundle\_before\_scheduling**\) property.

-   **Intelligent Task Recommendation**

    Task recommendations only show for the task bundle, not for subtasks within a bundle.

    If a bundle is schedule locked, the bundle isn't recommended.

-   **Dispatcher Workspace**

    Drag bundles directly to agent schedules.

    Drag the sides of the bundle to extend or reduce bundle work duration.

    Apply agent sorting to bundles and work order tasks based on skills, distance, and parts.

    Lock and unlock bundles directly from the calendar view.

    Consolidate bundled tasks and view bundle location on the map view.

-   **Territory Planning**

    Task bundling considers the agent's start and end locations from the **Resource Schedule Attributes** table for the given day.


