---
title: Create an ad-hoc task on a claim
description: Create a task in a Individual Life Claims case to help prioritize, check the case progress, and plan your claim work. An example is that you can request additional supporting documentation.
locale: en-US
release: xanadu
product: Insurance Claims
classification: insurance-claims
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Managing Individual Life Claims, Individual Life Claims, Claims applications, Insurance applications, Financial Services Operations \(FSO\)]
---

# Create an ad-hoc task on a claim

Create a task in a Individual Life Claims case to help prioritize, check the case progress, and plan your claim work. An example is that you can request additional supporting documentation.

## Before you begin

Role required: sn\_ins\_claim\_indl.dbn\_adjuster, sn\_ins\_claim\_indl.manager

## About this task

You can create additional tasks as needed on a claim by using the **Add task** button from the Actions menu, or by using the **Create a new record** button from the Related records panel.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Create a task from the **claim workspace** tab in a case or from the tasks list.

<table id="choicetable_otl_dtz_pbc"><thead><tr><th align="left" id="d80616e92">

Option

</th><th align="left" id="d80616e95">

Steps

</th></tr></thead><tbody><tr><td id="d80616e101">

**From the claim workspace in a case**

</td><td>

In the Tasks section, select **Add claim task**. The new task has the case set as the parent record.

</td></tr><tr><td id="d80616e113">

**From the tasks list**

</td><td>

1.  Select the lists icon \(![Lists icon.](../../../use/reporting/image/inline-data-vis-list.png)\).
2.  On the **Lists** tab, select **Individual death claims tasks**, and then select **All**.
3.  Select **New**.


</td></tr></tbody>
</table>3.  On the form, fill in the fields.

    For a description of the field values, see [Claim Task form fields](../../fso-common/reference/claim-task-form-fields.md).

4.  In the **Work notes** field, enter any necessary comments.

    The manually posted comments and system-generated work notes are added to the activity stream for the task.

5.  Assign the task to yourself or to another user.

6.  Select **Save**.

    The task status is now New. The active and inactive claim tasks are displayed on the claim case and on the claim Adjuster evaluation step.


## What to do next

After a task is created, the task can move to the following statuses depending on the requirement for the task.

-   Work in Progress: A task has this status if one of the following conditions occurs:
    -   After a new task is assigned to you if you have the either the sn\_ins\_claim\_indl.dbn\_adjuster or sn\_ins\_claim\_indl.manager role.
    -   A task assignee selects **Accept** to accept the task.
    -   A task assignee selects a task that is in the Awaiting info status.
    -   After a task assignee selects **Open task** to continue working on the task.
-   Awaiting info: A task assignee selects **Awaiting info**.
-   Closed complete: A task assignee selects **Close** to close the task.

