---
title: Review class mappings
description: Review and update the class mappings available for the Service Graph Connector for Microsoft Excel.
locale: en-US
release: yokohama
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring the Service Graph Connector for Microsoft Excel, Service Graph Connector for Microsoft Excel, Use, Operational Technology Manager, Operational Technology]
---

# Review class mappings

Review and update the class mappings available for the Service Graph Connector for Microsoft Excel.

## Before you begin

-   Ensure that the Industrial Core plugin is installed so you can view the class mapping tables available.
-   Role required: admin or cmdb\_ot\_admin

## About this task

The Service Graph Connector for Microsoft Excel uses the configuration available in the Excel SGC Class Mapping \[excel\_sgc\_class\_mapping\] table to determine the best ServiceNow Configuration Management Database \(CMDB\) class each configuration item \(CI\) should be placed into. You can modify these settings at any time but it is best to review the current configuration before running your first import.

## Procedure

1.  Navigate to **All** &gt; **OT Manager Admin** &gt; **Excel SGC Class Mappings**.

2.  Review and update the following fields in the class mapping records as needed.

<table id="table_b2z_zgx_cdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Source Class

</td><td>

The class of the source CI.

</td></tr><tr><td>

Target CMDB class

</td><td>

The expected ServiceNow class for the CI.

</td></tr><tr><td>

OT Device type

</td><td>

The category type that the OT device is classified as. The device type is also the function that the device plays on the OT network. For example:An IT device, such as a server, can be converted to an OT device, and the function it plays on the network is an HMI. Therefore, its class is **server** and its device type is **HMI**.

**Note:** In some cases, there are OT devices with no OT function or OT devices where the device type is unknown. For OT devices with no OT function, select **No OT Function**. For OT devices where the device type is unknown, select **Unknown**.

</td></tr><tr><td>

Allow OS classification

</td><td>

When set to **True**, if an operating system is found on the CI, the target is switched away from the target CMDB class to a ServiceNow class that matches its OS.

</td></tr><tr><td>

Active

</td><td>

When checked, the class mapping is set to **Active**.

</td></tr></tbody>
</table>
**Parent Topic:**[Configuring the Service Graph Connector for Microsoft Excel](../concept/configuring-service-graph-connector-for-excel.md)

