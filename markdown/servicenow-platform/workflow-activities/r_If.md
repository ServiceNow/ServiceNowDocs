---
title: If workflow activity
description: The If activity checks a condition or script to determine if a Yes or No transition should be taken.
locale: en-US
release: yokohama
product: Workflow Activities
classification: workflow-activities
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Condition Workflow activities, Workflow activities reference, Workflow activities, Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# If workflow activity

The **If** activity checks a condition or script to determine if a **Yes** or **No** transition should be taken.

If the workflow creator specifies both the **Condition** and the **Advanced** script, both must evaluate successfully for activity to take the **Yes** transition.

## Results

The workflow designer can assign a result value using activity.result from within the **Script** field on the activity record. By default, the result value of the activity is the final result of the condition or script specified. Possible result values are:

-   Yes
-   No

## Input variables

The following variables determine the behavior of the activity.

**Note:** Condition activities run as the user whose actions match the conditions the workflow was waiting for and advances the workflow.

|Field|Description|
|-----|-----------|
|Condition|If specified and the current record matches the condition, the **Yes** transition is taken.|
|Advanced and Script|To specify a script, select the **Advanced** check box. You may then enter a script that is evaluated. If your script sets the variable answer to `yes`, then the **Yes** transition is taken. Otherwise, the **No** transition is taken.|

## Conditions

The following conditions determine which transition comes after the activity.

|Condition| |
|---------|---|
|Yes|Taken when the condition, if specified, matches and the **Advanced** script, if specified, returns yes.|
|No|Taken when either the condition does not match or the **Advanced** script, if specified, returns no.|

## States

The activity state tells the workflow engine what to do with the activity.

|State|Description|
|-----|-----------|
|Executing|The workflow engine knows to start the onExecute function of the activity.|
|Waiting|The workflow engine ignores the activity until a specific event to restart the activity is fired.|
|Finished|The activity finished running. See the result value for the outcome of the activity.|
|Cancelled|This activity, or the workflow that contains this activty, was canceled.|
|Error|A JavaScript error occurred. Review the logs for error details.|

