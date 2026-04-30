---
title: Configure action steps within an action item
description: For an action item to perform multiple processes you must define separate action steps.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configure an action item, Action functions, Mobile functions, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure action steps within an action item

For an action item to perform multiple processes you must define separate action steps.

## Before you begin

To add action steps to an action item, the action item **Type** field must be **MultiStep**.

Role required: admin

## About this task

Use action steps when you must perform multiple actions after an action item is executed. You can also use action steps when an action must be performed in offline mode. For more information about working in offline mode, see [Configure data items in offline mode](config-offline-data-item.md).

## Procedure

1.  Navigate to **All** and in the filter enter `sys_sg_write_back_action_step.list`

2.  From the Actions steps form, select **New**.

3.  In the Action step new record form, complete the fields as needed.

<table id="table_arb_2lx_ztb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

A name for the action step. You can have multiple action steps associated with an action item. Make sure you choose a name that is easily identifiable.

</td></tr><tr><td>

Order

</td><td>

The order in which the action step is performed. The lower the number, the earlier the action is performed.

</td></tr><tr><td>

Active

</td><td>

Whether this action step should be implemented or not.

</td></tr><tr><td>

Writeback action item

</td><td>

The action item associated with this action step.**Note:** When associating action steps to an action item the action item **Type** field must be **MultiStep**.

</td></tr><tr><td>

Applicable for

</td><td>

Option for determining whether this action step is to be performed for online actions, offline mode actions, or for both online and offline modes.

</td></tr><tr><td>

Description

</td><td>

Information to help you identify the action step.

</td></tr><tr><td>

Type

</td><td>

The type of action step. Choose from the following:-   New
-   Update
-   Delete
-   Script

**Note:** Different fields appear on the action step form depending on the type of action that you select.

</td></tr><tr><td>

Use current record as condition

</td><td>

Whether you want a separate set of query conditions for the action step. If selected, the **Query conditions** field is inactive. For update or delete actions, you must define the record you are updating or deleting by providing a sys\_id. Marking **Use current record as condition** as true allows you to update or delete actions without creating a parameter.

</td></tr><tr><td>

Table

</td><td>

The table the action step applies to, for example, Incident.

</td></tr><tr><td>

Query condition

</td><td>

Filter conditions that apply to the action step.

</td></tr><tr><td>

Set field values

</td><td>

Determines the field values for an action step. For example, if you want to create an action that updates an incident with a state of Resolved, use the field values **State** = **Resolved**. You can also create parametrized items to pass into the field value.

</td></tr><tr><td>

Execution script

</td><td>

The script executed by the action. This field only appears if you select **Script** in the **Type** field.

 To use an input from an input form screen in your scripts, use `parm_input.<InputName>`

 To use a variable from an input form screen in your scripts, use `parm_variable.<VariableName>`

 To view an example of an execution script, see [Configure an action item](sg-studio-create-action-item.md).

</td></tr></tbody>
</table>4.  Repeat the procedure for any additional action steps that you want to add to the selected action item.

5.  Select **Submit**.


