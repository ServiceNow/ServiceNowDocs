---
title: Manage an assessment-type action task
description: Create and manage an action task for the Operational vulnerability, where the type of the task is assessment. You can then assign it to an appropriate task owner.
locale: en-US
release: australia
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Creating an action task for the operational vulnerability, Managing Operational vulnerability, Managing Operational Resilience, Operational Resilience, Governance, Risk, and Compliance]
---

# Manage an assessment-type action task

Create and manage an action task for the Operational vulnerability, where the type of the task is assessment. You can then assign it to an appropriate task owner.

## Before you begin

Role required: sn\_oper\_res.manager

## About this task

After completing the steps outlined in this section, the state of the Operational vulnerability record is updated to the **Assessment** state.

## Procedure

1.  Navigate to **Workspaces** &gt; **Operational Resilience Workspace** &gt; **All Operational Vulnerabilities** and open the Operational vulnerability record that is in the **Assessment** state.

2.  In the Operational vulnerability record, select the **Action tasks** related list and select **New**.

3.  On the Create New Action task form, fill in the fields.

    For more information, see [Create New Action task form](../reference/action-task-form.md).

4.  In the **Type** field, select **Assessment**.

    The **Assessment template** field is displayed.

5.  In the Assessment template window, select the assessment template that is used to perform the assessment.

6.  Select **Save**.

    The selected assessment template is displayed in the **Assessment template** field of the Action task form.

    The action task is in the **Draft** state.

7.  Navigate to the Assignment section of the Action task form and assign the task owner in the **Task owner** field.

8.  In the Schedule section, add the due date for the action task in the **Due date** field and select **Save**.

    The action task of assessment type is saved.

9.  To assign the action task to the action task owner, select **Update state** on the action task, update the state to **Assigned** in the Update state window, and select **Submit**.

    The action task is in the **Assigned** state.

    The action task is now assigned to the task owner. The example shows that the task is assigned to the user, Opres manager02.

    ![Action task assigned.](../image/assigned-state-action-task.png)

    An automated email notification as shown in the example is sent to the task owner to notify about the action task and review the task details.

    ![Email notification.](../image/vul-email-action-task.png)

    The task owner logs in, reviews the assigned action task, and completes the next steps.


## What to do next

The task owner then logs in, reviews the assigned action task, and creates an investigation-type action task if necessary, or directly requests for an approval for the assessment-type action task.

For more information, see [Manage an investigation-type action task](update-state-of-action-task.md) and [Request an approval for the action task](request-approval-for-action-task.md).

