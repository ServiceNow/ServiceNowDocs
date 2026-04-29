---
title: Installed with the legacy IBM PVU Process Pack
description: The following tables, fields, script includes, and business rules are installed with the legacy IBM PVU process pack.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Legacy IBM PVU Process Pack, Legacy Software Asset Management plugin, ITSM Software Asset Management, Asset Management, IT Service Management]
---

# Installed with the legacy IBM PVU Process Pack

The following tables, fields, script includes, and business rules are installed with the legacy IBM PVU process pack.

## Tables

|Table|Description|
|-----|-----------|
|Processor Definition \[cmdb\_processor\_definition\]|Each row in this table describes a computer in terms of the attributes IBM uses for its PVU licensing model. A row can be associated with one or more \(if they are all identical in terms of the attributes used for PVU licensing\) discovered computers.|

## Fields

|Field|Table|Description|
|-----|-----|-----------|
|ibm\_pvu\_mapping|Hardware \[cmdb\_ci\_hardware\]|PVU rule that applies to the software installation. Used for IBM PVU-based license counting.|
|ibm\_pvu\_mapping|Software Installation \[cmdb\_sam\_sw\_install\]|PVU rule that applies to the software installation. Used for IBM PVU-based license counting.|

## Script includes

|Name|Description|
|----|-----------|
|ProcessorDefinitionsUtils|Contains utilities for managing the Processor Definition \[cmdb\_processor\_definition\] table.|
|ProcessorValueUnitsUtils|Contains logic that determines the IBM PVU pricing associated with a given processor.|

## Business rules

<table id="table_pch_ywx_23b"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

One and only one default mapping`[sam_ibm_pvu_mapping]`

</td><td>

Ensures only one default mapping by resetting the last resort flag for modified records and setting it to false for new records.

</td></tr></tbody>
</table>**Parent Topic:**[Legacy IBM PVU Process Pack](../concept/c_IBMPVUProcessPack.md)

