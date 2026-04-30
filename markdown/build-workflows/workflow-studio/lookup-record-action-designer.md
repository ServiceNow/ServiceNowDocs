---
title: Look Up Record step
description: Look up a record from any table based on defined conditions.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Steps, Flows, subflows, and actions reference, Reference, Workflow Studio, Build workflows]
---

# Look Up Record step

Look up a record from any table based on defined conditions.

## Roles and availability

Available as an Workflow Studio action step. Users with the action\_designer role can create a custom action with one or more action steps.

## Fields

<table id="table_fdl_yhf_kcb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Select a table from the list.

</td></tr><tr><td>

Conditions

</td><td>

Set static or dynamic conditions to filter records. To define a static condition applied each time the action runs, define the conditions with the condition builder. To enable flow designers to dynamically apply conditions, define an input of type Conditions and drag-and-drop the input data pill into the **Conditions** field.

 When building a condition that looks up the value of a reference field, use a data pill that explicitly provides the Sys ID value. Ensure the condition has the format **\[reference field\]\[is\]\[Reference type data pill-&gt;Sys ID\]**. For example, both the Change and Incident tables contain a reference field to the User table. To look up change records where the requester is the caller from an incident record, create the condition **\[Requested by\]\[is\]\[Trigger-&gt;incident record-&gt;Caller-&gt;Sys ID\]**. **\[Requested by\]\[is\]\[action-&gt;incident-&gt;Caller-&gt;Sys ID\]** where **incident** is an input variable for an incident record.

</td></tr><tr><td>

Order by

</td><td>

Determines how to sort results when more than one record matches the defined conditions. Select the field you want to use to sort results.

</td></tr><tr><td>

Sort Type

</td><td>

Select whether to sort alphabetically in ascending or descending order.

</td></tr><tr><td>

If multiple records are found

</td><td>

Determines what is returned if more than one record matches the defined conditions. -   Return only the first record
-   Fail the step

</td></tr><tr><td>

Don't fail on error

</td><td>

Determines whether to fail the flow if a record can't be found.

</td></tr></tbody>
</table>## Outputs

These outputs appear in the Data panel. You can use them as inputs elsewhere in your flow.

-   **Record**

    Data type: **Record**

    Record found based on the conditions you specified in the **Conditions** input.

-   **Table**

    Data type: **Table**

    Name of the table associated with the returned record.

-   **Status**

    Data type: **Choice**

    1 if a record was found successfully, and 0 if there was an error.

-   **Error Message**

    Data type: **String**

    Message containing details about why the record could not be found.

    **Note:** This output's value is only populated if the **Status** output's value is 0.


## Action error evaluation

-   **If this step fails**

    Data type: **Choice**

    Option to continue running the next step or go to error evaluation. To use the step status code or message for a custom action error condition, see [Action error evaluation](../concept/action-error-evaluation.md).


## Example

![Example Look Up Record step in an action.](../images/look-up-record-example.png)

**Parent Topic:**[Workflow Studio steps](../concept/steps.md)

