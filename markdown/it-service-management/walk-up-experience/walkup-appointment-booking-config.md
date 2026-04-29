---
title: Configure Walk-up Experience appointment booking
description: Create or modify appointment booking configurations for the Walk-up Experience. You can view or modify the Walk-up Experience application appointment booking configuration and create or modify related service appointment configurations.
locale: en-US
release: australia
product: Walk-Up Experience
classification: walk-up-experience
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Walk-up Experience appointment booking administration, Book Walk-up Experience appointments, Configure, Walk-up Experience, IT Service Management]
---

# Configure Walk-up Experience appointment booking

Create or modify appointment booking configurations for the Walk-up Experience. You can view or modify the Walk-up Experience application appointment booking configuration and create or modify related service appointment configurations.

The base system Walk-up Experience application includes a default appointment booking configuration that can be modified. By default, the information stored in the Walk-up Experience application appointment booking configuration applies to all services within that application. Services within the Walk-up Experience application are defined as the actual walk-up queue locations. You can create new appointment booking service configurations for the Walk-up Experience application or modify existing configurations.

For example, you may want to configure one walk-up queue to accept appointment booking every day from Monday to Friday, but for another queue, you only want appointment booking available on Monday, Wednesday, and Friday. By configuring appointment booking at the service level, you can achieve this goal.

Specific Walk-up Experience set-up criteria for appointment booking include the following configurations:

-   Define different appointment schedules and time windows per queue location.
-   Define the time window in which you want to support appointments. For example, 15 minutes now\_V. 30 minutes.
-   Define the time window capacity. For example, the maximum number of appointments per time window.

-   **[View or modify a Walk-up Experience appointment booking configuration](../task/view-modify-walkup-appointment-app.md)**  
View the base system default appointment booking application configuration to determine if the criteria meets your walk-up appointment booking needs. You can modify the application configuration to uniquely manage appointment booking for your experience. The information stored in the Walk-up Experience appointment booking application configuration applies to all the services within the application.
-   **[Create a record producer to capture Walk-up Experience appointment records](../task/create-rp-walkup-appointment.md)**  
Capture Walk-up Experience appointment records by creating unique record producers for your individual walk-up locations. The Appointment Booking Service Configuration form contains required fields that refer to variables in the associated record producer.
-   **[Create or modify a Walk-up Experience appointment booking service configuration](../task/configure-walkup-appointments.md)**  
Create or modify appointment booking configurations for Walk-up Experience services. A service is defined as the actual physical location of a walk-up queue. The information stored in the Walk-up Experience application configuration applies to all services, or queue locations, within the application.
-   **[Configure daily schedules for Walk-up Experience appointment booking](../task/config-walkup-daily-appoint-schedule.md)**  
Define hours of operation and daily schedules for booking an appointment at your Walk-up Experience location.
-   **[Configure excluded hours for Walk-up Experience appointment booking](../task/config-walkup-excluded-booking-hours.md)**  
Using the **Appointment Booking** application, you can specify excluded appointment hours in the schedule for your Walk-up Experience location.
-   **[Activate and configure appointment booking reminders for Walk-up Experience](../task/activate-configure-appoint-reminders.md)**  
Configure scheduled appointment reminders for Walk-up Experience users. Reminders ensure users attend appointments in a timely manner or reschedule or cancel an appointment if they can no longer attend.

**Parent Topic:**[Walk-up Experience appointment booking administration](walkup-appointment-administration.md)

