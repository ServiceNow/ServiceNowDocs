---
title: Define a shift
description: Define shifts for your organization in the Industrial Connected Workforce by using the scheduling functionality. Configuring shifts is a prerequisite for scheduling standard tasks and for filtering tasks to see which shift they were created in or which shift they’re due.
locale: en-US
release: australia
product: Digital Factory Workspace
classification: digital-factory-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Prerequisites, Configure, Digital Factory Workspace, Industrial Connected Workforce]
---

# Define a shift

Define shifts for your organization in the Industrial Connected Workforce by using the scheduling functionality. Configuring shifts is a prerequisite for scheduling standard tasks and for filtering tasks to see which shift they were created in or which shift they’re due.

## Before you begin

Role required: sn\_icw.application\_admin or sn\_icw.admin

## About this task

Schedule records are saved in the Schedule \[cmn\_schedule\] table. Schedule entries are saved in the Schedule Entry \[cmn\_schedule\_span\] table. For more information about scheduling, see Define a schedule.

## Procedure

1.  Navigate to **All** &gt; **System Scheduler** &gt; **Schedules**.

2.  Select **New**.

3.  In the **Name** field, name the schedule as needed.

    For example, a name that relates to a functional location.

4.  In the **Type** field, enter `industrial_shift_config`.

    If you select **Floating** in the **Time zone** field, the time zone is relative to the process that accesses the item at the specified time.

    If you select a time zone, users in different time zones see the schedule with their own time zone applied.

5.  Select **Submit**.

6.  Create a child schedule.

    Create a child schedule for each shift and name them accordingly, for example, morning, afternoon and evening.

    1.  Open the schedule record and then select the **Child Schedules** tab.

    2.  Select **New**.

    3.  For the field **Type**, enter `industrial_shift_entry`.

    4.  Select **Submit**.

    5.  Open the child schedule and scroll down to the **Schedule Entries** tab.

        The **Schedule Entries** related list contains the definitions of the time periods that you want to include in or exclude from the schedule.

    6.  Create a schedule entry to define the schedule span or repeating pattern for that shift.

    7.  Select **New** and define the shift pattern, such as start and end time and the repeating pattern, such as daily.

        -   The fields **Type** and **Show as** aren’t important for this configuration and can be ignored.
        -   Set the end time to one second before the start of the next shift to avoid overlap.
        -   The value between **When** and **To** is smaller than 24 hours.
        -   Always select a value for the **Repeats** field. If no value is selected, the shift occurs only once.
        ![Morning shift configured](../../icw-industrial-connected-workforce/image/morning-shift.png)

    8.  Select **Submit**.

        ![Afternoon shift configured](../../icw-industrial-connected-workforce/image/afternoon-shift.png)

7.  Link functional locations to a schedule:

    1.  Navigate to **All** &gt; **Equipment Model Entities**.

    2.  Select the functional location that you want to link to the schedule.

    3.  For the column **Schedule**, enter the parent schedule that you created in the initial steps.

    4.  Select and hold \(or right-click\) and select **Save**.


## Result

The shift and its business calendar entries have been created successfully and are displayed in the **sn\_icw\_industrial\_calendar.list** list. Task lists in the Digital Factory Workspace and Industrial Connected Workforce Mobile Experience can be filtered by shifts. In the date/time fields, such as **Due date**, you can use the following date/time dynamic filter options:

-   My current shift
-   My next shift
-   My previous shift

**Parent Topic:**[Setting up prerequisites for Digital Factory Workspace](../concept/setting-up-prerequisites-digital-factory-workspace.md)

