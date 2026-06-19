---
title: Manage shifts from the Timeline view
description: Use the Timeline view of an On-Call schedule to update or manage shifts based on the geographical location of roster members.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/on-call-scheduling/customize-timeline-view-oncall.html
release: australia
product: On-Call Scheduling
classification: on-call-scheduling
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure or update an On-Call schedule, Managing schedules and shifts, On-Call Scheduling, IT Service Management]
---

# Manage shifts from the Timeline view

Use the Timeline view of an On-Call schedule to update or manage shifts based on the geographical location of roster members.

## Before you begin

Role required: rota\_admin, itil, rota\_manager, or admin

## About this task

-   For information on updating a shift, see [Update shift details from the On-Call calendar](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/on-call-scheduling/update-shift-from-calendar-oncall.md).
-   For information on managing a shift, see [Configure or update an On-Call shift](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/on-call-scheduling/config-update-shift-oncall.md).

## Procedure

1.  Navigate to **All** &gt; **On-Call Scheduling** &gt; **On-Call Calendars**.

2.  Click the Timeline view icon \(\[Omitted image "view-calendar-timeline-icon.png"\] Alt text: Timeline view con\).

    **Important:** The Calendar view on this page displays all shifts for a user group for a specified time interval. To open the Calendar view, click the Calendar View icon \(\[Omitted image "view-calendar-calendar-icon.png"\] Alt text: Calendar View icon\). See [Manage shifts from the Calendar view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/on-call-scheduling/customize-calendar-view-oncall.md).

3.  Perform any of the following operations to organize the view for your needs:

    -   Specify the time period that appears: View events for the current day, week, or month: In the title bar, click **Day**, **Week**, or **Month**.

        **Note:** You cannot view the calendar for a month in the Timeline view.

    -   Navigate to the previous or the next occurrence of the time period: In the title bar, click the left or the right arrow next to **Today** \(\[Omitted image "view-calendar-today.png"\] Alt text: Next and previous date icon\).
    -   View the event of any specific day, week, or month: In the title bar, click the Calendar icon \(\[Omitted image "view-calendar-icon.png"\] Alt text: Calendar icon\) and specify the date.
    -   View the list of navigation shortcuts: In the title bar, click the keyboard shortcuts icon \[Omitted image "view-calendar-keyboard-icon.png"\] Alt text: keyboard icon.
4.  Configure the view: Click the Filter icon \(\[Omitted image "filters-icon.png"\] Alt text: Filter icon\).

    -   To show working hours for a time zone, enable **Time zone**.
    -   To view roster assignments within a time zone, click the **Primary**, **Secondary**, or **Tertiary** check box as needed.
    -   To show gaps: In the **Review options** section, enable **Show gaps**. An info icon indicates a shift with gaps. Click the icon to view the gaps. Gaps occur when no one is on-call when support coverage is required. Possible reasons:

        -   Time off without coverage.
        -   User has been moved out of the group.
        -   User is marked as inactive.
        For information on resolving gaps and conflicts, see [Resolve gaps, conflicts, and time-off requests in a shift](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/on-call-scheduling/resolv-gap-conflct-timeoff-oncall.md).

    -   &gt;To show conflicts: In the **Review options** &gt; **Show conflicts**.

        For example, a conflict occurs when a user is assigned as both primary and secondary point of contact for a shift. An info icon indicates a shift with conflicts. Click the icon to view the conflicts.

        For information on resolving gaps and conflicts, see [Resolve gaps, conflicts, and time-off requests in a shift](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/on-call-scheduling/resolv-gap-conflct-timeoff-oncall.md).

5.  To save the view settings, click the Bookmark this filter icon \(\[Omitted image "view-favourite-icon.png"\] Alt text: Bookmark this filter icon\).


**Parent Topic:**[Configure or update an On-Call schedule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/on-call-scheduling/create-update-schedule-oncall.md)

