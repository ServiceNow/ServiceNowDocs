---
title: Create an opportunity in Microsoft Dynamics CRM
description: Create a renewal opportunity in the Microsoft Dynamics CRM platform from your ServiceNow instance.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Microsoft Dynamics CRM integration, Customer success, Configure, Customer Success Management]
---

# Create an opportunity in Microsoft Dynamics CRM

Create a renewal opportunity in the Microsoft Dynamics CRM platform from your ServiceNow instance.

## Before you begin

Role required: sn\_acct\_lc.customer\_success\_agent

## About this task

Customer success managers can create renewal opportunities based on contract expiration dates and identify any potential risks.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace** and select the **List** icon.

2.  Navigate to **Customer Success** &gt; **All Engagements** and open an engagement.

3.  Select **Create Success Play**.

4.  Select **Success Support** category and select the **Simple Renewal Play** card.

5.  In the Create Success Play form, specify the Due Date, Assigned to, and Priority and select **Finish**.

    You will see a message that an internal play has been created.

6.  Navigate to **Customer Success** &gt; **All Internal Plays** and open the renewal playbook that was created.

    ![Renewal playbook: core information](../image/account-lifecycle-crm-create-opp-1.png)

7.  In the Enter core information page, select the contract for which the renewal opportunity is to be created, enter a description and select **Mark complete**.

8.  In the Add squad page, select one or more squad members and select **Mark complete**.

9.  In the Assess Opportunity stage, select **Mark read** in the View contract record page to proceed to the next step.

10. In the Assess engagement page, enter any actions or steps required and select **Send and continue** to proceed to the next stage.

11. In the Communicate stage, select **Send email** to go to the next stage.

12. In the Create opportunity page, select **Open record**.

    You can see the recommended action for Microsoft Dynamics CRM displayed in the right panel. The details of the account associated with the engagement and the contract information is displayed. Select the **History** icon to see a log of previous recommended actions.

    ![MS Dynamics CRM recommended action](../image/account-lifecycle-crm-create-opp-2.png)

13. Select **Create**.

    You will see a message indicating that the opportunity record has been created. You can login to the Microsoft Dynamics CRM platform to view this record.

    **Note:** You can create the record only if you have defined the mappings in the **DynamicsCRMMappingConstants** script include. See [Enable integration with Microsoft Dynamics CRM](../concept/account-lifecycle-crm-integration.md) for details. If the mappings have not been configured, you will see the recommended action but the **Create** option will not work.


**Parent Topic:**[Enable integration with Microsoft Dynamics CRM](../concept/account-lifecycle-crm-integration.md)

