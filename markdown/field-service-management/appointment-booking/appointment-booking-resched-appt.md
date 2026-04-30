---
title: Reschedule an appointment for a customer
description: Dispatchers and agents can reschedule appointments for customers to dispatch agent to address the customer issue based on rescheduled time slot.
locale: en-US
release: zurich
product: Appointment Booking
classification: appointment-booking
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Managing appointments from a work order or work order task, Managing appointments on behalf of a customer, Appointment booking, Use, Field Service Management]
---

# Reschedule an appointment for a customer

Dispatchers and agents can reschedule appointments for customers to dispatch agent to address the customer issue based on rescheduled time slot.

## Before you begin

Role required: wm\_dispatch, sn\_customerservice\_agent, sn\_customerservice.consumer\_agent

Setup the **Field Service Order Configuration** to book an appointment for work orders and **Field Service Task Configuration** to book an appointment for work order tasks. For more information, see [Configuring Appointment Booking](../concept/appointment-booking-administer.md).

## About this task

A dispatcher or an agent can reschedule an appointment for a customer from a work order.

**Note:** An appointment cannot be rescheduled if the current time is within the reschedule/cancel window specified in the service configuration.

## Procedure

1.  Open either a work order or work order task.

    -   To reschedule an appointment for a work order, navigate to **All** &gt; **Field Service** &gt; **Work Order** &gt; **All Work Orders**, and then select the desired work order.
    -   To reschedule an appointment for a work order task, navigate to **All** &gt; **Field Service** &gt; **Work Order** &gt; **All Work Order Tasks**, and then select the desired work order task.
2.  Click **Reschedule Appointment** to open the Select Appointment pop-up window.

    The Select Appointment pop-up window displays the selected day and time of the current appointment.

3.  Select a different day and appointment time slot and then click **Select**.

    The date and time for the appointment are updated. Click the link in the information message to view the appointment details.

    Rescheduling an appointment triggers an appointment rescheduled email to the customer.


