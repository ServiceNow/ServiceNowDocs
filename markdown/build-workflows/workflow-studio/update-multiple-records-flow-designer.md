---
title: Update Multiple Records action
description: Look up and update multiple records as a single action. Using this action removes the need to separately look up a list of records and then process the list with For Each flow logic. Set field values with a template or add and configure them using data pills.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Workflow Studio actions, Flows, subflows, and actions reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Update Multiple Records action

Look up and update multiple records as a single action. Using this action removes the need to separately look up a list of records and then process the list with For Each flow logic. Set field values with a template or add and configure them using data pills.

## Roles and availability

Available as a Workflow Studio ServiceNow core action. Users with the flow\_designer or admin role can add an action to a flow and define configuration details.

## Fields

<table id="table_jx4_l23_pkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Select the table containing the records to look up and update.

</td></tr><tr><td>

Conditions

</td><td>

Define the filter conditions used to look up records.

</td></tr><tr><td>

Field Values

</td><td>

Set static or dynamic values of fields in the record. For example, to set the short description to a static value, select **Short description** and set the desired value.

 To add dynamic values, see [Create a template value input](../task/template-value.md).

 **Important:** The system does not support updating multiple journal fields such as the additional comments or work notes of a task record.

</td></tr><tr><td>

Order by

</td><td>

Select the field you want to use to sort the records when more than one record matches the defined conditions.

</td></tr><tr><td>

Sort Type

</td><td>

Determine whether to sort the records alphabetically in ascending or descending order.

</td></tr><tr><td>

Don't fail on error

</td><td>

Specify whether to continue running the flow when there is an error.

</td></tr></tbody>
</table>## Example

![Example Update Multiple Records action in a flow.](../images/update-multiple-records-flow-designer.png)

## Outputs

<table id="table_ewh_qqm_tkb"><thead><tr><th>

Field

</th><th>

Description

</th><th>

Data Type

</th></tr></thead><tbody><tr><td>

Count

</td><td>

Number of records updated. If no records are updated, the count is 0.

</td><td>

Integer

</td></tr><tr><td>

Error Message

</td><td>

Message that displays if the action produces an error.

</td><td>

String

</td></tr><tr><td>

Status

</td><td>

The completion status of the action as a numeric value.-   0 \(success\)
-   1 \(error\)

</td><td>

Choice

</td></tr></tbody>
</table>**Parent Topic:**[Workflow Studio actions](../concept/flow-actions.md)

