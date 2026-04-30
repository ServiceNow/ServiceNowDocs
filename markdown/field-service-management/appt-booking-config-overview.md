---
title: Learn about task assignment methods for an application configuration
description: The Appointment Booking feature works with Field Service Management task assignment methods to effectively assign tasks and manage appointments.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Field Service Management reference, Field Service Management]
---

# Learn about task assignment methods for an application configuration

The Appointment Booking feature works with Field Service Management task assignment methods to effectively assign tasks and manage appointments.

Appointment Booking supports these task assignment methods:

-   Auto-assignment
-   Dynamic scheduling
-   Manual

Appointment booking provides enhancements that help with scheduling efficiency:

-   Automatically identifies the most suitable dispatch group for each appointment-based task.
-   Prevents tasks with booked appointments from becoming unassigned.
-   Calculates agent and group availability accurately for appointment windows.

## Dynamic scheduling

Appointment booking adds unassignment criteria to the dynamic scheduling configuration that prevents work orders and work order tasks with appointment windows from being unassigned. It also adds criteria that prioritizes work orders and tasks with appointment windows.

Navigate to **Field Service** &gt; **Administration** &gt; **Dynamic Scheduling Configuration**.

-   The **Task Filters** related list includes an Appointment Tasks filter for tasks that have an appointment window and are in the **Pending Dispatch** state.
-   The **Un-Assignment Constraints** related list includes the **Has Appointment** constraint that prevents tasks with appointment windows from being unassigned.

## Rescheduling work start and work end times

When a work order is created for a booked appointment, or when an appointment is booked for an existing work order, the appointment window start and end times are used for the work order task **Window start** and **Window end** times.

For work order tasks that have scheduled appointments, dispatchers receive warning messages if they change any of the following fields:

-   Window start
-   Window end
-   Scheduled start
-   Scheduled travel start

**Parent Topic:**[Field Service Management reference](../../planning-and-policy/reference/fsm-reference.md)

**Related topics**  


[Global domain configurations](../../planning-and-policy/task/t_ConfigureFieldService.md)

[Schedules](https://www.servicenow.com/docs/access?context=c_UseSchedules&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)

