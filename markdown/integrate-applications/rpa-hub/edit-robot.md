---
title: Edit an unattended robot in RPA Hub
description: Edit an existing unattended robot in RPA Hub to modify a few details of the robot, convert the robot to a high density robot, and view the robot state.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Manage, RPA Hub, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Edit an unattended robot in RPA Hub

Edit an existing unattended robot in RPA Hub to modify a few details of the robot, convert the robot to a high density robot,and view the robot state.

## Before you begin

Create an unattended robot. Ensure to select the **Robot Type** field as **Unattended**. For more information, see [Creating an attended or an unattended robot in RPA Hub](../concept/create-robot.md).

You cannot edit an attended robot.

Verify that the life-cycle stage of the robot is **In Maintenance** on the robot form.

When changing the robot type from high density robot to standard or vice-versa, you must reconnect the unattended robot to ensure seamless execution of automations.

Role required: sn\_rpa\_fdn.rpa\_release\_manager or sn\_rpa\_fdn.rpa\_admin

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(![List icon.](../image/rpahublist-icon.png)\).

3.  On the **Lists** tab, under **Administration**, select **Robots**.

4.  Select the unattended robot that you want to modify.

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

</td></tr><tr><td>

High density robot

</td><td>

Option to create multiple robots with the same machine name.The machine must support multiple user sessions at the same time so that you can run multiple automations simultaneously.

**Note:** If you change the robot type from high density robot to standard or vice-versa, you must reconnect the unattended robot to ensure seamless execution of automations.

</td></tr><tr><td>

Screen resolution

</td><td>

Screen resolution used by a high density robot while establishing the RDP connection before executing the automation.You can have different screen resolutions for different high density robots that use the same machine name. But, it is ideal for all high density robots associated to the same bot process to have same screen resolution value.

This field appears only when the robot is marked as high density robot.

**Note:** You can change the default value of the screen resolution using the **sn\_rpa\_fdn.robot\_screen\_resolution** RPA Hub system property.

</td></tr><tr><td>

User

</td><td>

Authorized user who can access this robot.If you're upgrading to Xanadu, the **User** field is automatically mapped with the user name \(the user\) who has recently created the process job for the selected unattended robots. If no process jobs are found for a selected robot, the robot is moved to the In Maintenance status. An RPA release manager must manually map the appropriate users to the robots.

**Note:** This field appears when the **sn\_rpa\_fdn.enable\_unattended\_robot\_user\_mapping** system property is enabled.

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

