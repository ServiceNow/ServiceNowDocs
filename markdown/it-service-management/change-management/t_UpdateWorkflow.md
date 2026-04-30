---
title: Update the change request workflow
description: Update the change request workflow to reflect the addition of the Complete state.
locale: en-US
release: xanadu
product: Change Management
classification: change-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Tutorial: add a new change management state, Reference section for Change Management, Change Management, IT Service Management]
---

# Update the change request workflow

Update the change request workflow to reflect the addition of the **Complete** state.

## Before you begin

Role required: admin

## About this task

The Change Request – Normal workflow for the **Normal** type change request must be updated to progress the change request to **Complete** instead of **Review**.

In case of a change request of type **Normal**, in the **Assess** state, any user from the **Assignment group** can approve the change request. When the value of **Risk** is **Moderate** or **High**, a CAB approval is initiated in the **Authorization** state. In case the **Risk** is **Low**, an approval from the CAB team is not required. Instead, the manager of the assignment group can approve the change request.

**Note:** If the manager of the assignment group also happens to be the user who had approved the change request in the **Assess** state, the **Authorize** state is skipped and the state of the change request is set to **Scheduled**.

The functionality is available only for the new customers.

## Procedure

1.  Navigate to **All** &gt; **Workflow** &gt; **Workflow Editor**.

2.  Select **Change Request – Normal** from the list of workflows.

3.  Select the **Checkout** option from the **Context** menu to create a new version of this workflow.

4.  Open the **Set Values** activity that transitions to the **End** activity and modify the following fields.

    |Field|Value|
    |-----|-----|
    |Name|Move to Complete|
    |Set these values|State = Complete|

    ![Set Values activity properties](../image/Change_Workflow2.png)

5.  Click **Update**.

6.  Open the **Wait for conditions** activity that transitions to the End activity and modify the following fields.

    |Field|Value|
    |-----|-----|
    |Name|Change moves to Complete|
    |Set these values|\[State\] \[is\] \[Complete\]|

    ![Editing the condition](../image/Change_Workflow1.png)

7.  Click **Update**.

8.  Open the Workflow Actions menu and click **Publish**.


**Parent Topic:**[Tutorial: add a new change management state](t_AddNewStateTutorial.md)

**Previous topic:**[Create a process flow record](t_CreateNewProcessFlowRecord.md)

**Next topic:**[Change Management workflows](../concept/change-workflows.md#)

