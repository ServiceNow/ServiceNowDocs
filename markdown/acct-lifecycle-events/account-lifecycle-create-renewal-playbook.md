---
title: Create a renewal playbook
description: Create a renewal playbook to define processes to simplify contract renewals and identify expansion opportunities.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Configure customer success, Customer success, Customer Success Management]
---

# Create a renewal playbook

Create a renewal playbook to define processes to simplify contract renewals and identify expansion opportunities.

## Before you begin

Role required: sn\_acct\_lc.ale\_success\_agent

## Procedure

1.  Navigate to **Workspace** &gt; **CSM/FSM Configurable Workspace** and select the **List** icon.

2.  Select **Customer Success** &gt; **All Engagements** and click on an engagement in the list.

3.  Click **Create success play**.

4.  Select **Success Support** from the Category drop down list.

5.  In the sub-category section, select **Simple renewal play** and click **Next**.

6.  Specify the Due Date and select the user in the Assigned to field and click **Finish**.

    You will see a confirmation message and the renewal playbook record is created.

7.  Select **Customer Success** &gt; **All Internal Plays** to view the newly created renewal playbook.

8.  Click on the renewal playbook you have created to view the first stage of the playbook.

9.  In the `Initiate` phase, you can perform the following activities:

    -   Enter core information: Select the contract with which this renewal playbook is to be associated and select `Expansion and Renewal Support` in the Category field. Enter information in the other mandatory fields and click **Mark Complete** to move to the next activity.
    -   Add squad: Select one or more squad members who will involved in the renewal playbook activities and click **Mark Complete** to move to the next stage.
10. In the `Assess Opportunities` phase, you can perform the following activities:

    -   View contract record: The details of the contract you have selected are displayed. Click **Open record** to verify the contract details. Click **Mark read** to proceed to the next activity.
    -   Assess engagement: Enter any actions that need to be performed as part of this playbook and click **Send and continue** to proceed to the next activity. The actions you specify will appear as worknotes in the Activity stream.
11. In the `Communicate` phase, you can perform the following activities:

    -   Communicate renewal opportunity: In this activity, you can send an email request to the contracts approver or business owner to renew the contract. A sample email template is provided, you can modify this as required and click **Send Email**.

        **Note:**

        -   This activity creates an internal play task which is displayed as a worknote in the Activity Stream. Click on the internal play task link to view the record. When you click **Send Email**, the status of this task is set to `Closed`, and the Closure code and Close notes fields are updated to indicate that the email has been sent.
        -   If you click **Skip email**, the status of the internal play task is set to `Canceled` and the internal play task is canceled.
    -   Create opportunity: In this activity, you can create a new opportunity for your contract. This activity creates an internal play task. Update the task details as required to move to the next stage. Click **Open record** to view the internal play task. Review the opportunity details, update the status to Closed or Canceled, and click **Close** this activity and move on to the next stage.
12. In the `Track Opportunity` phase, review the contract details.

    Click **Open record** to make changes if necessary or click **Mark read** to proceed to the next stage.

13. In the Review &amp; Close, you can perform the following activities:

    -   Communicate the final outcome of the renewal: Enter details to describe the final renewal outcome and click **Send and continue** to proceed to the next activity. The final outcome information is displayed as a worknote in the Activity stream.
    -   Close record: Select the Closure code from the drop down list and Close notes for this playbook and click **Mark Complete**.
14. Click **Close** when all the activities have been completed.

    The renewal playbook State is set Closed and Progress is set to Completed.

    **Note:** If after creating the renewal playbook, you close or cancel the playbook, all pending activities and lanes are automatically canceled and playbook State is set to Canceled.


