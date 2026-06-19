---
title: Configure classification settings in SGC Central
description: In SGC Central, you can configure the Service Graph Connector for ServiceNow OT Discovery classifications settings to define how OT Discovery categories are mapped to the CMDB classes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/configure-class-settings.html
release: australia
product: Operational Technology
classification: operational-technology
topic_type: task
last_updated: "2026-05-19"
reading_time_minutes: 1
breadcrumb: [SGC Central, Service Graph Connector for ServiceNow Operational Technology \(OT\) Discovery, Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Configure classification settings in SGC Central

In SGC Central, you can configure the Service Graph Connector for ServiceNow OT Discovery classifications settings to define how OT Discovery categories are mapped to the CMDB classes.

## Before you begin

Role required: admin

## Procedure

1.  When you select Continue in the Configure and test connections step, the Configure classification settings step opens.

2.  Review the classification settings.

    **Note:** The OT Discovery classification settings define how OT Discovery categories are mapped to the target ServiceNow Instance CMDB classes. It also defines how they are configured to additional settings based on classification, such as the configuration item \(CI\) naming strategy and whether to permit OS classification. The default recommended classification settings are provided by the application, which you can then configure for your needs.

    \[Omitted image "config-classification-settings2.png"\] Alt text: Configure classification settings

3.  In this step, you can edit, export, or create settings.

    You can select **Skip** to skip this step.

4.  All the devices that are imported follow a default naming strategy.

5.  You have the flexibility at a class level to change the name.

6.  You can map the Target CMDG Class name to an OT Device type and can change the mapping settings.

7.  If any changes are needed, select the OT Device Type, open the classification settings record, and update the entries in the following fields:

<table id="table_vhj_kzr_m2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

True. If checked, the Classification Setting is used when classifying the devices. If unchecked, the Classification Setting is ignored.

</td></tr><tr><td>

Source Class

</td><td>

The class name of the source asset.

</td></tr><tr><td>

Network type

</td><td>

Defines whether this classification setting is for OT or IT devices only. Leave empty to include both types.If OT devices with a specific category must be classified into a separate class from IT devices, there are two definitions for the OT Discovery Category. One definition has the Network type set to **OT** with the classification for the OT devices. The other definition is set to **IT** for classifying the IT devices.

</td></tr><tr><td>

Target CMDB class

</td><td>

The CMDB class to target when importing the OT Discovery device.

</td></tr><tr><td>

OT device type

</td><td>

For OT devices, you can select the OT device type to apply the device type to the imported OT Discovery devices in the CMDB, if applicable.

</td></tr></tbody>
</table>8.  Select **Continue** to move to the next step.


