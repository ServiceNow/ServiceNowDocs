---
title: Create an Appointment schedule
description: An appointment schedule represents available slots as defined by its appointment window and service mapping configurations. Appointment schedules can be overridden for specific dates or slots to allow custom availability or capacity.
locale: en-US
release: australia
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Appointment schedule]
breadcrumb: [Configure Advanced Appointment Booking, Configuring Appointment Booking, Additional scheduling configuration options, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Create an Appointment schedule

An appointment schedule represents available slots as defined by its appointment window and service mapping configurations. Appointment schedules can be overridden for specific dates or slots to allow custom availability or capacity.

## Before you begin

Role required: appointment\_booking\_admin

Ensure that the Advanced Appointment Booking plugin is active. For more information, see [Activate Advanced Appointment Booking](activate-adv-appt-booking.md).

Ensure you have already created an **Appointment Window** and a **Service configuration mapping**. To create an appointment window and service configuration mapping see [Create an Appointment window configuration](create-appt-window-config.md) and [Create an Appointment service configuration mapping](create-appt-svc-config-mapping.md).

## About this task

An appointment schedule defines available time slots based on its configuration. With appointment schedules, you can configure advanced capabilities like a combination of appointment slots of different durations for a specific day, or adjust the number of appointments for a particular slot, or define a holiday schedule for a specific day.

For example, for a specific day, you can configure one slot of 3 hours duration, two slots of 2 hours duration and 4 slots for 1 hour duration.

For a service if demand is greater between 9:00 AM and 10:00 AM, Appointment Schedule lets you set more bookable appointments during that time, and fewer for other time slots.

You can also create an appointment schedule override to customize availability for specific dates or time slots. For more information on overrides, see [Create an Appointment Schedule Override](create-appt-sched-override.md).

You can optionally define work and travel durations in a schedule. When **Use durations from the schedule** is enabled, these durations are used to calculate appointment availability and will override the default work and travel durations set in the service configuration.

## Procedure

1.  Navigate to **All** &gt; **Appointment Booking** &gt; **Appointment schedule**.

2.  Click **New**.

3.  On the form, fill in the fields.

4.  <table id="table_nc3_s2r_zfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Service configuration mapping

</td><td>

The service configuration mapping that contains the type of service and territory for the schedule. For more information, see [Create an Appointment service configuration mapping](create-appt-svc-config-mapping.md).

</td></tr><tr><td>

Appointment window configuration

</td><td>

The appointment window configuration that contains the duration, break, and slot intervals. For more information, see [Create an Appointment window configuration](create-appt-window-config.md).

</td></tr><tr><td>

Start date

</td><td>

Start date of the appointment schedule.

</td></tr><tr><td>

End date

</td><td>

End date of the appointment schedule.If you don't specify the start and end date, the appointment schedule will apply for all the future days from the current date until you specify an end date.

</td></tr><tr><td>

Order

</td><td>

Value that determines the priority or sequence for the configuration. The lesser the value, the greater the priority.

</td></tr><tr><td>

Number of appointments

</td><td>

Number of available appointments for each configured appointment time slot. This number determines the number of available appointments that are displayed on the Select Appointment window.

</td></tr><tr><td>

Bookable days

</td><td>

The days of the week for which appointments can be booked. The default is Monday through Friday.

</td></tr><tr><td>

Use durations from schedule

</td><td>

When enabled, the work and travel durations are considered from the schedule and the duration defined in the service configuration is overridden.**Note:** Administrators can configure to add the field to the form.

</td></tr><tr><td>

Work duration

</td><td>

Estimated time needed to complete all tasks.

</td></tr><tr><td>

Travel duration

</td><td>

Average round-trip travel time to the appointment location. Travel duration is used to determine availability.

</td></tr></tbody>
</table>5.  Click **Submit**.


## What to do next

The appointment schedule can be applied to a new or existing service configuration. For more information, see [Create or modify service configuration for Appointment Booking](appt-booking-create-service-config.md).

Appointment schedules can also be overridden to accommodate specific date and slot needs. For more information on overrides, see [Create an Appointment Schedule Override](create-appt-sched-override.md).

