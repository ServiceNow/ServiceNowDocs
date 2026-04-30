---
title: Create a schedule within a bot process in RPA Hub
description: Create a schedule within an unattended bot process to enable users to execute jobs in a planned manner at regular intervals. More than one schedule can be associated with one bot process.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [unattended bot process intervals rpa hub]
breadcrumb: [Adding details for your bot process, Configuring a bot process record, Use, RPA Hub, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Create a schedule within a bot process in RPA Hub

Create a schedule within an unattended bot process to enable users to execute jobs in a planned manner at regular intervals. More than one schedule can be associated with one bot process.

## Before you begin

Do this task only when you select the **Process Type** field as **Unattended** on the Bot process configuration form, while you are creating a bot process. For more information, see [Configuring a bot process record in RPA Hub](../concept/create-botprocess.md), [Bot process configuration form in RPA Hub](../reference/bot-process-config-form.md), and [Bot Process form in RPA Hub](../reference/bot-process-form.md).

\(Optional\) Configure the system properties related to **Activity Stream**, to add or remove the fields. The changes to these fields are captured in the work notes. For more information, see [Configure the system properties for an activity stream in RPA Hub](configure-sys-properties-activity.md).

Role required: sn\_rpa\_fdn.rpa\_release\_manager, sn\_rpa\_fdn.rpa\_developer, sn\_rpa\_fdn.rpa\_support\_user, or sn\_rpa\_fdn.rpa\_admin

## About this task

You cannot delete a schedule that is associated to a published bot process.

You can also create a schedule from the Robot Calendar tab. For more information, see [Create a schedule on the robot calendar in RPA Hub](create-robot-schedule.md).

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(![List icon.](../image/rpahublist-icon.png)\).

3.  On the **Lists** tab, under **Build**, select **Bot Process**.

4.  Open the bot process that you want to create and associate a schedule to.

5.  On the **Schedules** tab, select **New**.

6.  On the form, fill in the fields.

7.  Select **Save**.

8.  In the **Activity** and **Compose** fields, view the activity of the form, work notes, and additional comments.


**Related topics**  


[Schedule form in RPA Hub](../reference/schedule-rpa-form.md)

[View Audit History](https://www.servicenow.com/docs/access?context=c_HistorySets&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)

