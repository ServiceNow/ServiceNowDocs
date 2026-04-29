---
title: Start an unattended bot process in RPA Hub
description: Start an unattended bot process in the specified robot machine to execute the automation by the selected robot.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Monitor, RPA Hub, Workflow Data Fabric]
---

# Start an unattended bot process in RPA Hub

Start an unattended bot process in the specified robot machine to execute the automation by the selected robot.

## Before you begin

Associate a package and a package version to the bot process. For more information, see [Configuring a bot process record in RPA Hub](../concept/create-botprocess.md).

Verify that the life cycle stage status of the bot process is either in **Published**, **In Maintenance**, or **Build**. For more information, see [Bot Process form in RPA Hub](select-botprocess.md#).

If the **External Credential** check box is selected in a robot credential record, then ensure that the associated external credential vault record is active. For more information, see [Create a robot credential in RPA Hub](create-credential-set-botprocess.md).

Role required: sn\_rpa\_fdn.rpa\_developer, sn\_rpa\_fdn.rpa\_support\_user, sn\_rpa\_fdn.rpa\_business\_user, or sn\_rpa\_fdn.rpa\_admin

## About this task

If robot pool is enabled, after you select the **Start Process** button, a certain number of robots from the assigned robot pool execute the bot process based on the following conditions:

-   Based on the value selected in the **Allocation Type** field on the Bot Process form.
-   Based on the pending work items and average handling time of previous successfully completed work items, calculate the number of robots needed.
-   Minimum value of calculated robots is 1.
-   Maximum value of calculated robots is equal to the number of robots in the pool.

**Note:** When a bot process is either in the **In Maintenance** or **Build** life-cycle stage status and is using a robot pool, new robots are not deployed for dynamic allocation. Dynamic allocation in the robot pool is only activated for published bot processes.

Only robots with an assigned credential group and in the **Available** and **Busy** states are displayed here to facilitate process job queuing. A job queue contains processes that are executed in a defined order.​​

You can also run an unattended automation using the Unattended Robot. For more information, see [Run an automation using Unattended Robot](../../rpa-runtime/task/run-rpa-robot.md).

Another way to start an unattended bot process is via triggering the **Start Process** Action in Workflow Studio. For more information, see [Workflow Studio actions and subflow in RPA Hub](../reference/rpa-hub-actions.md).

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(![List icon.](../image/rpahublist-icon.png)\).

3.  On the **Lists** tab, under **Build**, select **Bot Process**.

4.  Open the bot process to execute the unattended automation.

5.  In the form header, select **Start Process**.

6.  Select the robot that is assigned to the current bot process that you want to start.

    The robots that are in the **In Maintenance** life-cycle stage status are not displayed in the list.

7.  Select **Start Process**.

    Your organisation’s security policy may flag or prevent the automation from executing. To avoid that, consider allow listing the folders that store the binaries, user plugins, and script connectors on your computer. For example,

    -   For binaries, you can allow list the ServiceNowRPA folder in the path `Users\<username>\AppData\Local`
    -   For user plugins, you can allow list the user plugins folder in the path `<project folder name>\UserPlugins\<User plugin name>`
    -   For script connectors, you can allow list the Dependencies folder in the path `<project folder name>\Dependencies`

**Parent Topic:**[Monitoring automations](../concept/monitoring-automations-rpa.md)

**Related topics**  


[Edit a bot process in RPA Hub](edit-botprocess.md)

[Stop an unattended bot process in RPA Hub](stop-bot-process.md)

[Launch in Studio from RPA Hub](launch-studio.md)

[Publish a bot process in RPA Hub](publish-bot-process.md)

[Retire a bot process in RPA Hub](retire-bot-process.md)

