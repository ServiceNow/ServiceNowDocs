---
title: Create or modify service configuration for Appointment Booking
description: Service-level appointment booking enables customers to easily schedule specific services by customizing appointment availability, lead times, notifications, and booking rules.
locale: en-US
release: yokohama
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Configuring Appointment Booking, Additional scheduling configuration options, Setting up a Field Service scheduling method, Configuring Field Service Management, Field Service Management]
---

# Create or modify service configuration for Appointment Booking

Service-level appointment booking enables customers to easily schedule specific services by customizing appointment availability, lead times, notifications, and booking rules.

## Before you begin

Role required: appointment\_booking\_admin, admin

Verify you have an active application configuration \(**Field Service Order Configuration or Field Service Task Configuration**\) set up. You can create service-level configuration within an application-level configuration.

## About this task

To use the appointment booking feature, administrators must create a configuration for each service that is available to customers. In the service configuration, administrators can select a schedule from the **Schedules** list and set it as **Excluded** to exclude it from appointment availability.

## Procedure

1.  Navigate to **All** &gt; **Appointment Booking** &gt; **Appointment Booking Configuration**.

2.  Select the desired configuration.

    -   To configure appointment booking service for work orders, select **Field Service Order Configuration**
    -   To configure appointment booking service for work order tasks, select **Field Service Task Configuration**
3.  In the Appointment Booking Service Configuration related list, click **New**.

4.  On the form, fill in the following fields as needed.

<table id="table_vst_5nf_2r"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enable advanced configuration

</td><td>

Option to configure different schedule on a day level when booking appointments.

</td></tr><tr><td>

Active

</td><td>

Activates appointment booking for the service. **Note:** If deactivated, customers cannot schedule appointments for the service but can still create work orders.

</td></tr><tr><td>

Ignore Default Notifications

</td><td>

Sends notifications to customers.-   FALSE \(default\): Notifications are sent to the customer whenever an appointment is scheduled, rescheduled, or canceled.
-   TRUE: No notifications are sent.


</td></tr><tr><td class="sub-head" colspan="2">

General Information

</td></tr><tr><td>

Name

</td><td>

The name of the service configuration.

</td></tr><tr><td>

Configuration

</td><td>

The name of the appointment booking configuration to which this service belongs.

</td></tr><tr><td>

Availability table

</td><td>

The table that is used to calculate appointment availability. The default is the Work Order Task \[wm\_task\] table.

</td></tr><tr><td>

Holiday Schedule

</td><td>

The holiday schedule to use when determining availability. Appointment booking evaluates the holiday schedule when determining the number of available appointments and excludes any day in the schedule that is set to **Exclude**. Click the lookup icon and select a schedule from the Schedules list. **Note:** Holiday schedules are useful when the assignment method for tasks is set to **manually**, which does not consider agent schedules.

</td></tr><tr><td class="sub-head" colspan="2">

Catalog Information

</td></tr><tr><td>

Catalog Item

</td><td>

Select the catalog item \(service\) for which this configuration applies.**Note:** The catalog item must exist in the service catalog.

Before configuring appointment booking with work orders, ensure you create a work order template. Similarly, if you are using appointment booking with work order tasks, create a work order task template first.

</td></tr><tr><td>

Location

</td><td>

Field from the record producer that specifies the appointment location. Ensure that this field not left blank and is filled with the appropriate location to avoid issues when rescheduling an appointment.

</td></tr><tr><td>

Appointment is mandatory

</td><td>

Enable this check box if it is mandatory that a customer create an appointment when requesting this service. -   If enabled, the **Appointment** field appears on the record producer and the user must select an available appointment on the [Select Appointment window](../reference/appt-booking-select-appt-window.md) before submitting the service request.
-   If disabled, the user can submit the service request without selecting an appointment.


</td></tr><tr><td>

User contact

</td><td>

The field on the record provider that determines the individual for whom the appointment is being created. This is a reference field that looks for a sys\_user variable and sets variable on the record producer, for example, **Contact**.Ensure that this field not left blank and is filled with the appropriate value to avoid issues when rescheduling an appointment.

</td></tr><tr><td>

Timezone

</td><td>

Appointment timezone \(user contact or task location timezone\).

</td></tr><tr><td class="sub-head" colspan="2">

Booking

</td></tr><tr><td>

Appointments per window

</td><td>

Number of available appointments per time slot. Applies primarily for **manual assignment**. This setting does not apply for **auto-assignment or dynamic scheduling**, unless a location is not provided. Then, the configuration defaults to the number of appointments per window.

</td></tr><tr><td>

Lead time

</td><td>

Minimum time in hours or days required in advance for customers to book an appointment. Default time is 4 hours.

</td></tr><tr><td>

Future bookable max days

</td><td>

The number of days in advance of the current day for which an appointment can be booked for this service. The default is 14 days.

</td></tr><tr><td>

Reschedule / Cancel by time

</td><td>

The number of hours or days prior to an appointment when cancellation or rescheduling is permitted. The **Cancel** button is not available if a user attempts to cancel or reschedule an appointment within this time. The default is 4 hours.

</td></tr><tr><td>

Ignore lead time on reschedule

</td><td>

Select to skip lead-time validation when rescheduling appointments.

</td></tr><tr><td>

Consider holidays for lead time calculation

</td><td>

Select to exclude holidays to calculate booking lead times when displaying available appointment booking slots. For example, if a holiday occurs during the lead time calculation period, the system skips the holiday and calculates the lead time using the next available working day.

</td></tr><tr><td class="sub-head" colspan="2">

Appointments

</td></tr><tr><td>

Appointment window

</td><td>

The duration of the appointment window. **Note:** Allow enough time for the work to be started and completed within this window.

</td></tr><tr><td>

Use slot end time as

</td><td>

Select whether the agent should arrive by or complete the job before the window end time.

</td></tr><tr><td>

Work duration

</td><td>

Estimated time needed to complete all tasks created by the record producer. This duration is set for a task when it is created. Work duration is used to determine appointment availability.

</td></tr><tr><td>

Travel duration \(round trip\)

</td><td>

Average round-trip travel time to the appointment location. Travel duration is used to determine availability.

</td></tr><tr><td class="sub-head" colspan="2">

Daily Schedule

</td></tr><tr><td>

Bookable days

</td><td>

The days of the week for which appointments can be booked. The default is Monday through Friday.

</td></tr><tr><td>

Daily start time

</td><td>

The start of the work day and the earliest start time for an appointment window.

</td></tr><tr><td>

Daily end time

</td><td>

The end of the work day and the latest end time for an appointment window.

</td></tr><tr><td>

Include daily break

</td><td>

Enable this check box to schedule a break for each bookable day, then select the break start and end times. Can define one break which applies to all days.

</td></tr><tr><td>

Appointment booking preview

</td><td>

Provides a preview of the appointment windows and times based on the selected start and end times, break time, and appointment window.

</td></tr><tr><td class="sub-head" colspan="2">

Recommendation Configuration

</td></tr><tr><td>

Maximum slots to recommend

</td><td>

The maximum number of recommended slots.This field is available only if the Advanced Appointment Booking \(com.snc.advanced\_appointment\_booking\) plugin is activated.

</td></tr><tr><td>

Recommendation score

</td><td>

Indicates the minimum score to recommend a slot. Enter a value between 0 and 1.This field is available only if the Advanced Appointment Booking \(com.snc.advanced\_appointment\_booking\) plugin is activated.

</td></tr></tbody>
</table>5.  Click **Submit**.


## Result

The service-level appointment booking configuration is set up or updated. Users can book appointments based on these customized settings.

## What to do next

For further customization, you can create **service configuration rules** to define specific booking conditions or exceptions for individual locations or scenarios. For more information, see [Create service configuration rules for a service configuration](create-appt-booking-service-config-rules.md).

