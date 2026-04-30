---
title: Set default values for CMD formula operands
description: Set default values for formula operands so CMD calculations continue when operand data is missing or undefined.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-10-24"
reading_time_minutes: 1
breadcrumb: [Formula building in a calculated metric definition, Configuring GRC: Metrics, GRC: Metrics, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Set default values for CMD formula operands

Set default values for formula operands so CMD calculations continue when operand data is missing or undefined.

## Before you begin

Role required: sn\_esg.program\_manager

## About this task

If a formula operand has no value because metric data has not yet been collected for an entity, the calculation fails for that operand. You can specify default values in a metric definition mapping record so that the system completes the calculation even when data is unavailable.

## Procedure

1.  Navigate to **All** &gt; **Operational Sustainability Management** &gt; **Administration** &gt; **Metric Definition Mapping**.

2.  Create a new mapping record or modify an existing one.

<table id="choicetable_wzf_jzt_53c"><thead><tr><th align="left" id="d22076e81">

Option

</th><th align="left" id="d22076e84">

Actions

</th></tr></thead><tbody><tr><td id="d22076e90">

**Update an existing record**

</td><td>

1.  Select the record from the list.
2.  Make the necessary edits.
3.  Select **Update**.


</td></tr><tr><td id="d22076e114">

**Create a new record**

</td><td>

1.  Select **New**.
2.  On the form, fill in the fields.

For a description of the field values, see [Metric definition setting record form](../reference/metric-definition-setting-record-fields.md).

3.  Select **Submit**.


</td></tr></tbody>
</table>
-   **[Metric definition setting record form](../reference/metric-definition-setting-record-fields.md)**  
Field descriptions for creating a metric definition setting record.

**Parent Topic:**[Formula building in a calculated metric definition](formula-building-at-metric-definition-and-entity-level.md)

