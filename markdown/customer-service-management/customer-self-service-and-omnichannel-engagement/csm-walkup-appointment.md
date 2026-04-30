---
title: Configure appointment booking
description: Create or modify appointment booking configurations for Walk-up Experience services. A service is defined as the actual physical location of a walk-up queue. The information stored in the Walk-up Experience application configuration applies to all services or queue locations within the application.
locale: en-US
release: zurich
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Walk-up Experience appointment booking, Configure Walk-up Experience for Customer Service Management, Set up self-service, Configure, Customer Service Management]
---

# Configure appointment booking

Create or modify appointment booking configurations for Walk-up Experience services. A service is defined as the actual physical location of a walk-up queue. The information stored in the Walk-up Experience application configuration applies to all services or queue locations within the application.

## Before you begin

Role required: admin or sn\_csm\_walkup.walkup\_admin

## Procedure

1.  Navigate to **All** &gt; **CSM Walk-up Experience** &gt; **Administration** &gt; **Appointment Configurations**.

2.  Click **New** to create a new service configuration.

    Alternatively, you can click an existing service configuration to modify data.

3.  In the Appointment Booking Service Configuration form, fill in the following fields as needed.

<table id="table_ykq_ttq_xlb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the service configuration.

</td></tr><tr><td>

Active

</td><td>

Activates appointment booking for the service. **Note:** If deactivated, customers cannot schedule appointments for the service but can still create work orders.

</td></tr><tr><td class="sub-head" colspan="2">

General Information

</td></tr><tr><td>

Configuration

</td><td>

The name of the appointment booking configuration to which this service belongs.

</td></tr><tr><td>

Availability table

</td><td>

The table calculates appointment availability. For Walk-up Experience, choose Walk-up Appointment \[wu\_appointment\].

</td></tr><tr><td>

Enable advanced configurations

</td><td>

 

</td></tr><tr><td>

Holiday Schedule

</td><td>

The holiday schedule to use when determining availability. Appointment booking evaluates the holiday schedule when determining the number of available appointments and excludes any day in the schedule that is set to **Exclude**. Click the lookup icon and select a schedule from the Schedules list. **Note:** Holiday schedules are useful when you set the assignment method for tasks to **manually**, which does not consider agent schedules.

</td></tr><tr><td class="sub-head" colspan="2">

Catalog Information

</td></tr><tr><td>

Catalog item

</td><td>

The service in the service catalog for which you are creating this appointment booking configuration. Click the lookup icon and select the associated service from the Record Producers list.

 You must create a record producer for each walk-up service location.

**Note:** The catalog item must exist in the service catalog.

 If you are using appointment booking with work orders, create a work order template before you configure appointment booking.

</td></tr><tr><td>

Location

</td><td>

The field on the record provider that determines the appointment location. **Note:** Ensure the **Location** field on both this form and the Walk-up Location Queue \(wu\_location\_queue\) form are configured in alignment. Walk-up Experience contains the *location* reference variable, which is a Location \(cmn\_location\) record. Selecting **Location** from the search list ![search list icon](../../../common/image/List_SearchIcon.png) icon ensures you are aligning with the same time zone as the walk-up location you are configuring for. When you select **Location**, the online appointment scheduling calendar displays in the user time zone. If you leave this field empty or if you have not configured the user preference for the instance to have an associated time zone, the appointment scheduling calendar defaults to display in the user time zone.

If a user in Europe has User preferences for **Time zone** configured for **Europe/Brussels** and the Appointment Booking Configuration for the **Location** field is set to a cmn\_location with the time zone **US/Pacific**, then the appointment scheduling calendar displays in the US/Pacific time zone.

When a user creates an appointment, the system defaults to use the schedule associated with the Walk-up Location Queue \(wu\_location\_queue\), regardless of the **Location** field value of this record producer.

</td></tr><tr><td>

Appointment is mandatory

</td><td>

Enable this check box if it is required for a customer to create an appointment when requesting this service. -   If enabled, the **Appointment** field appears on the record producer and the user must select an available appointment before submitting the service request.
-   If disabled, the user can submit the service request without selecting an appointment.


</td></tr><tr><td>

User contact

</td><td>

The field on the record producer that determines for whom the appointment was created. Set this field to **Contact**. This is a reference field that looks for a sys\_user variable on the record producer.

</td></tr><tr><td class="sub-head" colspan="2">

Booking

</td></tr><tr><td>

Appointments per window

</td><td>

The number of available appointments for each configured appointment time slot. This number determines the number of available appointments displayed on the Select Appointment window. Enter a number in this field if the assignment method for tasks is set to **manually**. If set to either **using auto-assignment** or **using dynamic scheduling**, this setting does not apply, unless a location is not provided. Then the configuration defaults to the number of appointments per window.

</td></tr><tr><td>

Lead time

</td><td>

The number of hours or days from the current time after which you have booked an appointment for this service. Define the lead time in hours or days. The default is 4 hours.

</td></tr><tr><td>

Future bookable max days

</td><td>

The number of days after the current day for which an appointment can be booked for this service. The default is 14 days.

</td></tr><tr><td>

Reschedule/Cancel by time

</td><td>

The number of hours or days prior to an appointment start time that are required for cancelling an appointment or rescheduled. If a user attempts to cancel or reschedule an appointment within this number of hours, the **Cancel** button is not available. Define the time in hours or days. The default is 4 hours.

</td></tr><tr><td class="sub-head" colspan="2">

Appointments

</td></tr><tr><td>

Appointment window

</td><td>

The length or duration of the appointment window. **Note:** Allow enough time to start and complete the work within this window.

</td></tr><tr><td>

Work duration

</td><td>

The amount of time required to complete all tasks created by the record producer. You set the duration for a task when it is created which is used to determine availability. The default is 1 hour.

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
</table>4.  Click **Submit**.


