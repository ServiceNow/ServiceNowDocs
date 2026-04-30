---
title: Customize Appointment Booking email and SMS notifications
description: Customize email and SMS notifications for appointments. These notifications help users stay informed and engaged throughout the appointment scheduling process—providing clear confirmations, reminders, cancellations, and rescheduling notices.
locale: en-US
release: zurich
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring Appointment Booking, Additional scheduling configuration options, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Customize Appointment Booking email and SMS notifications

Customize email and SMS notifications for appointments. These notifications help users stay informed and engaged throughout the appointment scheduling process—providing clear confirmations, reminders, cancellations, and rescheduling notices.

An email and SMS notification for an appointment includes task information, such as the task number and description, as well as the appointment time. It can also include a link that enables the user to reschedule or cancel the appointment.

System administrators can configure both email and SMS notifications using the following appointment booking email templates.

-   appointment.confirmed
-   appointment.cancel
-   appointment.reschedule

These templates come included with the appointment booking plugin. You can customize them to meet specific requirements. For more information, see [Create an email notification](https://www.servicenow.com/docs/access?context=t_CreateANotification&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

**Note:** Ensure to install Customer Experience plugin to configure SMS. For more information, see [Activate Field Service Management Customer Experience](../concept/Configuring-cust-exp.md#).

Appointment booking email and SMS notifications are active for all services using the appointment booking feature. The following email notifications are included with the appointment booking feature:

|Email notification type|Description|
|-----------------------|-----------|
|Appointment Confirmation|Sent to the customer once the task for an appointment has been assigned to and accepted by a technician. If acceptance by the technician is not required, the notification is sent to the customer when the task is assigned.|
|Appointment Cancel|Sent to the customer when an appointment is canceled. Can include task information and also a reason for the cancellation.|
|Appointment Reschedule|Sent to the customer when an appointment is rescheduled.|

