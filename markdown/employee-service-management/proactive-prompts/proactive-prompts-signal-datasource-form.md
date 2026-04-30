---
title: Signal data source form
description: Form to create a data source for the signal.
locale: en-US
release: zurich
product: Proactive Prompts
classification: proactive-prompts
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Reference, Proactive Prompts, HR Service Delivery, Employee Service Management]
---

# Signal data source form

Form to create a data source for the signal.

<table id="table_fsl_sdc_pvb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the signal data source.

</td></tr><tr><td>

Description

</td><td>

Brief description of the signal data source.

</td></tr><tr><td>

Type

</td><td>

The type of data source that you want to create. The available values are:-   Simple
-   Aggregated
-   Scripted
-   Indicator \(Performance Analytics Indicator\)
-   Subflow

For more information, see [Types of data sources in Proactive Prompts](proactive-prompts-data-source.md).

</td></tr><tr><td>

Script

</td><td>

The script to retrieve the data source. Follow the example script provided in the field for successful execution of the script.**Note:** This field is available only when the Scripted option is selected in the **Type** field.

</td></tr><tr><td>

Subflow

</td><td>

Any published subflow created using Workflow Studio as the data source.

</td></tr><tr><td>

Indicator

</td><td>

The type of performance measurement for the Indicator data source type.**Note:** Only automated indicators that are published on the Analytics hub are supported.

</td></tr><tr><td>

Breakdown

</td><td>

The field to group or filter indicator scores by a qualitative attribute such as Priority, Category, or Assignment Group.**Note:** Only breakdowns whose breakdown source field is available in the User \[sys\_user\] table can be selected.

</td></tr><tr><td>

Table

</td><td>

The table used as the source to obtain the data.

</td></tr><tr><td>

Condition

</td><td>

Criteria that must be met to retrieve the data from the table. For example, the condition **\[Available balance\]\[Greater than\]\[10\]** would retrieve an unused PTO balance of more than 10 days.

</td></tr><tr><td>

User field

</td><td>

The field from the data table used to group the data source records.

</td></tr><tr><td>

Applies to

</td><td>

The user configuration to filter the data in the **User** field.

</td></tr><tr><td>

Can be evaluated for a single user

</td><td>

Enables the source to be supported for a single user execution. By selecting this option, the prompt is generated for the current logged-in user at run time.**Note:** For Script and Subflow data source types, an additional parameter is added to handle the user.

</td></tr><tr><td>

Can be evaluated for a given date

</td><td>

Enables the source to be executed for the selected date. By selecting this option, the prompt is generated on the selected date.**Note:** For Script and Subflow data source types, an additional parameter is added to handle the date.

</td></tr><tr><td>

Collect records

</td><td>

Option to get record details when delivering the prompt message.**Note:**

-   If Indicator is selected as the data source type, then the **Collect records** option must also be set to true on the selected indicator record.
-   Selecting this option stores the display field value in the Prompt details \[sn\_pp\_prompt\_details\] table.
-   Selecting this option influences the View details action.
-   If the **Include zero records** field is selected, the **Collect records** option cannot be used.

</td></tr><tr><td>

Display field

</td><td>

A field from the source table that is displayed in the View details action and in the prompt message to represent a record from the table. For example, in the HR Case \[sn\_hr\_core\_case\] table, an HR case can be represented with a case number, a short description, or any other field in the table.**Note:**

-   This field is displayed only when the **Collect records** field is selected.
-   The item token contains the value of this field.

</td></tr><tr><td class="sub-head" colspan="2">

Threshold Condition

</td></tr><tr><td>

Aggregate

</td><td>

Aggregate type. This field is available only when the selected data source is Aggregate.

</td></tr><tr><td>

Condition

</td><td>

Condition for the threshold value. The available values are:-   Less than
-   Less than or is
-   Is
-   Greater than or is
-   Greater than

</td></tr><tr><td>

Value

</td><td>

A value for the condition provided in the **Condition** field. For example, to find the count of more than five overdue tasks, the **Value** number would be 5, and the full condition would be **\[Overdue tasks\]\[Greater than\]\[5\]**.

</td></tr><tr><td>

Score field

</td><td>

The field used for score evaluation.**Note:** This field is available only when the selected data source type is Aggregated and the **Aggregate** field value is None. Only the fields that have numerical values can be selected.

</td></tr><tr><td>

Use percentile

</td><td>

Option to use relative comparison instead of static comparison against a fixed number.

</td></tr><tr><td>

Percentile value

</td><td>

Percentile value for the threshold condition. This field appears only when the **Use percentile** field is selected. The available values are:-   Lower outliers
-   25 percentile
-   Median
-   75 percentile
-   Higher outliers

</td></tr><tr><td>

Include zero records

</td><td>

Option to include users without any records in the table. For example, select this option to send a prompt to the employees who have no PTO balance.**Note:** You can narrow down the users with zero records by selecting a user configuration in the **Applies to** field. For example, you can send prompts to employees in the HR department with no records in the selected table.

</td></tr></tbody>
</table>**Parent Topic:**[Reference for Proactive Prompts](proactive-prompts-reference.md)

**Related topics**  


[Components installed with Proactive Prompts](proactive-prompts-components.md)

[Tokens in Proactive Prompts](proactive-prompts-tokens.md)

[Types of data sources in Proactive Prompts](proactive-prompts-data-source.md)

[Actions and action groups in Proactive Prompts](proactive-prompts-actions.md)

[Signal configuration form](proactive-prompts-create-signal-form.md)

