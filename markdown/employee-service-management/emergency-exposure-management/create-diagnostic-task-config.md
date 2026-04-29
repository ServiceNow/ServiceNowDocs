---
title: Create or modify a diagnostic request task configuration
description: Create or modify a diagnostic request task configuration to auto-create a diagnostic request task in a diagnostic request. Based on the selected tracing system in the diagnostic request, the corresponding task configuration creates a diagnostic request task to identify potentially impacted employees.
locale: en-US
release: australia
product: Emergency Exposure Management
classification: emergency-exposure-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up Emergency Exposure Management, Emergency Exposure Management, Emergency Response Management, Employee Service Management]
---

# Create or modify a diagnostic request task configuration

Create or modify a diagnostic request task configuration to auto-create a diagnostic request task in a diagnostic request. Based on the selected tracing system in the diagnostic request, the corresponding task configuration creates a diagnostic request task to identify potentially impacted employees.

## Before you begin

The **Diagnostic Request Task Configs** module in the application navigator is available only if you have the Contact Tracing application installed.

Role required: admin

## About this task

A diagnostic request task configuration is required only when a tracing system requires additional work to be performed to generate the diagnostic request report. For example, say you select the Wi-Fi access log tracing system in a diagnostic request, and Cisco DNA Spaces is the Wi-Fi input data source. You must work on a diagnostic request task to fetch potentially exposed employees by attaching a Wi-Fi access data file or generating a proximity report from the Cisco DNA Spaces portal.

## Procedure

1.  Navigate to **All** &gt; **Emergency Exposure Management** &gt; **Diagnostic Request Task Configs**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_k4m_3mp_ylb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of diagnostic request task configuration.

</td></tr><tr><td>

Import set table

</td><td>

Staging table in which records are imported from a data source before transforming those records.

</td></tr><tr><td>

Transform map

</td><td>

A set of field maps that define the relationships between fields in an import set and fields in the target table.For example, the target table to maps fields for Wi-Fi access data is Wi-Fi Access Register \[sn\_imt\_tracing\_wifi\_access\_register\].

 During transformation, data is copied from the Import Set table to the target table based on the transform map.

 A single import set field may be mapped to multiple fields on other tables.

</td></tr><tr><td>

Type

</td><td>

Data source type that is queried to identify the potentially impacted employees.

</td></tr><tr><td>

Active

</td><td>

Option for making the configuration active. Only active configurations can create a diagnostic request task.

</td></tr><tr><td>

Instructions

</td><td>

Set of instructions to process and complete the assigned diagnostic request task.

</td></tr><tr><td class="sub-head" colspan="2">

Conditions tab

</td></tr><tr><td>

Table

</td><td>

Diagnostic Request \[sn\_imt\_diagnosis\_diagnostic\_request\] table to check which data source is selected.

</td></tr><tr><td>

Condition

</td><td>

Conditions to get the selected data source in the diagnostic request.

</td></tr><tr><td>

Script condition

</td><td>

Script condition that evaluates any additional parameters.

</td></tr><tr><td class="sub-head" colspan="2">

Post processing tab

</td></tr><tr><td>

Processing script

</td><td>

Script to run after the completion of the data import.

</td></tr></tbody>
</table>4.  Click **Submit**.


## Result

A diagnostic request task configuration for a data source type is created.

