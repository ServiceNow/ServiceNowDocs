---
title: Create an internal play playbook
description: Create an internal play playbook to define planned or unplanned activities that the customer does not have access to during the engagement lifecycle. This playbook is your starting point to define any internal processes required by your organization.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure customer success, Customer success, Customer Success Management]
---

# Create an internal play playbook

Create an internal play playbook to define planned or unplanned activities that the customer does not have access to during the engagement lifecycle. This playbook is your starting point to define any internal processes required by your organization.

## Before you begin

Role required: sn\_acct\_lc.ale\_success\_agent

## Procedure

1.  Navigate to **Workspace** &gt; **CSM/FSM Configurable Workspace** and select the **List** icon.

2.  Navigate to the **Customer Success** &gt; **All Internal Plays** and click **New**.

3.  In the `Initiate` phase, you can perform the following activities:

    -   Select engagement: In the Number field, a unique number for the internal play is auto populated. In the Engagement field, select the engagement for which the internal play playbook is being created and click **Continue**. An internal play playbook record is created.
    -   Enter core information: In this page, enter the details for the success case record and click **Mark Complete** to move to the next activity. See [Create an internal play playbook record](account-lifecycle-create-internal-play.md) for a detailed description of this form.
    -   Add squad: Select one or more squad members who will involved in the internal play and the related activities and click **Mark Complete** to move to the next stage.
4.  In the `Assist` phase, you can perform the following activities:

    -   Formulate the action steps: Specify the action plan for this playbook. This will appear in the worknote. Click **Send and continue** to proceed to the next activity. The action plan will appear as work in the Activity Stream section of the playbook.
    -   Related work: Click **Create task** to create an internal play task. See [Create an internal play task](account-lifecycle-create-internal-play-task.md) for a detailed description of this form.

        **Note:** Internal play tasks that are in New, In-progress, or Paused state are displayed in this page. To continue to the next activity, update the `State` to Complete or Canceled. After all the internal play tasks have been closed or canceled, click **Mark Complete** to continue with the next activity.

5.  In the Review &amp; Close, you can perform the following activities:

    -   Communicate the final outcome: Enter a comment to describe the final outcome for this playbook. Click **Send and continue** to proceed to the next activity.
    -   Close record: Select the Closure code from the drop down list and Close notes for this playbook and click **Mark Complete**.
6.  Click **Close** after all the activities have been completed.

    The internal play playbook State is set **Closed** and Progress is set to **Completed**.

    **Note:** If after creating the internal play playbook, you close or cancel the playbook, all pending activities and lanes are automatically canceled and playbook State is set to Canceled.


