---
title: Associate a bot process to a bot process configuration record
description: Select a bot process configuration record to associate it with a bot process. This action creates a bot process record in RPA Hub.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
keywords: [associate bot process to bot process configuration record, rpa Hub, assign bot process to bot process configuration record, bot process settings, attended bot process, unattended bot process, bot process rpa hub, bot process configuration rpa hub]
breadcrumb: [Configuring a bot process record in RPA Hub, Using RPA Hub, RPA Hub, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Associate a bot process to a bot process configuration record

Select a bot process configuration record to associate it with a bot process. This action creates a bot process record in RPA Hub.

## Before you begin

Create a package. For more information, see [Create a package to assign to a bot process](create-package.md).

Create a robot. For more information, see [Creating a robot in RPA Hub](../concept/create-robot.md).

Configure the related system property to view the activity stream. For more information, see [Display an activity stream for bot processes and robots in RPA Hub](display-activity-stream-sys-property-rpahub.md).

Before you can access a bot process, ensure that the RPA business user \(sn\_rpa\_fdn.rpa\_business\_user\), RPA developer \(sn\_rpa\_fdn.rpa\_developer\), or the RPA support user \(sn\_rpa\_fdn.rpa\_support\_user\) are in the Managed by Group list.

Role required: sn\_rpa\_fdn.rpa\_release\_manager or sn\_rpa\_fdn.rpa\_admin

## About this task

A bot process is a predefined sequence of actions that a robot follows to accomplish a specific task or achieve a particular goal.

A bot process configuration record contains the bot process settings. The bot process configuration record is mapped to a bot process record. It is a one to one mapping. You can only select one bot process record to associate with a bot process configuration record. You can't edit a bot process configuration record that is associated with a bot process.

When you retire a bot process record, you can't associate the related bot process configuration record to other bot processes.

You can create a bot process configuration record in two ways. The first way is when you create and save a bot process configuration record.

The second way is when you move an update set from a lower environment to a higher environment, an orphan bot process configuration record is created. After you select the **Assign Configuration** button and its record, the bot process record that is associated to the bot process configuration is created.

For more information about migrating your metadata from a lower environment to a higher environment, see [Migrating your data from a lower environment to a higher environment in RPA Hub](../concept/migrate-data-rpa-hub.md).

## Procedure

1.  You can associate a bot process to a bot process configuration record by choosing one of these options.

<table id="choicetable_nkf_c3k_xvb"><thead><tr><th align="left" id="d480770e158">

Option

</th><th align="left" id="d480770e161">

Action

</th></tr></thead><tbody><tr><td id="d480770e167">

**Perform this task in workspace**

</td><td>

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.
2.  Select the list icon \(![List icon.](../image/rpahublist-icon.png)\).
3.  On the **Lists** tab, under **Build**, select **Bot Process**.
4.  In the form header, select the down arrow in the **Create Configuration** button.

![Down arrow in the Create Configuration button.](../image/down-arrow-create-config-rpa.png "Down arrow in the Create Configuration button")

5.  Select **Assign Configuration**.
6.  Select a bot process configuration record to associate it with a bot process.
7.  Select **Submit**.
8.  On the form, fill in the fields.

For a description of the field values, see [Bot Process form in RPA Hub](../reference/bot-process-form.md).

9.  Select **Save**.
10. On the **Details** tab, in **Activity** and **Compose** fields, view the activity of the form, work notes, and additional comments.


</td></tr><tr><td id="d480770e278">

**Perform this task in the classic environment**

</td><td>

1.  Switch to the classic environment.
2.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **Build** &gt; **Bot Process**.
3.  In the form header, select **New**.
4.  Select a bot process configuration record to associate it with a bot process.
5.  Select **Submit**.
6.  On the form, fill in the fields.

For a description of the field values, see [Bot Process form in RPA Hub](../reference/bot-process-form.md).

7.  Select **Save**.


</td></tr></tbody>
</table>
## What to do next

You can add other details that pertain to the bot process, such as the business applications, credential groups, robots, process robot credential sets, schedules, process parameters, attended users, or groups. For more information, see [Adding details for your bot process in RPA Hub](../concept/post-req-bot-process-rpa.md).

**Related topics**  


[Create a bot process configuration record in RPA Hub](create-botprocess-config.md)

[Bot process configuration form in RPA Hub](../reference/bot-process-config-form.md)

[Edit a bot process in RPA Hub](edit-botprocess.md)

[Publish an RPA Hub bot process](publish-bot-process.md)

[Retire an RPA Hub bot process](retire-bot-process.md)

[View Audit History](https://www.servicenow.com/docs/access?context=c_HistorySets&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)

