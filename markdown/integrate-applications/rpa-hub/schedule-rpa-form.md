---
title: Schedule form in RPA Hub
description: Use the Schedule form to create a schedule within a Unattended Robot bot process. A schedule enables the users to execute jobs in a planned manner at regular intervals. More than one schedule can be associated with one bot process.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
keywords: [unattended bot process intervals rpa hub]
breadcrumb: [Reference, RPA Hub, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Schedule form in RPA Hub

Use the Schedule form to create a schedule within a Unattended Robot bot process. A schedule enables the users to execute jobs in a planned manner at regular intervals. More than one schedule can be associated with one bot process.

<table id="table_pyx_mhd_4qb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Process Schedule

</td></tr><tr><td>

Name

</td><td>

Name of the process schedule.

</td></tr><tr><td>

Start Date

</td><td>

Start date of the schedule.

</td></tr><tr><td>

Active

</td><td>

Option to activate the schedule.On clearing this option, the schedule becomes inactive.

</td></tr><tr><td>

Application

</td><td>

\[Auto generated\] Application containing this record.Role required to view this field: admin.

</td></tr><tr><td>

Bot Process Configuration

</td><td>

Name of the associated bot process.

</td></tr><tr><td>

End Date

</td><td>

End date of the schedule.

</td></tr><tr><td class="sub-head" colspan="2">

Frequency &amp; Time

</td></tr><tr><td>

Interval Type

</td><td>

Schedule execution interval:-   **Minutes**: The bot process executes every n minutes that are specified in the **Frequency** field.
-   **Hours**: The bot process executes every n hours that are specified in the **Frequency** field.
-   **Daily**: The bot process executes every day at the time that is specified in the **Start time** field.
-   **Weekly**: The bot process executes on the specific days that are selected in the **Weekdays** field at a specified time in the **Start time** field.
-   **Monthly**: The bot process executes every n days at t time based on the value that is selected in the **On** field. “t” is the time that is specified in the **Start time** field. “n” is the value of the **Frequency** field.

The default value is set to `Daily`.

</td></tr><tr><td>

Frequency

</td><td>

Frequency of the schedule execution interval.This field appears only when **Minutes**, **Hours**, or **Monthly** is selected from the **Interval Type** field.

 If the frequency is too low, the performance in the Robot Calendar can be impacted.

</td></tr><tr><td>

Weekdays

</td><td>

Specific days of the week for the robot to run.For example, if the robot must run on Monday, select **Monday** in this field.

 This field does not appear if you select either **Days of Month** or **Week Occurrence** in the **On** field.

 This field appears only when **Minutes**, **Hours**, **Weekly**, or **Monthly** is selected from the **Interval Type** field.

</td></tr><tr><td>

Workstation Timezone

</td><td>

Option to consider the robot machine time zone.On enabling this option, the **Timezone** field does not appear.

</td></tr><tr><td>

Timezone

</td><td>

Time zone of the schedule.

</td></tr><tr><td>

Start Time

</td><td>

Time of the day to start the schedule.

</td></tr><tr><td>

End Time Required

</td><td>

Option to consider if the robot is not supposed to pick up a new job after a specific time.On enabling this option, the **End Time** field appears.

 This option appears only when either **Minutes** or **Hours** is selected from the **Interval Type** field.

</td></tr><tr><td>

End Time

</td><td>

Time of the day to end the schedule. The bot process triggered before this time will continue execution.This option appears only when the **End Time Required** field is selected.

</td></tr><tr><td>

On

</td><td>

Frequency of the execution: -   Weekdays
-   Days of Month
-   Week Occurrence

 This field appears only when **Monthly** is selected from the **Interval Type** field.

</td></tr><tr><td>

Days of Month

</td><td>

Specific days of the month for the schedule to run.For example, if the robot must run on the 5th, 6th, and 7th day of the month, select **5**, **6**, and **7** in this field.

 This field appears only when **Days of Month** is selected from the **On** field.

</td></tr><tr><td>

Occur On

</td><td>

Specific week of a month for the robot to run.For example, if the robot must run on the first Friday of a month, select **First** in this field.

 This field appears only when **Week Occurrence** is selected from the **On** field.

</td></tr><tr><td>

Day

</td><td>

Specific day of a month for the robot to run.For example, if the robot must run on the first Friday of a month, select **Friday** in this field.

 This field appears only when **Week Occurrence** is selected from the **On** field.

</td></tr><tr><td class="sub-head" colspan="2">

Compose

</td></tr><tr><td>

Work notes \(Private\)

</td><td>

Work notes for the process schedule.

</td></tr><tr><td>

Additional Comments

</td><td>

Additional comments related to the schedule.

</td></tr></tbody>
</table>**Parent Topic:**[RPA Hub reference](rpa-hub-reference.md)

**Related topics**  


[Create a schedule within a bot process in RPA Hub](../task/create-schedule-botprocess.md)

