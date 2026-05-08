---
title: Learn about appointment availability settings
description: Settings in the application configuration determine how the appointment booking feature determines availability.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference, Field Service Management]
---

# Learn about appointment availability settings

Settings in the application configuration determine how the appointment booking feature determines availability.

Different methods are provided for determining availability:

-   **Number of appointments per slot**

    This method uses a specified number of available appointments per time window. The actual number of appointments is specified in the service configuration. For example, if the administrator specifies 10 appointments per window, then each appointment window will have 10 available appointments. The number of available appointments for an appointment window decreases by one each time an appointment within that window is booked.

    **Note:**

    The Appointments per window are shared across different locations in the same time zone.

    You can configure the number of available appointments per window for different locations by creating a Service Configuration rule and its Advanced Configuration for each location. Apply conditions by selecting **Location** as the **Task Condition** while creating the Service Configuration rule.

-   **Scripted**

    This method uses a custom script to determine the number of available appointments per time window. For example, you can use a customized script to check for agent schedule and skills to assign the task.

    The default script included with the Field Service Management application configuration uses the task assignment method set in the Field Service Order configuration or Field Service Task configuration to determine availability. If the task assignment method is set to manual, the availability defaults to the **Number of appointments per slot** availability method. If the task assignment is set to auto-assignment or dynamic scheduling, the configurations associated with these task assignment methods are considered while calculating availability.

-   **Based on capacity**

    This option is available when Field Service  Capacity and Reservations Management plugin is installed, and the Task Table is Work Order or Work Order Task. This method determines appointments based on the capacity and reservations defined in the capacity management settings when Capacity and Reservation Management is activated.

    **Note:**

    -   The capacity is shared across different cities in the same time zone.
    -   There could be a slight delay in the creation of work order tasks for appointments booked through Service Portal as the tasks are created asynchronously after capacity calculation.

## Excluding days from appointment availability

In the service configuration, the appointment booking administrator can select a schedule of days that are excluded from appointment availability. The **Holiday Schedule** field is a reference field that points to the Schedules table \[cmn\_schedule\]. Selecting a schedule from the Schedules list defines the days and times to exclude from appointment availability. In the schedule selected, those days must be set to **Excluded**.

**Parent Topic:**[Field Service Management reference](../../planning-and-policy/reference/fsm-reference.md)

**Related topics**  


[Global domain configurations](../../planning-and-policy/task/t_ConfigureFieldService.md)

[bundle-platadm.c_UseSchedules]

