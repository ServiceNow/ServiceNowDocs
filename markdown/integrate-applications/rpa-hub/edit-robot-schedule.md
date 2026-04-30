---
title: Edit a robot schedule in RPA Hub
description: Edit a robot schedule of a bot process on the Robot Calendar tab in RPA Hub to resolve any scheduling conflicts or to modify the details on the schedule form.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Managing RPA Hub, RPA Hub, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Edit a robot schedule in RPA Hub

Edit a robot schedule of a bot process on the **Robot Calendar** tab in RPA Hub to resolve any scheduling conflicts or to modify the details on the schedule form.

## Before you begin

Perform the following tasks before you edit a robot schedule:

-   Ensure you are familiar with robot calendar concepts. For more information, see [Using the robot calendar for RPA Hub](../concept/robot-calendar-rpa.md) and [View robot events in RPA Hub](view-robot-calendar.md).
-   Create an unattended robot. On the robot form, ensure that you select the **Robot Type** field as **Unattended**. For more information, see [Creating a robot in RPA Hub](../concept/create-robot.md).
-   Establish the robot connection to an unattended bot process. For more information, see [Assign a robot to a bot process in RPA Hub](assign-robots.md).
-   Create a schedule for a unattended bot process to view some schedules on the robot calendar. For more information, see [Create a schedule on the robot calendar](create-robot-schedule.md) or [Create a schedule within a bot process in RPA Hub](create-schedule-botprocess.md).
-   Verify that the life-cycle stage of the associated bot process isn’t set to **Retired**.
-   Ensure that the RPA developer \(sn\_rpa\_fdn.rpa\_developer\) or the RPA support user \(sn\_rpa\_fdn.rpa\_support\_user\) are in the Managed by Group list of the associated bot process.

Role required: sn\_rpa\_fdn.rpa\_release\_manager, sn\_rpa\_fdn.rpa\_developer, sn\_rpa\_fdn.rpa\_support\_user, or sn\_rpa\_fdn.rpa\_admin

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(![List icon.](../image/rpahublist-icon.png)\).

3.  View a robot calendar either from a robot or from a bot process.

<table id="choicetable_kgc_jxm_frb"><thead><tr><th align="left" id="d490714e186">

Option

</th><th align="left" id="d490714e189">

Action

</th></tr></thead><tbody><tr><td id="d490714e195">

**View a robot calendar from a robot**

</td><td>

1.  On the **Lists** tab, under **Administration**, select **Robots**.
2.  Open a robot to view the robot calendar.
3.  In the form header, select **Robot Calendar**.


</td></tr><tr><td id="d490714e228">

**View a robot calendar from a bot process**

</td><td>

1.  On the **Lists** tab, under **Build**, select **Bot Process**.
2.  Open a bot process to view the robot calendar.
3.  In the form header, select **Show Robot Calendar**.
4.  In the **Select the robot to view the calendar** dialog box, select a robot from the Robot list.
5.  Select **Continue**.


</td></tr></tbody>
</table>4.  To view more bot processes, select the filter icon \(![Filter icon.](../image/filter-rc-rpa.png)\) and add the appropriate **Process Name** filter and **Life Cycle Stage Status** filter.

5.  To edit a schedule, perform any of the following tasks.

    |Option|Action|
    |------|------|
    |**Right-click an event**|Right-click an event \(schedule\) and select **Edit schedule**.|
    |**Select the event pop-up window**|Select the edit schedule icon \(![Edit schedule icon.](../../../release-notes/image/icon-edit-schedule-rpa.png)\) on the event pop-up window.|

6.  If the life-cycle stage status of the bot process is set to **Published** and you want to change the status to **In Maintenance**, select **Continue** in the Confirmation dialog box.

7.  On the Edit schedule form, update the fields as appropriate.

8.  To identify any further conflicts in the schedule or preview the schedule, select **Preview**.

9.  Perform any of the following tasks to save the schedule:

    -   To save the schedule, select **Save**.
    -   To save the schedule and publish the bot process, select the down arrow in the **Save** button and select **Save and Publish**.

**Parent Topic:**[Managing RPA Hub](../concept/managing-rpa-hub.md)

**Related topics**  


[Schedule form in RPA Hub](../reference/schedule-rpa-form.md)

[Delete a robot schedule in RPA Hub](delete-robot-schedule.md)

