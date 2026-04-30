---
title: Setting up dynamic scheduling in Dispatcher Workspace
description: Dynamic scheduling enables you as a dispatcher to efficiently assign, unassign, or reassign work order tasks.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Dispatcher Workspace, Setting up CSM/FSM Configurable Workspace, Configuring Field Service Management, Field Service Management]
---

# Setting up dynamic scheduling in Dispatcher Workspace

Dynamic scheduling enables you as a dispatcher to efficiently assign, unassign, or reassign work order tasks.

The Dispatcher Workspace integration with dynamic scheduling enables you to automatically select an agent and assign work order tasks. When you attempt to assign the new task, dynamic scheduling unassigns or reassigns the existing tasks and assigns the new task to an agent.

**Note:** Tasks that are already set to Work in Progress can’t be unassigned. Only tasks that are scheduled but not started can be reassigned or unassigned.

## Task priorities

If you assign a higher priority task when a lower priority task is already assigned, dynamic scheduling assigns the higher priority task and attempts to reassign the lower priority task. If you drag a lower priority task over a higher priority task, a warning message appears and you must acknowledge it to continue.

## Enabling double-booking

If double-booking is enabled, you can manually double-book an agent for more than one work order task with overlapping time. When you drag and drop a task on top of an already assigned task, the new tasks overlaps with the already assigned task and the estimated travel time is updated.

-   When dynamic scheduling and double-booking are enabled, dragging a task on an already assigned task overlaps the assigned task and update its estimated travel time.
-   If double-booking isn’t enabled and dynamic scheduling is enabled, dragging a task onto an already assigned task displays a dynamic scheduling pop-up window so you can reschedule the task.
-   When double-booking and dynamic scheduling are disabled, dragging a task on an already assigned task displays an error message stating that the agent isn’t available at that time.

**Note:**

System administrators enable double-booking by setting the **work.management.allow.doublebooking.dynamicscheduling**.

**Related topics**  


[Dynamic scheduling](dynamic-scheduling.md)

