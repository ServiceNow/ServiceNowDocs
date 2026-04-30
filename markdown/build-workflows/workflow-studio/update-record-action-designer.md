---
title: Update Record step
description: Update an existing record in a table. You can dynamically add and configure fields for the record, or use a template to set field values.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2025-03-10"
reading_time_minutes: 1
breadcrumb: [Workflow Studio steps, Flows, subflows, and actions reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Update Record step

Update an existing record in a table. You can dynamically add and configure fields for the record, or use a template to set field values.

## Roles and availability

Available as an Workflow Studio action step. Users with the action\_designer role can create a custom action with one or more action steps.

## Fields

<table id="table_zmc_z3f_kcb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Record

</td><td>

The record to be updated. Drag-and-drop a record data pill or use the data pill picker to select a record.**Warning:** When using script to select a record, always add a condition to check for a matching record. Some GlideRecord methods return a list of records whenever the method query produces no results. Without a condition check, the action may update all records in a table. For example, this script uses an If condition to verify that a record exists. If the record exists, it returns a Sys ID value. If no record exists, it returns a null result.

```
var configurationItem = new GlideRecord('cmdb_ci');
if (configurationItem.get(fd_data.trigger.cmdb_ci.sys_id))
return configurationItem;
else
return null;

```

</td></tr><tr><td>

Table

</td><td>

The table associated with the record. When you select a record, this field is automatically set to the table associated with the record.

</td></tr><tr><td>

Field Values

</td><td>

Set static or dynamic values of fields in the record. For example, to set the short description to a static value, select **Short description** and set the desired value.

 To add dynamic values, see [Create a template value input](../task/template-value.md).

 **Important:** The system does not support updating multiple journal fields such as the additional comments or work notes of a task record.

</td></tr></tbody>
</table>## Action error evaluation

-   **If this step fails**

    Data type: **Choice**

    Option to continue running the next step or go to error evaluation. To use the step status code or message for a custom action error condition, see [Action error evaluation](../concept/action-error-evaluation.md).


**Parent Topic:**[Workflow Studio steps](../concept/steps.md)

