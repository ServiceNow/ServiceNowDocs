---
title: Decision Builder system properties
description: Use system properties to set limits on the maximum number of inputs and decisions for decision tables created in Decision Builder.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Decision tables reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Decision Builder system properties

Use system properties to set limits on the maximum number of inputs and decisions for decision tables created in Decision Builder.

These properties are available for decision tables in Decision Builder.

**Note:** To open the System Properties \[sys\_properties\] table where these properties are located, enter `sys_properties.list` in the navigation filter.

<table id="table_qtp_ts3_4fb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

com.glide.decision\_table.excel\_hide\_references

</td><td>

When set to true, decision tables exported to Excel will not include drop-down lists of records for condition or result columns with type = reference.-   Type: true/false
-   Default value: False

</td></tr><tr><td>

com.glide.decision\_table.max\_inputs

</td><td>

Maximum number of decision inputs that can be defined on a model \(sys\_decision\) record.-   Type: integer
-   Default value: Empty. There are no limits on inputs when this property is left empty.

</td></tr><tr><td>

com.glide.decision\_table.max\_questions

</td><td>

Maximum number of decision questions that can be defined on a decision table \(sys\_decision\) record. -   Type: integer
-   Default value: Empty. There are no limits on inputs when this property is left empty.

</td></tr></tbody>
</table>**Note:**

-   A warning message is displayed when the inputs or decisions exceed the maximum limit set by the administrator.
-   By default, decision tables in Decision Builder display the first 20 rows. To view 20 more rows, select **Show more**.

**Parent Topic:**[Decision tables reference](../concept/decision-builder-reference.md)

