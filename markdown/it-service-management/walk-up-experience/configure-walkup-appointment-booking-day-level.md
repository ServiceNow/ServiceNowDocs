---
title: Configure day-level appointment booking
description: Create or modify different schedules at a day level when booking appointments for a service. The appointments can be scheduled for different slots such as morning, afternoon, and evening.
locale: en-US
release: yokohama
product: Walk-Up Experience
classification: walk-up-experience
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Create or modify a Walk-up Experience appointment booking service configuration, Configure Walk-up Experience appointment booking, Walk-up Experience appointment booking administration, Book Walk-up Experience appointments, Configure, Walk-up Experience, IT Service Management]
---

# Configure day-level appointment booking

Create or modify different schedules at a day level when booking appointments for a service. The appointments can be scheduled for different slots such as morning, afternoon, and evening.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Appointment Booking** &gt; **Appointment Booking Configuration**.

2.  Select **Walk-up Experience**.

3.  In the Appointment Booking Service Configuration related list, select a service configuration for which you want to configure the appointment schedules.

4.  Select **Enable Advanced Configuration**.

5.  In the Appointment Booking Day Configuration related list, click **New**.

6.  On the form, fill in the fields.

<table id="table_r3s_hr2_yrb"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the day level configuration, such as Morning, Afternoon, or Evening

</td></tr><tr><td>

Active

</td><td>

Option to indicate if the appointment slot is active or not.

</td></tr><tr><td>

Start date

</td><td>

Start date of the appointment booking window

</td></tr><tr><td>

End date

</td><td>

End date of the appointment booking window

</td></tr><tr><td>

Daily start time

</td><td>

Start of the work day and the earliest start time for an appointment window. The field is automatically set to 9a.m.

</td></tr><tr><td>

Daily end time

</td><td>

End of the work day and the latest end time for an appointment window. The default is 6p.m.

</td></tr><tr><td>

Service configuration

</td><td>

Name of the service configuration for which you are scheduling configurations at a day level, such as Point-of-Sale Installation.

</td></tr><tr><td>

Work duration

</td><td>

Time required to complete all tasks created by the record producer. This duration is set for a task when it is created. Used to determine availability. The default is 1 hour.

</td></tr><tr><td>

Travel duration \(round trip\)

</td><td>

Estimated value of the average travel time required \(round trip\) for the agent performing the task. Used to determine availability. The default is 15 minutes.

</td></tr><tr><td>

Appointment window

</td><td>

Duration of the appointment window.**Note:** Allow enough time for the work to be started and completed within this window.

</td></tr><tr><td>

Appointments per window

</td><td>

Number of available appointments for each configured appointment time slot. This number determines the number of available appointments that are displayed on the Select Appointment window. Enter a number in this field if the assignment method for tasks is set to manually. If set to either using auto-assignment or using dynamic scheduling, this setting does not apply, unless a location is not provided. Then the configuration defaults to the number of appointments per window.

</td></tr><tr><td>

Include daily break

</td><td>

Option to schedule a break for each bookable day. Set the break start and end times. You can also define one break which applies to all days.

</td></tr><tr><td>

Appointment booking preview

</td><td>

Provides a preview of the appointment windows and times based on the selected start and end times, break time, and appointment window.

</td></tr></tbody>
</table>7.  Select **Submit**.


**Parent Topic:**[Create or modify a Walk-up Experience appointment booking service configuration](configure-walkup-appointments.md)

