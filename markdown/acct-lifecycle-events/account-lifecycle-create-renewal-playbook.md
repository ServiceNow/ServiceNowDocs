---
title: Create a renewal playbook
description: Create a renewal playbook to define processes to simplify contract renewals and identify expansion opportunities.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Manage playbooks, Customer success, Configure, Customer Success Management]
---

# Create a renewal playbook

Create a renewal playbook to define processes to simplify contract renewals and identify expansion opportunities.

## Before you begin

Role required: sn\_acct\_lc.customer\_success\_agent

## Procedure

1.  Navigate to **Workspace** &gt; **CSM/FSM Configurable Workspace** and select the **List** icon.

2.  Select **Customer Success** &gt; **All Engagements** and select an engagement in the list.

3.  Select **Create success play**.

4.  Select **Success Support** from the Category drop down list.

5.  In the subcategory section, select **Simple renewal play** and select **Next**.

6.  Specify the Due Date and select the user in the Assigned to field and select **Finish**.

    You see a confirmation message and the renewal playbook record is created.

7.  Select **Customer Success** &gt; **All Internal Plays** to view the newly created renewal playbook.

8.  Select the renewal playbook that you have created to view the first stage of the playbook.

9.  In the `Initiate` phase, you can perform the following activities:

    -   Enter core information: Select the contract with which this renewal playbook is to be associated and select `Expansion and Renewal Support` in the Category field. Enter information in the other required fields and select **Mark Complete** to move to the next activity.
    -   Add squad: Select one or more squad members who will involved in the renewal playbook activities and select **Mark Complete** to move to the next stage.
10. In the `Assess Opportunities` phase, you can perform the following activities:

    -   View contract record: The details of the contract you have selected are displayed. Select **Open record** to verify the contract details. Select **Mark read** to proceed to the next activity.
    -   Assess engagement: Enter any actions that must be performed as part of this playbook and select **Send and continue** to proceed to the next activity. The actions you specify will appear as worknotes in the Activity stream.
11. In the `Communicate` phase, you can perform the following activities:

    -   Communicate renewal opportunity: In this activity, you can send an email request to the contracts approver or business owner to renew the contract. A sample email template is provided. You can modify this as required and select **Send Email**.

        **Note:**

        -   This activity creates an internal play task that is displayed as a worknote in the Activity stream. Select the internal play task link to view the record. When you select **Send Email**, the status of this task is set to `Closed`, and the Closure code and Close notes fields are updated to indicate that the email has been sent.
        -   If you select **Skip email**, the status of the internal play task is set to `Canceled` and the internal play task is canceled.
    -   Create opportunity: In this activity, you can create opportunity for your contract. This activity creates an internal play task. Update the task details as required to move to the next stage. Select **Open record** to view the internal play task. Review the opportunity details, update the status to Closed or Canceled, and select **Close** this activity and move on to the next stage.
12. In the `Track Opportunity` phase, review the contract details.

    Select **Open record** to change if necessary or select **Mark read** to proceed to the next stage.

13. In the Review &amp; Close, you can perform the following activities:

    -   Communicate the final outcome of the renewal: Enter details to describe the final renewal outcome and select **Send and continue** to proceed to the next activity. The final outcome information is displayed as a worknote in the Activity stream.
    -   Close record: Select the Closure code from the drop-down list and Close notes for this playbook and select **Mark Complete**.
14. Select **Close** when all the activities have been completed.

    The renewal playbook State is set Closed and Progress is set to Completed.

    **Note:** If after creating the renewal playbook, you close or cancel the playbook, all pending activities, and lanes are automatically canceled and the playbook State is set to Canceled.


**Parent Topic:**[Manage customer success playbooks](../concept/account-lifecycle-manage-cust-succ-playbooks.md)

