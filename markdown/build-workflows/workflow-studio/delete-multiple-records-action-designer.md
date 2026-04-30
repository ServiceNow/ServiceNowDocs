---
title: Delete Multiple Records step
description: Look up and delete multiple existing records as a single operation. This Workflow Studio step removes the need to first look up a list of records and then delete each record in the list.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Workflow Studio steps, Flows, subflows, and actions reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Delete Multiple Records step

Look up and delete multiple existing records as a single operation. This Workflow Studio step removes the need to first look up a list of records and then delete each record in the list.

## Roles and availability

Available as an Workflow Studio action step. Users with the action\_designer role can create a custom action with one or more action steps.

## Fields

|Field|Description|
|-----|-----------|
|Table|Select the table containing the records to delete.|
|Conditions|Define the filter condition used to look up records.|
|Order by|Select the field that you want to use to sort the records when more than one record matches the defined conditions.|
|Sort Type|Determine whether to sort the records alphabetically in ascending or descending order.|
|Run Business Rules and Workflow|Determine whether to call any business rules and workflows associated with the table.|
|Don't fail on error|Specify whether to continue running the flow when there is an error.|

## Action error evaluation

-   **If this step fails**

    Data type: **Choice**

    Option to continue running the next step or go to error evaluation. To use the step status code or message for a custom action error condition, see [Action error evaluation](../concept/action-error-evaluation.md).


## Example

![Example Delete Multiple Records step.](../images/delete-multiple-records-action-designer.png)

**Note:** The example is for illustration purposes only.

## Outputs

<table id="table_my4_hrm_tkb"><thead><tr><th>

Field

</th><th>

Description

</th><th>

Data Type

</th></tr></thead><tbody><tr><td>

Count

</td><td>

Number of records deleted. If no records are deleted, the count is 0.

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

