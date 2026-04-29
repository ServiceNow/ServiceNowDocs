---
title: Time zones in Dispatcher Workspace
description: There are a few ways that dispatchers can choose to control the time zones that show on the calendar in Dispatcher Workspace.
locale: en-US
release: australia
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Using Dispatcher Workspace, Assigning tasks from Dispatcher Workspace, Scheduling and dispatching, Use, Field Service Management]
---

# Time zones in Dispatcher Workspace

There are a few ways that dispatchers can choose to control the time zones that show on the calendar in Dispatcher Workspace.

## Using a single time zone on the calendar

Dispatchers can use the calendar in Dispatcher Workspace with a single time zone. Using a single time zone can be helpful if you and all of your agents are in one place. With this configuration there’s a single time zone shown on the calendar, and no time zones are available in the time zone drop-down menu.

To use a single time zone you must have **Show multiple time zone rows** inactive, and no entries in the **Select time zones for calendar** field.

![single time zone in dispatcher workspace](../image/one-time-zone.png)

## Using a single time zone with multiple selection options

Dispatcher Workspace can also be configured to show a single time zone on the calendar, with the ability to switch between time zones. Single time zones with multiple options can be helpful for dispatchers who manage agents across different time zones. For example, if you’re a dispatcher in California, but manage agents across the United States. Dispatchers can quickly switch between time zones and minimize the mental calculations needed to understand what the agent’s schedule is like in their local time.

To use single time zone with multiple selections, you must have **Show multiple time zone rows** inactive with multiple time zones entries in the **Select time zones for calendar** field.

For more information, see [Change the time zone in Dispatcher Workspace](../task/change-timezone-calendar.md).

![change single selection in dispatcher workspace](../image/select-one-time-zone.png)

## Using multiple time zones on the calendar

Dispatchers can choose to show multiple time zones on the calendar, with several time zone options to select from. Multiple time zones can be helpful if you regularly manage agents across multiple time zones and want to see the time zones where your agents are located. You can configure up to three time zones to display on the calendar at once, and you can also switch between these time zones as needed.

To use multiple time zones you must have **Show multiple time zone rows** enabled, and multiple entries in the **Select time zones for calendar** field.

For more information, see [Show multiple time zones in Dispatcher Workspace](../task/use-stacked-time-zones.md).

![stacked time zones in dispatcher workspace](../image/stacked-time-zone.png)

## Resource time indicators

Resource time indicators show all the technicians' schedules lined up and not offset based on the time zone they're in. The different time zones that technicians are in are indicated by a segmented time indicator.

Dispatchers can turn on Resource time indicators in the settings in Dispatcher Workspace. For more information, see [Enable Dispatcher Workspace settings](../task/dispatcher-wrkspc-settings.md).

![equalized time zones in dispatcher workspace](../image/time-zone-agnostic.png)

When the resource time indicators are turned on:

-   A new line on the calendar in Dispatcher Workspace shows for each user in a different time zone. If a technician is in a different time zone, but with the same offset, then the time indicator in Dispatcher Workspace shows two lines with a dot denoting the time zone difference. For example, if two technicians are shown on the calendar in Dispatcher Workspace, with one user located in US Mountain Time, and the other user in Canadian Mountain Time, then two lines show with a dot denoting the time zone difference.
-   When you drag and drop a work order task to the calendar, a green box shows indicating the time zone for the task and the dispatcher's local time zone.
-   Assignment assistance shows the time zone that the task is scheduled in.
-   The technician schedules are shown on the calendar, the popover, and the contextual side panel in the technician’s time zone.
-   If there’s a task with multiple technicians assigned to it, like a crew task, and the members are in different time zones, then the task shows on the calendar in the task’s time zone.
-   Tasks show on the calendar in Dispatcher Workspace in the task’s time zone. For example, if a technician in California has WOT123 scheduled for 1-2 Pacific Time assigned to them, and another task WOT456 scheduled for 1-2 Mountain Time also assigned to them, then the tasks show as overlapped on the calendar but they’re sequential. Alternatively, if a technician located in California has WOT123 scheduled for 8-9 Pacific Time assigned to them, and another task WOT456 scheduled for 10-11 Mountain Time also assigned to them, then the tasks show as one after another but there’s an hour gap between the two tasks.
-   New events use the technician's time zone if there's one technician or if multiple technicians are added from the same zone. If you add more than one technician to the event and they’re in different time zones, then the dispatcher’s time zone is used. If you add a location to the event, then the location’s time zone takes priority and is used.

