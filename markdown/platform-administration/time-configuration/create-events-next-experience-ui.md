---
title: Create schedule entries in the Schedule calendar
description: Add events such as meeting, time-off, or appointment to display them in the schedule calendar.
locale: en-US
release: zurich
product: Time Configuration
classification: time-configuration
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use, Time configuration, Configure core features, Administer]
---

# Create schedule entries in the Schedule calendar

Add events such as meeting, time-off, or appointment to display them in the schedule calendar.

## Before you begin

Role required: schedule\_admin, itil\_admin, admin

## About this task

You can add and analyze the events using a calendar view. You can also do this in a time line view for a given day, week, or month, which is defined as four weeks in the time line view.

A calendar view displays events for a specified time period. A time line view displays all events for the selected time line in the calendar.

## Procedure

1.  Navigate to **All** &gt; **System Scheduler** &gt; **Schedules** &gt; **Schedules**.

2.  Select a schedule.

3.  Select **Show Schedule** related link.

    Using the Next Experience user interface, you can view the schedules in the schedule calendar for all schedule types except the roster type. The schedules of roster type display in the [on-call schedule.](https://www.servicenow.com/docs/access?context=c_OnCallScheduling&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)

4.  Create a schedule entry.

    1.  Do any of the following to open the **Add event** form:

        -   Select a day in the calendar.
        -   Drag the span of days for which you want to create the event.
    2.  In the **Name** field, enter a name for the event.

    3.  From the **Type** menu, select the type of event.

    4.  From the **Show as** field, select the status you want to display for this event.

    5.  In the **Start** field, select the calendar icon and select the start date for the event.

    6.  In the **End** field, select the calendar icon and select the end date for the event.

        If the event is for the entire day, select **All Day**.

    7.  From the **Repeats** menu, select how often you want this event repeated.

    8.  Select **Save**.

    -   The schedule entry displays in the calendar for that time period and is based on the user's time zone.
    -   You can reschedule an event by dragging and moving it to another date. You can also update that particular occurrence or all occurrences for an event.
    -   You can click on an event to view the details in a pop-up display and edit or delete the event by selecting the respective icon.
        -   When you add or edit an event, the time zone in the event displays the **Timezone** field value from the schedule record.

            **Note:** If the **Timezone** field value is **Floating**, then the time zone isn’t displayed.

        -   When you add or edit an event, the calendar uses the start and end dates from the time zone of the schedule.

            **Note:** If the **Timezone** field value is **Floating**, then the calendar uses the start and end dates from the time zone of the logged-in user.


**Parent Topic:**[Using time configuration](../using-time-configuration.md)

