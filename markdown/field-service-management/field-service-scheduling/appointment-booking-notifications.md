---
title: Appointment booking email and SMS notifications
description: The system administrator can customize email and SMS notifications for appointment confirmation and cancellation notices and appointment reminders.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/field-service-management/field-service-scheduling/appointment-booking-notifications.html
release: xanadu
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Appointment Booking, Additional scheduling configuration options, Setting up a Field Service scheduling method, Configuring Field Service Management, Field Service Management]
---

# Appointment booking email and SMS notifications

The system administrator can customize email and SMS notifications for appointment confirmation and cancellation notices and appointment reminders.

An email and SMS notification for an appointment includes task information, such as the task number and description, as well as the appointment time. It can also include a link that enables the user to reschedule or cancel the appointment.

System administrators can configure both email and SMS notifications using the following appointment booking email templates.

-   appointment.confirmed
-   appointment.cancel
-   appointment.reschedule

These templates come included with the appointment booking plugin. You can customize them to meet specific requirements. For more information, see .

**Note:** Ensure to install Customer Experience plugin to configure SMS. For more information, see [Activate Field Service Management Customer Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/field-service-management/work-order-management/activate-customer-experience-fsm.md).

Appointment booking email and SMS notifications are active for all services using the appointment booking feature. The following email notifications are included with the appointment booking feature:

-   **Appointment Confirmation**: Sent to the customer once the task for an appointment has been assigned to and accepted by a technician. If acceptance by the technician is not required, the notification is sent to the customer when the task is assigned.
-   **Appointment Cancel**: Sent to the customer when an appointment is canceled. Can include task information and also a reason for the cancellation.
-   **Appointment Reschedule**: Sent to the customer when an appointment is rescheduled. Can include task information.

**Parent Topic:**[Configuring Appointment Booking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/field-service-management/field-service-scheduling/appointment-booking-administer.md)

