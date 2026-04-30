---
title: Create an Appointment window configuration
description: An Appointment window configuration defines the daily schedule for appointments, including start and end times, slot duration, breaks, and slot repetition intervals.
locale: en-US
release: zurich
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [Appointment window configuration, Appointment schedule]
breadcrumb: [Create an Appointment schedule, Configure daily and advanced schedules, Configuring Appointment Booking, Additional scheduling configuration options, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Create an Appointment window configuration

An Appointment window configuration defines the daily schedule for appointments, including start and end times, slot duration, breaks, and slot repetition intervals.

## Before you begin

Role required: appointment\_booking\_admin

Ensure that the Advanced Appointment Booking plugin is active. For more information, see [Activate Advanced Appointment Booking](activate-adv-appt-booking.md).

## Procedure

1.  Navigate to **All** &gt; **Appointment Booking** &gt; **Appointment window configuration**.

2.  Click **New**.

3.  On the form, fill in the fields.

4.  |Field|Description|
|-----|-----------|
|Name|Descriptive name of the configuration, such as "Breakfix \[2hour\]" or "Install \[4hour\]".|
|Appointment Window|Duration of the appointment window.|
|Start time|Start time of the appointment window.|
|End time|End date of the appointment booking window.|
|Include break|Enable to schedule a consistent daily break period.|
|Break from|Start time of the break window. Only appears if **Include break** is enabled.|
|Break to|End time of the break window. Only appears if **Include break** is enabled.|
|Repeat slot every|How often the slot repeats.|

5.  Click **Submit**.


## What to do next

Both an appointment window configuration and a service configuration mapping are required to create an Appointment schedule. For more information on service configuration mappings, see [Create an Appointment service configuration mapping](create-appt-svc-config-mapping.md).

If a service configuration mapping already exists, see [Create an Appointment schedule](create-appt-sched.md).

