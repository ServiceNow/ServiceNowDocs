---
title: Create appointment booking advanced configuration
description: Create advanced appointment schedules to offer customers specific time slots—like Morning, Afternoon, and Evening—for scheduling appointments. Advanced schedules let you customize availability to meet unique business needs.
locale: en-US
release: zurich
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configure daily and advanced schedules, Configuring Appointment Booking, Additional scheduling configuration options, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Create appointment booking advanced configuration

Create advanced appointment schedules to offer customers specific time slots—like Morning, Afternoon, and Evening—for scheduling appointments. Advanced schedules let you customize availability to meet unique business needs.

## Before you begin

Role required: sn\_apptmnt\_booking.appointment\_booking\_admin

Ensure you have already created a **Service Configuration** and enabled the **Advanced Configuration** option.

## About this task

For each service, you can define multiple advanced schedules that override the default availability, based on conditions specified in service configuration rules.

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

Descriptive name of the configuration, such as Morning, Afternoon, or Evening.

</td></tr><tr><td>

Active

</td><td>

Option to activate the advanced schedule.

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

Estimated time needed to complete the tasks created by the record producer. Work duration for a task is set when the task is created and is used to determine the availability.

</td></tr><tr><td>

Use duration from template or task

</td><td>

Ignore the configured work duration and use the duration from the template or task.-   FALSE \(default\): Use the duration as set in the Work duration field.The sum of work and travel durations must be less than or equal to the appointment window to show available slots.
-   TRUE: Ignore manually configured work and travel durations. Instead, use values from templates or tasks.


</td></tr><tr><td>

Travel Duration \(round trip\)

</td><td>

Average round-trip travel time for the assigned agent. Travel Duration is used to determine availability. The default time is 15 minutes.

</td></tr><tr><td>

Appointment window

</td><td>

Duration of each appointment slot. **Note:** Allow enough time for the work to be started and completed within this window.

</td></tr><tr><td>

Appointments per window

</td><td>

Number of appointments available per slot. Applicable primarily for manual task assignment method. This number determines the available appointments that are displayed on the **Select Appointment** window. If the task assignment method is either auto-assignment or by dynamic scheduling, this setting does not apply unless you provide a location. The configuration defaults to the number of appointments per window if the location is not provided.

</td></tr><tr><td>

Include daily break

</td><td>

Enable to schedule a consistent daily break period. Select the break start time and end time. You can define one break which applies to all the days.

</td></tr><tr><td>

Appointment booking preview

</td><td>

Provides a preview of the appointment windows and times based on the selected start and end times, break time, and appointment window.

</td></tr></tbody>
</table>8.  Click Submit.


## Result

The advanced appointment schedule is active. Customers can select specific time slots such as morning, afternoon, or evening appointments based on this configuration.

