---
title: Create appointment booking advanced configuration
description: Create or modify different schedules on an advanced level when booking appointments for a service. The appointments can be scheduled at different time slots of a day, such as morning, afternoon, and evening.
locale: en-US
release: xanadu
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring Appointment Booking, Additional scheduling configuration options, Setting up a Field Service scheduling method, Configuring Field Service Management, Field Service Management]
---

# Create appointment booking advanced configuration

Create or modify different schedules on an advanced level when booking appointments for a service. The appointments can be scheduled at different time slots of a day, such as morning, afternoon, and evening.

## Before you begin

Role required: sn\_apptmnt\_booking.appointment\_booking\_admin

## About this task

Advanced configurations can be customized for individual services within the appointment booking feature. When enabled, these configurations override the default settings, provided the conditions specified in the Service Configuration Rule's **Task Conditions** field are met.

## Procedure

1.  Navigate to **All** &gt; **Appointment Booking** &gt; **Appointment Booking Configuration**.

2.  Select the desired configuration.

    -   To configure different appointment schedules for work orders, select **Field Service Order Configuration**
    -   To configure different appointment schedules for work order tasks, select **Field Service Task Configuration**
3.  In the Appointment Booking Service Configuration related list, click a service configuration to which you want to configure different appointment schedules.

4.  Select **Enable advanced configurations** check box if not already selected.

5.  In the Advanced Configurations related list, click **New**.

6.  On the form, fill in the fields.

7.  <table id="table_lws_gcg_fqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the day level configuration, such as Morning, Afternoon, or Evening.

</td></tr><tr><td>

Active

</td><td>

Option to indicate if the appointment slot is active or not.

</td></tr><tr><td>

Start date

</td><td>

Start date of the appointment booking window.

</td></tr><tr><td>

End date

</td><td>

End date of the appointment booking window.

</td></tr><tr><td>

Daily start time

</td><td>

The start of the work day and the earliest start time for an appointment window.

</td></tr><tr><td>

Daily end time

</td><td>

The end of the work day and the latest end time for an appointment window.

</td></tr><tr><td>

Bookable days

</td><td>

The days of the week for which appointments can be booked. The default is Monday through Friday.

</td></tr><tr><td>

Service configuration

</td><td>

The name of the service configuration for which you are scheduling configurations on an advanced level, for example, Point-of-Sale Installation.**Note:** The Point-of-Sale Installation is available only for the **Field Service Order Configuration**.

</td></tr><tr><td>

Rule

</td><td>

The name of the service configuration rule based on which you are scheduling configurations on an advanced level.

</td></tr><tr><td>

Work duration

</td><td>

The amount of time required to complete all the tasks created by the record producer. Work duration for a task is set when the task is created and is used to determine the availability.

</td></tr><tr><td>

Travel Duration \(round trip\)

</td><td>

An estimated value of the average travel time required \(round trip\) for the agent performing the task. Used to determine availability. The default is 15 minutes.

</td></tr><tr><td>

Appointment window

</td><td>

The length or duration of the appointment window. **Note:** Allow enough time for the work to be started and completed within this window.

</td></tr><tr><td>

Appointments per window

</td><td>

The number of available appointments for each configured appointment time slot. This number determines the available appointments that are displayed on the **Select Appointment** window. Enter a number in this field if the task assignment method is manual. If the task assignment method is either auto-assignment or by dynamic scheduling, this setting does not apply unless you provide a location. The configuration defaults to the number of appointments per window if the location is not provided.

</td></tr><tr><td>

Include daily break

</td><td>

Enable this check box to schedule a break for each bookable day. Select the break start time and end time. You can define one break which applies to all the days.

</td></tr><tr><td>

Appointment booking preview

</td><td>

Provides a preview of the appointment windows and times based on the selected start and end times, break time, and appointment window.

</td></tr></tbody>
</table>8.  Click Submit.


## Result

Appointment booking advanced configuration is created.

**Parent Topic:**[Configuring Appointment Booking](../concept/appointment-booking-administer.md)

