---
title: Create or enable access to event types to add them to the team calendar
description: Create multiple events from the same category and add them to the calendar in ITSM Manager Workspace. Enable agents or managers to create specific event types.
locale: en-US
release: zurich
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Setting up, Scheduling, Workforce Optimization for ITSM, IT Service Management]
---

# Create or enable access to event types to add them to the team calendar

Create multiple events from the same category and add them to the calendar in ITSM Manager Workspace. Enable agents or managers to create specific event types.

## Before you begin

Role required: sn\_shift\_planning.admin

## Procedure

1.  Create an event type.

    1.  Navigate to **All** &gt; **Workforce Optimization for ITSM** &gt; **Scheduling** &gt; **Event Types**.

    2.  Click **New**.

    3.  On the form, fill in the fields.

<table id="table_kb2_yfx_3nb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the event type.

</td></tr><tr><td>

Priority Order

</td><td>

Priority of the event type that you want to exclude from the coverage. The higher the number means the higher the priority. For example, let's say you are attending a work event for four hours in a day. You have marked that time window as both a time off and as a meeting event type. If time off has a higher order of priority, then the application excludes that event type from coverage.

</td></tr><tr><td>

Color

</td><td>

Color that identifies this type of event in the team calendar.

</td></tr><tr><td>

Use custom colors

</td><td>

Preferred color that you can select to display the background and border of the event type in the team calendar.

</td></tr><tr><td>

Active

</td><td>

Option that when enabled, displays the event type on the calendar.

</td></tr><tr><td>

Category

</td><td>

Type of event, for example, custom, meeting, break, or time off.

</td></tr></tbody>
</table>    4.  Click **Submit**.

2.  Enable agents or managers to create specific event types.

    For information on adding or removing access to user for event types, see [Include or exclude access for event types.](../concept/understanding-user-criteria-event-types-wfo-itsm.md)


## What to do next

[Add events to the team calendar](add-events-team-calendar-wfo-itsm.md)

**Parent Topic:**[Setting up Scheduling in Workforce Optimization for ITSM](../concept/setup-scheduling-configurable-workforce-optimization-itsm.md)

