---
title: Create an internal play
description: Create an internal play to define planned or unplanned activities that the customer does not have access to during the engagement lifecycle.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/acct-lifecycle-events/customer-success-management/account-lifecycle-create-internal-play-playbook.html
release: australia
product: Customer Success Management
classification: customer-success-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Manage playbooks, Customer success, Use, Customer Success Management]
---

# Create an internal play

Create an internal play to define planned or unplanned activities that the customer does not have access to during the engagement lifecycle.

## Before you begin

Role required: sn\_acct\_lc.customer\_success\_agent

## About this task

An internal play is used to monitor internal activities that the customer does not have access to during the engagement lifecycle. For example, the renewal phase of a contract can be triggered 90-120 days before it is due to expire. This can launch a series of planned internal actions that can increase the chances of the contract being renewed or extended. An internal play can contain one or more sub-tasks and follows a playbook with predefined activities.

## Procedure

1.  Navigate to **Workspace** &gt; **CSM/FSM Configurable Workspace** and select the **List** icon.

2.  Navigate to the **Customer Success Management** &gt; **All Internal Plays** and select **New**.

3.  In the **Initiate** phase, you can perform the following activities:

    -   Select engagement: In the Number field, a unique number for the internal play is auto-populated. In the Engagement field, select the engagement for which the internal play is being created and select **Continue**.
    -   Enter core information: In this page, enter the purpose of the internal play including the following details:

        -   Assigned to: The key internal team member responsible for this internal play.
        -   Priority: Priority of this internal play in comparison to others. This can be:
            -   Critical
            -   High
            -   Medium
            -   Low
            -   Very Low
        -   Category: The internal play category. This can be:
            -   General
            -   Account health
            -   Adoption support
            -   Expansion and renewal support
            -   Governance and audits
            -   Partner reviews
        -   Due date: Date by which the internal play should be completed.
        -   Short description: The short description for the internal play. This is a mandatory field.
        -   Description: The description for the internal play. This is a mandatory field.
        Select **Mark Complete** to move to the next activity.

    -   Add squad: Select one or more squad members who will involved in the internal play and the related activities and select **Mark Complete** to move to the next stage.
4.  In the **Define the Action Plan** phase, you can perform the following activities:

    -   Formulate the action steps: Specify the action plan for this playbook. This will appear in the worknote. Select **Send and continue** to proceed to the next activity. The action plan will appear as work in the Activity stream section of the playbook.
    -   Related work: Select **Create task** to create an internal play task. See [Create an internal play task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/customer-success-management/account-lifecycle-create-internal-play-task.md) for a detailed description of this form.

        **Note:** Internal play tasks that are in New, In-progress, or Paused state are displayed in this page. To continue to the next activity, update the `State` to Complete or Canceled. After all the internal play tasks have been closed or canceled, select **Mark Complete** to continue with the next activity.

5.  In the **Review &amp; Close** phase, you can perform the following activities:

    -   Communicate the final outcome: Enter a comment to describe the final outcome for this playbook. Select **Send and continue** to proceed to the next activity.
    -   Close record: Select the Closure code from the drop down list and Close notes for this playbook and select **Mark Complete**.
6.  Select **Close** after all the activities have been completed.

    The internal play playbook State is set **Closed** and Progress is set to **Completed**.

    **Note:** If after creating the internal play, you close or cancel the internal play record, all pending activities and lanes in the internal play record are automatically canceled and the State is set to Canceled.


## What to do next

-   Create internal play tasks to define tasks that should be performed when an internal play is launched. See [Create an internal play task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/customer-success-management/account-lifecycle-create-internal-play-task.md).
-   Select **Discuss** to start a sidebar discussion about this internal play. In the pop-up window, select the participants who need to participate in the discussion, enter a brief message, and select **Start discussion**. A window appears with a link to the record for this internal play. Select **Open record** and start the discussion. When the discussion has been completed, you can see the details in the Activity stream.
-   Email: Open the Activity stream and select **Email** from the More drop down list. Enter the required details and select **Send email**.

.

-   **[Create an internal play task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/customer-success-management/account-lifecycle-create-internal-play-task.md)**  
Create an internal play task that must be performed when the internal play is launched. An internal play task must have a clear purpose and specifies the activity that must be performed. It is not visible to customers.
-   **[Close or cancel an internal play](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/customer-success-management/account-lifecycle-cancel-internal-play.md)**  
You can close or cancel an internal play and all the related tasks.

**Parent Topic:**[Manage customer success playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/customer-success-management/account-lifecycle-manage-cust-succ-playbooks.md)

