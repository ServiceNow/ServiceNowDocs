---
title: Create a schedule on the robot calendar in RPA Hub
description: Create a schedule on the Robot Calendar tab in RPA Hub to execute unattended robots. You can also identify any conflicts in the schedule by selecting the Preview button.Use the Schedule form to create a schedule within a Unattended Robot bot process. A schedule enables the users to execute jobs in a planned manner at regular intervals. More than one schedule can be associated with one bot process.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 8
keywords: [unattended bot process intervals rpa hub]
breadcrumb: [Robot calendar, Use, RPA Hub, Workflow Data Fabric]
---

# Create a schedule on the robot calendar in RPA Hub

Create a schedule on the **Robot Calendar** tab in RPA Hub to execute unattended robots. You can also identify any conflicts in the schedule by selecting the **Preview** button.

## Before you begin

Perform the following tasks before you create a schedule on the robot calendar:

-   Ensure you are familiar with robot calendar concepts. For more information, see [Using the robot calendar for RPA Hub](../concept/robot-calendar-rpa.md) and [View current robot events in RPA Hub](view-robot-calendar.md).
-   Create an unattended robot. On the robot form, ensure that you select the **Robot Type** field as **Unattended**. For more information, see [Create an unattended robot in RPA Hub](create-unattended-robot.md).
-   Establish the robot connection to an unattended bot process. For more information, see [Assign a robot to a bot process in RPA Hub](assign-robots.md).
-   Verify that the life-cycle stage of the associated bot process isn’t set to **Retired**.
-   Ensure that the RPA developer \(sn\_rpa\_fdn.rpa\_developer\) or the RPA support user \(sn\_rpa\_fdn.rpa\_support\_user\) are in the Managed by Group list of the associated bot process.

Role required: sn\_rpa\_fdn.rpa\_release\_manager, sn\_rpa\_fdn.rpa\_developer, sn\_rpa\_fdn.rpa\_support\_user, or sn\_rpa\_fdn.rpa\_admin

## About this task

To create a schedule within an unattended bot process, see [Create a schedule within a bot process in RPA Hub](create-schedule-botprocess.md).

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(![List icon.](../image/rpahublist-icon.png)\).

3.  View a robot calendar either from a robot or from a bot process.

<table id="choicetable_kgc_jxm_frb"><thead><tr><th align="left" id="d552786e186">

Option

</th><th align="left" id="d552786e189">

Action

</th></tr></thead><tbody><tr><td id="d552786e195">

**View a robot calendar from a robot**

</td><td>

1.  On the **Lists** tab, under **Administration**, select **Robots**.
2.  Open a robot to view the robot calendar.
3.  In the form header, select **Robot Calendar**.


</td></tr><tr><td id="d552786e228">

**View a robot calendar from a bot process**

</td><td>

1.  On the **Lists** tab, under **Build**, select **Bot Process**.
2.  Open a bot process to view the robot calendar.
3.  In the form header, select **Show Robot Calendar**.
4.  In the **Select the robot to view the calendar** dialog box, select a robot from the Robot list.
5.  Select **Continue**.


</td></tr></tbody>
</table>4.  To create a new schedule, perform any of the following tasks:

    -   On the **Robot Calendar** tab, select **New Schedule**.
    -   Right-click an empty slot of the calendar. Then, select **New Schedule**.
    -   Double-click an empty slot of the calendar.
    The **Create a new schedule** contextual side panel opens.

5.  To view more bot processes, select the filter icon \(![Filter icon.](../image/filter-rc-rpa.png)\) and add the appropriate **Process Name** filter and **Life Cycle Stage Status** filter.

6.  In the **Create a new schedule** contextual side panel, select a bot process that you want to create a schedule for.

7.  Select one of the following options, depending on what the life cycle stage status is of your bot process:

    -   If the life cycle stage status of the bot process is either Build or In Maintenance, select **Continue**.
    -   If the life cycle stage status of the bot process is Published, to change the status to In Maintenance, in the Confirmation dialog box, select **Continue**.
8.  On the schedule form, update the fields as appropriate.

    For more information, see [Schedule form in RPA Hub](create-robot-schedule.md#).

9.  To identify any conflicts in the schedule or preview the schedule, select **Preview**.

    To edit or delete a schedule, see [Edit a robot schedule in RPA Hub](edit-robot-schedule.md) and [Delete a robot schedule in RPA Hub](delete-robot-schedule.md).

10. To view more details about an event, perform any of the following tasks:

    -   Select the view event details icon \(![View event details icon.](../../../release-notes/image/icon-view-event-rpa.png)\) on the event pop-up window.
    -   Right-click an event and select **View event details**.
    An event card with details of the schedule appears in the contextual side panel.

11. To view the bot process details in a new tab, select the view bot process details icon \(![View bot process details icon.](../../../release-notes/image/icon-view-bp-rpa.png)\) on the event pop-up window.

12. Perform any of the following tasks to save the schedule.

    |Option|Action|
    |------|------|
    |**Only save the schedule**|Select **Save**.|
    |**Save the schedule and publish the bot process**|Select the down arrow in the **Save** button and then select **Save and Publish**.|


**Parent Topic:**[Using the robot calendar for RPA Hub](../concept/robot-calendar-rpa.md)

## Schedule form in RPA Hub

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
</table>