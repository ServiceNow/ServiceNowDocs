---
title: Configuring Appointment Booking
description: Set up appointment booking to allow customers and service providers to schedule and manage service appointments efficiently.
locale: en-US
release: yokohama
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Additional scheduling configuration options, Setting up a Field Service scheduling method, Configuring Field Service Management, Field Service Management]
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

**Important:**

Upgrading to Yokohama may extend the upgrade maintenance time of a customer because of Appointment Booking. The Appointment Booking configuration tables \(sn\_apptmnt\_booking\_config, sn\_apptmnt\_booking\_service\_config, sn\_apptmnt\_booking\_config\_rule\) get extended to the Application File \[sys\_metadata\] table as a part of the upgrade.

After upgrading to Yokohama, re-parenting of the tables happens automatically, and the duration of the re-parenting depends on the number of records in various sys\_metadata table and its dependent tables \(sys\_dictionary, sys\_db\_object, sys\_documentation, sys\_storage\_alias\).

For example, if the sys\_metadata table roughly has 29,000,000 records, the time taken to re-parent the tables is approximately estimated to be 36 minutes. If the sys\_metadata table roughly has 5,000 records, the time taken to re-parent the tables is approximately estimated to be 3 minutes.

## Configuration overview

The steps for configuring appointment booking are:

1.  [Activate Appointment Booking](../task/activate-plugins-for-appointment-booking.md)

    Activate the Appointment Booking feature by installing the required plugins.

2.  [Enable or disable appointment booking for an application](../task/appointment-booking-enable.md)

    Enable or disable the appointment booking feature for an application as well as for services within the application that are provided to customers.

3.  [Create or modify an application configuration for Appointment Booking](../task/appt-booking-create-app-config.md)

    Create or modify an appointment booking configuration for an application. The information stored in this configuration applies to all the services within that application.

4.  [Configure variables in a record producer for appointment booking](../task/create-variable-in-catalog-record-producer-for-appoinment-booking.md)

    Create variables for the catalog item attributes within the appointment booking service configuration. Configuring distinct variables for location and user contact, enables you to specify both the location and contact details when booking an appointment on the calendar.

5.  [Configure an appointment booking record producer](../task/appt-booking-config-record-producer.md)

    Configure an appointment booking record producer and enable the appointment booking variable set to display the correct fields in that record producer.

6.  [Create or modify service configuration for Appointment Booking](../task/appt-booking-create-service-config.md)

    Create or modify an appointment booking configuration for a service within an application that is provided to customers.

7.  [Create service configuration rules for a service configuration](../task/create-appt-booking-service-config-rules.md)

    Configure appointment booking rules for a service configuration, for example, Point-of-Sale-Installation, to enable varying duration of appointments for this service.

8.  \(Optional\) [Configure daily and advanced schedules](configure-daily-and-advanced-schedules.md)

    Create advanced appointment schedules to provide customers with precise time slots, or adjust the beginning day of the week on your booking calendar to align with your organization's scheduling preferences.

9.  [Create a business rule to automatically generate appointment records from catalog item variables](../task/create-business-rules-to-automatically-create-appointment-record.md)

    Create a before insert business rule on the service table to automatically add a variable for service catalog in the appointment booking table. This ensures that the variable record is visible on the appointment calendar for users when booking an appointment.

10. \(Optional\) [Enable or disable seismic Appointment Booking calendar](../task/enable-or-disable-seismic-appointment-booking-calendar.md)

    Use the seismic appointment booking calendar across all user interfaces to ensure a consistent and seamless scheduling experience.

11. \(Optional\) [Enable and configure appointment slot recommendation](enable-and-configure-appointment-slot.md)

    Appointment Booking slot recommendation rules assist in identifying the optimal appointment times for customers. These recommended slots enable customers to efficiently choose the most suitable available appointment times.

12. \(Optional\) [Customize Appointment Booking email and SMS notifications](../reference/appointment-booking-notifications.md)

    The system administrator can customize email and SMS notifications for appointment confirmation and cancellation notices and appointment reminders.

13. \(Optional\) [Extension points in Field Service Management](../reference/extension-points-field-service.md)

    Use extension points to customize appointment booking configurations.

14. \(Optional\) [Use Appointment API for interacting with the appointment booking application.](https://www.servicenow.com/docs/bundle/xanadu-api-reference/page/integrate/inbound-rest/concept/appointment-api.html)

    Use this API to book and reschedule appointments, check available appointment slots, and fetch appointment booking configuration details.


**Related topics**  


[Manage appointments](managing-appointments.md)

[Appointment booking components](../reference/appointment-booking-components.md)

[Learn about appointment availability settings for an application configuration](../reference/appt-booking-task-assignment.md)

[Learn about task assignment methods for an application configuration](../reference/appt-booking-config-overview.md)

