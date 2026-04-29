---
title: Configuring Appointment Booking
description: Set up appointment booking to allow customers and service providers to schedule and manage service appointments efficiently.
locale: en-US
release: australia
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Additional scheduling configuration options, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Configuring Appointment Booking

Set up appointment booking to allow customers and service providers to schedule and manage service appointments efficiently.

Appointment booking requires configuration at both the application level and the service level.

**Note:**

Both application-level and corresponding service-level configurations must be active for appointment booking to function properly.

**Application-Level configuration**

Appointment booking requires an active **application-level configuration** for Field Service Management. This configuration includes global settings that apply to all services supporting appointment booking within the application. Only a system administrator can create, modify, and enable an application-level configuration.

The appointment booking feature provides predefined application-level configurations:

-   **Field Service Order Configuration**
-   **Field Service Task Configuration**

Administrators can use these default configurations directly, modify them to meet specific business requirements, or use them as examples to create new application-level configurations.

**Service-Level configuration**

In addition to the application-level configuration, each service offering scheduled appointments must have its own active **service-level configuration**. A service-level configuration contains settings unique to that specific service.

**Appointment booking administrators \(appointment\_booking\_admin\)** can:

-   Create new configurations for individual services.
-   Modify existing service configurations as needed.
-   Enable service configurations to activate appointment booking functionality.

## Configuration overview

The steps for configuring Appointment Booking are:

1.  [Configure Appointment Booking](configure-appointment-booking.md)
2.  \(Optional\) [Configure Advanced Appointment Booking](configure-advanced-appointment-booking.md)

    Advanced Appointment Booking allows you to configure flexible schedules, holidays and appointment window durations for a territory.

3.  \(Optional\) [Customize Appointment Booking email and SMS notifications](../reference/appointment-booking-notifications.md)

    The system administrator can customize email and SMS notifications for appointment confirmation and cancellation notices and appointment reminders.

4.  \(Optional\) [Extension points in Field Service Management](../reference/extension-points-field-service.md)

    Use extension points to customize appointment booking configurations.

5.  \(Optional\) [Use Appointment API for interacting with the appointment booking application.](https://www.servicenow.com/docs/bundle/xanadu-api-reference/page/integrate/inbound-rest/concept/appointment-api.html)

    Use this API to book and reschedule appointments, check available appointment slots, and fetch appointment booking configuration details.


**Related topics**  


[Appointment booking](appointment-booking.md)

[Managing appointments](managing-appointments.md)

[Appointment booking components](../reference/appointment-booking-components.md)

[Learn about appointment availability settings](../reference/appt-booking-task-assignment.md)

[Learn about task assignment](../reference/appt-booking-config-overview.md)

