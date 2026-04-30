---
title: Create an Operational Technology device in the Industrial Workspace
description: Create an Operational Technology \(OT\) device in the Industrial Workspace.
locale: en-US
release: yokohama
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: task
last_updated: "2025-06-20"
reading_time_minutes: 1
breadcrumb: [Use, Operational Technology Manager, Operational Technology]
---

# Create an Operational Technology device in the Industrial Workspace

Create an Operational Technology \(OT\) device in the Industrial Workspace.

## Before you begin

Role required: cmdb\_ot\_editor

## About this task

You can manually create an OT device in the Industrial Workspace, which creates an OT Entity \[cmdb\_ot\_entity\] record and associates it with a CI.

## Procedure

1.  Navigate to **All** &gt; **Industrial Workspace**.

2.  Select the **List** \(![List icon](../../../common/image/icon-list.png)\) icon.

3.  Under the **Operational Technology \(OT\)** module, select one of the following lists.

    -   All OT Devices
    -   OT Supervisory Systems
    -   OT Control Systems
    -   OT Field Devices
    -   OT Computer and Servers
    -   OT Network Gear
    -   Industrial IoT \(IIoT\)
    -   OT Systems
    -   Unclassed OT Devices
4.  Select **Create New CI**.

5.  In the Create OT CI tab, complete the following sections as needed.

    -   Select class
    -   Required attributes
    -   Additional attributes
    -   Relationship definition
    -   Review
6.  Select **Create**.

7.  In the New CI created window, select **Review new CI** to redirect you to the form of the created OT CI.

    If there's an existing CI, select **Review existing CI**.

8.  On the form, fill in the following fields.

<table id="table_inf_nzl_d1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display name

</td><td>

The name of the OT device displayed in the record.**Note:** You can add any string value to this field. Multiple devices can have the same OT display name. This is meant for easier understanding of the OT device and is different from the unique CI name generated when you import OT devices from the staging table.

</td></tr><tr><td>

Purdue level

</td><td>

Assigned Purdue level. The level ranges are 0–5.**Note:** To learn more about the Purdue levels in Industrial Control Systems, see [https://subscription.packtpub.com/book/networking\_and\_servers/9781788395151/1/ch01lvl1sec10/the-purdue-model-for-industrial-control-systems](https://subscription.packtpub.com/book/networking_and_servers/9781788395151/1/ch01lvl1sec10/the-purdue-model-for-industrial-control-systems).

</td></tr><tr><td>

Device criticality

</td><td>

Measure of the relative risk to the site process if the device fails:-   1 - Most critical
-   4 - Not critical


</td></tr><tr><td>

Site

</td><td>

The top-level parent entity, or industrial site, where the device is located or assigned to.

</td></tr></tbody>
</table>9.  Select **Save**.


**Parent Topic:**[Using the Operational Technology Manager](../concept/using-operational-technology-manager.md)

