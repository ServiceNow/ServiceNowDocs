---
title: Create a success case playbook
description: Create a success case playbook to define planned and unplanned activities that are required to support an engagement. The success case playbook is your starting point to configure the success processes required in your organization.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure customer success, Customer success, Customer Success Management]
---

# Create a success case playbook

Create a success case playbook to define planned and unplanned activities that are required to support an engagement. The success case playbook is your starting point to configure the success processes required in your organization.

## Before you begin

Role required: sn\_acct\_lc.ale\_success\_agent

## Procedure

1.  Navigate to **Workspace** &gt; **CSM/FSM Configurable Workspace** and select the **List** icon.

2.  Navigate to the **Customer Success** &gt; **All Success Cases** and click **New**.

3.  In the `Initiate` phase, you can perform the following activities:

    -   Select engagement: In the Number field, a unique number for the success case is auto populated. In the Engagement field, select the engagement for which the success case is being created and click **Continue**. A success case record is created.
    -   Enter core information: In this page, enter the details for the success case record and click **Mark Complete** to move to the next activity. See [Create a success case record](account-lifecycle-create-success-case.md) for a detailed description of this form.
    -   Add squad: Select one or more squad members who will involved in the success case and the related activities and click **Mark Complete** to move to the next stage.
4.  In the `Assist` phase, you can perform the following activities:

    -   Communicate the intended outcome: Enter a comment to describe the expected outcome for this playbook. Click **Send and continue** to proceed to the next activity.
    -   Define the action plan: Specify the action plan for this playbook. This will appear in the worknote. Click **Send and continue** to proceed to the next activity.
    -   Related meeting: Create a meeting for this success case. See &lt;Create meeting&gt; for details.

        **Note:** Meetings that are in a Draft or Scheduled state displayed in the Related meeting page. To continue to the next activity, update the State to Complete or Canceled. After all meetings have been closed or canceled, you can click **Mark Complete** to continue with the next activity.

    -   Related work: Click **Create Task** to create a success case task. See [Create a success case task](account-lifecycle-create-success-case-task.md) for a detailed description of this form.

        **Note:** Success case tasks that are in a New, In-progress, or Paused state are displayed in the Related meeting page. To continue to the next activity, update the State to Complete or Canceled. After all success case tasks have been closed or canceled, click **Mark Complete** to continue with the next activity.

5.  In the Review &amp; Close phase, you can perform the following activities:

    -   Communicate the final outcome: Enter a comment to describe the final outcome for this playbook. Click **Send and continue** to proceed to the next activity.
    -   Close record: Select the Closure code from the drop down list and Close notes for this playbook and click **Mark Complete**.
6.  When all the activities have been completed, you can click **Close success case**.

    The success case record State is set **Closed** and Progress is set to **Completed**.

    **Note:** If after creating the success case playbook, you close or cancel the playbook, all pending activities and lanes are automatically canceled and playbook State is set to Canceled.


