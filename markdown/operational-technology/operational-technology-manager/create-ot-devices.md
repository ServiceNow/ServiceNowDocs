---
title: Create an OT device
description: Create an OT device manually in the Import OT Devices staging table.
locale: en-US
release: xanadu
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: task
last_updated: "2025-05-02"
reading_time_minutes: 2
breadcrumb: [Easy import, Service Graph Connector for Microsoft Excel, Use, Operational Technology Manager, Operational Technology]
---

# Create an OT device

Create an OT device manually in the Import OT Devices staging table.

## Before you begin

Role required: ot\_staging\_user, cmdb\_ot\_admin, or admin

## About this task

You can manually create an OT device in the Import OT Devices staging table instead of importing your device through the Excel template.

For more information about using the Excel template, see the following topics:

-   [Download the Excel template](download-excel-template.md)
-   [Prepare your Pre-import OT Worksheet Entry Review tool for Service Graph Connector import](preparing-your-pre-import-ot-worksheet-entry-review-tool-for-sgc-import.md)
-   [Import the Excel template](import-excel-template.md)

## Procedure

1.  Navigate to **All** &gt; **Industrial Workspace Admin** &gt; **OT Manager Admin** &gt; **Import OT Devices - Staging Table**.

2.  Select the **New** button.

3.  From the **What is the type of the device?** list, select the OT device type.

    The device type that you select is automatically added to the form.

4.  On the **SG OT Excel Staging - New Record** form, fill in the fields as needed.

<table id="table_inf_nzl_d1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display name

</td><td>

The name of the OT device displayed in the record.**Note:** You can add any string value to this field. Multiple devices can have the same OT display name. This is meant for easier understanding of the OT device and is different from the unique CI name generated when you import OT devices from the staging table.

</td></tr><tr><td>

Name

</td><td>

Unique CI generated name.

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

Correlation id

</td><td>

Site that the device belongs to.

</td></tr><tr><td>

Site

</td><td>

The top-level parent entity, or industrial site, where the device is located or assigned to.

</td></tr><tr><td>

Equipment model entity path

</td><td>

Equipment model entity path that the device is on.

</td></tr></tbody>
</table>5.  Add any additional info in the following related lists as needed.

    -   Additional Info
    -   Network Adapters
    -   IP Address
    -   Serial Number
    -   OS Info
    -   Control System Info
    -   Control Module Info
    -   Software Info
    -   Memory Module Info
    -   Backup Store Informations
6.  Select **Create OT Device**.


## Result

The OT device is created and added to the staging table.

**Parent Topic:**[Easy import](../concept/easy-import.md)

