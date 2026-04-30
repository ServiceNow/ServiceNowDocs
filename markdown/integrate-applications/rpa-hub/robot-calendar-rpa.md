---
title: Using the robot calendar for RPA Hub
description: You can use the robot calendar in RPA Hub to view and create the schedule for the unattended robots. It’s a simple, efficient, and interactive way to work with robots and schedules. By using the calendar, you can manage and plan a robot's schedule in a single view.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
keywords: [unattended bot process intervals rpa hub, bot process schedule rpa hub]
breadcrumb: [Explore, RPA Hub, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Using the robot calendar for RPA Hub

You can use the robot calendar in RPA Hub to view and create the schedule for the unattended robots. It’s a simple, efficient, and interactive way to work with robots and schedules. By using the calendar, you can manage and plan a robot's schedule in a single view.

**Note:**

Robot calendar is applicable for unattended robots and unattended bot processes only.

## Robot calendar overview

By using the robot calendar in RPA Hub, you get the following benefits:

-   Manage robots with multiple schedules across different time zones.
-   Create and manage robot schedules.
-   Check the robot availability, avoid potential conflicts, and schedule a run for the bot process.​
-   Perform robot capacity planning with better visibility and rich visual plotting in a single view.
-   Optimize the robot utilization and avoid any potential issues related to scheduled maintenance windows.

## Robot Calendar button

You can view the calendar from either a robot or a bot process in the workspace. If the robot is associated with a bot process that has active, inactive, or no schedules, you can view the **Robot Calendar** button.

The following roles are required to view the **Robot Calendar** button:

-   sn\_rpa\_fdn.rpa\_release\_manager
-   sn\_rpa\_fdn.rpa\_business\_user
-   sn\_rpa\_fdn.rpa\_developer
-   sn\_rpa\_fdn.rpa\_support\_user
-   sn\_rpa\_fdn.rpa\_admin

The following example shows the robot landing page with the **Robot Calendar** button, when accessed from a robot.

![Robot landing page with the Robot Calendar button.](../image/robot-calendar.png "Robot landing page with the Robot Calendar button")

On the ribbon of the robot calendar, you can see the robot type, life cycle stage status, robot state, machine name, the associated bot processes, and the associated robot pool name.

![Example: Snapshot of the robot calendar ribbon.](../image/robot-calendar-ribbon.png "Example: Snapshot of the robot calendar ribbon")

You can view the calendar from a bot process in the workspace, by selecting the **Show Robot Calendar** button. In the **Select the robot to view the calendar** dialog box, you can select a robot from the Robot list. Then, select **Continue**.

The following example shows the robot calendar when accessed from a bot process.

![Snapshot of a robot calendar when accessed from a bot process.](../image/rc-access-bot-process-rpa.gif "Robot Calendar from a bot process")

## Robot calendar landing page

On the landing page of the robot calendar, you can view the events of the bot processes. The schedules are for different interval types such as minutes, hourly, daily, weekly, or monthly. For more information about viewing the robot events, see [View current robot events in RPA Hub](../task/view-robot-calendar.md). However, you can't see the past events on the robot calendar.

You can view the robot calendar by the day, week, or month.

![Robot calendar views - day, week, and month](../image/rc-views.png "Robot calendar views - day, week, and month")

If the robot is associated with multiple bot processes, events of each bot process is differentiated with unique color.

## Week view

The following example shows the week view of the landing page of the robot calendar, with two bot processes. The week view starts from Sunday to Saturday.

![Week view of the landing page of the robot calendar.](../image/robot-calendar-week.png "Week view of the landing page of the robot calendar")

## Month view

The following example shows the month view of the landing page of the robot calendar.

![Month view of the landing page of the robot calendar.](../image/robot-calendar-month.png "Month view of the landing page of the robot calendar")

## Manage schedules

You can create a schedule on the **Robot Calendar** tab in RPA Hub to execute unattended robots. You can also identify any conflicts in the schedule by selecting the **Preview** button. For more information, see [Create a schedule on the robot calendar in RPA Hub](../task/create-robot-schedule.md).

You can edit a robot schedule to resolve any scheduling conflicts or to modify the details on the schedule form. You can also delete an existing robot schedule that you no longer need. For more information, see [Edit a robot schedule in RPA Hub](../task/edit-robot-schedule.md) and [Delete a robot schedule in RPA Hub](../task/delete-robot-schedule.md).

## Scheduled maintenance days

You can track scheduled maintenance \(SM\) days on the robot calendar to manage your future automations. Robotic Process Automation \(RPA\) release managers and RPA admins have visibility to the potential impacts of current or future automation executions to take an appropriate call to action, such as, either accepting or rejecting an associated SM event card on the robot calendar.

For more information, see [Scheduled maintenance days in RPA Hub](sm-days-rpa.md) and [Manage scheduled maintenance days in RPA Hub](../task/manage-sm-request-rpa.md).

## Plotting event duration

The value in the **Runtime Threshold \(Mins\)** field on the bot process form and the configuration in the related **sn\_rpa\_fdn.process.runtime\_threshold** system property are used for plotting the event duration in the robot calendar. Based on value in the **Runtime Threshold \(Mins\)** field, the robot calendar shows as busy. For example, if this value is set to 60 \(that is 1 hour\), then in the robot calendar of this robot, it is displayed as blocked for that one hour.

For more information about the bot process form, see [Bot Process form in RPA Hub](../reference/bot-process-form.md).

For more information about the system property, see [Configure RPA Hub properties](../reference/rpahub-sys-properties.md).

