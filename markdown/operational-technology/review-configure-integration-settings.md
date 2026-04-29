---
title: Review and configure integration settings
description: The Service Graph Connector for ServiceNow OT Discovery offers configurable options. These options let you customize the integration behavior to meet your business needs.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Service Graph Connector for ServiceNow Operational Technology\(OT\) Discovery, Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Review and configure integration settings

The Service Graph Connector for ServiceNow OT Discovery offers configurable options. These options let you customize the integration behavior to meet your business needs.

## Before you begin

Be sure to complete all previous configurations for the Service Graph Connector for ServiceNow OT Discovery before beginning the following tasks.

Role required: admin

## About this task

The application provides recommended default Classification Settings that define how OT Discovery categories map to CMDB classes. You can customize these settings to meet your needs, including the category mappings, CI naming strategy, and OS classification preferences.

## Procedure

1.  Select **Configure classification settings**.

2.  Next to the Configure classification settings task, select **Configure**.

3.  Review the default OT Discovery Classification Settings.

4.  All the devices that are imported follow a default naming strategy.

5.  You have the flexibility at a class level to change the name.

6.  You can map the Target CMDG Class name to an OT Device type and can change the mapping settings.

7.  If any changes are needed, open the OT Discovery Classification Setting record and update the entries in the following fields.

<table id="table_vhj_kzr_m2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

If checked, the Classification Setting is used when classifying the devices. If unchecked, the Classification Setting is ignored.

</td></tr><tr><td>

Source Class

</td><td>

The class name of the source asset.

</td></tr><tr><td>

Network type

</td><td>

Defines whether this classification setting is for OT or IT devices only. Leave empty to include both types.If OT devices with a specific category need to be classified into a separate class from IT devices, there are two definitions for the OT Discovery Category. One definition has the Network type set to **OT** with the classification for the OT devices. The other definition is set to **IT** for classifying the IT devices.

</td></tr><tr><td>

Target CMDB class

</td><td>

The CMDB class to target when importing the OT Discovery device.

</td></tr><tr><td>

OT device type

</td><td>

For OT devices, you can select the OT device type to apply the device type to the imported OT Discovery devices in the CMDB, if applicable.

</td></tr></tbody>
</table>8.  Next, **Configure system properties**.

9.  Next to the Configure system properties task, select **Configure**.

    ![Configure Systems properties](../images/config-sys-properties-sgc.png)

10. The Configure System properties window opens.

11. Review the System properties and adjust as needed for your instance configuration.

<table id="table_fc2_xcs_m2c"><thead><tr><th>

System property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\(Optional\) Comma-separated list of OT Discovery categories to filter the Asset imports.

</td><td>

Filters the Asset import to only import assets of particular categories. For example, if you wanted to only import ICS Host and PLC category devices from the OT Discovery Console, you could set this to `PLC,IcsHost`.Default: blank

**Note:** These are categories defined on the Console side.

</td></tr><tr><td>

API Page Size

</td><td>

Maximum number of rows to be returned from a single REST call. Default: 500

</td></tr><tr><td>

API Max Timeout

</td><td>

Maximum amount of time to wait for a response when making REST calls to OT Discovery.Default: 30000

</td></tr><tr><td>

Load Raw API Data into Staging Table

</td><td>

When set to true, the raw API data for each row is included in the staging tables along with the parsed data. This is useful when trying to compare data imported data into ServiceNow versus what is available in the OT Discovery API.

</td></tr><tr><td>

Log Levels

</td><td>

Logging level verbosity to use for the application.Default: Info

</td></tr></tbody>
</table>12. Select **Save** and close the window.

13. Return to the Configure system properties task and select **Mark as complete**.

14. Return to the Guided Setup page.


## What to do next

The next setup step is to [Set up scheduled import jobs](setup-scheduled-jobs.md).

