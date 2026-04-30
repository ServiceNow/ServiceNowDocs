---
title: My Calendar
description: Any user with the resource\_user role can open My Calendar to view, add, and modify their planned work, actual work, operational work, administrative tasks, and personal activities.
locale: en-US
release: zurich
product: Resource Management
classification: resource-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Resource Management classic, Project Portfolio Management, Strategic Portfolio Management]
---

# My Calendar

Any user with the resource\_user role can open My Calendar to view, add, and modify their planned work, actual work, operational work, administrative tasks, and personal activities.

After a user adds an event to the calendar, the time blocks for that event appear as red, indicating busy, on the resource console and the resource availability dashboard.

Resource managers view users' calendars to determine who has open time to complete tasks, and can add tasks to any resource's personal calendar. For every event that is created on a user's calendar, a record is created in the User Calendar Event \[user\_calendar\_event\] table. Resource events are chunks of busy time for the user. Users and resource managers can sometimes modify these records. See [Resource event modifications](c_ModifyAResourceEvent.md).

The calendar uses time zones. Time is displayed to users in their local time zone according to user preferences. See [Time zones in resource plans](c_TimeZonesInResourcePlans.md).

Each resource event is represented with a specific color. PPS admin can change these colors. See [Change the resource event color](../task/t_ChangeTheResourceEventColor.md)

**Note:** Although a user can add tasks, such as incidents, to their calendar, the user isn’t added to the task's **Assigned to** field.

-   **[Add events to your calendar](../task/t_AddEventsToYourCalendar.md)**  
Add tasks, events, and appointments to your calendar.
-   **[Create repeatable events](../task/t_CreateRepeatableEvents.md)**  
Events can be set to repeat on a regular schedule, such as every day, week, or month.
-   **[View a user calendar](../task/t_ViewAUserCalendar.md)**  
View the calendar of a user to check availability.
-   **[Add events to a user calendar](../task/t_AddEventsToAUserCalendar.md)**  
Resource managers can add events to user calendars.
-   **[Delete events](../task/t_DeleteEvents.md)**  
You can delete events you created at any time.

**Parent Topic:**[Resource Management classic](c_ResourceManagement.md)

