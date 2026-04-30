---
title: Wait for condition workflow activity
description: The Wait for condition activity causes the workflow to wait at this activity until the current record matches the specified condition.
locale: en-US
release: yokohama
product: Workflow Activities
classification: workflow-activities
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Condition Workflow activities, Workflow activities reference, Workflow activities, Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Wait for condition workflow activity

The **Wait for condition** activity causes the workflow to wait at this activity until the current record matches the specified condition.

The workflow evaluates the **Wait for condition** activity each time the current record is updated. Use this activity to pause a workflow indefinitely until a particular criteria is met by a record update. To pause a workflow for a timed duration see [Timer workflow activities](../concept/c_TimerActivities.md).

For workflow to consider the condition met, all conditions specified – whether in the builder or in a script – must be true.

**Note:** A **Wait for condition activity** should only be used to wait for an external event such as a record update, and not one from a workflow setting a value. If you have a workflow setting a value and want to wait for that same field to be seen as 'changed,' try inserting a one-second timer.

## Results

The workflow designer can assign a result value using `activity.result` from within a script field of the activity. The activity transitions when the result value is true.

## Input variables

The following variables determine the behavior of the activity.

**Note:** Condition activities run as the user whose actions match the conditions the workflow was waiting for and advances the workflow.

<table id="table_uml_1qt_jp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Condition

</td><td>

The workflow is paused at this activity until this condition matches the current record.

</td></tr><tr><td>

Condition script

</td><td>

If specified, the workflow is paused at this activity until this script sets the *answer* variable to true.

</td></tr><tr><td>

Enable Timeout

</td><td>

Option to limit the amount of time that the workflow waits for the activity to be completed before continuing.**Note:** Use the **Enable timeout** option to prevent this activity from continuing to run. If the condition to continue is never met, a timeout value specifies when the system skips the Wait for Condition activity and goes to the next item in the workflow. You must set a Duration value to enable a timeout. You can also select a Schedule if you want to compute the duration end date based on a specific work schedule.

</td></tr><tr><td>

Duration

</td><td>

Amount of time that the workflow waits before continuing when the **Enable timeout** option is selected. Enter the time to wait in hours, minutes, and seconds. If you leave this field empty, the workflow does not wait.

</td></tr></tbody>
</table>## States

The activity state tells the workflow engine what to do with the activity.

|State|Description|
|-----|-----------|
|Executing|The workflow engine knows to start the onExecute function of the activity.|
|Waiting|The workflow engine ignores the activity until a specific event to restart the activity is fired.|
|Finished|The activity finished running. See the result value for the outcome of the activity.|
|Cancelled|This activity, or the workflow that contains this activty, was canceled.|
|Error|A JavaScript error occurred. Review the logs for error details.|

**Parent Topic:**[Condition Workflow activities](r_ConditionActivites.md)

