---
title: Appointment booking components
description: The roles, properties, and tables for the appointment booking feature.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Components installed with additional plugins for Field Service Management, Field Service Management reference, Field Service Management]
---

# Appointment booking components

The roles, properties, and tables for the appointment booking feature.

The Appointment Booking plugin \(com.snc.appointment\_booking\) is activated automatically when you activate the Field Service Management plugin. A demo data plugin, Appointment Booking Demo Data \(com.snc.appointment\_booking\_demo\), is also available.

The Appointment Booking plugin \(com.snc.appointment\_booking\) is activated automatically when you activate the Field Service Management plugin.

This plugin activates the Appointment Booking Demo Data \(com.snc.appointment\_booking\_demo\) plugin which provides the demo data.

Appointment booking adds the Appointment Booking menu to the application navigator and the following modules:

-   **Appointment Booking Configuration**: Use this module to create an appointment booking configuration for an application and then configurations for each service within that application.
-   **Appointment Bookings**: Use this module to view a list of appointments that have been booked for services. This list includes the work orders associated with each appointment.

## Roles

Appointment booking adds the following roles.

<table id="table_iyg_cvj_jbb"><thead><tr><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Appointment booking admin\[sn\_apptmnt\_booking.appointment\_booking\_admin\]

</td><td>

Creates appointment booking configurations for services within an application.

</td></tr><tr><td>

Appointment booking manager\[sn\_apptmnt\_booking.appointment\_booking\_manager\]

</td><td>

Creates and updates appointment booking records.

</td></tr><tr><td>

Appointment booking user\[sn\_apptmnt\_booking.appointment\_booking\_user\]

</td><td>

Books appointments for services from the Customer or Consumer Service Portal. This user can also reschedule or cancel appointments and view appointment details.

</td></tr></tbody>
</table>## Properties

Appointment booking adds the following properties.

<table id="table_j15_yvj_jbb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_apptmnt\_booking.user\_max\_new\_appointments\_daily

</td><td>

The maximum number of appointments that a user can create daily. The upper limit is 100 appointments per day.-   **Type**: Integer
-   **Default value**: 100
-   **Location**: System Properties list

</td></tr><tr><td>

sn\_apptmnt\_booking.max\_appointments\_returned

</td><td>

The maximum number of appointment availability windows displayed in the Select Appointment window.-   **Type**: Integer
-   **Default value**: 100
-   **Location**: System Properties list

</td></tr><tr><td>

sn\_apptmnt\_booking.return\_unavailable\_slots

</td><td>

Disabling this property enables you to display only available slots in the appointment window for appointment booking.-   **Type**: True/False
-   **Default value**: true
-   **Location**: System Properties list

</td></tr><tr><td>

sn\_apptmnt\_booking.DisableLockingOnBRLevel

</td><td>

Allows you to specify tables where locking is managed differently to prevent double bookings when booking appointments. Enter a list of these tables, separated by commas, to disable lock validation at the business rule level.-   **Type**: String
-   **Default value**: \(blank\)
-   **Location**: System Properties list

</td></tr><tr><td>

sn\_apptmnt\_booking.DisableMaxApptLimitForUsersList

</td><td>

Stores a list of users \(sys\_ids\) who are allowed an unlimited number of appointments per day.-   **Type**: String
-   **Default value**: \(empty\)
-   **Location**: System Properties list

</td></tr><tr><td>

sn\_apptmnt\_booking.fetch\_next\_available\_slot

</td><td>

Toggle the flag to enable or disable fetching the next available slot on opening the new Appointment Booking modal.-   **Type**: True/False
-   **Default value**: false
-   **Location**: System Properties list

</td></tr><tr><td>

sn\_apptmnt\_booking.logging.verbosity

</td><td>

Control users logging for Appointment Booking.-   **Type**: Choice list
-   **Default value**: error
-   **Location**: System Properties list

</td></tr><tr><td>

sn\_apptmnt\_booking.SingleConcurrentLockAppointmentConfigs

</td><td>

List of tables where Appointment Booking only allows one lock per time slot. Multiple concurrent locks are not supported for these tables.-   **Type**: String
-   **Default value**: wm\_order,wm\_task
-   **Location**: System Properties list

</td></tr><tr><td>

sn\_apptmnt\_booking.use\_read\_replica\_from\_ui

</td><td>

Creates a read replica of the Appointment Bookings \(sn\_apptmnt\_booking\_appointment\_booking\) table when triggered from the UI.-   **Type**: True/False
-   **Default value**: true
-   **Location**: System Properties list

</td></tr><tr><td>

sn\_apptmnt\_booking.use\_task\_activity\_catalog

</td><td>

Enables the use of the column activity\_catalog created on task\_activity for querying \(filters the task activities for a work order task based on appointments\). ServiceNow recommends not to modify the value of the property as it affects performance of Appointment Booking.-   **Type**: True/False
-   **Default value**: true
-   **Location**: System Properties list

</td></tr></tbody>
</table>## Tables

Appointment booking adds the following tables.

<table id="table_crw_gwj_jbb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Appointment Booking Service Configuration\[sn\_apptmnt\_booking\_service\_config\]

</td><td>

Stores service configuration records for appointment booking.

</td></tr><tr><td>

Appointment Booking Configuration\[sn\_apptmnt\_booking\_config\]

</td><td>

Stores application configurations records for appointment booking.

</td></tr><tr><td>

Appointment Bookings\[sn\_apptmnt\_booking\_appointment\_booking\]

</td><td>

Stores records for all appointments, including booked, rescheduled, and canceled appointments.

</td></tr></tbody>
</table>**Parent Topic:**[Components installed with additional plugins for Field Service Management](components-inst-additional-plugin.md)

