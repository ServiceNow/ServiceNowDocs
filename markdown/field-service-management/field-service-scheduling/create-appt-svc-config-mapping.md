---
title: Create an Appointment service configuration mapping
description: An appointment service configuration mapping contains the service configuration, service configuration rule, and territory for use in an appointment schedule.
locale: en-US
release: australia
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Appointment service configuration mapping, Appointment schedule]
breadcrumb: [Configure Advanced Appointment Booking, Configuring Appointment Booking, Additional scheduling configuration options, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Create an Appointment service configuration mapping

An appointment service configuration mapping contains the service configuration, service configuration rule, and territory for use in an appointment schedule.

## Before you begin

Role required: appointment\_booking\_admin

Ensure that the Advanced Appointment Booking plugin is active. For more information, see [Activate Advanced Appointment Booking](activate-adv-appt-booking.md).

Ensure you have already created a **Service Configuration**. For more information see, [Create or modify service configuration for Appointment Booking](appt-booking-create-service-config.md).

## About this task

Through service configuration mapping, you can define the number of appointment slots, appointment window duration, and have flexible holiday schedules for a service or demand channels within a territory. You can configure multiple service configuration mappings for a service in a territory based on your organizational requirements.

For example, consider the service Point-of-Sale Installation. You can configure different holiday schedules and appointment slots for San Jose and San Francisco territories through service configuration mapping.

## Procedure

1.  Navigate to **All** &gt; **Appointment Booking** &gt; **Appointment service mapping**.

2.  Click **New**.

3.  On the form, fill in the fields.

4.  <table id="table_nc3_s2r_zfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Descriptive name of the service configuration mapping, such as "POSI + SF" or "POSI".

</td></tr><tr><td>

Service configuration

</td><td>

The name of the service for which you are configuring the mapping, such as "Point-of-Sale Installation".

</td></tr><tr><td>

Service configuration rule

</td><td>

The name of the service configuration rule to apply for this mapping. For more information, see [Create service configuration rules for a service configuration](create-appt-booking-service-config-rules.md).

</td></tr><tr><td>

Territory

</td><td>

The territory where this configuration applies.

</td></tr><tr><td>

Order

</td><td>

Value that determines the priority or sequence for the configuration. The lower the value, the higher the priority.

</td></tr><tr><td>

Dedicated appointments per slot

</td><td>

Option to have dedicated appointments per slot. For example, if two slots overlap \(8:00-10:00 slot and 8:00-11:00 slot\), booking one slot will not affect the availability of the other slot.

</td></tr><tr><td>

Demand channel

</td><td>

The demand channel for which the configuration applies. For more information, see [Create a demand channel](create-a-demand-channel.md). **Note:** Applies only if territory plugin is installed.

</td></tr><tr><td>

Holiday Schedule

</td><td>

The schedule that defines which days are considered as holidays and excluded from appointment availability for the territory.**Note:** Administrators can configure the form layout to add **Holiday Schedule** to the form.

</td></tr></tbody>
</table>5.  Click **Submit**.


## What to do next

Both a service configuration mapping and an appointment window configuration are required to create an Appointment schedule. For more information on appointment window configurations, see [Create an Appointment window configuration](create-appt-window-config.md).

If a service configuration mapping already exists, see [Create an Appointment schedule](create-appt-sched.md).

