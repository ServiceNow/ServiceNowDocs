---
title: Retire a robot in RPA Hub
description: Retire a robot to turn it off. It is one of the life-cycle stages of a robot. After you retire a robot, it cannot be used further.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage, RPA Hub, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Retire a robot in RPA Hub

Retire a robot to turn it off. It is one of the life-cycle stages of a robot. After you retire a robot, it cannot be used further.

## Before you begin

Create a robot. For more information, see [Creating an attended or an unattended robot in RPA Hub](../concept/create-robot.md).

Verify that the robot is not assigned to any bot process or robot pool.

Role required: sn\_rpa\_fdn.rpa\_release\_manager or sn\_rpa\_fdn.rpa\_admin

## About this task

Retiring an attended robot removes the associated user from all the associated bot processes.

If the associated user is a part of a bot process in the assigned users, that record gets deleted.

If there are no attended assigned users or groups associated to an attended robot, the life cycle stage status of the associated bot process is moved from Publish to In-Maintenance.

You cannot retire an unattended robot if it is associated to an unattended bot process.

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(![List icon.](../image/rpahublist-icon.png)\).

3.  On the **Lists** tab, under **Administration**, select **Robots**.

4.  Open the robot that you want to retire.

5.  In the form header, select **Retire**.

6.  In the Confirmation dialog box, select **Retire**.


**Parent Topic:**[Managing RPA Hub](../concept/managing-rpa-hub.md)

