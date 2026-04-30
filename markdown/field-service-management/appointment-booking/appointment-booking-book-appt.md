---
title: Book an appointment for a customer
description: Dispatchers and agents can book appointments for customers.
locale: en-US
release: yokohama
product: Appointment Booking
classification: appointment-booking
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Manage appointments from a work order or work order task, Manage appointments on behalf of a customer, Manage appointments, Using Field Service Management, Field Service Management]
---

# Book an appointment for a customer

Dispatchers and agents can book appointments for customers.

## Before you begin

Role required: wm\_dispatch, sn\_customerservice\_agent, sn\_customerservice.consumer\_agent

You must activate and set up the Field Service Order Configuration, Field Service Task Configuration to book an appointment for work order and work order tasks respectively. For more information, see [Configuring Appointment Booking](../concept/appointment-booking-administer.md).

## About this task

Dispatchers and agents can click "Book Appointment" on the work order or work order task form. This button appears on the form after the work order is qualified.

**Note:** The Book Appointment feature isn’t available for work orders if the related work order task is assigned to an external group or agent, or if an appointment is already booked for one of the work order tasks in the work order. Similarly, the feature is unavailable for a work order task if an appointment is already booked for the related work order.

## Procedure

1.  Open either work order or work order task.

    -   If you want to book an appointment for a work order, navigate to **All** &gt; **Field Service** &gt; **Work Order**, and then open a work order.
    -   If you want to book an appointment for a work order task, navigate to **All** &gt; **Field Service** &gt; **Work Order Task**, and then open a work order task.
    In the work order and work order task pages, the **Template** field indicates the service for which you’re booking an appointment. To book an appointment, the template must have an active service configuration.

2.  Select **Book Appointment**.

    This Select Appointment pop-up window displays available appointments for either a single day or for a week. If no appointments are available, select a different day or week.

3.  Use the left and right arrows or the calendar icon to display the desired day or week.

    Available appointment time slots for the selected day or week are displayed.

4.  Select the desired time slot and then select **Select**.

    The appointment is created for the selected date and time.


## Result

The **Window start** and **Window end** fields on the work order task are updated with the selected appointment start and end times. The **Estimated work duration** field is updated with the duration of the selected appointment time slot.

**Parent Topic:**[Manage appointments from a work order or work order task](../concept/managing-appts-from-work-order.md)

