---
title: Viewing agents and tasks in the Dispatcher Workspace map
description: You can use the Dispatcher Workspace map to track, manage, and analyze agent assignments and work order tasks in specific locations. The map is found in the Dispatcher Dashboard and Dispatcher Workspace.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Working in Dispatcher Workspace, Scheduling and dispatching work order tasks to agents, Using Field Service Management, Field Service Management]
---

# Viewing agents and tasks in the Dispatcher Workspace map

You can use the Dispatcher Workspace map to track, manage, and analyze agent assignments and work order tasks in specific locations. The map is found in the Dispatcher Dashboard and Dispatcher Workspace.

You can manage tasks and routing from the map, filter the view, and determine which agents are on time or behind schedule. The Dispatcher Workspace map uses geolocation data to display tasks and agents in field locations. When you select a map pin in the Dispatcher Workspace map, the record for that task or agent shows in the contextual side panel. The map pins serve as quick access points.

-   The Dispatcher Workspace map view centers based on the map pin clusters. Map pin clusters group the map pins near one another into a single cluster. You can zoom in, zoom out, and view the map in full screen. Select the map cluster to zoom the map to show the map markers of work order tasks and agents.
-   Map pins in the Dispatcher Workspace map mark the location of tasks and agents in the dispatcher's area. The icons serve as access points to corresponding records. Unique task pins are displayed based on the state of the work order task.
-   Map pins corresponding to a single task or agent show in the contextual side panel with scheduling information.
-   The map shows individual markers, not every task on the map. This is important because multiple tasks or agents might be at a single location, but only indicated by a single map marker.
-   In order to optimize performance, the map only renders current tasks that are loaded on the calendar, not every single task that’s available. You can change this setting so that more tasks are loaded on the page, which will cause more markers to show on the map. For more information, see [Determine the tasks to appear in the task panel](../task/configuring-filters-for-taskpanel.md).
-   If you want to change each cluster to show the total count of tasks and agents, see the sn\_fsm\_disp\_wrkspc.dispatcher\_workspace.cluster\_label property here: [Configure the appearance of the map in Dispatcher Workspace](../task/configuring-map-settings.md).

-   If an agent has a closed task today or a work in progress task, then the map pin shows the agent at the task location of whichever is latest: the task work end time for a closed task, or task work start time for a work in progress task. Otherwise, the map pin will show the agent's location in user record \(the default location\).

**Note:** The map can load at most 2000 records from the task panel and the scheduler. When more than 2000 records, the map displays a message to refine the query to ensure that all records are displayed on the map.

![Map with tasks located in San Diego.](../image/agent-location-map.png)

**Related topics**  


[Execute a task from the agent map](../../planning-and-policy/task/t_ExecuteATaskFromTheAgentMap.md)

