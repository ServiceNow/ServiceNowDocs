---
title: Convert existing unattended robots to high density robots in RPA Hub
description: Run multiple unattended automations simultaneously on a single machine by batch converting one or more existing robots to high density robots using the Actions on selected rows option.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Robots, Use, RPA Hub, Workflow Data Fabric]
---

# Convert existing unattended robots to high density robots in RPA Hub

Run multiple unattended automations simultaneously on a single machine by batch converting one or more existing robots to high density robots using the **Actions on selected rows** option.

## Before you begin

You must do this task in the classic environment.

Familiarise yourself with the high density robot concept in RPA Hub. For more information, see [High density robots in RPA Hub](../concept/high-density-robots-rpa-hub.md).

Only the unattended robots that are in **New** or **Disconnected** states and are not associated with any robot pool can be converted to high density robots.

When changing the robot type from high density robot to standard or vice-versa, you must reconnect the unattended robot to ensure seamless execution of automations.

Role required: sn\_rpa\_fdn.rpa\_release\_manager or sn\_rpa\_fdn.rpa\_admin

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **Administration** &gt; **Robots**.

2.  Select one or more unattended robots from the list.

    The selected robots must be in **New** or **Disconnected** states and must not be associated with any robot pool.

3.  From the **Actions on selected rows** drop-down menu, select **Convert to High density robots**.

    ![Convert to High density robots option in the Actions on selected rows drop-down menu.](../image/convert-hdr.png)

4.  In the **Machine Name** field, enter the computer name of the physical or virtual machine that supports multiple user sessions and on which the Unattended Robot application is installed.

5.  In the **Screen Resolution** field, select the screen resolution for the user sessions used by the high density robots.


## Result

The unattended robots are converted to high density robots with the state set to **New**.

