---
title: Add events to your calendar
description: Add tasks, events, and appointments to your calendar.
locale: en-US
release: zurich
product: Resource Management
classification: resource-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [My Calendar, Resource Management classic, Project Portfolio Management, Strategic Portfolio Management]
---

# Add events to your calendar

Add tasks, events, and appointments to your calendar.

## Before you begin

Role required: pps\_resource or resource\_manager

## About this task

To create an event that repeats daily, weekly, or monthly, see [Create repeatable events](t_CreateRepeatableEvents.md).

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **My Calendar**.

    The calendar appears in the week view by default, highlighting today's schedule. The user's off-duty schedule in gray.

2.  Change the view as necessary.

    -   Select Day, Week, or Month.
    -   Use the forward or back arrows to navigate between days, weeks, and months.
    -   Select a date using the calendar icon ![Date picker](../image/CalendarPicker.png).
    -   Select **Today** to reset your calendar view to show today's calendar.
3.  Open the Add Event form by double-clicking an empty cell on the calendar.

4.  On the New event form, fill the fields.

    For a description of the field names, see [New event form](../reference/new-event-form.md).

5.  Select **Submit**.


## Result

-   When you add a calender event, the resource aggregate daily, weekly, and monthly tables are updated. The resource aggregate daily table isn’t enabled by default. To generate daily aggregates and store them in this table, create the **com.snc.resource\_management.generate\_daily\_aggregates** property and set its value to true.
-   All the non-project events created for you from the calender appear as Operational Work for you in [Resource Finder](create-resource-plan-with-finder.md).

**Parent Topic:**[My Calendar](../concept/c_MyCalendar.md)

**Related topics**  


[Create repeatable events](t_CreateRepeatableEvents.md)

[View a user calendar](t_ViewAUserCalendar.md)

[Add events to a user calendar](t_AddEventsToAUserCalendar.md)

[Delete events](t_DeleteEvents.md)

