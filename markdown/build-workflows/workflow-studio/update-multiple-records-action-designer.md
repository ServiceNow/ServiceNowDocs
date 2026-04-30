---
title: Update Multiple Records step
description: Look up and update multiple records as a single step. Using this step removes the need to separately look up a list of records and then process the list with a Script step. Set field values with a template or add and configure them using data pills.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Steps, Flows, subflows, and actions reference, Reference, Workflow Studio, Build workflows]
---

# Update Multiple Records step

Look up and update multiple records as a single step. Using this step removes the need to separately look up a list of records and then process the list with a Script step. Set field values with a template or add and configure them using data pills.

## Roles and availability

Available as an Workflow Studio action step. Users with the action\_designer role can create a custom action with one or more action steps.

## Fields

<table id="table_gzy_vb3_pkb"><thead><tr><th>

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

Select the field that you want to use to sort the records when more than one record matches the defined conditions.

</td></tr><tr><td>

Sort Type

</td><td>

Determine whether to sort the records alphabetically in ascending or descending order.

</td></tr><tr><td>

Run Business Rules and Workflow

</td><td>

Determine whether to call any business rules and workflows associated with the table.

</td></tr><tr><td>

Update System Fields

</td><td>

Select if you want to automatically update [system fields](https://www.servicenow.com/docs/access?context=r_GlobalDefaultFields&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) such as **Updated by**.

</td></tr><tr><td>

Don't fail on error

</td><td>

Specify whether to continue running the flow when there is an error.

</td></tr></tbody>
</table>## Action error evaluation

-   **If this step fails**

    Data type: **Choice**

    Option to continue running the next step or go to error evaluation. To use the step status code or message for a custom action error condition, see [Action error evaluation](../concept/action-error-evaluation.md).


## Example

![Example Update Multiple Records step.](../images/update-multiple-records-action-designer.png)

## Outputs

<table id="table_zyy_crm_tkb"><thead><tr><th>

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

Message that is displayed if the step produces an error.

</td><td>

String

</td></tr><tr><td>

Status

</td><td>

The completion status of the step as a numeric value.-   0 \(success\)
-   1 \(error\)

</td><td>

Choice

</td></tr></tbody>
</table>**Parent Topic:**[Workflow Studio steps](../concept/steps.md)

