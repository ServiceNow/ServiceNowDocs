---
title: Create new process start/end condition
description: Crop your process by setting the new process start condition and new process end condition. This configuration defines which part of the process should be included in the Process Mining project and made available for analysis. The Create new process start and end condition forms have the same fields.
locale: en-US
release: australia
product: Process Mining
classification: process-mining
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Process Mining, Platform Analytics]
---

# Create new process start/end condition

Crop your process by setting the new process start condition and new process end condition. This configuration defines which part of the process should be included in the Process Mining project and made available for analysis. The Create new process start and end condition forms have the same fields.

<table id="table_sxw_r4h_hvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the condition.

</td></tr><tr><td>

Table

</td><td>

Table for the condition. This field is automatically populated with the table selected in your table configuration record.

</td></tr><tr><td>

Condition type

</td><td>

The condition type used for this condition.-   Field/Value condition
-   Contextual field/Value condition
-   Performed by
-   And
-   Or
-   Process start condition
-   Process stop condition

</td></tr><tr><td>

Language

</td><td>

Language for the condition. This field is automatically populated with the current language.

</td></tr><tr><td>

Field

</td><td>

Field used for the condition. These are field from the table in the **Table** field. The designated start and stop field should be configured as activity definition to make the start or stop condition working.

</td></tr><tr><td>

Predicate

</td><td>

The qualifier for the condition.-   is
-   is not
-   is anything
-   is one of
-   is not one of
-   starts with
-   ends with
-   contains
-   does not contain

**Note:** When you select "is one of", you can select multiple values at once. Type the first two letters, and select the **Select all** icon to select all matching values.![Selecting multiple values for is one of predicate](../image/filter-isoneof.gif)

</td></tr><tr><td>

Field value

</td><td>

The value use along with the predicate to define this condition. If the field is a reference field, you can select values using the reference icon \(![Reference icon](../image/reference-icon.png)\).

</td></tr><tr><td>

Occurrence\(s\) to match

</td><td>

Select the occurrence to match for this condition.-   All
-   First only
-   Last only

</td></tr><tr><td>

Contextual Condition

</td><td>

Additional condition that must be true when the current condition is triggered. For example, you configure your condition to trigger when a record is in the New state. If you wanted to also specify that the **Priority** is high, you can do that using the **Contextual Condition** field.

</td></tr></tbody>
</table>**Parent Topic:**[Process Mining reference](../concept/process-mining-reference.md)

