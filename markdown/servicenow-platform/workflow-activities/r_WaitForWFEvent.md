---
title: Wait for WF Event workflow activity
description: The Wait for WF Event activity causes the workflow to wait at this activity until the specified event is fired.
locale: en-US
release: yokohama
product: Workflow Activities
classification: workflow-activities
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Condition Workflow activities, Workflow activities reference, Workflow activities, Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Wait for WF Event workflow activity

The **Wait for WF Event** activity causes the workflow to wait at this activity until the specified event is fired.

Use this activity to wait for another activity to fire an event. Events from other activities are fired in a script using the workflow.fireEvent\('eventName'\) API call.

## Results

The workflow designer can assign a result value using `activity.result` from within a script field of the activity. This activity transitions when the specified event fires.

## Input variables

The following variables determine the behavior of the activity.

**Note:** Condition activities run as the user whose actions match the conditions the workflow was waiting for and advances the workflow.

|Field|Description|
|-----|-----------|
|Wait for Event|An event name to trigger the workflow.|

## States

The activity state tells the workflow engine what to do with the activity.

|State|Description|
|-----|-----------|
|Executing|The workflow engine knows to start the onExecute function of the activity.|
|Waiting|The workflow engine ignores the activity until a specific event to restart the activity is fired.|
|Finished|The activity finished running. See the result value for the outcome of the activity.|
|Cancelled|This activity, or the workflow that contains this activity, was canceled.|
|Error|A JavaScript error occurred. Review the logs for error details.|

**Parent Topic:**[Condition Workflow activities](r_ConditionActivites.md)

