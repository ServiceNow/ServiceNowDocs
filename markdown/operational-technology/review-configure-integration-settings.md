---
title: Review and configure integration settings
description: To make the Service Graph Connector for ServiceNow OT Discovery simple to use, set options that let you modify the integration behavior to meet your business needs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/review-configure-integration-settings.html
release: australia
product: Operational Technology
classification: operational-technology
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Service Graph Connector for ServiceNow Operational Technology \(OT\) Discovery, Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Review and configure integration settings

To make the Service Graph Connector for ServiceNow OT Discovery simple to use, set options that let you modify the integration behavior to meet your business needs.

## Before you begin

Be sure to complete all previous configurations for the Service Graph Connector for ServiceNow OT Discovery before beginning the following tasks.

Role required: admin

## About this task

Configure the ServiceNow OT Discovery Classification Settings which define how ServiceNow OT Discovery categories are mapped to target CMDB classes. Configure additional settings based on Classification such as the CI naming strategy and if you permit OS classification. Default recommended classification settings are provided by the application which you can then configure for your needs.

## Procedure

1.  Select **Configure classification settings**.

    1.  Next to the Configure classification settings task, select **Configure**.
    2.  Review the default OT Discovery Classification Settings.

        **Note:** The OT Discovery Classification Settings define how OT Discovery categories are mapped to the target ServiceNow Instance CMDB classes. It also defines how they are configured to additional settings based on classification, such as the configuration item \(CI\) naming strategy and whether to permit OS classification. The default recommended classification settings are provided by the application, which you can then configure for your needs.

    3.  All the devices that are imported follow a default naming strategy.
    4.  You have the flexibility at a class level to change the name.
    5.  You can map the Target CMDG Class name to an OT Device type and can change the mapping settings.
    6.  If any changes are needed, open the OT Discovery Classification Setting record and update the entries in the following fields.

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
</table>2.  Next, **Configure system properties**.

    1.  Next to the Configure system properties task, select **Configure**.

        \[Omitted image "config-sys-properties-sgc.png"\] Alt text: Configure Systems properties

    2.  The Configure System properties window opens.
    3.  Review the System properties and adjust as needed for your instance configuration.

<table id="table_fc2_xcs_m2c"><thead><tr><th>

System property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\(Optional\) Comma-separated list of OT Discovery categories to filter the Asset imports.

</td><td>

Filters the Asset import to only import assets of particular categories. For example, if you wanted to only import ICS Host and PLC category devices from the OT Discovery Console, you could set this to `PLC,IcsHost`.Default: empty

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

When set to true, the raw API data for each row is included in the staging tables along with the parsed data. This is useful when trying to compare data imported data into ServiceNow vs. what is available in the OT Discovery API.

</td></tr><tr><td>

Log Levels

</td><td>

Logging level verbosity to use for the application.Default: Info

</td></tr></tbody>
</table>    4.  Select **Save** and close the window.
    5.  Return to the Configure system properties task and select **Mark as complete**.
    6.  Return to the Guided Setup page.

## What to do next

The next setup step is to[Set up scheduled import jobs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/setup-scheduled-jobs.md).

