---
title: Configure event visibility in Workforce when Workforce Optimization for Field Service is installed
description: Enable users to control the visibility of events and work order tasks that appear in the Calendars tab when Workforce Optimization for Field Service is enabled.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Workforce, CSM/FSM Configurable Workspace, Configure, Field Service Management]
---

# Configure event visibility in Workforce when Workforce Optimization for Field Service is installed

Enable users to control the visibility of events and work order tasks that appear in the Calendars tab when Workforce Optimization for Field Service is enabled.

## Before you begin

[Configure event visibility in Workforce when Workforce Optimization for Field Service is installed](configure-work-order-task-visibility.md)

Role required: wm\_admin

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Administration** &gt; **Configuration**.

2.  Select the **Assignment** tab.

3.  In the Scheduling section, toggle the **Enable shift Scheduling for FSM to Determine Availability** property.

4.  Select **Save**.

5.  Navigate to **All** &gt; **Agent Schedule** &gt; **Event Configuration**.

6.  Review the list of event types.

    When Workforce Optimization for Field Service is installed, the choices by default are:

    -   Appointments
    -   Case tasks
    -   Work Order Tasks
7.  Set the **Active** field for the event to **true** to display it on the Team calendar.

    Users are able to toggle the selected events to display on the Team calendar in Workforce.

8.  Adjust the default filter conditions for the selected event type.

    1.  Select the name of the event type to open the record.

    2.  Update the filter conditions.

    3.  Select **Update**.

    **Note:** To ensure the event type appears on the team calendar, make sure the user, start date, and end date fields are all completed.


**Related topics**  


[View events on the Team calendar in Workforce when Workforce Optimization for Field Service is installed](view-work-order-tasks-on-the-team-calendar-when-wfo-is-installed.md)

