---
title: Create appointment booking service configuration rules
description: Configure appointment booking rules for a service configuration, for example, Point-of-Sale-Installation, to enable varying duration of appointments for this service.
locale: en-US
release: xanadu
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Configuring Appointment Booking, Additional scheduling configuration options, Setting up a Field Service scheduling method, Configuring Field Service Management, Field Service Management]
---

# Create appointment booking service configuration rules

Configure appointment booking rules for a service configuration, for example, Point-of-Sale-Installation, to enable varying duration of appointments for this service.

## Before you begin

Role required: admin

## About this task

Service Configuration Rules are used to define which advanced configuration applies for which specific use case of the service.

## Procedure

1.  Navigate to **All** &gt; **Appointment Booking** &gt; **Appointment Booking Configuration**.

2.  Select the desired configuration.

    -   To create appointment booking service configuration rules for work orders, select **Field Service Order Configuration**
    -   To create appointment booking service configuration rules for work order tasks, select **Field Service Task Configuration**
3.  In the Appointment Booking Service Configuration related list, select a service configuration to which you want to add rules.

4.  Select **Enable advanced configurations** check box if not already selected.

5.  In the Service Configuration Rules related list, click **New**.

6.  On the form, fill in the fields.

<table id="table_ydv_ywx_rtb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the service configuration rule.

</td></tr><tr><td>

Service configuration

</td><td>

The name of the service for which you are configuring rules. This field is automatically set to the name of the service configuration, for example, Point-of-Sale Installation.**Note:** The Point-of-Sale-Installation is available only for **Field Service Order Configuration**.

</td></tr><tr><td>

Task Table

</td><td>

The table where appointment booking rules are created for the selected service configuration. This field is automatically populated with the Work Order \[wm\_order\] or Work Order Task \[wm\_task\] table, based on the selected application configuration, to configure service rules.

</td></tr><tr><td>

Task Conditions

</td><td>

Apply conditions to help determine the best matched appointment slot for a service provided to the customer.When the conditions are met, this service configuration rule is applied, and the default configuration is overridden by the advanced configuration.

</td></tr><tr><td>

Lead time

</td><td>

Number of hours or days from the current time after which an appointment can be booked based on this service configuration rule. Define the lead time in hours or days. The default is four hours.

</td></tr><tr><td>

Ignore lead time on reschedule

</td><td>

This option skips the calculation of lead time mentioned beforehand when rescheduling an appointment.

</td></tr><tr><td>

Reschedule/Cancel by time

</td><td>

The number of hours or days prior to an appointment start time that are required for an appointment to be canceled or rescheduled. The default is 4 hours.**Note:** The **Cancel** button is not available within this number of hours.

</td></tr><tr><td>

Dedicated appointments per slot

</td><td>

An option to make it mandatory to include a certain number of appointments in each slot.

</td></tr><tr><td>

Active

</td><td>

Option to set the application service configuration rule.

</td></tr><tr><td>

Order

</td><td>

Order in which the service configuration rule must be executed. A rule with a lesser order is executed first.

</td></tr><tr><td>

Max bookable days in future

</td><td>

Number of days in advance of the current day for which an appointment can be booked for this service. The default is 14 days.

</td></tr><tr><td>

Appointments per window

</td><td>

Number of available appointments for each configured appointment time slot. This number determines the number of available appointments that are displayed on the Select Appointment window. Enter a number in this field if the assignment method for tasks is set to manually. If set to either using auto-assignment or using dynamic scheduling, this setting does not apply, unless a location is not provided. Then the configuration defaults to the number of appointments per window.

</td></tr></tbody>
</table>7.  Click **Submit**.


## Result

The service configuration rules are configured and provides varying duration of appointments for the service.

## What to do next

Create an appointment booking advanced configuration for this service configuration rule. For more information, see [Create appointment booking advanced configuration](appintment-booking-day-level-config.md).

**Parent Topic:**[Configuring Appointment Booking](../concept/appointment-booking-administer.md)

