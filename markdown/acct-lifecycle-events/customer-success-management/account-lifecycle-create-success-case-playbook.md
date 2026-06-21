---
title: Create a customer play
description: Create a customer play in collaboration with customers to define planned and unplanned activities required to support an engagement.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/acct-lifecycle-events/customer-success-management/account-lifecycle-create-success-case-playbook.html
release: australia
product: Customer Success Management
classification: customer-success-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Manage playbooks, Customer success, Use, Customer Success Management]
---

# Create a customer play

Create a customer play in collaboration with customers to define planned and unplanned activities required to support an engagement.

## Before you begin

Role required: sn\_acct\_lc.customer\_success\_agent

## About this task

A customer play is used to monitor external activities of an unplanned set of actions that a provider may take to support a customer touchpoint, stakeholder request, or an engagement activity. A customer play may not be associated with an objective or outcome, but can be based on the nature of the customer play and why it was created. A customer play is a form of case type with its own case tasks.

## Procedure

1.  Navigate to **Workspace** &gt; **CSM/FSM Configurable Workspace** and select the **List** icon.

2.  Navigate to the **Customer Success Management** &gt; **All Customer Plays** and select **New**.

3.  In the `Initiate` phase, you can perform the following activities:

    -   Select engagement: In the Number field, a unique number for the customer play is auto-populated. In the Engagement field, select the engagement for which the customer play is being created and select **Continue**. A customer play record is created.
    -   Enter core information: In this page, enter the purpose of the customer play including the following details:

        -   Assigned to: The key internal team member responsible for this internal play.
        -   Priority: Priority of this internal play in comparison to others. This can be:
            -   Critical
            -   High
            -   Medium
            -   Low
            -   Very Low
        -   The category associated with this internal play. This can be:
            -   Guidance
            -   Architecture review
            -   Demos and POCs
            -   Training
        -   Due date: Date by which the customer play should be completed.
        -   Short description" The short description for the customer play. This is a mandatory field.
        -   Description: The description for the customer play. This is a mandatory field.
        Select **Mark Complete** to move to the next activity.

    -   Add squad: Select one or more squad members who will involved in the customer play and the related activities and select **Mark Complete** to move to the next stage.
4.  In the `Assist` phase, you can perform the following activities:

    -   Communicate the intended outcome: Enter a comment to describe the expected outcome for this playbook. Select **Send and continue** to proceed to the next activity.
    -   Define the action plan: Specify the action plan for this playbook. This appears in the worknote. Select **Send and continue** to proceed to the next activity.
    -   Related meeting: Create a meeting for this customer play. See &lt;Create meeting&gt; for details.

        **Note:** Meetings that are in a Draft or Scheduled state displayed in the Related meeting page. To continue to the next activity, update the State to Complete or Canceled. After all meetings have been closed or canceled, you can select **Mark Complete** to continue with the next activity.

    -   Related work: Select **Create Task** to create a customer play task. See [Create a customer play task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/customer-success-management/account-lifecycle-create-success-case-task.md) for a detailed description of this form.

        **Note:** customer play tasks that are in a New, In-progress, or Paused state are displayed in the Related meeting page. To continue to the next activity, update the State to Complete or Canceled. After all customer play tasks have been closed or canceled, select **Mark Complete** to continue with the next activity.

5.  In the Review &amp; Close phase, you can perform the following activities:

    -   Communicate the final outcome: Enter a comment to describe the final outcome for this playbook. Select **Send and continue** to proceed to the next activity.
    -   Close record: Select the Closure code from the drop-down list and Close notes for this playbook and select **Mark Complete**.
6.  When all the activities have been completed, you can select **Close customer play**.

    The customer play record State is set **Closed** and Progress is set to **Completed**.

    **Note:** If after creating the customer play record, you close or cancel the record, all pending activities and lanes of the playbook are automatically canceled, and the record State is set to Closed or Canceled.


## What to do next

-   Select **Discuss** to start a sidebar discussion about this customer play. In the pop-up window, select the participants who must participate in the discussion, enter a brief message, and select **Start discussion**. A window appears with a link to the record for this initiative. Select **Open record** and start the discussion. When the discussion has been completed, you can see the details in the **Activity stream**.
-   Create success play: See [Create a success play](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/customer-success-management/account-lifecycle-create-success-play.md).

-   **[Create a customer play task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/customer-success-management/account-lifecycle-create-success-case-task.md)**  
Create a customer play task to define a planned action that a provider or customer must complete in support of a customer play. A customer play task must be clearly defined and can be visible to internal stakeholders or external customers.
-   **[Close or cancel a customer play](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/customer-success-management/account-lifecycle-cancel-success-case.md)**  
You can close or cancel a customer play and all the related tasks.

**Parent Topic:**[Manage customer success playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/customer-success-management/account-lifecycle-manage-cust-succ-playbooks.md)

