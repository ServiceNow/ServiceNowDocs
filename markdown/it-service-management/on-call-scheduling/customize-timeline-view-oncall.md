---
title: Manage shifts from the Timeline view
description: Use the Timeline view of an On-Call schedule to update or manage shifts based on the geographical location of roster members.
locale: en-US
release: yokohama
product: On-Call Scheduling
classification: on-call-scheduling
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure or update an On-Call schedule, Manage schedules and shifts, On-Call Scheduling, IT Service Management]
---

# Manage shifts from the Timeline view

Use the Timeline view of an On-Call schedule to update or manage shifts based on the geographical location of roster members.

## Before you begin

Role required: rota\_admin, itil, rota\_manager, or admin

## About this task

-   For information on updating a shift, see [Update shift details from the On-Call calendar](update-shift-from-calendar-oncall.md).
-   For information on managing a shift, see [Configure or update an On-Call shift](config-update-shift-oncall.md).

## Procedure

1.  Navigate to **All** &gt; **On-Call Scheduling** &gt; **On-Call Calendars**.

2.  Click the Timeline view icon \(![Timeline view con](../image/view-calendar-timeline-icon.png)\).

    **Important:** The Calendar view on this page displays all shifts for a user group for a specified time interval. To open the Calendar view, click the Calendar View icon \(![Calendar View icon](../image/view-calendar-calendar-icon.png)\). See [Manage shifts from the Calendar view](customize-calendar-view-oncall.md).

3.  Perform any of the following operations to organize the view for your needs:

    -   Specify the time period that appears: View events for the current day, week, or month: In the title bar, click **Day**, **Week**, or **Month**.

        **Note:** You cannot view the calendar for a month in the Timeline view.

    -   Navigate to the previous or the next occurrence of the time period: In the title bar, click the left or the right arrow next to **Today** \(![Next and previous date icon](../image/view-calendar-today.png)\).
    -   View the event of any specific day, week, or month: In the title bar, click the Calendar icon \(![Calendar icon](../../../product/change-management/image/view-calendar-icon.png)\) and specify the date.
    -   View the list of navigation shortcuts: In the title bar, click the keyboard shortcuts icon ![keyboard icon](../image/view-calendar-keyboard-icon.png).
4.  Configure the view: Click the Filter icon \(![Filter icon](../image/filters-icon.png)\).

    -   To show working hours for a time zone, enable **Time zone**.
    -   To view roster assignments within a time zone, click the **Primary**, **Secondary**, or **Tertiary** check box as needed.
    -   To show gaps: In the **Review options** section, enable **Show gaps**. An info icon indicates a shift with gaps. Click the icon to view the gaps. Gaps occur when no one is on-call when support coverage is required. Possible reasons:

        -   Time off without coverage.
        -   User has been moved out of the group.
        -   User is marked as inactive.
        For information on resolving gaps and conflicts, see [Resolve gaps, conflicts, and time-off requests in a shift](resolv-gap-conflct-timeoff-oncall.md).

    -   &gt;To show conflicts: In the **Review options** &gt; **Show conflicts**.

        For example, a conflict occurs when a user is assigned as both primary and secondary point of contact for a shift. An info icon indicates a shift with conflicts. Click the icon to view the conflicts.

        For information on resolving gaps and conflicts, see [Resolve gaps, conflicts, and time-off requests in a shift](resolv-gap-conflct-timeoff-oncall.md).

5.  To save the view settings, click the Bookmark this filter icon \(![Bookmark this filter icon](../image/view-favourite-icon.png)\).


**Parent Topic:**[Configure or update an On-Call schedule](create-update-schedule-oncall.md)

