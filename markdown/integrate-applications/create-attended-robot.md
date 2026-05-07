---
title: Create an attended robot in RPA Hub
description: Create an attended robot in RPA Hub to run the attended bot process.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Robots, Use, RPA Hub, Workflow Data Fabric]
---

# Create an attended robot in RPA Hub

Create an attended robot in RPA Hub to run the attended bot process.

## Before you begin

Configure the related system property to view the activity stream. For more information, see [Display an activity stream for bot processes and robots in RPA Hub](display-activity-stream-sys-property-rpahub.md).

Role required: sn\_rpa\_fdn.rpa\_release\_manager, or sn\_rpa\_fdn.rpa\_admin

## About this task

A robot runs a bot process \(automation\).

Attended robots can execute attended automations that require human intervention. Using the Attended Robot application, you can run an attended robot to execute the attended bot process \(attended automations\).

An attended robot is mapped to only one user.

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Create a robot by doing one of the following actions.

<table id="choicetable_kgc_jxm_frb"><thead><tr><th align="left" id="d342427e109">

Option

</th><th align="left" id="d342427e112">

Action

</th></tr></thead><tbody><tr><td id="d342427e118">

**From the list icon**

</td><td>

1.  Select the list icon \(![List icon.](../image/rpahublist-icon.png)\).
2.  On the **Lists** tab, under **Administration**, select **Robots**.
3.  Select **New**.


</td></tr><tr><td id="d342427e157">

**From the plus icon**

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

Unique name of the attended robot.

</td></tr><tr><td>

Robot Type

</td><td>

Type of the robot.**Attended**: Robot for an attended automation.

</td></tr><tr><td>

Attended Robot User

</td><td>

Assigned user for the attended robot.The assigned user must have the RPA assisted user role \(sn\_rpa\_fdn.rpa\_assisted\_user\).

 This field appears only when **Attended** is selected from the **Robot Type** field.

</td></tr><tr><td>

Department

</td><td>

Associated department of the robot.This field is automatically filled in based on the department information in the associated Attended Robot User's record.

The value in this field corresponds to the value at the time that the Robot record is created and is not based on real-time data.

</td></tr><tr><td>

Description

</td><td>

Brief description of the robot.

</td></tr></tbody>
</table>4.  Select **Save**.

5.  In the **Activity** and **Compose** fields, view the activity of the form, work notes, and additional comments.


## What to do next

Install Attended Robot. For more information, see [Install Attended Robot](../../rda-runtime/task/install-rda-runtime.md).

Set up the Attended Robot application. For more information, see [Set up Attended Robot](../../rda-runtime/task/set-up-rda-runtime.md).

Create a bot process. For more information, see [Configuring a bot process record in RPA Hub](../concept/create-botprocess.md).

**Related topics**  


[Retire a robot in RPA Hub](retire-robot.md)

[View Audit History](https://www.servicenow.com/docs/access?context=c_HistorySets&version=australia&pubname=australia-platform-security&ft:locale=en-US)

