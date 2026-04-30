---
title: Show and optimize the agent task route in Dispatcher Workspace
description: View agent records, agent schedules, and view or optimize the scheduled task route of an agent for that day. You can help them manage their schedules and tasks more efficiently.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Working in Dispatcher Workspace, Scheduling and dispatching work order tasks to agents, Using Field Service Management, Field Service Management]
---

# Show and optimize the agent task route in Dispatcher Workspace

View agent records, agent schedules, and view or optimize the scheduled task route of an agent for that day. You can help them manage their schedules and tasks more efficiently.

## Before you begin

You must enable the sn\_fsm\_disp\_wrkspc.sn\_fsm.dispatch\_ws\_map.route\_enabled system property to display the Route icon in your dispatcher workspace.

You must select the work.management.optimization.conflict\_handling system property to avoid conflicts due to overflow tasks when optimizing the route. For more information, see [Properties installed with Field Service Management](../../planning-and-policy/reference/r_PropInstallWFieldServMgmnt.md).

Role required: wm\_dispatcher and wm\_manager

## About this task

In the Dispatcher Workspace, you can view the routes of all the tasks for a single or multiple agents for that day by using the route feature.

You can also optimize the task route for an agent to reorder the tasks as efficiently as possible. The route optimization feature considers the following attributes when reordering the agent tasks for the day:

-   Respects the agent personal time-off and reroutes the tasks before or after the break.
-   Doesn’t reorder the work order tasks that are scheduled lock.
-   Controls the scheduling of overflow tasks to avoid conflicts by selecting any one of the behavioral methods, such as stop route optimization, unassign overflow tasks, or adjust the overflow task by assigning it toward the end of the agent's schedule.
-   Considers the agent's start of the day and end of the day locations from the **Agent Schedule Attribute Plans** table for the given day if the Territory Planning plugin is activated. For more information, see [Activate Field Service Territory Planning](Activate-fsm-territory-planning.md).

## Procedure

1.  Navigate to **Field Service** &gt; **Dispatching** &gt; **Dispatcher Workspace**.

2.  Select **Dispatcher Workspace**.

3.  Search for a field service agent whose route you want to view.

    For more information, see [Search for appropriate field service agents](search-agents-tasks.md).

4.  Select **Map** or **Hybrid** from the **Schedule** drop-down list.

5.  Right-click on an agent pin and do one of the following:

    -   **Show/ hide route**- shows the route if the route is hidden, hides the route if the route is shown.
    -   **Optimize route**- opens the route optimization window. In the Optimize Route dialog box, select **Optimize**.
    If you chose **Optimize route**, then the following happens:

    The tasks are rearranged based on the route sequence.

    The Optimize Route dialog box displays the compared details of the new and old routes, such as map visualization, driving time, driving distance, and number of tasks. The new route is displayed in blue, while and the old route is grayed out.

    The overflow tasks are managed based on the selected route optimization behavior.

6.  To clear the agent route from the map, select **Hide all routes** in the map view.


