---
title: Create a schedule on the robot calendar
description: Create a schedule on the Robot Calendar tab in RPA Hub to execute unattended robots. You can also identify any conflicts in the schedule by selecting the Preview button.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Managing RPA Hub, RPA Hub, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Create a schedule on the robot calendar

Create a schedule on the **Robot Calendar** tab in RPA Hub to execute unattended robots. You can also identify any conflicts in the schedule by selecting the **Preview** button.

## Before you begin

Perform the following tasks before you create a schedule on the robot calendar:

-   Ensure you are familiar with robot calendar concepts. For more information, see [Using the robot calendar for RPA Hub](../concept/robot-calendar-rpa.md) and [View robot events in RPA Hub](view-robot-calendar.md).
-   Create an unattended robot. On the robot form, ensure that you select the **Robot Type** field as **Unattended**. For more information, see [Creating a robot in RPA Hub](../concept/create-robot.md).
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

<table id="choicetable_kgc_jxm_frb"><thead><tr><th align="left" id="d493459e174">

Option

</th><th align="left" id="d493459e177">

Action

</th></tr></thead><tbody><tr><td id="d493459e183">

**View a robot calendar from a robot**

</td><td>

1.  On the **Lists** tab, under **Administration**, select **Robots**.
2.  Open a robot to view the robot calendar.
3.  In the form header, select **Robot Calendar**.


</td></tr><tr><td id="d493459e216">

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

    For more information, see [Schedule form in RPA Hub](../reference/schedule-rpa-form.md).

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


**Parent Topic:**[Managing RPA Hub](../concept/managing-rpa-hub.md)

