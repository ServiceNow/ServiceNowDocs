---
title: Types of data sources in Proactive Prompts
description: Data sources are the different type of data retrieving methods from data tables in Proactive Prompts.
locale: en-US
release: xanadu
product: Proactive Prompts
classification: proactive-prompts
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Reference for Proactive Prompts, Proactive Prompts, HR Service Delivery, Employee Service Management]
---

# Types of data sources in Proactive Prompts

Data sources are the different type of data retrieving methods from data tables in Proactive Prompts.

<table id="table_r3c_3dg_vvb"><thead><tr><th>

Data source type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Simple

</td><td>

Retrieves data from a single data table. For example, this type of table can be used to prompt the manager about employee not changing the current role, or prompt the employee about high unused PTO balance.**Note:**

Use the Simple type of data source when you’re sure that the data source output returns one record per user selected from the **User** field. Otherwise, the framework considers only the first record and skips the remaining records. For multiple records, choose the Aggregated data source.

</td></tr><tr><td>

Aggregate

</td><td>

Allows use of aggregate functions on the data source, for example, Count. For example, this type of table can be used to prompt the managers about large number of requests from new hires, or prompt the employee about the number of overdue tasks. **Note:**

-   If the Aggregate value is none, the admin should select a score field from the table to be used in the Threshold evaluation.
-   The aggregation \(Count\) is grouped by the **User** field.

</td></tr><tr><td>

Script

</td><td>

For complex conditions, use this data source to write code and retrieve data. For example, this type of table can be used to prompt the manager about large number of comments on a case.The script should return a comma-separated list of objects with the following key-value pairs:

-   user: sys\_id of the sys\_user record.
-   score: Numerical score string if Collect records is checked.
-   record: sys\_id of the corresponding record in the sourceTable.
-   sourceTable: The table from which the scores are obtained.
-   displayValue: Name shown in the View details.
-   displayLabel: Label name that represents the displayValue.

</td></tr><tr><td>

Performance Analytics Indicator

</td><td>

Uses the data collected by the Performance Analytics job for the selected indicator and breakdown. For example, this type of table can be used to prompt the manager about number of open incidents.**Note:** The Performance Analytics job must be run to process the data. For more information, see [Activate Performance Analytics jobs](../task/activae-pa-indicator-jobs-sdb.md).

</td></tr></tbody>
</table>**Parent Topic:**[Reference for Proactive Prompts](proactive-prompts-reference.md)

**Related topics**  


[Components installed with Proactive Prompts](proactive-prompts-components.md)

[Tokens in Proactive Prompts](proactive-prompts-tokens.md)

[Actions and action groups in Proactive Prompts](proactive-prompts-actions.md)

[Signal data source form](proactive-prompts-signal-datasource-form.md)

[Signal configuration form](proactive-prompts-create-signal-form.md)

