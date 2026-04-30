---
title: Create an Appointment service configuration mapping
description: An appointment service configuration mapping contains the service configuration, service configuration rule, and territory for use in an appointment schedule.
locale: en-US
release: zurich
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [Appointment service configuration mapping, Appointment schedule]
breadcrumb: [Create an Appointment schedule, Configure daily and advanced schedules, Configuring Appointment Booking, Additional scheduling configuration options, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Create an Appointment service configuration mapping

An appointment service configuration mapping contains the service configuration, service configuration rule, and territory for use in an appointment schedule.

## Before you begin

Role required: appointment\_booking\_admin

Ensure that the Advanced Appointment Booking plugin is active. For more information, see [Activate Advanced Appointment Booking](activate-adv-appt-booking.md).

Ensure you have already created a **Service Configuration**

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

The name of the service configuration rule to apply for this mapping.

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

Select the demand channel for the configuration. For more information, see [Create a demand channel](create-a-demand-channel.md). **Note:** Applies only if territory plugin is installed.

</td></tr></tbody>
</table>5.  Click **Submit**.


## What to do next

Both a service configuration mapping and an appointment window configuration are required to create an Appointment schedule. For more information on appointment window configurations, see [Create an Appointment window configuration](create-appt-window-config.md).

If a service configuration mapping already exists, see [Create an Appointment schedule](create-appt-sched.md).

