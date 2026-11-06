---
title: Rollback To workflow activity
description: The Rollback To activity transitions directly to the activity specified by the outgoing transition line arrow.The Rollback To activity transitions directly to the activity specified by the transition line arrow.When conditions in a workflow trigger a Rollback To activity, the workflow moves processing backward to a specified activity in the workflow and resets certain activities that have already executed back to their original state. This is useful when handling an unexpected failure or as part of a programmed logical flow.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 3
---

# Rollback To workflow activity

The **Rollback To** activity transitions directly to the activity specified by the outgoing transition line arrow.

**Note:** This activity is only available when the workflow runs on a table that extends Task.

**Rollback To** determines which activities to reset based on the actual workflow sequence \(transition line attachments\) of activities between itself and the transitioned to activity, not the execution order. **Rollback To** then marks all the approvals that have transitioned between the rollback and the transitioned to activity as **Not Yet Requested** and the tasks as either **Open** or **Pending**.

Use the **Rollback To** activity for all workflows in which multiple rollbacks are required. **Rollback To** has no variables.

## Conditions

The conditions determine which transition runs after this activity.

|Condition|Description|
|---------|-----------|
|Always|The event or condition that causes the approval to revert to the previous workflow step.|
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

**Parent Topic:**[Approval and rollback workflow activities]()

## Rollback To behavior

The **Rollback To** activity transitions directly to the activity specified by the transition line arrow.

Use the **Rollback To** activity for all workflows that use multiple or nested rollbacks. **Rollback To** resets the targeted task \(the direct transition\) to **Open**. All tasks that have executed between the **Rollback To** activity and the targeted task \(rolled back task\) are set to **Pending**.

\(0\) Begin

\(1\) Log Message

\(2\) Task 1

\(3\) Task 3

\(4\) Task 2

\(5\) Timer

\(6\) Approval 1

\(7\) Roll back to first task

\(8\) Task 1

\(9\) Task 2

\(10\) Approval 1

\(11\) Log approval

\(12\) Join

\(14\) Send email

\(15\) End

\[Omitted image "WorkflowRollbackTo.png"\] Alt text:

### Transition history

The state of \(3\) Task 3 does not change, since this activity does not directly transition from the rollback target activity. To see what activities were rolled back, select the **Workflow Transition History** related list and look at the **Rolled back** column.

The **Rollback To** activity \(7\) updates the following activities:

\(8\) Task 1: reset to **Open**

\(9\) Task 2: reset to **Pending**

\(10\) Approval 1: reset to **Not Yet Requested**

\[Omitted image "WorkflowTransitionRollbackTo.png"\] Alt text:

## Rollback To activity

When conditions in a workflow trigger a **Rollback To** activity, the workflow moves processing backward to a specified activity in the workflow and resets certain activities that have already executed back to their original state. This is useful when handling an unexpected failure or as part of a programmed logical flow.

When an activity is reset during a workflow rollback, the following happens:

-   Approvals are reset to **Not Requested**.
-   Tasks are reset to either **Open** or **Pending**. A rollback workflow path cannot create new tasks.

Activities that perform external system operations, such as deleting a file or sending an email, are not rolled back. Only approval and task activity states are reset.

A workflow can contain a single rollback, multiple rollbacks, or nested rollbacks in more complex workflows. The **Rollback To** activity resets activities based on the actual workflow sequence \(transition line attachments\) of activities between itself and the transitioned to activity, rather than using the execution order to determine where processing should restart.

