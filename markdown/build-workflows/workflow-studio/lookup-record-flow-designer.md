---
title: Look Up Record action
description: Look up a record from any table based on defined conditions.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Actions, Flows, subflows, and actions reference, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Look Up Record action

Look up a record from any table based on defined conditions.

## Roles and availability

Available as a Workflow Studio ServiceNow core action. Users with the flow\_designer or admin role can add an action to a flow and define configuration details.

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

Conditions the returned record must meet.

 When building a condition that looks up the value of a reference field, use a data pill that explicitly provides the Sys ID value. Ensure the condition has the format **\[reference field\]\[is\]\[Reference type data pill-&gt;Sys ID\]**. For example, both the Change and Incident tables contain a reference field to the User table. To look up change records where the requester is the caller from an incident record, create the condition **\[Requested by\]\[is\]\[Trigger-&gt;incident record-&gt;Caller-&gt;Sys ID\]**.

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

Determines what information to return when more than one record matches the defined conditions. -   Return only the first record
-   Fail the step

</td></tr><tr><td>

Don't fail on error

</td><td>

Determines whether to fail the flow when the lookup can't find a record.

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

    0 if a record was found successfully, and 1 if there was an error.

-   **Error Message**

    Data type: **String**

    Message containing details about why the record could not be found.

    **Note:** This output's value is only populated if the **Status** output's value is 1.


## Example

![Example Look Up Record action in a flow.](../images/flow-example-look-up-record.png)

**Parent Topic:**[Workflow Studio actions](../concept/flow-actions.md)

