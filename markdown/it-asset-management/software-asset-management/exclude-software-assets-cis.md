---
title: Exclude software assets on CIs
description: You may want to manage software assets installed on a subset of your configuration items in the Software Asset Management application.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Software Asset Management administration, Software Asset Management, IT Asset Management]
---

# Exclude software assets on CIs

You may want to manage software assets installed on a subset of your configuration items in the Software Asset Management application.

## Before you begin

Role required: sam\_admin

## About this task

For example, some of your devices may be leased from a third party and you are not responsible for license compliance for the software on those devices. Or, you may want to start with managing software installed on devices only at a specific location \(for example the New York office\). Then, you can expand to managing software on devices in other locations. Convey to the Software Asset Management application which devices you want to exclude. The system excludes any software installed on these devices in license compliance calculations.

## Procedure

1.  In the Hardware \[cmdb\_ci\_hardware\] table, add a true/false column, for example, Exclude from SAM \[u\_exclude\_from\_sam\].

2.  Set the value of the Exclude from SAM column to true for devices you don’t want to manage installed software for in the application.

    **Note:** The default value of the Exclude from SAM column is false. By default, the system manages installed software on all devices.

3.  Navigate to **Software Asset** &gt; **Administration** &gt; **Properties** and then enter the column name, \[u\_exclude\_from\_sam\], in the field next to the property **Enter the name of the true/false field added to cmdb\_ci\_hardware table to exclude software installed on selected devices from Software Asset Management**.

    Ensure that you enter the column name without the brackets.

    Once the scheduled job \(SAM — Adjust Installs for excluded CIs\) runs, the software installed on devices with the Exclude from SAM column set to true are excluded from the application.

4.  To start managing software installs on previously excluded devices in the application, set the value of the Exclude from SAM column for the device to false.

    Once the scheduled job \(SAM — Adjust Installs for excluded CIs\) runs, the system starts managing software installs on these devices.

5.  Complete the following steps to start managing the software installs on all previously excluded devices.

    1.  Navigate to **Software Asset** &gt; **Administration** &gt; **Properties**.

    2.  Delete the column name \[u\_exclude\_from\_sam\] from the property

    3.  Select **Save**.

        Once the scheduled job \(SAM — Adjust Installs for excluded CIs\) runs, the system starts managing the software installed on all previously excluded devices.


**Parent Topic:**[Software Asset Management administration](../concept/c_SAMAdministration.md)

