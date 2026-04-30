---
title: Advanced appointment booking components
description: The roles, properties, and tables for the advanced appointment booking feature.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Appointment booking components, Components installed with additional plugins, Reference, Field Service Management]
---

# Advanced appointment booking components

The roles, properties, and tables for the advanced appointment booking feature.

This plugin activates the following plugins if they aren't already installed:

-   Appointment Booking \(com.snc.appointment\_booking\)
-   Resource Matching Engine \(com.snc.matching\_rule\)

## Tables

Appointment booking adds the following tables.

<table id="table_crw_gwj_jbb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Appointment Window Configuration\[sn\_apptmnt\_booking\_window\_config\]

</td><td>

Store configuration setting for appointment windows.

</td></tr><tr><td>

Appointment Window​\[sn\_apptmnt\_booking\_config\]

</td><td>

Defines appointment windows for bookings.

</td></tr><tr><td>

Bookable Window​\[sn\_apptmnt\_booking\_bookable\_window\]

</td><td>

Represents specific time slots available for booking.

</td></tr><tr><td>

Service Configuration Mapping​\[sn\_apptmnt\_booking\_config\_mapping\]

</td><td>

Configuration to map available services to territories or any conditions.​

</td></tr><tr><td>

Appointment Schedule​\[sn\_apptmnt\_booking\_schedule\]

</td><td>

Mapping the service configuration to appointment slots​.

</td></tr><tr><td>

Appointment Schedule Override​\[sn\_apptmnt\_booking\_schedule\_override\]

</td><td>

Stores override schedule changes. ​

</td></tr></tbody>
</table>**Parent Topic:**[Appointment booking components](appointment-booking-components.md)

