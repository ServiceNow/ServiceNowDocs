---
title: Create an Appointment Schedule Override
description: An appointment schedule override modifies default slot configurations for specific dates or scenarios, providing flexible appointment management.
locale: en-US
release: zurich
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure daily and advanced schedules, Configuring Appointment Booking, Additional scheduling configuration options, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Create an Appointment Schedule Override

An appointment schedule override modifies default slot configurations for specific dates or scenarios, providing flexible appointment management.

## Before you begin

Role required: appointment\_booking\_admin

Ensure that the Advanced Appointment Booking plugin is active. For more information, see [Activate Advanced Appointment Booking](activate-adv-appt-booking.md).

Ensure you have already created an **Appointment Window** and a **Service configuration mapping**.

## Procedure

1.  Navigate to **All** &gt; **Appointment Booking** &gt; **Appointment service mapping**.

2.  Select an existing Appointment service configuration mapping.

3.  Select the **Appointment Schedule Override**

4.  Select **New**.

5.  On the form, fill in the fields.

6.  |Field|Description|
|-----|-----------|
|Service configuration mapping|Name of the service configuration mapping, such as "POSI + SF" or "POSI".|
|Date|The appointment date that will be overridden.|
|Appointment slot|The appointment slot that will be overridden.|
|Number of appointments|The number of appointments that will be made available at the override date and slot.|

7.  Click **Submit**.


## Result

By adding an override, the specific slot and date will have available slots regardless of what was defined in the appointment schedule.

