---
title: Create an unattended robot in RPA Hub
description: Create an unattended robot in RPA Hub to run the unattended bot process.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Robots, Use, RPA Hub, Workflow Data Fabric]
---

# Create an unattended robot in RPA Hub

Create an unattended robot in RPA Hub to run the unattended bot process.

## Before you begin

Configure the related system property to view the activity stream. For more information, see [Display an activity stream for bot processes and robots in RPA Hub](display-activity-stream-sys-property-rpahub.md).

Make sure that the **sn\_rpa\_fdn.enable\_unattended\_robot\_user\_mapping** system property is set to True to allow only the authorized users to access the robot and robot assets. This system property enables the **User** field on the Unattended Robot form. If you have the admin role, you can edit this system property. By default, this property is set to True.

Role required: sn\_rpa\_fdn.rpa\_release\_manager or sn\_rpa\_fdn.rpa\_admin

## About this task

A robot runs a bot process, which is an automation.

An unattended robot can execute an unattended bot process, which is an automation that requires no human intervention.

By using the Unattended Robot application, you can enable an unattended robot to execute an unattended bot process that is triggered either by a schedule, API, or manually set.

You can map multiple unattended robots as high density robots to one virtual machine. For more information, see [High density robots in RPA Hub](../concept/high-density-robots-rpa-hub.md).

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Create an unattended robot from either the list icon or from the plus icon.

<table id="choicetable_kgc_jxm_frb"><thead><tr><th align="left" id="d659887e134">

Option

</th><th align="left" id="d659887e137">

Action

</th></tr></thead><tbody><tr><td id="d659887e143">

**Create an unattended robot from the list icon**

</td><td>

1.  Select the list icon \(![List icon.](../image/rpahublist-icon.png)\).
2.  On the **Lists** tab, under **Administration**, select **Robots**.
3.  Select **New**.


</td></tr><tr><td id="d659887e182">

**Create an unattended robot from the plus icon**

</td><td>

1.  Select the plus icon \(![Plus icon.](../image/icon-plus.png)\).
2.  Select **New Robot**.


</td></tr></tbody>
</table>3.  On the form, fill in the fields.

<table id="table_pyx_mhd_4qb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name of the unattended robot.

</td></tr><tr><td>

Robot Type

</td><td>

Type of the robot.**Unattended**: Robot for an unattended automation.

</td></tr><tr><td>

Machine Name

</td><td>

Computer name of the physical or virtual machine on which the Unattended Robot application is installed.This field appears only when **Unattended** is selected from the **Robot Type** field.

 The machine name is a string-type field that you use when you don't want to enable the **sn\_rpa\_fdn.enable\_unattended\_robot\_machine\_name\_lookup** system property.

 If you enable the **sn\_rpa\_fdn.enable\_unattended\_robot\_machine\_name\_lookup** system property, this string type field changes to a reference type field on the robot form.

 The machine name fetches the unique value references from the Configuration Item \(CI\) tables that are defined in the **sn\_rpa\_fdn.machine\_name\_reference\_fields** system property.

 The bot process table \(cmdb\_ci\_rpa\_process\) and robot table \(cmdb\_ci\_rpa\_robot\) are excluded from the search results when you provide the names of the CI tables to reference the unattended robot's machine name in the **sn\_rpa\_fdn.machine\_name\_reference\_fields** system property.

 The **Machine Lookup value change** scheduled job validates the values in the **Machine Name Lookup** field and **Machine Name** field.

 For more information, see the Scheduled jobs installed section in [Components installed with RPA Hub](../reference/installed-with-rpa-hub.md) and [Configure RPA Hub properties](../reference/rpahub-sys-properties.md).

</td></tr><tr><td>

High density robot

</td><td>

Option to create multiple robots with the same machine name.The machine must support multiple user sessions at the same time so that you can run multiple automations simultaneously.

This field appears only when **Unattended** is selected from the **Robot Type** field.

</td></tr><tr><td>

Screen resolution

</td><td>

Screen resolution used by a high density robot while establishing the RDP connection before executing the automation.High density robots can operate with different screen resolutions for each robot on the same machine without any issues if they are running different bot processes. However, if all high density robots on the same machine are executing the same process and utilizing Computer Vision actions, they must maintain the same resolution. Otherwise, the automation may fail.

This field appears only when the robot is marked as high density robot.

**Note:** You can change the default value of the screen resolution using the **sn\_rpa\_fdn.robot\_screen\_resolution** RPA Hub system property.

</td></tr><tr><td>

User

</td><td>

Authorized user who can access this robot.If you're upgrading to Xanadu, the **User** field is automatically mapped with the user name \(the user\) who has recently created the process job for the selected unattended robots. If no process jobs are found for a selected robot, the robot is moved to the In Maintenance status. An RPA release manager must manually map the appropriate users to the robots.

**Note:** This field appears when the **sn\_rpa\_fdn.enable\_unattended\_robot\_user\_mapping** system property is enabled.

</td></tr><tr><td>

Department

</td><td>

Associated department of the robot. This field is automatically filled in with the information that is based on the department in the associated Attended Robot User's record.

The value in this field corresponds to the value at the time that the Robot record is created and isn’t based on real-time data.

</td></tr><tr><td>

Description

</td><td>

Brief description of the robot.

</td></tr></tbody>
</table>4.  Select **Save**.

5.  In the **Activity** and **Compose** fields, view the activity of the form, work notes, and additional comments.


## What to do next

Install Unattended Robot. For more information, see [Install Unattended Robot](../../rpa-runtime/task/install-rpa-runtime.md)

Set up the Unattended Robot application. For more information, see [Set up Unattended Robot](../../rpa-runtime/task/set-up-rpa-runtime.md).

Create a bot process. For more information, see [Configuring a bot process record in RPA Hub](../concept/create-botprocess.md).

**Related topics**  


[Edit an unattended robot in RPA Hub](edit-robot.md)

[Retire a robot in RPA Hub](retire-robot.md)

[View Audit History](https://www.servicenow.com/docs/access?context=c_HistorySets&version=australia&pubname=australia-platform-security&ft:locale=en-US)

