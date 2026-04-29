---
title: Add assigned studio users to an unattended robot
description: In RPA Hub, assign one or more users \(RPA developers or RPA admins\) to an unattended robot, so that the users can access the specific robot in the Assigned Bot Process section of the RPA Desktop Design Studio application.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Robots, Use, RPA Hub, Workflow Data Fabric]
---

# Add assigned studio users to an unattended robot

In RPA Hub, assign one or more users \(RPA developers or RPA admins\) to an unattended robot, so that the users can access the specific robot in the **Assigned Bot Process** section of the RPA Desktop Design Studio application.

## Before you begin

Familiarise yourself with the Assigned Bot Process feature in RPA Desktop Design Studio. For more information, see [Assign bot process to an automation project](../../rpa-studio/task/assign-bot-process.md).

Only users with RPA developer or RPA admin roles can be associated to a robot.

Role required: sn\_rpa\_fdn.rpa\_release\_manager or sn\_rpa\_fdn.rpa\_admin

## About this task

The Assign Bot Process feature provides a capability for the users to access the bot process information \(such as queues, process parameters, and so on\) in RPA Hub and debug the automation in the RPA Desktop Design Studio. The users listed in the **Assigned Studio Users** tab can utilize the robots from RPA Desktop Design Studio, depending on the associated bot process access.

This helps in impersonating as a robot, so that the following benefits are achieved from the RPA Desktop Design Studio:

-   Get the process and shared parameters
-   Interact with work items and other RPA Hub related components \(wherever applicable\).

You can select a robot for impersonating as a robot in two ways. One way is by enabling **sn\_rpa\_fdn.restrict\_robots\_in\_assign\_bot\_process\_by\_machine\_name** system property. Then, the robots assigned to the bot process are filtered based on the robot machine name, where the RPA Desktop Design Studio is launched. For example, if the user launches the RPA Desktop Design Studio from the `ABC` robot machine, then the user can access only the `ABC` robot machine.

For more information about this system property, see [Configure RPA Hub properties](../reference/rpahub-sys-properties.md).

**Important:**

The users listed in the **Assigned Studio Users** tab are purged based on the time interval defined. The default time interval is 4 hours.

To change the time interval, enter `sys_auto_flush.LIST` in the navigation filter and search for the **sn\_rpa\_fdn\_assigned\_studio\_user** table name. Modify the value in the **Age in seconds** field. To deactivate this setting, clear the **Active** check box. Only admins can access the `sys_auto_flush.LIST` table.

The other way is by adding one or more users to an unattended robot from the **Assigned Studio Users** tab in RPA Hub. To do so, perform this task.

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(![List icon.](../image/rpahublist-icon.png)\).

3.  On the **Lists** tab, under **Administration**, select **Robots**.

4.  Open the robot that you want to associate a studio user to.

5.  On the **Assigned Studio Users** tab, select **Add**.

6.  On the **Available Studio Users** tab, select the required user.

7.  Select **Add**.

8.  Select **Save**.


