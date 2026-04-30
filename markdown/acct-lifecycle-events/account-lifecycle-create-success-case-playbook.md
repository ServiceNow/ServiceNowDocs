---
title: Create a customer play
description: Create a customer play in collaboration with customers to define planned and unplanned activities that are required to support an engagement. The customer play playbook is your starting point to configure the success processes required in your organization.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Manage playbooks, Customer success, Configure, Customer Success Management]
---

# Create a customer play

Create a customer play in collaboration with customers to define planned and unplanned activities that are required to support an engagement. The customer play playbook is your starting point to configure the success processes required in your organization.

## Before you begin

Role required: sn\_acct\_lc.customer\_success\_agent

## Procedure

1.  Navigate to **Workspace** &gt; **CSM/FSM Configurable Workspace** and select the **List** icon.

2.  Navigate to the **Customer Success** &gt; **All Customer Plays** and select **New**.

3.  In the `Initiate` phase, you can perform the following activities:

    -   Select engagement: In the Number field, a unique number for the customer play is auto-populated. In the Engagement field, select the engagement for which the customer play is being created and select **Continue**. A customer play record is created.
    -   Enter core information: In this page, enter the details for the customer play record and select **Mark Complete** to move to the next activity. See [Create a customer play record](account-lifecycle-create-success-case.md) for a detailed description of this form.
    -   Add squad: Select one or more squad members who will involved in the customer play and the related activities and select **Mark Complete** to move to the next stage.
4.  In the `Assist` phase, you can perform the following activities:

    -   Communicate the intended outcome: Enter a comment to describe the expected outcome for this playbook. Select **Send and continue** to proceed to the next activity.
    -   Define the action plan: Specify the action plan for this playbook. This appears in the worknote. Select **Send and continue** to proceed to the next activity.
    -   Related meeting: Create a meeting for this customer play. See &lt;Create meeting&gt; for details.

        **Note:** Meetings that are in a Draft or Scheduled state displayed in the Related meeting page. To continue to the next activity, update the State to Complete or Canceled. After all meetings have been closed or canceled, you can select **Mark Complete** to continue with the next activity.

    -   Related work: Select **Create Task** to create a customer play task. See [Create a customer play task](account-lifecycle-create-success-case-task.md) for a detailed description of this form.

        **Note:** customer play tasks that are in a New, In-progress, or Paused state are displayed in the Related meeting page. To continue to the next activity, update the State to Complete or Canceled. After all customer play tasks have been closed or canceled, select **Mark Complete** to continue with the next activity.

5.  In the Review &amp; Close phase, you can perform the following activities:

    -   Communicate the final outcome: Enter a comment to describe the final outcome for this playbook. Select **Send and continue** to proceed to the next activity.
    -   Close record: Select the Closure code from the drop-down list and Close notes for this playbook and select **Mark Complete**.
6.  When all the activities have been completed, you can select **Close customer play**.

    The customer play record State is set **Closed** and Progress is set to **Completed**.

    **Note:** If after creating the customer play playbook, you close or cancel the playbook, all pending activities, and lanes are automatically canceled and the playbook State is set to Canceled.


-   **[Create a customer play record](account-lifecycle-create-success-case.md)**  
Create a customer play to specify an unplanned activity required to support an engagement. customer plays can be monitored by the customer during the engagement life cycle.
-   **[Close or cancel a customer play](account-lifecycle-cancel-success-case.md)**  
You can close or cancel a customer play and all the related tasks.

**Parent Topic:**[Manage customer success playbooks](../concept/account-lifecycle-manage-cust-succ-playbooks.md)

