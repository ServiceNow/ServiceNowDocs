---
title: Data type descriptions
description: The following is a list of the most common data types for creating a variable.
locale: en-US
release: australia
product: Policy as Code Engine \(PaCE\)
classification: policy-as-code-engine-pace
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create new variables for policy, Passing parameters to PaCE policies, Administer PaCE policies, Policy as Code Engine \(PaCE\), Extend ServiceNow AI Platform capabilities]
---

# Data type descriptions

The following is a list of the most common data types for creating a variable.

<table id="table_i5g_2yk_pwb"><thead><tr><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Basic Date/Time

</td><td>

Day and time of day, which can be selected with a calendar widget.

</td></tr><tr><td>

Basic Time

</td><td>

Specific time.

</td></tr><tr><td>

Choice

</td><td>

Script that returns an array of choices that will be displayed for selection in a drop-down menu. If you select the **Multi select** check box, then multiple options can be selected from the drop-down. If it’s unselected, then only one option can be selected.

</td></tr><tr><td>

Data Array

</td><td>

Data Array structure represented as a String.

</td></tr><tr><td>

Data Object

</td><td>

The Data Object input enables you to select the plus icon ![Add icon.](../../devops-config/image/pace-output-type-add.png) to add a new property to the data object or the minus icon ![Delete icon.](../../devops-config/image/pace-output-type-delete.png) to delete it. Additionally, you can select the Star icon ![Wild card icon.](../../devops-config/image/pace-star-icon.png) that will search for a name if you don't know the structure of the JSON format property. A JSON path and match criteria field will appear and enable you to search for a key in the JSON structure.

</td></tr><tr><td>

Decimal

</td><td>

Number with up to two digits after the decimal points.

</td></tr><tr><td>

Email

</td><td>

Email represented as a String.

</td></tr><tr><td>

Integer

</td><td>

Number with zero decimal points.

</td></tr><tr><td>

IP Address

</td><td>

Variable character field that stores IPv4 and IPv6 addresses.

</td></tr><tr><td>

JSON

</td><td>

JavaScript Object Notation represented as a String.

</td></tr><tr><td>

Other Date

</td><td>

Date, which can be selected with a calendar widget.

</td></tr><tr><td>

Reference

</td><td>

Query that displays records from another table. The data type includes a match criteria field and qualifier conditions that you can set.

</td></tr><tr><td>

String

</td><td>

For 255 characters or less, the string field is a single-line text field.

</td></tr><tr><td>

Sys ID \(GUID\)

</td><td>

Field that contains a unique identifier for each record.

</td></tr><tr><td>

True/False

</td><td>

Boolean field that appears as a one-digit integer.

</td></tr></tbody>
</table>