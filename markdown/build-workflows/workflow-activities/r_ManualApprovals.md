---
title: Manual Approvals workflow activity
description: The Manual Approvals activity watches and manages any approvals that users add manually outside of the workflow process. This activity only selects approvals that are in the Not requested state.
locale: en-US
release: xanadu
product: Workflow Activities
classification: workflow-activities
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Approval and rollback workflow activities, Workflow activities reference, Workflow activities, Classic Workflow, Build workflows]
---

# Manual Approvals workflow activity

The **Manual Approvals** activity watches and manages any approvals that users add manually outside of the workflow process. This activity only selects approvals that are in the Not requested state.

**Note:** This activity is only available when the workflow runs on a table that extends Task.

If there are no pending manual approvals when this activity executes, the activity immediately completes with a result of **approved**. This activity does not create approval records. Use this activity to pause the workflow when a user adds a manual approval to a record with an associated workflow, and it is in the Not requested state. The workflow waits for the approval to be closed before proceeding.

## Results

The workflow designer can assign a result value using `activity.result` from within a script field of the activity. By default, the result value of the activity is the final approval disposition determined by the approval actions take by the approvers. Possible result values are:

-   Approved
-   Rejected
-   Deleted
-   Cancelled
-   Error

## Input variables

Input variables determine the initial behavior of the activity.

<table id="table_xql_rnw_w4"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Wait for

</td><td>

Indicate what to wait for to indicate that the approval activity is approved or rejected. Options are:

-   **Any manual user or group approval:** Any user can approve and the first approval causes the activity to complete with a result of **approved**.
-   **All manual user or group approvals:** All users must approve \(see below for how a rejection is handled\).
-   **The first response from any manual approval:** The first approval or rejection from any user causes the activity to complete.

</td></tr><tr><td>

When anyone rejects

</td><td>

Indicate what happens when any user rejects their approval request. Options are:

-   **Reject the approval:** Immediately complete the activity with a result of **rejected**.
-   **Wait for other responses before deciding:** Wait until we get other responses before making an approval or rejection decision. This allows users to change their mind until a decision is made.

 In addition, if **Wait for** is set to **Anyone to approve** then a single approval will cause the activity to complete with a result of **approved** even if one or more users reject.

</td></tr></tbody>
</table>## Conditions

The conditions determine which transition runs after this activity.

**Note:** Approval activities run as the user whose actions match the approve or reject conditions the workflow was waiting for and advances the workflow.

|Condition|Description|
|---------|-----------|
|Approved|The users from the groups have approved the request based on the **Wait for** rules.|
|Rejected|The users from the groups have rejected the request based on the **Wait for** rules.|

## States

The activity state tells the workflow engine what to do with the activity.

|State|Description|
|-----|-----------|
|Executing|The workflow engine starts the execute function of the activity.|
|Waiting|The workflow engine ignores the activity until a specific event to restart the activity is fired.|
|Finished|The activity finished running. See the result value for the outcome of the activity.|
|Cancelled|This activity, or the workflow that contains this activity, was canceled.|
|Error|A JavaScript error occurred. Review the logs for error details.|

