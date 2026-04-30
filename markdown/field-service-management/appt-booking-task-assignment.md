---
title: Learn about appointment availability settings for an application configuration
description: Appointment availability defines how many customer appointments can be scheduled within each time slot. You can control availability using different methods based on your organization's needs.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Field Service Management reference, Field Service Management]
---

# Learn about appointment availability settings for an application configuration

Appointment availability defines how many customer appointments can be scheduled within each time slot. You can control availability using different methods based on your organization's needs.

As an administrator, you can configure availability settings at the application level, choosing from the following three methods:

-   **Number of appointments per slot \(Fixed\)**

    Set a fixed number of available appointments for each time slot. For example, if you set **10 appointments per slot**, each slot starts with 10 openings. Every appointment booked reduces availability by one.

    **Example:**

    You configure 10 appointments per 1-hour slot. After booking one appointment, 9 slots remain available.

    **Important:**

    Appointment limits per slot apply across all locations in the same time zone. If you need different appointment limits for specific locations, create individual **Service Configuration** rules, with advanced conditions using the **Location** as a criterion.

-   **Scripted**

    Use scripts to dynamically calculate availability for each time slot. This method adapts availability based on your scheduling rules. The default script included with Field Service Management uses your task assignment method \(configured in either the **Field Service Order** or **Field Service Task configuration**\).

    **Manual assignment**: Defaults to the fixed appointments-per-slot method.

    **Auto-assignment or Dynamic scheduling**: Calculates availability based on resource assignments and scheduling configurations.

-   **Based on capacity**

    Calculates available appointments based on capacity and reservation settings. Capacity indicates how many tasks your resources can handle at a given time.

    The capacity is shared across different cities in the same time zone.

    **Important:** Available only if the Field Service Capacity and Reservations Management plugin is installed, and the Task table is Work Order or Work Order Task.


## Excluding days from appointment availability

You can exclude certain days, such as holidays, from appointment availability: In the Service Configuration, select a Holiday Schedule. Days marked as Excluded in the selected schedule will not be available for appointments.

**Note:** The **Holiday Schedule** references the Schedules table \(cmn\_schedule\).

**Parent Topic:**[Field Service Management reference](../../planning-and-policy/reference/fsm-reference.md)

**Related topics**  


[Global domain configurations](../../planning-and-policy/task/t_ConfigureFieldService.md)

[Schedules](https://www.servicenow.com/docs/access?context=c_UseSchedules&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)

