---
title: Configuring Workforce
description: Workforce provides tools for managing schedules, events, and tasks in one workspace.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [CSM/FSM Configurable Workspace, Configure, Field Service Management]
---

# Configuring Workforce

Workforce provides tools for managing schedules, events, and tasks in one workspace.

Workforce is part of the CSM/FSM Configurable Workspace. Use Workforce to:

-   View agent schedules and team calendars.
-   Create personal events.
-   Track tasks and agent movements on a map.

These tools help you manage schedules and geographical data from one location.

Workforce supports configuration of the following options to improve scheduling and visibility:

-   Customize the team calendar to control which event types appear.
-   Modify the Workforce configuration to enable visibility for both group and territory views.
-   Increase team calendar visibility so teams can better coordinate meetings, events, and tasks.
-   Assign managers to territories and configure roles for access.
-   Add additional managers when Workforce Optimization for Field Service is active.

Territory view in Workforce depends on [Configuring Field Service Territory Planning](configuring-territory-planning-fsm.md). Each territory must have an assigned manager, and managers need the wm\_manager role to view schedules. For details on assigning territories to managers, see [Managing territories and agents from Territory Planning console](using-territory-planning-console.md).

When Workforce Optimization for Field Service is active, you can assign additional managers to user groups. This enables more team leaders to access Workforce and manage scheduling effectively. For details on adding managers, see [Assign additional managers to user groups when Workforce Optimization for Field Service is installed](../task/assign-additional-managers-to-user-groups.md).

Workforce supports a high volume of agents and tasks by default. If your workforce management requires expanded capacity, you can contact support or submit a change control request to adjust the configuration.

## Configuration overview

The steps for setting up Workforce are:

-   [Configure event types to appear on the Team calendar in Workforce](configure-event-types-to-appear-on-the-team-calendar.md)

    Select which event types appear on the team calendar.

-   [Set your Workforce system properties](workforce-system-properties.md)

    Enable system properties for group and territory views.

-   [Configure team calendar visibility for group members](../task/configure-team-cal-visibility-grp-members.md)

    Make team schedules accessible across groups.

-   [Configure territory view to allow users to see other members' schedules](../task/enable-territory-view.md)

    Enable toggling between assignment groups and territories.


