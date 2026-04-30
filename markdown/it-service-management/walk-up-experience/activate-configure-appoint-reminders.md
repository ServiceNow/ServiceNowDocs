---
title: Activate and configure appointment booking reminders for Walk-up Experience
description: Configure scheduled appointment reminders for Walk-up Experience users. Reminders ensure users attend appointments in a timely manner or reschedule or cancel an appointment if they can no longer attend.
locale: en-US
release: zurich
product: Walk-Up Experience
classification: walk-up-experience
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure Walk-up Experience appointment booking, Walk-up Experience appointment booking administration, Book Walk-up Experience appointments, Configure, Walk-up Experience, IT Service Management]
---

# Activate and configure appointment booking reminders for Walk-up Experience

Configure scheduled appointment reminders for Walk-up Experience users. Reminders ensure users attend appointments in a timely manner or reschedule or cancel an appointment if they can no longer attend.

## Before you begin

Role required: sn\_walkup.walkup\_admin or admin

## About this task

To operate appointment booking reminders, activate the **Appointment Booking Reminders** Scheduled Job, since it is not active by default. In addition, the **Appointment reminder** field does not appear on the **Appointment Booking Service Configuration** form by default. You must add it to the form and configure reminders. Reminders are inactive unless a configuration is set.

## Procedure

1.  Navigate to **System Definition** &gt; **Scheduled Jobs**.

2.  Search for **Appointment Booking Reminders** by name and select to open.

3.  Click the **Active** field to activate the scheduled job.

4.  Click **Update**.

5.  To add the **Appointment reminder** field to the **Appointment Booking Service Configuration** form, navigate to **Walk-up Experience** &gt; **Administration** &gt; **Appointment Configurations**.

6.  Select a Walk-up Experience service configuration from the list.

7.  Click the menu button \( ![menu icon](../../../common/image/Form_MenuIcon.png)\) and scroll to **Configure** &gt; **Form Layout**.

8.  Select **Appointment reminder** from the **Available** list and move it to the **Selected** list using the add button.

9.  Select **Save**.

    The **Appointment Booking Service Configuration** form is displayed with the **Appointment reminder** field.

10. To configure an appointment reminder, choose time, in hours, from the **Appointment reminder** field drop-down list.

    The time represents the time before a scheduled appointment that you want to send a reminder. For example, a reminder is sent, two hours before a scheduled appointment.

11. Select **Update** to add the appointment reminder configuration.


**Parent Topic:**[Configure Walk-up Experience appointment booking](../concept/walkup-appointment-booking-config.md)

