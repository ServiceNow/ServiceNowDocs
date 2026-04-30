---
title: Configuring collapsed mode in Dispatcher Workspace
description: Collapsing assignment groups or territories allows Dispatcher Workspace to load faster. Administrators can disable the property to see all assignment groups or territories at once, but at the cost of higher load times.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Dispatcher Workspace, CSM/FSM Configurable Workspace, Configure, Field Service Management]
---

# Configuring collapsed mode in Dispatcher Workspace

Collapsing assignment groups or territories allows Dispatcher Workspace to load faster. Administrators can disable the property to see all assignment groups or territories at once, but at the cost of higher load times.

## Collapsed mode

Starting with the Xanadu release, assignment groups and territories are collapsed by default. If this is the behavior that you want dispatchers to have, there is nothing to do. The first assignment group or territory on the calendar is expanded, but the assignment groups or territories below it are collapsed.

![Dispatcher workspace with collapse mode on](../image/collapsed-mode.png)

## Non-collapsed mode

You can disable collapsed mode. This loads X number of agents that are part of your default assignment groups or territories. Where X equals the calendar page size, which controlled by this system property: `sn_fsm_disp_wrkspc.dispatcher_workspace.calendar_resources_page_size`. Dispatchers must then select Load more at the bottom of the calendar to see more agents and assignment groups or territories. To use non-collapsed mode and to see assignment groups and territories expanded, you must set the property `sn_fsm_disp_wrkspc.calendarCollapsedBehavior` to false.

![Dispatcher workspace with collapse mode off](../image/non-collapsed.png)

