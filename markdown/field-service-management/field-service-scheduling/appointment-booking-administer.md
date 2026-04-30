---
title: Configuring Appointment Booking
description: Create or modify and enable the application configuration and the individual service configurations for the appointment booking feature.
locale: en-US
release: xanadu
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Additional scheduling configuration options, Setting up a Field Service scheduling method, Configuring Field Service Management, Field Service Management]
---

# Configuring Appointment Booking

Create or modify and enable the application configuration and the individual service configurations for the appointment booking feature.

## Configuration overview

Appointment booking in Field Service Management involves setting up both application-level and service-level configurations.

1.  Plugin activation:
    -   Field Service Management: Ensure that the Field Service Management plugin is activated.
    -   Appointment Booking plugin: The Appointment Booking plugin \(com.snc.appointment\_booking\) is automatically activated when you enable the Field Service Management plugin.
    -   Customer Service with Field Service Management Plugin: The Customer Service with Field Service Management plugin \(com.snc.csm\_fsm\_integration\) integrates the Field Service Management and Customer Service Management applications.
    -   Dynamic Scheduling: The Dynamic Scheduling plugin \(com.snc.dynamic\_scheduling\) enables dynamic scheduling for Service Management applications and provides support for bulk task recommendations and interval-based auto assignment. It enables **Scripted** availability method in the Appointment Booking Configuration which allows advanced scheduling for the work order task requests created from appointments.
    -   Demo data: The Appointment Booking Demo Data plugin \(com.snc.appointment\_booking\_demo\) provides the demo data to help you get started.
2.  Role Requirements:
    -   System administrator: Responsible for creating, modifying, and enabling the application-level configuration.
    -   Appointment Booking administrators: Users with the `appointment_booking_admin` role can create, modify, and enable configurations for individual services within the application.
    -   Appointment Booking manager: Users with the `appointment_booking_manager` role can create and update appointment booking records on behalf of the customer.
    -   Appointment Booking user: Users with the `appointment_booking_user` role can create and view appointments through the portal.
3.  Application-level configuration:
    -   Required for the entire application and includes settings that apply to all services within the application that support appointment booking.
    -   Field Service Management provides a default application-level configuration, known as the `Field Service Order Configuration` and `Field Service Task Configuration`. These configurations come pre-set with service-level configurations.
    -   Administrators can modify these default configurations or use them as templates to create new configurations.
4.  Service-level configuration:
    -   Required for each individual service within the application that offers scheduled appointments.
    -   A service configuration contains settings specific to that service and must be active for appointment booking to function.
5.  Enabling configurations: Ensure that both the application-level configuration and the individual service-level configurations are active. If either configuration is inactive, appointment booking will not be possible for the affected services.
6.  \(Optional\) Customize appointment booking configurations: Use extension points to customize appointment booking configurations. You can create multiple implementations for each extension point and provide an order number for each implementation. The implementation that has the lowest order number is executed.

-   **[Appointment availability](../reference/appt-booking-task-assignment.md)**  
Settings in the application configuration determine how the appointment booking feature determines availability.
-   **[Task assignment](../reference/appt-booking-config-overview.md)**  
The application configuration works with the Field Service Management configuration for task assignment.
-   **[Appointment booking email and SMS notifications](../reference/appointment-booking-notifications.md)**  
The system administrator can customize email and SMS notifications for appointment confirmation and cancellation notices and appointment reminders.
-   **[Enable or disable appointment booking](../task/appointment-booking-enable.md)**  
Enable or disable the appointment booking feature for an application as well as for services within the application that are provided to customers.
-   **[Create or modify an appointment booking application configuration](../task/appt-booking-create-app-config.md)**  
Create or modify an appointment booking configuration for an application. The information stored in this configuration applies to all the services within that application.
-   **[Configure an appointment booking record producer](../task/appt-booking-config-record-producer.md)**  
Configure an appointment booking record producer and enable the appointment booking variable set to display the correct fields in that record producer.
-   **[Create or modify an appointment booking service configuration](../task/appt-booking-create-service-config.md)**  
Create or modify an appointment booking configuration for a service within an application that is provided to customers.
-   **[Create appointment booking service configuration rules](../task/create-appt-booking-service-config-rules.md)**  
Configure appointment booking rules for a service configuration, for example, Point-of-Sale-Installation, to enable varying duration of appointments for this service.
-   **[Create appointment booking advanced configuration](../task/appintment-booking-day-level-config.md)**  
Create or modify different schedules on an advanced level when booking appointments for a service. The appointments can be scheduled at different time slots of a day, such as morning, afternoon, and evening.
-   **[Configure variable in service catalog record producer for appointment booking](../task/create-variable-in-catalog-record-producer-for-appoinment-booking.md)**  
Create variables for the catalog item attributes within the appointment booking service configuration. Configuring distinct variables for location and user contact, enables you to specify both the location and contact details when booking an appointment on the calendar.
-   **[Create business rules to automatically create an appointment record for the catalog item variable](../task/create-business-rules-to-automatically-create-appointment-record.md)**  
Create a before insert business rule on the service table to automatically add a variable for service catalog in the appointment booking table. This ensures that the variable record is visible on the appointment calendar for users when booking an appointment.
-   **[Change the day of the week that the appointment booking calendar starts on](../task/configure-week-appt-book.md)**  
You can make the appointment booking calendar start on a day other than Sunday, the default. If the start day of the week was changed, you can also change the start of the week back to Sunday.

**Parent Topic:**[Additional scheduling configuration options](advanced-scheduling-and-dispatching-capabilities.md)

**Related topics**  


[Managing appointments in Field Service Management](managing-appointments-fsm.md)

[Appointment booking components](../reference/appointment-booking-components.md)

[Extension points in Field Service Management](../reference/extension-points-field-service.md)

