---
title: Configure Appointment Booking
description: Set up appointment booking to allow customers and service providers to schedule and manage service appointments efficiently.
locale: en-US
release: australia
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configuring Appointment Booking, Additional scheduling configuration options, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Configure Appointment Booking

Set up appointment booking to allow customers and service providers to schedule and manage service appointments efficiently.

The steps to configure Appointment Booking are:

1.  [Activate Appointment Booking](../task/activate-plugins-for-appointment-booking.md)

    Activate the Appointment Booking feature by installing the required plugins.

2.  [Domain Separation and Appointment Booking](domain-separation-appt-booking.md)

    Learn about Demain Separation and Appointment Booking.

3.  [Enable or disable appointment booking](../task/appointment-booking-enable.md)

    Enable or disable the appointment booking feature for an application as well as for services within the application that are provided to customers.

4.  [Create or modify an application configuration for Appointment Booking](../task/appt-booking-create-app-config.md)

    Create or modify an appointment booking configuration for an application. The information stored in this configuration applies to all the services within that application.

5.  [Configure variables in a record producer for appointment booking](../task/create-variable-in-catalog-record-producer-for-appoinment-booking.md)

    Create variables for the catalog item attributes within the appointment booking service configuration. Configuring distinct variables for location and user contact, enables you to specify both the location and contact details when booking an appointment on the calendar.

6.  [Configure an appointment booking record producer](../task/appt-booking-config-record-producer.md)

    Configure an appointment booking record producer and enable the appointment booking variable set to display the correct fields in that record producer.

7.  [Create a business rule to automatically generate appointment records from catalog item variables](../task/create-business-rules-to-automatically-create-appointment-record.md)

    Create a before insert business rule on the service table to automatically add a variable for service catalog in the appointment booking table. This ensures that the variable record is visible on the appointment calendar for users when booking an appointment.

8.  [Create or modify service configuration for Appointment Booking](../task/appt-booking-create-service-config.md)

    Create or modify an appointment booking configuration for a service within an application that is provided to customers.

9.  \(Optional\) [Create service configuration rules for a service configuration](../task/create-appt-booking-service-config-rules.md)

    Configure appointment booking rules for a service configuration, for example, Point-of-Sale-Installation, to enable varying duration of appointments for this service.

10. [Create appointment booking advanced configuration](../task/appintment-booking-day-level-config.md)
11. \(Optional\) [Enable or disable seismic appointment booking calendar](../task/enable-or-disable-seismic-appointment-booking-calendar.md)

    Use the seismic appointment booking calendar across all user interfaces to ensure a consistent and seamless scheduling experience.

12. \(Optional\) [Enable and configure appointment slot recommendation](enable-and-configure-appointment-slot-recommendation.md)

    Appointment Booking slot recommendation rules assist in identifying the optimal appointment times for customers. These recommended slots enable customers to efficiently choose the most suitable available appointment times.

13. \(Optional\) [Set the starting day of the week on the appointment booking calendar](../task/configure-week-appt-book.md)

