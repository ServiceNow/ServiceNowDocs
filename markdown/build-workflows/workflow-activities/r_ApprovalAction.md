---
title: Approval Action workflow activity
description: The Approval Action activity performs an approval action on the current task.
locale: en-US
release: yokohama
product: Workflow Activities
classification: workflow-activities
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Approval and rollback workflow activities, Workflow activities reference, Workflow activities, Classic Workflow, Build workflows]
---

# Approval Action workflow activity

The **Approval Action** activity performs an approval action on the current task.

Use this activity to mark the current task record as approved or rejected.

**Note:** When an **Approval Action** activity is used to mark a task approved, the activity marks all pending approvals as **No Longer Required**. This activity behaves differently from **Set Values** or **Run Script** when used to set the **Approval** field's value.

## Results

The result value of the activity is the final approval disposition selected by the approver. The result value can be **Approved** or **Rejected**. A workflow designer can assign a result value using the *activity.result* variable from within a script field of the activity.

## Input variables

Input variables determine the initial behavior of the activity.

<table id="table_xql_rnw_w4"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Action

</td><td>

The action to perform on the task. Options are:-   Mark task approved
-   Mark task rejected
-   Mark task requested
-   Disregard pending approvals: the system sets approval records to **no longer required** and marks the activity as **approved**.

</td></tr></tbody>
</table>## Conditions

The conditions determine which transition runs after this activity.

**Note:** Approval activities run as the user whose actions match the approve or reject conditions the workflow was waiting for and advances the workflow.

|Condition|Description|
|---------|-----------|
|Always|The event or condition that causes the approval to move to the next workflow step.|
|Error|The event or condition that generates an error.|
|Skipped|The event or condition that allows a skipped approval.|

## States

The activity state tells the workflow engine what to do with the activity.

|State|Description|
|-----|-----------|
|Executing|The workflow engine starts the execute function of the activity.|
|Waiting|The workflow engine ignores the activity until a specific event to restart the activity is fired.|
|Finished|The activity finished running. See the result value for the outcome of the activity.|
|Cancelled|This activity, or the workflow that contains this activity, was canceled.|
|Error|A JavaScript error occurred. Review the logs for error details.|

**Parent Topic:**[Approval and rollback workflow activities](../concept/c_ApprovalAndRollbackActivities.md)

