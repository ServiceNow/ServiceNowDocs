---
title: Reschedule an appointment as a customer
description: Reschedule a service appointment from either the Customer or the Consumer Service Portal.
locale: en-US
release: yokohama
product: Appointment Booking
classification: appointment-booking
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Manage appointments as a customer, Manage appointments, Using Field Service Management, Field Service Management]
---

# Reschedule an appointment as a customer

Reschedule a service appointment from either the Customer or the Consumer Service Portal.

## Before you begin

Role required: appointment\_booking\_user

Setup the **Field Service Order Configuration** to book an appointment for work orders and **Field Service Task Configuration** to book an appointment for work order tasks. For more information, see [Configuring Appointment Booking](../concept/appointment-booking-administer.md).

## About this task

The details for the scheduled appointment appear on the work order and work order task forms. Access the appointment information by selecting it from the list of upcoming appointments or by going directly to the respective work order or work order task.

**Note:** An appointment cannot be rescheduled if the current time is within the reschedule/cancel window specified in the service configuration.

## Procedure

1.  Log in to the Customer or Consumer Service Portal.

2.  In the portal header, click **Support** &gt; **Appointments** to display the Appointment Listing page.

3.  Click **Upcoming** to view a list of upcoming appointments.

4.  Select the appointment to reschedule.

    This opens the work order for the selected appointment.

5.  Click the **Appointment** field to open the Select Appointment pop-up window.

    The Select Appointment pop-up window displays the day or week of the current appointment and highlights the selected time slot.

6.  Select a different day and appointment time slot and then click **Select**.

    The **Appointment** field displays the new date and time.

    Information about the rescheduled appointment is noted in the **Activities** field on the work order or the work ordert task form. This information includes the original appointment window, the rescheduled appointment window, and the user who made the change.

    The user receives a confirmation email that the appointment has been rescheduled.


## Result

The customer receives SMS and email notification that their appointment is rescheduled.

**Parent Topic:**[Manage appointments as a customer](../concept/manage-appts-as-a-customer.md)

