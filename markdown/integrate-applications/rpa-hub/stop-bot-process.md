---
title: Stop an unattended bot process in RPA Hub
description: Stop the unattended bot process to abort the automation by the selected robot. If robot pool is enabled for a particular bot process, then the execution is stopped for all the robots of the robot pool.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Managing RPA Hub, RPA Hub, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Stop an unattended bot process in RPA Hub

Stop the unattended bot process to abort the automation by the selected robot.If robot pool is enabled for a particular bot process, then the execution is stopped for all the robots of the robot pool.

## Before you begin

Start a bot process. For more information, see [Start an unattended bot process in RPA Hub](start-bot-process.md).

Verify that the life cycle stage status of the bot process is either in **Published**, **In Maintenance**, or **Build**. For more information, see [Bot Process form in RPA Hub](../reference/bot-process-form.md).

Verify that the life cycle stage status of the assigned robot is **In Use** and the state of the robot is **Busy**.

Ensure you are familiar with graceful stop concepts. For more information, see [Using Graceful Stop functionality in RPA Hub](../concept/graceful-stop-rpa.md).

To use the **Graceful Stop** toggle, ensure the Graceful Stop component is used in the selected package version in RPA Desktop Design Studio. Graceful stop is applicable for assigned robots as well as robots in robot pool.

Role required: sn\_rpa\_fdn.rpa\_developer, sn\_rpa\_fdn.rpa\_support\_user, sn\_rpa\_fdn.rpa\_business\_user, or sn\_rpa\_fdn.rpa\_admin

## About this task

Another way to stop an unattended bot process is via triggering the **Stop Process** Action in Workflow Studio. For more information, see [RPA Hub actions and subflow](../reference/rpa-hub-actions.md).

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(![List icon.](../image/rpahublist-icon.png)\).

3.  On the **Lists** tab, under **Build**, select **Bot Process**.

4.  To stop the unattended automation, open the bot process.

5.  In the form header, select the down arrow in the **Start Process** button.

6.  Select **Stop Process**.

7.  To terminate the bot process gracefully, enable the **Graceful Stop** toggle switch.

8.  Select the robot that is assigned to the current bot process that you want to stop.

    **Note:** Only the robots that are assigned to the current bot process and execute the same bot process are displayed.

9.  Select **Stop Process**.


**Parent Topic:**[Managing RPA Hub](../concept/managing-rpa-hub.md)

**Related topics**  


[Edit a bot process in RPA Hub](edit-botprocess.md)

[Launch in Studio from RPA Hub](launch-studio.md)

[Publish an RPA Hub bot process](publish-bot-process.md)

[Retire an RPA Hub bot process](retire-bot-process.md)

