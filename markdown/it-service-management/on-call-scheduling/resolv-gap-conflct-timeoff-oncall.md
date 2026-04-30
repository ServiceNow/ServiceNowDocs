---
title: Resolve gaps, conflicts, and time-off requests in a shift
description: Review and resolve gaps and conflicts. Find a replacement on-call member for time-off requests to ensure proper support coverage.
locale: en-US
release: xanadu
product: On-Call Scheduling
classification: on-call-scheduling
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure or update an On-Call shift, Manage schedules and shifts, On-Call Scheduling, IT Service Management]
---

# Resolve gaps, conflicts, and time-off requests in a shift

Review and resolve gaps and conflicts. Find a replacement on-call member for time-off requests to ensure proper support coverage.

## Before you begin

Role required: rota\_manager

## About this task

Possible reasons for gaps are:

-   Time off without coverage
-   User has been moved out of the group
-   User is marked as inactive

A conflict is possible if a user is assigned as both the primary and secondary point of contact for a shift.

## Procedure

1.  Navigate to **All** &gt; **On-Call Scheduling** &gt; **On-Call Schedules**.

2.  Click a shift card.

    **Note:** If you are a shift manager or roster member, the schedule view opens. In all other cases, you are redirected to the calendar view. For more information on on-call scheduling calendars, see [Manage shifts from the Calendar view](customize-calendar-view-oncall.md).

    -   The On-Call Schedules page open. For more information, see [Updating an On-Call schedule](update-schedule-oncall.md)
    -   The pending actions for the current shift appear in the **Pending Actions** section.
    .

3.  To resolve gaps or conflicts, perform the following steps.

    1.  Click **Review** in the **Pending Actions** section.

        The calendar view appears, and gaps or conflicts are highlighted.

    2.  Click the Information icon \(![Information icon](../image/icon-information.png)\) to view gaps.

    3.  Right-click the shift and select **Edit shift** from the **Actions** list.

    4.  Scroll down to the **Rosters** list and select the roster where the user is unavailable.

    5.  In the **Members** related list, add a **To** value for the unavailable user.

    6.  Add a new member with a **From** value to close the gap.

4.  To resolve a time-off request, perform the following steps.

    1.  Click **Review** in the **Pending Actions** section.

        The calendar view appears, and time-off requests are highlighted.

    2.  Right-click the shift and select **Manage shift** from the **Actions** list.

        The Manage Shift dialog box appears.

    3.  Approve the time-off requests.


**Parent Topic:**[Configure or update an On-Call shift](config-update-shift-oncall.md)

