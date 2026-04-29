---
title: Installed with the legacy Oracle Process Pack
description: The following tables, fields, and license calculation types are installed with the legacy Oracle process pack.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Legacy Oracle process pack, Legacy Software Asset Management plugin, ITSM Software Asset Management, Asset Management, IT Service Management]
---

# Installed with the legacy Oracle Process Pack

The following tables, fields, and license calculation types are installed with the legacy Oracle process pack.

The information from this table appears in the Software Counter Compliance Violations section of the Software Model form.

<table id="table_rw1_1xp_dq"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Software Counter Compliance Violations \[sam\_sw\_counter\_violation\]

</td><td>

Used to store counter violations that are due to violations other than installs exceeding rights, such as:-   Maximum CPU/user count exceeded \(based on model limits\)
-   Maximum or minimum rights rules not followed \(based on model limits\)
-   Option installed on a server with a non-option-supporting license \(Oracle\)

</td></tr></tbody>
</table>|Field|Table|Description|
|-----|-----|-----------|
|Software counter \[counter\]|Software Counter Compliance Violations \[sam\_sw\_counter\_violation\]|References the software counter that this violation belongs to. \(Reference field to Software Counter table \[sam\_sw\_counter\].\)|
|Cause \[name\]|Software Counter Compliance Violations \[sam\_sw\_counter\_violation\]|An explanation of the violation.|
|Is an option \(is\_option\)|Software Model \[cmdb\_software\_product\_model\]|Indicates if the software model is an option or pack for some other software, such as Active Data Guard or Data Mining options for Oracle Enterprise Edition. This field only appears if the manufacturer is Oracle.|
|License metric \(metric\_type\)|Software License \[alm\_license\]|A glide list reference to the License Calculation \[cmdb\_sw\_license\_calculation\] table. This list contains all of the license calculations that apply to this license and identifies the preferred metric types to use when running software counters.|
|License metric \(metric\_type\)|Hardware \[cmdb\_ci\_hardware\]|A glide list reference to the License Calculation \[cmdb\_sw\_license\_calculation\] table. This list contains all of the license calculations that apply to this license. and identifies the preferred metric types to use when running software counters. This field does not appear on the form by default.|

The Oracle Process Pack adds the following license calculation types.

|Name|Description|
|----|-----------|
|Oracle Named User|Oracle licensing scheme that counts by the number of unique users.|
|Oracle Named User Plus|Oracle licensing scheme that counts by the number of unique users and devices.|
|Oracle Processor|Oracle licensing scheme that counts by the number of processors on a server.|

**Parent Topic:**[Legacy Oracle process pack](../concept/c_OracleProcessPack.md)

