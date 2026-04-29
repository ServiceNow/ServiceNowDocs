---
title: Lock workflow activity
description: The Lock activity prevents other instances of this workflow from continuing past this activity until the lock is released.
locale: en-US
release: australia
product: Workflow Activities
classification: workflow-activities
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Utility workflow activities, Workflow activities reference, Workflow activities, Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Lock workflow activity

The **Lock** activity prevents other instances of this workflow from continuing past this activity until the lock is released.

Several instances of the same workflow may run concurrently. For example, if a workflow triggers when a record is added to a particular table. That workflow triggers multiple times if multiple records are added one after the other, once by each record insertion. You can use the lock activity to ensure that this instance of the workflow has finished one or more activities before any other instance of the workflow can proceed.

A workflow can explicitly release a lock with the **Unlock** activity. The lock may also be released when the **Max duration** is reached.

When an instance of the workflow reaches the **Lock** activity, it attempts to obtain a lock using the key specified in the lock activity. If another instance has already obtained the lock and has not yet released it, this lock attempt fails. The instance continues trying to obtain the lock until **Max attempts** has been reached.

**Note:**

We recommend placing a one-second timer activity before the lock activity. This helps prevent a rare condition in which the lock activity may not be able to distinguish one workflow instance from another. This condition can occur because the entity owning the lock is not the specific workflow instance, but rather the code-execution thread in which that instance is running. In most cases, each workflow instance runs on a different thread. Adding a timer activity ensures that this is the case.

![Workflow with timer activity before lock activity](../image/WF_lock_with_timer_before.png "Example of Lock Activity Preceded by Timer Activity")

Since a **Lock** activity can only temporarily prevent processing of other workflow instances, do not add activities that cause the workflow to wait between a **Lock** and **Unlock** activity block. This may cause the **Unlock** activity to be unable to acquire the lock to release it and instead take 60 seconds to complete. Restricted wait activities include:

-   Approval activities
-   Task activities
-   Timer activities
-   Wait for condition activity
-   Wait for WF Event activity
-   MID server activities such as a PowerShell script

## Results

|Result|Description|
|------|-----------|
|Success|The activity successfully obtained a lock. This instance of the workflow can proceed past this point, but other instances cannot proceed until the lock is released.|
|Failure|After attempting to obtain the lock **Max attempts** times, the activity could not obtain the lock.|

## Input variables

Input variables determine the initial behavior of the activity.

<table id="table_dfz_zwv_yr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Key

</td><td>

A unique mutex key. The [Unlock activity](r_UnlockActivity-1.md) activity uses this key to release the lock.

</td></tr><tr><td class="subhead" colspan="2">

Duration

</td></tr><tr><td>

Max. duration

</td><td>

The maximum time the lock persists. The lock is released after it reaches this duration. Releasing a lock this way is equivalent to running the **Unlock** activity.

</td></tr><tr><td class="subhead" colspan="2">

Lock attemptsSpecify how the activity behaves if the lock attempt is denied. If the final lock attempt fails, the activity state is set to 'timeout' and the activity result is set to 'failed'.

</td></tr><tr><td>

Max. attempts

</td><td>

Specify the maximum number of times the activity may attempt to obtain the lock.

</td></tr><tr><td>

Delay between attempts

</td><td>

The amount of time required after a failed lock attempt before another lock attempt is allowed.

</td></tr></tbody>
</table>## States

The activity state tells the workflow engine what to do with the activity.

|State|Description|
|-----|-----------|
|Waiting|The workflow engine is waiting to obtain a lock.|
|Finished|The activity successfully obtained the lock.|
|Timeout|The activity could not obtain a lock within the number of attempts specified by the **Max. attempts** input variable.|

