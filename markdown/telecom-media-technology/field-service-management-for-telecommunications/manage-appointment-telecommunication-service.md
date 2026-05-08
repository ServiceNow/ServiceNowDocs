---
title: Manage appointments for telecommunication services
description: Manage the appointments for the field services to enable the installation, activation, and site assessments that are needed for connectivity services.
locale: en-US
release: australia
product: Field Service Management for Telecommunications
classification: field-service-management-for-telecommunications
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Field Service Management for Telecommunications, Telecommunications, Media, and Technology \(TMT\)]
---

# Manage appointments for telecommunication services

Manage the appointments for the field services to enable the installation, activation, and site assessments that are needed for connectivity services.

With the use of the ServiceNow Telecommunication Open API application, you create appointments from your system for the connectivity-related field services. You can book an appointment on an existing work order and assigned it to the field service agent. To learn more about booking appointments, see Managing appointments.

The Telecommunication Open API application uses the TM Forum 646 API to support the external system to create and manage appointments for the field services.

This feature supports the following:

-   Supports POST operation for appointment via `appointment management API`.
-   Understands the appointment data model available in the Field Service Management application.
-   Supports POST operation to create an appointment in the Field Service Management application for a work order.
-   Supports required validations for the incoming data for appointment creation for an available time slot via `search time slot API`.

## Configuring the appointment booking feature

To manage appointment bookings in your system, you must create, modify, or enable the application configuration and the individual service configurations. Do the following steps to configure the appointment booking feature:

1.  Configure an appointment booking record producer.
2.  Create or modify service configuration for Appointment Booking.
3.  Configure variables in a record producer for appointment booking.

