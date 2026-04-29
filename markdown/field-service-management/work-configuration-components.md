---
title: Field Service Work Configurations components
description: Several type of components like tables, business rules, and script includes are installed for Work Configurations.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Components installed with additional plugins, Reference, Field Service Management]
---

# Field Service Work Configurations components

Several type of components like tables, business rules, and script includes are installed for Work Configurations.

Install the Field Service Work Configurations \(com.snc.fsm\_work\_types\) to activate Field Service Work Configurations. For more information see [Configuring Field Service Work Configurations](../concept/configuring-work-configs.md).

## Tables

Field Service Work Configurations add the following table.

<table id="table_byc_cx3_qfc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Work Configuration\[wm\_work\_configuration\]

</td><td>

Stores details about work configurations.

</td></tr></tbody>
</table>## Business rules

Field Service Work Configurations adds the following business rules.

<table id="table_bvg_ty3_qfc"><thead><tr><th>

Business rules

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Block update/delete for default config

</td><td>

Work Configuration\[wm\_work\_configuration\]

</td><td>

Prevents updating or deleting the default work configuration.

</td></tr><tr><td>

PostProcessWmConfigCreation

</td><td>

Work Configuration\[wm\_work\_configuration\]

</td><td>

Handles the post processing of the work configuration.

</td></tr><tr><td>

SNCSM Cache Update With SMConfig Prop Up

</td><td>

SM Configuration \[sm\_config\]

</td><td>

Updates cache when SM Configuration \(sm\_config\) table is updated.

</td></tr><tr><td>

SNCSM Cache Update With SMConfig Update

</td><td>

Work Configuration \[wm\_work\_configuration\]

</td><td>

Updates the cache when the work configuration SMConfig is updated.

</td></tr><tr><td>

Sync interceptor

</td><td>

Work Configuration\[wm\_work\_configuration\]

</td><td>

Handles interceptors based on Work Configuration \[wm\_work\_configuration\]

 table.

</td></tr><tr><td>

Validate

</td><td>

Work Type Category \[wm\_work\_type\_category\]

</td><td>

Validates Work Type category table.

</td></tr><tr><td>

Validate

</td><td>

Work Configuration\[wm\_work\_configuration\]

</td><td>

Validates Work Configuration table.

</td></tr></tbody>
</table>## Script includes

Field Service Work Configurations adds the following script includes.

|Script includes|Description|
|---------------|-----------|
|WorkConfigurationDao|DAO file that contains queries to handle database operations on Work Configuration \(wm\_work\_configuration\) table.|
|WorkConfigurationHelper|Helper class that fetches the details of the SMConfiguration.|
|WorkConfigurationImpl|Implements the `global.WorkConfigurationExtensionPoint` extension point.|
|WorkConfigUtil|Utility functions for Work Configurations.|
|WorkConfigValidationsOOB|Implements extension point `sn_fsm_wt.WorkConfigValidationExtPoint`. This extension point validates insertions or updates made to the tables Work Configuration \(wm\_work\_configuration\) and Work Type Category \(wm\_work\_type\_category\).|

**Parent Topic:**[Components installed with additional plugins for Field Service Management](components-inst-additional-plugin.md)

