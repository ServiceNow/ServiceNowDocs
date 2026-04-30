---
title: Create a robot pool in RPA Hub
description: Create a robot pool in RPA Hub for an optimum utilization of robots to execute the bot processes.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Using RPA Hub, RPA Hub, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Create a robot pool in RPA Hub

Create a robot pool in RPA Hub for an optimum utilization of robots to execute the bot processes.

## Before you begin

Familiarize yourself with robot pool concepts. For more information, see [Robot pool in RPA Hub](../concept/robot-pool-rpa.md).

Role required: sn\_rpa\_fdn.rpa\_release\_manager or sn\_rpa\_fdn.rpa\_admin

## About this task

Robot pool is used to distribute the workload among multiple robots.

To add or remove robots from the pool that are associated with one or more published bot processes, move the bot process to In Maintenance state.

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(![List icon.](../image/rpahublist-icon.png)\).

3.  On the **Lists** tab, under **Administration**, select **Robot Pool**.

4.  Select **New**.

5.  On the form, in the **Name** field, enter a unique robot pool name for a domain.

6.  Select **Save**.

7.  To assign robots to the robot pool, do the following steps:

    1.  On the Robots tab, select **Add**.

    2.  On the **Available Robots** tab, select the required robot.

        **Note:** You can add an unattended robot \(whose life cycle stage status isn’t Retired\) to an existing robot pool at any time. Robots that aren’t associated to any bot process or robot pool are displayed in the **Available Robots** tab.

    3.  Select **Add**.

    4.  Select **Save**.

    5.  To remove a robot, select the robot and select **Remove**.

        **Note:**

        If you associate a robot pool to a bot process, you can’t remove that robot if it’s the only robot in the pool.

        Robots with process jobs in running state must not be removed from the Robot Pool until the process job is either completed or cancelled.

8.  To delete a robot pool, select the three-dot icon next to the **Save** button and select **Delete**.

    **Note:** Verify that the robot pool isn’t associated to any bot process.

9.  In the **Activity** and **Compose** fields, view the activity of the robot pool and robot, work notes, and additional comments.


## What to do next

Enable robot pool option for a bot process to map a bot process to the robot pool. For more information, see [Enable robot pool for a bot process in RPA Hub](enable-robot-pool.md).

\(Optional\) Calculate the number of robots required to allocate those robots from the selected pool to execute the bot process. For more information, see [Calculate the number of robots in RPA Hub](calculate-robots.md).

