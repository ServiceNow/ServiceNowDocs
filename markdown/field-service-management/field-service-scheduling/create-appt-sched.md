---
title: Create an Appointment schedule
description: An appointment schedule represents available slots as defined by its appointment window and service mapping configurations. Appointment schedules can be overridden for specific dates or slots to allow custom availability or capacity.
locale: en-US
release: zurich
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [Appointment schedule]
breadcrumb: [Configure daily and advanced schedules, Configuring Appointment Booking, Additional scheduling configuration options, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Create an Appointment schedule

An appointment schedule represents available slots as defined by its appointment window and service mapping configurations. Appointment schedules can be overridden for specific dates or slots to allow custom availability or capacity.

## Before you begin

Role required: appointment\_booking\_admin

Ensure that the Advanced Appointment Booking plugin is active. For more information, see [Activate Advanced Appointment Booking](activate-adv-appt-booking.md).

Ensure you have already created an **Appointment Window** and a **Service configuration mapping**.

## About this task

An appointment schedule defines available time slots based on its configuration. You can also create an appointment schedule override to customize availability for specific dates or time slots. For more information on overrides, see [Create an Appointment Schedule Override](create-appt-sched-override.md).

## Procedure

1.  Navigate to **All** &gt; **Appointment Booking** &gt; **Appointment schedule**.

2.  Click **New**.

3.  On the form, fill in the fields.

4.  |Field|Description|
|-----|-----------|
|Service configuration mapping|The service configuration mapping that contains the type of service and territory for the schedule. For more information, see [Create an Appointment service configuration mapping](create-appt-svc-config-mapping.md).|
|Appointment window configuration|The appointment window configuration that contains the duration, break, and slot intervals. For more information, see [Create an Appointment window configuration](create-appt-window-config.md).|
|Start date|Start date of the appointment schedule.|
|End date|End date of the appointment schedule.|
|Order|Value that determines the priority or sequence for the configuration. The lesser the value, the greater the priority.|
|Number of appointments|Number of available appointments for each configured appointment time slot. This number determines the number of available appointments that are displayed on the Select Appointment window.|
|Bookable days|The days of the week for which appointments can be booked. The default is Monday through Friday.|

5.  Click **Submit**.


## What to do next

The appointment schedule can be applied to a new or existing service configuration. For more information, see [Create or modify service configuration for Appointment Booking](appt-booking-create-service-config.md).

Appointment schedules can also be overridden to accommodate specific date and slot needs. For more information on overrides, see [Create an Appointment Schedule Override](create-appt-sched-override.md).

