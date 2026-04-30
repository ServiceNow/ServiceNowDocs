---
title: Bot process configuration form in RPA Hub
description: Use the Bot Process Configuration form to define the preliminary fields for a bot process record.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
keywords: [attended bot process form, unattended bot process form, rpa hub]
breadcrumb: [RPA Hub reference, RPA Hub, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Bot process configuration form in RPA Hub

Use the Bot Process Configuration form to define the preliminary fields for a bot process record.

<table id="table_pyx_mhd_4qb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name of the bot process configuration.The name of the bot process configuration is reused for the bot process that is associated with this configuration record.

</td></tr><tr><td>

Process Type

</td><td>

Type of the bot process:-   **Unattended**: Automations that don’t require any human intervention.
-   **Attended**: Automations that require human intervention.

</td></tr><tr><td>

Order

</td><td>

Execution priority of the bot process:-   **1**: Highest priority
-   **999999**: Least priority

The default value is set to 1.

RPA business user can view this field.

This field appears only when **Unattended** is selected from the **Process Type** field.

</td></tr><tr><td>

Package

</td><td>

Associated package of the bot process.For an unattended bot process, associate an unattended type package.

For an attended bot process, associate an attended type package.

Only published packages can be associated.

</td></tr><tr><td>

Package Version

</td><td>

Version of the active package in use. Only published package versions can be associated.

Ensure that the version belongs to the populated package.

</td></tr><tr><td>

Application

</td><td>

Application that contains this record. This field is auto-generated.Role required to view this field: admin.

</td></tr><tr><td>

Run Time Threshold \(mins\)

</td><td>

Expected duration for the bot process to run.The default value is 60 minutes.

RPA business user can view this field.

This field appears only when **Unattended** is selected from the **Process Type** field.

This is a required field.

</td></tr><tr><td>

Job Purging \(days\)

</td><td>

Number of days after which the job data is deleted.

</td></tr><tr><td>

Description

</td><td>

Description of the bot process.

</td></tr></tbody>
</table>**Parent Topic:**[RPA Hub reference](rpa-hub-reference.md)

**Related topics**  


[Create a bot process configuration record in RPA Hub](../task/create-botprocess-config.md)

[Configuring a bot process record in RPA Hub](../concept/create-botprocess.md)

