---
title: Assign a process robot credential within a bot process
description: Assign a process robot credential within an unattended bot process so that the selected robot can perform the automation in the Windows machine.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Adding details for your bot process in RPA Hub, Configuring a bot process record in RPA Hub, Using RPA Hub, RPA Hub, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Assign a process robot credential within a bot process

Assign a process robot credential within an unattended bot process so that the selected robot can perform the automation in the Windows machine.

## Before you begin

Do this task only when you select the **Process Type** field as **Unattended** on the Bot process configuration form while you're creating a bot process. For more information, see [Configuring a bot process record in RPA Hub](../concept/create-botprocess.md), [Bot process configuration form in RPA Hub](../reference/bot-process-config-form.md), and [Bot Process form in RPA Hub](../reference/bot-process-form.md).

Assign a robot to the bot process. For more information, see [Assign a robot to a bot process in RPA Hub](assign-robots.md).

Create a credential group. For more information, see [Create a credential group in RPA Hub](create-credential-group.md#).

Role required: sn\_rpa\_fdn.rpa\_developer, sn\_rpa\_fdn.rpa\_release\_manager, or sn\_rpa\_fdn.rpa\_admin

## About this task

One credential group can be associated to more than one robot, but one robot can't have more than one credential groups. All the robots assigned to the bot process must be mapped to a process robot credential record. After the mapping is done, if you delete the credential group or robot, the process robot credential record is also deleted.

If a robot is a part of a robot pool, ensure to map process robot credentials for each robot in the robot pool.

If any robot in the robot pool is deleted, then the associated process credentials for all the related bot processes are also deleted.

If the bot process using the robot pool is deleted or if the robot pool is deactivated on the bot process, then all the process credentials for that bot process are also deleted.

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(![List icon.](../image/rpahublist-icon.png)\).

3.  On the **Lists** tab, under **Build**, select **Bot Process**.

4.  Open the bot process that you want to assign the credentials to a robot to.

5.  On the **Process Robot Credentials** tab, select **New**.

6.  On the form, fill in the fields.

<table id="table_pyx_mhd_4qb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Credential Group

</td><td>

Credential group to be associated with this bot process and the assigned robot.

</td></tr><tr><td>

Robot

</td><td>

Robot to associate with this bot process and the credential group combination.

</td></tr><tr><td>

Process

</td><td>

Name of the bot process.This field is read-only.

</td></tr></tbody>
</table>7.  Select **Save**.

8.  In the **Activity** and **Compose** fields, view the activity of the form, work notes, and additional comments.


