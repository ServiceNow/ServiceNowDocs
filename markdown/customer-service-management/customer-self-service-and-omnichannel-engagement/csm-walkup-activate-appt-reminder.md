---
title: Activate and configure appointment booking reminders for Walk-up Experience
description: Configure scheduled appointment reminders for Walk-up Experience users. Reminders ensure that users attend appointments in a timely manner, and if they can't attend then reschedule or cancel an appointment.
locale: en-US
release: australia
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Appointment booking configuration, Walk-up Experience appointment booking, Configure Walk-up Experience for Customer Service Management, Set up self-service, Configure, Customer Service Management]
---

# Activate and configure appointment booking reminders for Walk-up Experience

Configure scheduled appointment reminders for Walk-up Experience users. Reminders ensure that users attend appointments in a timely manner, and if they can't attend then reschedule or cancel an appointment.

## Before you begin

Role required: sn\_csm\_walkup.walkup\_admin

## About this task

For using appointment booking reminders, you must activate the **Appointment Booking Reminders** Scheduled Job, which is not active by default. In addition, the **Appointment reminder** field doesn't appear on the **Appointment Booking Service Configuration** form by default. You must add it to the form and configure reminders. Reminders are inactive unless a configuration is set.

## Procedure

1.  To activate the **Appointment Booking Reminders** Scheduled Job, navigate to **System Definition** &gt; **Scheduled Jobs**.

2.  Search for **Appointment Booking Reminders** by name and click to open.

3.  Click the **Active** field to activate the scheduled job.

4.  Click **Update**.

5.  To add the **Appointment reminder** field to the **Appointment Booking Service Configuration** form, navigate to **Walk-up Experience** &gt; **Administration** &gt; **Appointment Configurations**.

6.  Select a Walk-up Experience service configuration from the list.

    The system opens an **Appointment Booking Service Configuration** form.

7.  Click the menu button \( ![Menu icon.](../../../common/image/Form_MenuIcon.png)\) and scroll to **Configure** &gt; **Form Layout**.

8.  Select **Appointment reminder** from the **Available** list and move it to the **Selected** list using the add button.

9.  Click **Save**.

    The **Appointment Booking Service Configuration** form displays with the **Appointment reminder** field.

10. To configure an appointment reminder, choose an amount of time, in hours, from the **Appointment reminder** field drop-down list.

    The hour/hours you choose represents the amount of time before a scheduled appointment that you want to send a reminder for. For example, two hours before a scheduled appointment.

11. Click **Update** to add the appointment reminder configuration.


