---
title: Approval Coordinator workflow activity
description: The Approval Coordinator activity creates an approval whose outcome depends on the outcome of one or more child activities, including one or more Approval - User, Approval - Group, and/or Manual Approval activities.
locale: en-US
release: yokohama
product: Workflow Activities
classification: workflow-activities
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Approval and rollback workflow activities, Workflow activities reference, Workflow activities, Classic Workflow, Build workflows]
---

# Approval Coordinator workflow activity

The **Approval Coordinator** activity creates an approval whose outcome depends on the outcome of one or more child activities, including one or more **Approval - User**, **Approval - Group**, and/or **Manual Approval** activities.

**Note:** This activity is only available when the workflow runs on a table that extends Task.

To create an **Approval Coordinator** activity, first drag the activity onto the workflow canvas, causing the activity form to display. On the activity form, fill in the appropriate fields, then click **Submit**.

After you click **Submit**, the activity appears on the workflow canvas. From there, specify the child activities by clicking the links that appear on the body of the activity.

When the **Approval Coordinator** activity completes, all pending approvals that were created by any of the **Approval Coordinator** approval activities are immediately set to **No Longer Required**. If a single user is called as an approver twice by the same workflow, such as when a single user is both a product approver and an executive approver, any approvals for that user after the first are skipped.

## Results

The result value of the **Approval Coordinator** activity depends on the approval actions taken by the approvers and the approval conditions specified in the **Wait for** field. Possible result values are:

-   Approved
-   Rejected
-   Deleted
-   Cancelled

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

-   **Any child activity to be approved:** Any child activity \(User, Group, or Manual Approval\) that completes with a result of **approved** causes the **Approval Coordinator** activity to complete with a result of **approved**.
-   **All child activities to be approved:** All child activities of the **Approval Coordinator** activity must complete with a a result of **approved** to cause the **Approval Coordinator** activity to complete with a result of **approved**.
-   **The first approval or rejection from any child activity:** The first child activity that completes with a result of **approved** or **rejected** causes the **Approval Coordinator** activity to complete with the same result.
-   **Condition based on script:**Call a script to determine how to manage an approval or rejection.

</td></tr><tr><td>

When a rejection occursOnly appears if **Wait for** is set to **All child activities to be approved** or **Any child activity to be approved**.

</td><td>

Specify what the coordinator should do when it sees a rejection from any one of the child activities. Options are: -   **Reject the approval:** Immediately complete the **Approval Coordinator** activity with a result of **rejected**.
-   **Wait for other responses before deciding:** Wait until we get other responses from other child activities before making an approval or rejection decision.

This allows users to change their minds until a decision is made.

In addition, if **Wait for** is set to **Any child activity to approve** then a single child activity completion with a result of **approved** will cause the **Approval Coordinator** activity to complete with a result of **approved** even if other child activities have completed with a result of **rejected**.


</td></tr><tr><td>

Approval scriptOnly appears if **Wait for** is set to **Condition based on script**.

</td><td>

If the **Wait for** variable is set to **Condition based on script** this script is called to determine how to handle an approval or rejection. The script needs to set the variable *answer* to , approved or rejected to indicate the overall approval status for this approval. When called, the following variable is available to the script:```
counts.total = total number of child approval activities that are part of this approval
      counts.approved = # of child approval activities that approved so far
      counts.rejected = # of child approval activities that rejected so far
      counts.requested = # of child approval activities that are pending approval
```

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
|Executing|The workflow engine starts the *execute* function of the activity.|
|Waiting|The workflow engine ignores the activity until a specific event to restart the activity is fired.|
|Finished|The activity finished running. See the result value for the outcome of the activity.|
|Cancelled|This activity, or the workflow that contains this activity, was canceled.|
|Error|A JavaScript error occurred. Review the logs for error details.|

**Parent Topic:**[Approval and rollback workflow activities](../concept/c_ApprovalAndRollbackActivities.md)

