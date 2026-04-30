---
title: Switch workflow activity
description: The Switch activity checks if the value of a passed field or variable is equivalent to one of several case values.
locale: en-US
release: zurich
product: Workflow Activities
classification: workflow-activities
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Condition Workflow activities, Workflow activities reference, Workflow activities, Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Switch workflow activity

The **Switch** activity checks if the value of a passed field or variable is equivalent to one of several case values.

The switch activity behavior is similar to a switch statement in Java.

When creating a switch activity, select a **Variable** or **Field** to check against activity conditions for a matching field value. When the value passed in this variable or field matches the value defined in the **Condition** field of the activity condition, the workflow progresses through that activity condition.

**Note:** Condition activities run as the user whose actions match the conditions the workflow was waiting for and advances the workflow.

## Results

The variable or field selected in the **Variable** or **Field** activity variable determines the possible result values.

## Input variables

The following variables determine the behavior of the activity.

<table id="table_uml_1qt_jp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Type

</td><td>

Select **Variable** or **Field** as the type of value to check against available conditions. This selection sets the label and available options for the other field.

</td></tr><tr><td>

Variable or Field

</td><td>

Select the source of the value compared against the switch activity conditions. The field label and available options depend on the **Type** selection.

-   **Variable:** select any service catalog variable.
-   **Field:** select any field from the **Table** defined in the workflow properties.

</td></tr></tbody>
</table>## States

The activity state tells the workflow engine what to do with the activity.

|State|Description|
|-----|-----------|
|Executing|The workflow engine knows to start the onExecute function of the activity.|
|Waiting|The workflow engine ignores the activity until a specific event to restart the activity is fired.|
|Finished|The activity finished running. See the result value for the outcome of the activity.|
|Cancelled|This activity, or the workflow that contains this activity, was canceled.|
|Error|A JavaScript error occurred. Review the logs for error details.|

## Example

You can create a switch activity that sets different field values on an incident based on the Assignment group of the incident record.

![](../image/SwitchConditionActivityFieldValues.png "Switch activity example")

The **Field** selected is the incident **Assigned to** field.

![](../image/SwitchActivityFieldAssignedTo.png "Switch activity Field")

If the value of the **Assigned to** field of the workflow-triggering incident is **Service Desk** or **Field Services**, the workflow populates values on the incident record before continuing. If the **Assigned to** value is **Hardware**, the workflow continues without populating any field values.

Condition type \(Standard, Else, or Error\) is used. For more information, see [Manage workflow activity conditions](../../using-workflows/task/t_ManageActivityConditions.md#).

![](../image/ConditionPropertiesHardware.png "Hardware group condition")

**Parent Topic:**[Condition Workflow activities](r_ConditionActivites.md)

