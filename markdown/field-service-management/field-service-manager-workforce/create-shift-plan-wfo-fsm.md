---
title: Create a work shift plan in Workforce Optimization for Field Service
description: Schedule shifts for your team so that you can make sure that you are covering all work assignments and breaks. You can also specify the days of the week that you might need to override scheduled shifts.
locale: en-US
release: yokohama
product: Field Service Manager Workforce
classification: field-service-manager-workforce
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Scheduling in Workforce Optimization for Field Service, Workforce Optimization, Manage workforce, Using Field Service Management, Field Service Management]
---

# Create a work shift plan in Workforce Optimization for Field Service

Schedule shifts for your team so that you can make sure that you are covering all work assignments and breaks. You can also specify the days of the week that you might need to override scheduled shifts.

## Before you begin

Role required: sn\_shift\_planning.admin

## About this task

Create a work shift plan in Workforce Optimization for Field Service Management

In the **Shifts** tab, the shifts are grouped by active and inactive shifts. The contextual side panel displays the active and inactive shifts in the order displayed in the **Shifts** tab.

## Procedure

1.  Navigate to **All** &gt; **Workspaces** &gt; **Manager Workspace**.

2.  Click the Schedule icon \(![Schedule icon.](../../workforce-optimization-for-customer-service-configurable/image/schedule-new.png)\).

3.  Click the **Shifts** tab.

4.  In the contextual side panel, click the Show Shift Plans icon \(![Show Shifts Plans icon.](../image/show-schedule-new.png)\) to display the schedules.

5.  Click the Create Work shift plans or On-call shifts \(![Create Work shift plans or On-call shifts icon.](../image/add.png)\) icon.

6.  Click **Work shift**.

7.  In the **Name** field, enter a name for the shift.

8.  Set the time window for the shift.

    1.  In the **Time zone** field, select the time zone of the users that you want to allocate to the shift.

        **Note:** To add a shift for agents working in their local time zones, select the **Use agent time zone** option. The system uses the time zone that is specified in the agent's user record.

    2.  In the **Start time** field, enter the time of day when you want to start the shift.

    3.  In the **End time** field, enter the time of day when you want to end the shift.

    4.  Select the Active check box to make the work shift active.

    5.  Select the days of the week for which you want to add this shift.

    6.  Select **Save**.

9.  Add schedule breaks to the shift.

    1.  Select the shift.

    2.  Click **Add break**.

    3.  In the **Name** field, enter a name for the break.

    4.  Set a duration for the break.

    5.  In the **Duration** field, enter the length of time for the break.

    6.  In the **Earliest Start time** field, enter the earliest time to start the break.

    7.  In the **Latest End time** field, enter the latest time to end the break.

        For example, you can set the earliest start time as 11:00, the latest end time as 15:00, and the duration of the break as one hour. If you add four agents to that work shift, the Scheduling application automatically staggers the break duration for each agent. Stagger breaks to ensure that your four agents can cover the entire shift span.

    8.  Click **Save**.

10. View the number of agents for each hour or day on the shift span window.


**Parent Topic:**[Scheduling in Workforce Optimization for Field Service](../concept/scheduling-wfo-fsm.md)

