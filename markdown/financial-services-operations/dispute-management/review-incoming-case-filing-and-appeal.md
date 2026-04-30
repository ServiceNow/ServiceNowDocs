---
title: Review incoming case filing and appeal
description: Review the incoming case filing created by the acquirer and create an appeal if required.
locale: en-US
release: zurich
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Allocation workflow, Chargeback, Processing a Visa dispute, Resolving disputes with Visa, Processing, Use, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Review incoming case filing and appeal

Review the incoming case filing created by the acquirer and create an appeal if required.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector

## About this task

If you refuse the acquirer’s pre-arbitration request, the acquirer may create an arbitration request. You can review the arbitration and create an appeal, if required.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon](../../../use/reporting/image/inline-data-vis-96px-list.png)\).

3.  In the **Lists** tab under **Card disputes service cases**, open the case list.

    -   For your assigned cases, select **Assigned to me**.
    -   For all dispute cases, select **All**.
4.  In the list, select which case you want to work on.

    If you want to work on a case that isn't assigned to you yet, you can assign it to yourself by selecting **Assign to me**.

5.  Select the **Playbook** tab.

6.  In the transaction level Playbook of the **Processing** tab, select the transaction ID.

7.  The **Chargeback** stage is initiated for the transaction.

8.  Select the **Review incoming case filing appeal** activity.

9.  Select **Get case filing detail** to get the details about the amount and reason for case filing.

    The reason is displayed in the **Reason for filing** field.

10. To withdraw from the case filing:

    -   Select **Withdraw**.
    -   Update the **Case withdrawn status** field to indicate who initiated the withdrawal.
    -   Update the **Reverse provisional credit** field. This field appears only for the IPC policy. If it's no credit, the **Final Credit** field appears.
11. Select **Close task**.

12. Select **Get case filing response** to view the case filing decision from Visa.

13. Select your response in the **Response outcome** field.

    -   To accept the outcome, select **Resolved**.
    -   To appeal the outcome, select **Unresolved**.
14. If the response is **Unresolved**, select `Yes` in the **Create appeal** drop-down.

    An appeal can be created only if certain conditions are met. For more information, see [Allocation workflow overview](../concept/allocation-workflow.md).

15. Enter the **Appeal amount**.

16. Provide the **Reason for appeal**.

17. Select **Create appeal**.


## Result

After the request executes successfully, the transaction state moves to **Awaiting External Info**. The form is set to read-only mode while waiting on a response.

## What to do next

Visa confirms the appeal with an acknowledgment letter. Retrieve the letter by selecting `Get acknowledgement letter` in the**Review case filing appeal** activity.

**Parent Topic:**[Allocation dispute workflow](../concept/allocation-dispute-work-flow.md)

