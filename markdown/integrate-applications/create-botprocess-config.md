---
title: Create a bot process configuration record in RPA Hub
description: Create a bot process configuration record in RPA Hub so that you can define the preliminary fields for a bot process record.Use the Bot Process Configuration form to define the preliminary fields for a bot process record.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [rpa hub, bot process settings, attended bot process, unattended bot process, bot process rpa hub, bot process configuration rpa hub, attended bot process form, unattended bot process form, rpa hub]
breadcrumb: [Configuring a bot process record, Use, RPA Hub, Workflow Data Fabric]
---

# Create a bot process configuration record in RPA Hub

Create a bot process configuration record in RPA Hub so that you can define the preliminary fields for a bot process record.

## Before you begin

Create a package. For more information, see [Create a package to assign to a bot process](create-package.md#).

Create a robot. For more information, see [Robots in RPA Hub](../concept/robots-rpa-hub.md).

Configure the related system property to view the activity stream. For more information, see [Display an activity stream for bot processes and robots in RPA Hub](display-activity-stream-sys-property-rpahub.md).

Before you can access a bot process, ensure that the RPA business user \(sn\_rpa\_fdn.rpa\_business\_user\), RPA developer \(sn\_rpa\_fdn.rpa\_developer\), or the RPA support user \(sn\_rpa\_fdn.rpa\_support\_user\) are in the Managed by Group list.

Role required: sn\_rpa\_fdn.rpa\_release\_manager or sn\_rpa\_fdn.rpa\_admin

## About this task

A bot process is a predefined sequence of actions that a robot follows to accomplish a specific task or achieve a particular goal.

A bot process configuration record contains the bot process settings.

The bot process configuration record is mapped to a bot process record. It is a one to one mapping.

When you associate the bot process configuration record with a bot process record, you can't dissociate the mapping, regardless of the life-cycle stage status of the bot process.

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Create a bot process configuration record from either the list icon or from the plus icon.

<table id="choicetable_kgc_jxm_frb"><thead><tr><th align="left" id="d584071e162">

Option

</th><th align="left" id="d584071e165">

Action

</th></tr></thead><tbody><tr><td id="d584071e171">

**Create a bot process configuration record from the list icon**

</td><td>

1.  Select the list icon \(![List icon.](../image/rpahublist-icon.png)\).
2.  On the **Lists** tab, in **Build**, select **Bot Process**.
3.  Select **Create Configuration**.


</td></tr><tr><td id="d584071e210">

**Create a bot process configuration record from the plus icon**

</td><td>

1.  Select the plus icon \(![Plus icon.](../image/icon-plus.png)\).
2.  Select **New Bot Process Configuration**.


</td></tr></tbody>
</table>3.  On the form, fill in the fields.

    For a description of the field values, see [Bot process configuration form in RPA Hub](create-botprocess-config.md#).

4.  Save the configuration record only or create a configuration record and bot process and then associate the record with the bot process.

<table id="choicetable_twb_ds5_tvb"><thead><tr><th align="left" id="d584071e262">

Option

</th><th align="left" id="d584071e265">

Action

</th></tr></thead><tbody><tr><td id="d584071e271">

**Only save the bot process configuration record**

</td><td>

Select **Save**.Skip the post-requisite task.

This configuration record is not associated to a bot process. It remains orphaned.

 If you want to associate it with a bot process record later, follow the steps in [Associate a bot process to a bot process configuration record](select-botprocess.md#).

</td></tr><tr><td id="d584071e301">

**Create a bot process and bot process configuration record. Then associate the record with the bot process**

</td><td>

1.  Select **Assign Assets**.
2.  On the form, complete the remaining fields.

For a description of the field values, see [Bot Process form in RPA Hub](select-botprocess.md#).

3.  Select **Save**.
4.  On the **Details** tab, under **Activity** and **Compose** fields, view the activity of the form, work notes, and additional comments.


</td></tr></tbody>
</table>
## What to do next

You can add other details to the bot process, such as the business applications, credential groups, robots, process robot credential sets, schedules, process parameters, attended users, or groups. For more information, see [Adding details to your bot process in RPA Hub](../concept/post-req-bot-process-rpa.md).

\(Optional\) On the bot process configuration record, select the **Bot Process** button to navigate to the Overview tab of the bot process. You can't view this Bot Process button if the bot process configuration record is not associated to any bot process.

**Parent Topic:**[Configuring a bot process record in RPA Hub](../concept/create-botprocess.md)

**Related topics**  


[Edit a bot process in RPA Hub](edit-botprocess.md)

[Publish a bot process in RPA Hub](publish-bot-process.md)

[Retire a bot process in RPA Hub](retire-bot-process.md)

[bundle-psec.c_HistorySets]

## Bot process configuration form in RPA Hub

Use the Bot Process Configuration form to define the preliminary fields for a bot process record.

<table id="table_pyx_mhd_4qb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name of the bot process configuration.The name of the bot process configuration is reused for the bot process that is associated with this configuration record.

</td></tr><tr><td>

Process Type

</td><td>

Type of the bot process:-   **Unattended**: Automations that don’t require any human intervention.
-   **Attended**: Automations that require human intervention.

</td></tr><tr><td>

Order

</td><td>

Execution priority of the bot process:-   **1**: Highest priority
-   **999999**: Least priority

The default value is set to 1.

RPA business user can view this field.

This field appears only when **Unattended** is selected from the **Process Type** field.

</td></tr><tr><td>

Package

</td><td>

Associated package of the bot process.For an unattended bot process, associate an unattended type package.

For an attended bot process, associate an attended type package.

Only published packages can be associated.

</td></tr><tr><td>

Package Version

</td><td>

Version of the active package in use. Only published package versions can be associated.

Ensure that the version belongs to the populated package.

</td></tr><tr><td>

Application

</td><td>

Application that contains this record. This field is auto-generated.Role required to view this field: admin.

</td></tr><tr><td>

Run Time Threshold \(mins\)

</td><td>

Expected duration for the bot process to run.The default value is 60 minutes.

RPA business user can view this field.

This field appears only when **Unattended** is selected from the **Process Type** field.

This is a required field.

</td></tr><tr><td>

Job Purging \(days\)

</td><td>

Number of days after which the job data is deleted.

</td></tr><tr><td>

Description

</td><td>

Description of the bot process.

</td></tr></tbody>
</table>**Related topics**  


[Configuring a bot process record in RPA Hub](../concept/create-botprocess.md)

