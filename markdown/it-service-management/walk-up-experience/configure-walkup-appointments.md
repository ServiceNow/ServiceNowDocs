---
title: Create or modify a Walk-up Experience appointment booking service configuration
description: Create or modify appointment booking configurations for Walk-up Experience services. A service is defined as the actual physical location of a walk-up queue. The information stored in the Walk-up Experience application configuration applies to all services, or queue locations, within the application.
locale: en-US
release: zurich
product: Walk-Up Experience
classification: walk-up-experience
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Configure Walk-up Experience appointment booking, Walk-up Experience appointment booking administration, Book Walk-up Experience appointments, Configure, Walk-up Experience, IT Service Management]
---

# Create or modify a Walk-up Experience appointment booking service configuration

Create or modify appointment booking configurations for Walk-up Experience services. A service is defined as the actual physical location of a walk-up queue. The information stored in the Walk-up Experience application configuration applies to all services, or queue locations, within the application.

## Before you begin

Role required: appointment\_booking\_admin or admin

## About this task

To use the appointment booking feature, administrators must create a configuration for each service, or queue location, that is available to walk-up customers. Service configurations are created within the **Walk-up Experience** application configuration, as part of the **Appointment Booking** application.

## Procedure

1.  Navigate to **All** &gt; **Appointment Booking** &gt; **Appointment Booking Configuration**.

2.  Select **Walk-up Experience**.

3.  Create or modify Appointment Booking Configuration.

    -   To create configuration for appointment booking, select **New.**
    -   To modify an existing configuration, select the configuration from the list.
4.  On the form, fill in the fields.

<table id="table_vst_5nf_2r"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

Option to enable appointment booking for the service. **Note:** If inactive, customers cannot schedule appointments for the service but can still create work orders.

</td></tr><tr><td>

Enable day level configuration

</td><td>

Option to configure the schedule at a day level. For more information, see [Configure day-level appointment booking](configure-walkup-appointment-booking-day-level.md).

</td></tr><tr><td class="sub-head" colspan="2">

General Information

</td></tr><tr><td>

Name

</td><td>

Name of the service configuration.

</td></tr><tr><td>

Configuration

</td><td>

Name of the appointment booking configuration to which this service belongs.

</td></tr><tr><td>

Availability table

</td><td>

Table used to calculate appointment availability. For Walk-up Experience, choose Walk-up Appointment \[wu\_appointment\].

</td></tr><tr><td>

Holiday Schedule

</td><td>

Holiday schedule to use when determining availability. Appointment booking evaluates the holiday schedule when determining the number of available appointments and excludes any day in the schedule that is set to **Exclude**. Select the lookup icon and select a schedule from the Schedules list. **Note:** Holiday schedules are useful when the assignment method for tasks is set to **manually**, which does not consider agent schedules.

</td></tr><tr><td class="sub-head" colspan="2">

Catalog Information

</td></tr><tr><td>

Catalog item

</td><td>

The service in the service catalog for which this appointment booking configuration is being created. The catalog item must exist in the service catalog. Select the lookup icon and select the associated service from the Record Producers list. You must create a record producer for each walk-up service location. Refer to [Create a record producer to capture Walk-up Experience appointment records](create-rp-walkup-appointment.md).

 If you’re using appointment booking with work orders, create a work order template before you configure appointment booking.

</td></tr><tr><td>

Location

</td><td>

The field on the record provider that determines the appointment location. **Note:** Ensure the **Location** field on both this form and the Walk-up Location Queue \(wu\_location\_queue\) form are configured in alignment. Walk-up Experience contains the *location* reference variable, which is a Location \(cmn\_location\) record. Selecting **Location** from the search list ![search list icon](../../../common/image/List_SearchIcon.png) icon ensures that you’re aligning with the same time zone as the walk-up location you are configuring for. When you select **Location**, the online appointment scheduling calendar displays in the requester time zone. If this field is kept empty or if the requester preference for the instance is not configured to have an associated time zone, the appointment scheduling calendar defaults to display in the requester time zone.

If a requester in Europe has User preferences for **Time zone** configured for **Europe/Brussels** and the Appointment Booking Configuration for the **Location** field is set to a cmn\_location with the time zone **US/Pacific**, then the appointment scheduling calendar will display in the US/Pacific time zone.

When a requester creates an appointment, the system defaults to use the schedule associated with the Walk-up Location Queue \(wu\_location\_queue\), regardless of the **Location** field value of this record producer.

</td></tr><tr><td>

Timezone

</td><td>

Time zone used for the location. Select **Appointment location** from the drop-down list.

</td></tr><tr><td>

Appointment is mandatory

</td><td>

Option for enabling the feature to make it mandatory for a requester to create an appointment when requesting this service. -   If selected, the **Appointment** field appears on the record producer, and the requester selects an available appointment before submitting the service request.
-   If not selected, the requester can submit the service request without selecting an appointment.


</td></tr><tr><td>

User contact

</td><td>

The field on the record producer that determines who the appointment is being created for. Set this field to **Contact**. This is a reference field that looks for a sys\_user variable on the record producer.

</td></tr><tr><td class="sub-head" colspan="2">

Booking

</td></tr><tr><td>

Appointments per window

</td><td>

Number of available appointments for each configured appointment time slot. This number determines the number of available appointments that are displayed on the Select Appointment window. Enter a number in this field if the assignment method for tasks is set to **manually**. If set to either **using auto-assignment** or **using dynamic scheduling**, this setting does not apply, unless a location is not provided. Then the configuration defaults to the number of appointments per window.

</td></tr><tr><td>

Lead time

</td><td>

Number of hours or days from the current time after which an appointment can be booked for this service. Define the lead time in hours or days. The default is four hours.

</td></tr><tr><td>

Future bookable max days

</td><td>

Number of days in advance of the current day for which an appointment can be booked for this service. The default is 14 days.

</td></tr><tr><td>

Reschedule / Cancel by time

</td><td>

Number of hours or days prior to an appointment start time that are required for an appointment to be canceled or rescheduled. If a requester attempts to cancel or reschedule an appointment within this number of hours, the **Cancel** button is not available. Define the time in hours or days. The default is four hours.

</td></tr><tr><td class="sub-head" colspan="2">

Appointments

</td></tr><tr><td>

Appointment window

</td><td>

Duration of the appointment window. **Note:** Allow enough time for the work to be started and completed within this window.

</td></tr><tr><td>

Work duration

</td><td>

Time required to complete all tasks created by the record producer. This duration is set for a task when it is created. Used to determine availability. The default is one hour.

</td></tr><tr><td>

Travel duration \(round trip\)

</td><td>

Estimated value of the average travel time required \(round trip\) for the agent performing the task. Set the value to 0 because the work is performed on site and travel time is not needed.

</td></tr><tr><td class="sub-head" colspan="2">

Daily Schedule

</td></tr><tr><td>

Bookable days

</td><td>

Days of the week for which appointments can be booked. The default is Monday through Friday. Bookable days should reflect the appointment schedule. **Note:** Appointment schedules are separate from the walk-up queue location schedule but should be the same days and hours as the walk-up queue location schedule.

</td></tr><tr><td>

Daily start time

</td><td>

Start of the work day and the earliest start time for an appointment window. The default is 9:00.

</td></tr><tr><td>

Daily end time

</td><td>

End of the work day and the latest end time for an appointment window. The default is 18:00 PM.

</td></tr><tr><td>

Include daily break

</td><td>

Option to schedule a break for each bookable day, then select the break start and end times. You can define one break which applies to all days.

</td></tr><tr><td>

Appointment booking preview

</td><td>

Option to provide a preview of the appointment windows and times based on the selected start and end times, break time, and appointment window.

</td></tr></tbody>
</table>5.  Select **Submit**.


-   **[Configure day-level appointment booking](configure-walkup-appointment-booking-day-level.md)**  
Create or modify different schedules at a day level when booking appointments for a service. The appointments can be scheduled for different slots such as morning, afternoon, and evening.

**Parent Topic:**[Configure Walk-up Experience appointment booking](../concept/walkup-appointment-booking-config.md)

