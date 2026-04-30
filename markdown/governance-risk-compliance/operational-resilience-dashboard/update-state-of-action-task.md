---
title: Manage an investigation-type action task
description: Manage an investigation-type action task for the Operational vulnerability. An investigation-type action task is initiated when additional investigation is needed to resolve the vulnerability. If the approver rejects the Operational vulnerability and requests more investigation, the task owner can create an investigation-type of action task, assign it to an appropriate user, review their completed work, and then request an approval again.
locale: en-US
release: xanadu
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Creating an action task for the operational vulnerability, Managing Operational vulnerability, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Manage an investigation-type action task

Manage an investigation-type action task for the Operational vulnerability. An investigation-type action task is initiated when additional investigation is needed to resolve the vulnerability. If the approver rejects the Operational vulnerability and requests more investigation, the task owner can create an investigation-type of action task, assign it to an appropriate user, review their completed work, and then request an approval again.

## Before you begin

Role required: sn\_oper\_res.manager

## About this task

If the approver rejects the vulnerability, its state is updated to **Treatment**. The vulnerability may need further investigation. The task owner completes the following steps to complete the work on the vulnerability record:

1.  Create an investigation-type action task for the vulnerability.
2.  Assign the action task to an appropriate user.
3.  Review the investigation work related to the action task.
4.  Update the vulnerability state to pending approval and request for its approval.

## Procedure

1.  Navigate to **Workspaces** &gt; **Operational Resilience Workspace** &gt; **All Operational Vulnerabilities**.

2.  Navigate to the vulnerability record and select **New** in the Action tasks related list.

    You can open the operational vulnerability record from the list and review the information in the **Details** tab. When an investigation-type action task is created, the state of the record is updated to the **New** state.

3.  On the Create New Action task form, fill in the fields.

    For more information, see [Create New Action task form](../reference/action-task-form.md).

4.  Select the type of the action task as **Investigation**.

5.  Assign the task to a task owner and add people on the watchlist of the action task.

6.  Add a due date for the action task.

7.  Select **Save**.

    The action task is saved in the operational vulnerability record. An email notification is sent to the action task owner about the action task.

8.  To complete work on the action task of the rejected vulnerability record, assign it to an appropriate user.

    An email notification is sent to the user about the action task. The user navigates to the vulnerability action task, review the details, provides observations in the Summary section of the action task form, and saves the action task.

    The task owner receives an email notification about the completion of the work and assigns the action task to the user as outlined in the next step.

9.  Navigate to the action task in the vulnerability record, select **Update state** UI action, select the **Assigned** state, and select **Submit**.

    The action task is assigned to the user. The user completes the next step on the action task.

10. Log in as the user and select **Accept work** in the action task record.

    The user accepts the work and completes the following steps for the action task of the vulnerability record.

    1.  Finish work on the action task, select the **Ready for review** UI action, add work notes in the Confirmation window, and select **Ready for review**.

        The action task is in the **Ready for review** state. A notification is sent to the action task owner about completion of the work.


## What to do next

The task owner reviews the work on the action task and then requests an approval for the vulnerability record. For more information on the steps, see [Request an approval](submit-vul-for-approval.md).

