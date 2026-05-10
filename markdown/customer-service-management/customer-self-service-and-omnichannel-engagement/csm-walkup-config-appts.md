---
title: Create a Walk-up Experience appointment booking configuration for a service
description: Create or modify appointment booking configurations for Walk-up Experience services. A service is defined as the actual physical location of a walk-up queue. The information stored in the Walk-up Experience application configuration applies to all services,or queue locations, within the application.
locale: en-US
release: australia
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Appointment booking configuration, Walk-up Experience appointment booking, Walk-up Experience for Customer Service Management, Set up self-service, Configure, Customer Service Management]
---

# Create a Walk-up Experience appointment booking configuration for a service

Create or modify appointment booking configurations for Walk-up Experience services. A service is defined as the actual physical location of a walk-up queue. The information stored in the Walk-up Experience application configuration applies to all services,or queue locations, within the application.

## Before you begin

Role required: sn\_apptmnt\_booking.appointment\_booking\_admin

## About this task

To use the appointment booking feature, administrators must create a configuration for each service, or queue location, that is available to walk-up customers. Service configurations are created within the **Walk-up Experience** application configuration, as part of the **Appointment Booking** application.

## Procedure

1.  Navigate to **All** &gt; **Appointment Booking** &gt; **Appointment Booking Configuration**.

2.  Click **Walk-up Experience**.

3.  In the Appointment Booking Service Configuration related list, click **New** to create a new service configuration.

    Alternatively, you can click an existing service configuration to modify data.

4.  In the Appointment Booking Service Configuration form, fill in the following fields as needed.

<table id="table_vst_5nf_2r"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

Activates appointment booking for the service. **Note:** If deactivated, customers cannot schedule appointments for the service but can still create work orders.

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

The table that is used to calculate appointment availability. For Walk-up Experience, choose Walk-up Appointment \[wu\_appointment\].

</td></tr><tr><td>

Holiday Schedule

</td><td>

The holiday schedule to use when determining availability. Appointment booking evaluates the holiday schedule when determining the number of available appointments and excludes any day in the schedule that is set to **Exclude**. Click the lookup icon and select a schedule from the Schedules list. **Note:** Holiday schedules are useful when the assignment method for tasks is set to **manually**, which does not consider agent schedules.

</td></tr><tr><td class="sub-head" colspan="2">

Catalog Information

</td></tr><tr><td>

Catalog Item

</td><td>

The service in the service catalog for which this appointment booking configuration is being created. Click the lookup icon and select a service from the Record Producers list.

**Note:** The catalog item must exist in the service catalog.

 If you are using appointment booking with work orders, create a work order template before you configure appointment booking.

</td></tr><tr><td>

Location

</td><td>

The field on the record provider that determines the appointment location.

</td></tr><tr><td>

Appointment is mandatory

</td><td>

Enable this check box if it is mandatory that a customer create an appointment when requesting this service. -   If enabled, the **Appointment** field appears on the record producer and the user must select an available appointment on the [Select Appointment window](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/appointment-booking/appt-booking-select-appt-window.md) before submitting the service request.
-   If disabled, the user can submit the service request without selecting an appointment.


</td></tr><tr><td>

User contact

</td><td>

The field on the record provider that determines who the appointment is being created for. This is a reference field that looks for a sys\_user variable on the record producer, for example, **Contact**.

</td></tr><tr><td>

Timezone

</td><td>

The appointment window based on the **Timezone** field specified in the user contact record or the location where the appointment for the task is scheduled.

</td></tr><tr><td class="sub-head" colspan="2">

Booking

</td></tr><tr><td>

Appointments per window

</td><td>

The number of available appointments for each configured appointment time slot. This number determines the number of available appointments that are displayed on the Select Appointment window. Enter a number in this field if the assignment method for tasks is set to **manually**. If set to either **using auto-assignment** or **using dynamic scheduling**, this setting does not apply, unless a location is not provided. Then the configuration defaults to the number of appointments per window.

</td></tr><tr><td>

Lead time

</td><td>

The number of hours or days from the current time after which an appointment can be booked for this service. Define the lead time in hours or days. The default is 4 hours.

</td></tr><tr><td>

Future bookable max days

</td><td>

The number of days in advance of the current day for which an appointment can be booked for this service. The default is 14 days.

</td></tr><tr><td>

Reschedule / Cancel by time

</td><td>

The number of hours or days prior to an appointment start time that are required for an appointment to be canceled or rescheduled. If a user attempts to cancel or reschedule an appointment within this number of hours, the **Cancel** button is not available. Define the time in hours or days. The default is 4 hours.

</td></tr><tr><td class="sub-head" colspan="2">

Appointments

</td></tr><tr><td>

Appointment window

</td><td>

The length or duration of the appointment window. **Note:** Allow enough time for the work to be started and completed within this window.

</td></tr><tr><td>

Work duration

</td><td>

The amount of time required to complete all tasks created by the record producer. This duration is set for a task when it is created. Used to determine availability. The default is 1 hour.

</td></tr><tr><td>

Travel duration \(round trip\)

</td><td>

An estimated value of the average travel time required \(round trip\) for the agent performing the task. Set the value to 0 since the work is performed onsite and travel time is not needed.

</td></tr><tr><td class="sub-head" colspan="2">

Daily Schedule

</td></tr><tr><td>

Bookable days

</td><td>

The days of the week for which appointments can be booked. The default is Monday through Friday. Bookable days should reflect the appointment schedule. **Note:** Appointment schedules are separate from the walk-up queue location schedule but should be the same days and hours as the walk-up queue location schedule.

</td></tr><tr><td>

Daily start time

</td><td>

The start of the work day and the earliest start time for an appointment window. The default is 9:00.

</td></tr><tr><td>

Daily end time

</td><td>

The end of the work day and the latest end time for an appointment window. The default is 18:00 PM.

</td></tr><tr><td>

Include daily break

</td><td>

Enable this check box to schedule a break for each bookable day, then select the break start and end times. Can define one break which applies to all days.

</td></tr><tr><td>

Appointment booking preview

</td><td>

Provides a preview of the appointment windows and times based on the selected start and end times, break time, and appointment window.

</td></tr></tbody>
</table>5.  Click **Submit**.


