---
title: Task assignment
description: The application configuration works with the Field Service Management configuration for task assignment.
locale: en-US
release: xanadu
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Appointment Booking, Additional scheduling configuration options, Setting up a Field Service scheduling method, Configuring Field Service Management, Field Service Management]
---

# Task assignment

The application configuration works with the Field Service Management configuration for task assignment.

Appointment booking works with the task-driven process life cycle and the following task assignment methods:

-   Auto-assignment
-   Dynamic scheduling
-   Manual

Auto-assignment and dynamic scheduling include enhancements that support appointment booking:

-   Identifying the best dispatch group for task assignment.
-   Preventing tasks with appointment windows from being unassigned.
-   Calculating availability for agents and groups.

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

**Parent Topic:**[Configuring Appointment Booking](../concept/appointment-booking-administer.md)

**Related topics**  


[Global domain configurations](../../planning-and-policy/task/t_ConfigureFieldService.md)

[Schedules](https://www.servicenow.com/docs/access?context=c_UseSchedules&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)

