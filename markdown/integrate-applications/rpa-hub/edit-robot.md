---
title: Edit an unattended robot in RPA Hub
description: Edit an existing unattended robot in RPA Hub to modify a few details of the robot and to view the robot state.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Managing RPA Hub, RPA Hub, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Edit an unattended robot in RPA Hub

Edit an existing unattended robot in RPA Hub to modify a few details of the robot and to view the robot state.

## Before you begin

Create an unattended robot. Ensure to select the **Robot Type** field as **Unattended**. For more information, see [Creating a robot in RPA Hub](../concept/create-robot.md).

You cannot edit an attended robot.

Verify that the life-cycle stage of the robot is **In Maintenance** on the robot form.

Role required: sn\_rpa\_fdn.rpa\_release\_manager or sn\_rpa\_fdn.rpa\_admin

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(![List icon.](../image/rpahublist-icon.png)\).

3.  On the **Lists** tab, under **Administration**, select **Robots**.

4.  Open the robot that you want to modify.

5.  On the **Details** tab, update the following fields as appropriate.

<table id="table_pyx_mhd_4qb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the robot.

</td></tr><tr><td>

Department

</td><td>

Associated department of the robot.This field is auto-populated based on the department information in the associated Attended Robot User's record.

 The value in this field corresponds to the value at the time the Robot record is created and not on real-time data.

</td></tr><tr><td>

Description

</td><td>

Brief description of the robot.

</td></tr></tbody>
</table>6.  On the form, view the states of the unattended and attended robots.

<table id="table_dvx_x3l_rrb"><thead><tr><th>

State

</th><th>

Description for Unattended Robot

</th><th>

Description for Attended Robot

</th></tr></thead><tbody><tr><td>

New

</td><td>

Default value when a new robot is created or saved.

</td><td>

Default value when a new robot is created or saved.

</td></tr><tr><td>

Available

</td><td>

Robot is connected to the Unattended Robot application.

</td><td>

Attended user is connected to the Attended Robot application.

</td></tr><tr><td>

Busy

</td><td>

Robot has executed executing the automation.

</td><td>

Attended user started the automation by selecting the run icon \(![Run icon.](../../rda-runtime/image/rda-runtime-icon-run.png)\) or desktop in desktop icon \(![Desktop In Desktop icon.](../../rda-runtime/image/rda-runtime-icon-run-desktop.png)\).

</td></tr><tr><td>

Disconnected

</td><td>

Robot is disconnected from the Unattended Robot application.

</td><td>

Either the attended user closed or logged out from the Attended Robot application.

</td></tr><tr><td>

Unresponsive

</td><td colspan="2">

Robot runtime isn’t responding. This state occurs when the difference between current time and last heart beat time equals or greater than the value specified in the **sn\_rpa\_fdn.robot.unresponsive** property.

</td></tr></tbody>
</table>7.  Select **Save**.

8.  In the **Activity** and **Compose** fields, view the activity of the form, work notes, and additional comments.


**Parent Topic:**[Managing RPA Hub](../concept/managing-rpa-hub.md)

