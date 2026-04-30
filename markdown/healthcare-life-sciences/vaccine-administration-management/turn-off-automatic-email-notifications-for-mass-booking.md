---
title: Turn off automatic email notifications for mass booking
description: Turn off automatic email notifications by first turning off the default notification for the appointment configuration, then turn off the corresponding business rule. By default, email notifications are automatically sent to users when the appointments are scheduled as part of mass booking.
locale: en-US
release: zurich
product: Vaccine Administration Management
classification: vaccine-administration-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Vaccine Administration Management, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Turn off automatic email notifications for mass booking

Turn off automatic email notifications by first turning off the default notification for the appointment configuration, then turn off the corresponding business rule. By default, email notifications are automatically sent to users when the appointments are scheduled as part of mass booking.

## Before you begin

Role required: admin or sn\_vaccine\_sm.admin

## About this task

Emails are auto-generated and shared when users request a vaccination through the self-service portal. Vaccine Administration Management provides an appointment configuration that you can modify to stop emails from being sent for mass scheduling vaccine appointments.

With the help of admin access, you can configure and modify the business rules to meet your organization’s requirements.

## Procedure

1.  To turn off the default notification for the appointment configuration.

    1.  Navigate to **Vaccine Administration Management** &gt; **Administration** &gt; **Appointment Configurations**.

    2.  Open the Schedule Vaccine Appointment record.

    3.  Select the **Ignore Default Notifications** check box.

    4.  Click **Update**.

    You can’t disable email notifications for mass booking alone. If you disable the email notification events for mass booking, it applies to the self-service booking as well.

    To turn off email notifications during mass booking.

    1.  Navigate to **System Notification** &gt; **Email** &gt; **Notifications**.
    2.  Open the Vaccine Appointment Confirmed record.
    3.  In the **Active** field, select **False**.
    4.  Click **Update**.

**Parent Topic:**[Configuring Vaccine Administration Management](../concept/vaccine-mgmt-config.md)

