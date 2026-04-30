---
title: Change the fields that display calendar event icons
description: Change the fields that determine whether icons are displayed on calendar events to something you find more useful, like a priority indication.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Dispatcher Workspace settings, Dispatcher Workspace, CSM/FSM Configurable Workspace, Configure, Field Service Management]
---

# Change the fields that display calendar event icons

Change the fields that determine whether icons are displayed on calendar events to something you find more useful, like a priority indication.

## Before you begin

Role required: wm\_admin

## About this task

The icon in the top left indicates work type. The first icon on the bottom right indicates if the task is a crew task, and the second icon on the bottom right indicates if the task is locked. See [Calendar event icons in Dispatcher Workspace](../reference/calendar-event-icons.md) for the full list of calendar event icons.

For information on changing the icon graphic for calendar events, see [Change the graphic for calendar event icons](customize-icons-dispatcher-wrkspc.md).

**Warning:** You must be familiar with the JSON code format to perform this procedure.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Dispatcher Workspace Configuration** &gt; **Calendar Event Body Iconography**.

2.  Select **here** if you see a message about editing the Global application.

3.  In the **Value** field, find and edit the `type` or `field` value for the calendar event icon that you want to change.

    The icon positions and default field values are:

    -   topIcon - The icon at the top left indicates the work type \(work\_type\)
    -   bottomFirstIcon - The first icon at the bottom right indicates whether a task is a crew task \(crew\)
    -   bottomSecondIcon - The second icon at the bottom right indicates whether a task is locked \(lock\)
    For information on changing the icon graphic, see [Change the graphic for calendar event icons](customize-icons-dispatcher-wrkspc.md).

4.  Select **Update**.


## Result

The selected field values will now trigger the icons that display in calendar events.

