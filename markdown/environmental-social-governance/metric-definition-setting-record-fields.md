---
title: Metric definition setting record form
description: Field descriptions for creating a metric definition setting record.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-10-24"
reading_time_minutes: 1
breadcrumb: [Set default values for CMD formula operands, Formula building in a calculated metric definition, Configuring GRC: Metrics, GRC: Metrics, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Metric definition setting record form

Field descriptions for creating a metric definition setting record.

|Field|Description|
|-----|-----------|
|Name|Name for the record..|
|Active|Option to mark the default values record as active.|
|One for null record|You can select relevant operators in the field. If a metric operand is null or undefined during formula execution, and the adjacent operator matches the one selected, the system assigns a default value of 1 to that operand—ensuring the calculation proceeds without error.|
|Order|Determines the priority of the record when multiple records are available. Higher numbers have a higher priority.|
|Skip null record|You can select relevant operators in the field. If a metric operand is null or undefined during formula execution and the adjacent operator matches the one selected, the system will skip that operand from the calculation. This prevents errors and ensures the formula continues without interruption.|
|Zero for null record|You can select relevant operators in the field.If a metric operand is null or undefined during formula execution and the adjacent operator matches the one selected in this field, the system assigns a value of 0 to that operand. This ensures the calculation proceeds without error and maintains consistency in results.|
|Type|The type of the metric definition. This field is automatically set to **Calculated metric definition**.|
|Table name|Specifies the name of the table where the default values are stored. This field is auto-populated.|
|Filter|Specifies the condition under which the default values defined in this record should be applied during CMD formula execution. You can set up multiple criteria conditions.|

**Parent Topic:**[Set default values for CMD formula operands](../concept/activate-default-values-for-cmd-calculations.md)

