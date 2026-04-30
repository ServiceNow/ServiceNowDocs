---
title: Assign a robot to a bot process in RPA Hub
description: Assign a robot to an unattended bot process to execute the automation \(package\) that is mapped to it.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Adding details for your bot process, Configuring a bot process record, Use, RPA Hub, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Assign a robot to a bot process in RPA Hub

Assign a robot to an unattended bot process to execute the automation \(package\) that is mapped to it.

## Before you begin

Ensure that the **Enable Robot Pool** option isn’t selected in the Robot Pool section of the Details tab of the bot process.

Familiarize yourself with robot pool concepts. For more information, see [Robot pool in RPA Hub](../concept/robot-pool-rpa.md).

You can assign robots with a life cycle stage status of **In Use** to a bot process.

Do this task only when you select the **Process Type** field as **Unattended** on the Bot process configuration form while you're creating a bot process. For more information, see [Configuring a bot process record in RPA Hub](../concept/create-botprocess.md), [Bot process configuration form in RPA Hub](../reference/bot-process-config-form.md), and [Bot Process form in RPA Hub](../reference/bot-process-form.md).

Role required: sn\_rpa\_fdn.rpa\_release\_manager or sn\_rpa\_fdn.rpa\_admin

## About this task

If the bot process has enabled the robot pool option, then you can’t assign robots. The **Assigned Robots** tab is hidden.

To assign robots via robot pool, enable the robot pool option on the bot process form. For more information, see [Enable robot pool for a bot process in RPA Hub](enable-robot-pool.md).

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(![List icon.](../image/rpahublist-icon.png)\).

3.  On the **Lists** tab, under **Build**, select **Bot Process**.

4.  Open the bot process that you want to associate a robot to.

5.  On the **Assigned Robots** tab, select **Add**.

6.  On the **Available Robots** tab, select the required robot.

7.  Select **Add**.

8.  Select **Save**.


