---
title: Create a state flow
description: Creating State Flows.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Use state flows, State flows, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create a state flow

Creating State Flows.

## Before you begin

Role required: none

## Procedure

1.  Navigate to **All** &gt; **State Flows** &gt; **State Flows** and click **New**.

2.  Fill in the fields, as appropriate.

    The system enforces the field controls with the same client script that filters the choice list for the State field.

<table id="table_qfl_nwk_cp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Automatically generated record number

</td></tr><tr><td>

Table

</td><td>

\[Required\] Table on which the state flow record runs. Only tables that extend the Task `[task]` table are available in the list.

</td></tr><tr><td>

Starting state

</td><td>

Name of the state at the beginning of the transition. The selections in this field are filtered by the possible states for the table selected.

</td></tr><tr><td>

Ending state

</td><td>

Name of the state at the end of the transition. The selections in this field are filtered by the possible states for the table selected.

</td></tr><tr><td>

Client script

</td><td>

Client script to run for this transition. The client script controls the available states you can select by limiting the contents of the State choice list to valid states. This client script also controls specific field behavior configured for state changes in the Field Controls section of the form.

</td></tr><tr><td>

Event

</td><td>

Name of an existing event to trigger when this transition occurs. See [evernts triggered on state changes](../concept/c_StateFlows.md) for more information.

</td></tr><tr><td>

Name

</td><td>

Name of this record. Make sure the name is descriptive of the state transition or the processing that the record is performing. This name does not have to be unique.

</td></tr><tr><td>

Roles

</td><td>

Not used for any processing.

</td></tr><tr><td>

Active

</td><td>

Enables or disables this state flow record.

</td></tr><tr><td>

Class

</td><td>

Defines the state flow class for this record. The system selects the appropriate class from these options:-   State Flow: Records created for state flows in all task-based tables except those in work management.
-   Work Order Flow: Records created for state flows in the Work Order `[wm_order]` table. This class is available when work management is activated.
-   Work Task Flow: Records created for state flows in the Work Order Task `[wm_task]` table. This class is available when work management is activated.


</td></tr><tr><td>

Dictionary override

</td><td>

Sets the starting value for the State field on all new records for the table named in the state flow record. See [dictionary overrides](../concept/c_StateFlows.md) for configuration procedures.

</td></tr><tr><td>

Work notes

</td><td>

Noteworthy comments about this state flow transition. For details about how these notes are used, see [Work Notes](../concept/c_WorkNotes.md).

</td></tr><tr><td>

Comment

</td><td>

Details about the customized record.

</td></tr><tr><td colspan="2">

Manual \(Runs scripts from a UI action that require the user to click a button or related link.\)

</td></tr><tr><td>

Manual condition string

</td><td>

Conditions for enabling a UI action that cannot be defined with the condition builder. For example, you can use this string to define UI actions for mobile devices. This condition has an \[and\] relationship with the condition in the Manual condition field.

</td></tr><tr><td>

Manual condition

</td><td>

Conditions for enabling a UI action that can be defined for fields in the target table. This condition has an \[and\] relationship with the condition in the Manual condition string field.

</td></tr><tr><td>

Manual script

</td><td>

Script that defines what the UI action does when the conditions are true. This script runs when the user clicks a button or a related link.

</td></tr><tr><td>

UI action

</td><td>

\[Read Only\] Name of the button that the system creates to enable this transition. The system creates the label using the same name as the state flow record that created it.

</td></tr><tr><td colspan="2">

Automatic \(Runs a business rule automatically when a task record is changed and updated.\)

</td></tr><tr><td>

Automatic condition string

</td><td>

Conditions for running the business rule that cannot be defined with the condition builder, such as evaluating if the proposed transition is a valid flow. This condition has an \[and\] relationship with the condition in the Automatic condition field.

</td></tr><tr><td>

Automatic condition

</td><td>

Conditions for running the business rule that can be defined for fields in the target table. This condition has an \[and\] relationship with the condition in the Automatic condition string field.

</td></tr><tr><td>

Automatic script

</td><td>

Script that performs additional work when the condition is true. This script can do tasks such as update the date and time the transition occurred or notify someone using email when a specific state change occurs. Automatic state transitions occur when changes are made to the task record.

</td></tr><tr><td>

Business rule

</td><td>

Name of the business rule created for this transition. Two conditions must be satisfied before this business rule can run. The task must be on a specific starting state, and the Automatic condition must be true. If both of these conditions are satisfied, the business rule performs the transition requested, using the starting and ending states from the State Flow form.

</td></tr><tr><td colspan="2">

Field Controls \(Determines [field properties](../concept/c_StateFlows.md) when a record transitions between states or reaches a specific end state.\)

</td></tr><tr><td>

Mandatory fields

</td><td>

Makes the selected fields required when this transition occurs, or when the end state is the current state.

</td></tr><tr><td>

Read only fields

</td><td>

Prevents the selected fields from being edited when this transition occurs, or when the end state is the current state.

</td></tr><tr><td>

Visible fields

</td><td>

Displays the selected fields when this transition occurs, or when the end state is the current state.

</td></tr><tr><td>

Not mandatory

</td><td>

Makes the selected fields optional when this transition occurs, or when the end state is the current state.

</td></tr><tr><td>

Not read only

</td><td>

Makes the selected fields editable when this transition occurs, or when the end state is the current state.

</td></tr><tr><td>

Not visible

</td><td>

Hides the selected fields when this transition occurs, or when the end state is the current state.

</td></tr></tbody>
</table>3.  Determine if you want the state transition method to be manual or automatic and open the appropriate section on the form.

    -   Manual: Click **Create UI Action** to create a button on the task form that enables users to execute the transition manually. The system uses the value in the Name field as the label for the UI action. The UI action executes the script in the Manual Script field when the conditions are true. For example, a manual transition can create an **Activate** button when an incident is in the New state that enables a user to mark the incident as active.
    -   Automatic: Click **Create Business Rule** to create the business rule. The business rule executes the script in the Automatic Script field when the conditions are true. For example, a business rule created by the system can set an incident state to Assigned when theAssigned to field is populated. Business rules are automatically deleted when the state flow record is deleted. For more information, see Business rules.
4.  Click **Create Client Script** to create the script that limits the values offered in a task record's State field to valid states for that transition.

5.  Configure the fields in the Field Controls section to control how specific fields display when a task record changes states.


**Parent Topic:**[Use state flows](../concept/c_UseStateFlows.md)

**Related topics**  


[Use state flows](../concept/c_UseStateFlows.md)

