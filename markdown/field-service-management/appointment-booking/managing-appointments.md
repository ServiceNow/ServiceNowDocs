---
title: Managing appointments
description: Book, reschedule, and cancel appointments for available services.
locale: en-US
release: australia
product: Appointment Booking
classification: appointment-booking
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use, Field Service Management]
---

# Managing appointments

Book, reschedule, and cancel appointments for available services.

With the Appointment Booking feature, customers can view available appointment windows, make a selection, and book a service appointment from the service portal.

Agents and dispatchers can also book appointments on behalf of customers. Booking an appointment creates a work order and one or more work order tasks, depending on the type of service. Booked appointments can be rescheduled and canceled within the time constraints identified in the configuration.

**Note:**

-   Work order tasks are scheduled according to the dependencies set in the template.
-   The predecessor task must be assigned first. You cannot book an appointment for a successor task until the predecessor task is assigned.
-   The start and end times for successor tasks are automatically adjusted according to when the predecessor task is completed.
    -   If the predecessor task ends at 11:00 AM on a given day, the appointment for a successor task is scheduled only after 11:00 AM on that day.
    -   When a minimum lag time is defined between tasks, the window start of the successor task is calculated as per the specified lag time. For example, if the predecessor task ends on 12 May, 1.00 p.m, and the lag time is 3 days, the appointment for the successor task is scheduled only after 1.00 p.m on 15 May.
    -   If a maximum lag time is specified in the predecessor task, the successor task must be completed within that window. For example, if the appointment for the successor task is scheduled on May 15 and the maximum lag time specified is 3 days, the successor task must be scheduled and completed by May 18.

When Capacity and Reservations Management is installed, the system factors in capacity and reservation rules from the Capacity Management module as it presents available slots for booking new appointments or rescheduling existing ones. For more information, see [Capacity and Reservations Management](capacity-management.md).

## Using overview

Managing appointments includes one of the following activities.

-   [Managing appointments on behalf of a customer](managing-appts-on-behalf-of-customer.md)

    Agents and dispatchers can manage appointments on behalf of a customer from a work order, work order task, or in the CSM/ FSM Configurable Workspace.

-   [Managing appointments as a customer](manage-appts-as-a-customer.md)

    Customers can book, reschedule, or cancel appointments. Booking an appointment from the portal creates a work order for the selected service.


**Related topics**  


[Appointment booking](appointment-booking.md)

[Configuring Appointment Booking](appointment-booking-administer.md)

