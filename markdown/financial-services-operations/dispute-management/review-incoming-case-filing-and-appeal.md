---
title: Review incoming case filing and appeal
description: Review the incoming case filing created by the acquirer and create an appeal if required.
locale: en-US
release: yokohama
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2025-03-03"
reading_time_minutes: 2
breadcrumb: [Allocation dispute workflow, Chargeback stage, Processing a dispute case with the Card Dispute Transaction playbook, Working on a dispute case integrated with Visa, Managing dispute service requests, Dispute Management, Using banking applications, Financial Services Operations \(FSO\)]
---

# Review incoming case filing and appeal

Review the incoming case filing created by the acquirer and create an appeal if required.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector

## About this task

If the issuer refuse the acquirer’s pre-arbitration request, the acquirer can create an arbitration request. The issuer reviews the arbitration and creates an appeal, if required.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon.](../image/list-icon.png)\).

3.  In the **Lists** tab, under **Card disputes service cases**, open the case list.

4.  In the list, select the case to work on.

    To work on a case that is not assigned to you yet, assign it to yourself by selecting **Assign to me**.

5.  Select the **Playbook** tab.

6.  In the transaction level Playbook of the **Processing** tab, select the transaction ID.

7.  The **Chargeback** stage is initiated for the transaction.

8.  Select the **Review incoming case filing appeal** activity.

9.  Select **Get case filing detail** to get the details about the amount and reason for case filing.

    The reason is displayed in the **Reason for filing** field.

10. To withdraw the case:

    -   Select **Withdraw**.
    -   Update the **Case withdrawn status** field to indicate who initiated the withdrawal.
    -   Update the **Reverse provisional credit** field. This field appears only for the IPC policy. If it's no credit, the **Final Credit** field appears.
11. Select **Close task**.

12. Select **Get case filing response** to view the case filing decision from Visa.

13. Select your response in the **Response outcome** field.

<table id="choicetable_pcd_wkt_nfc"><thead><tr><th align="left" id="d83011e225">

Option

</th><th align="left" id="d83011e228">

Description

</th></tr></thead><tbody><tr><td id="d83011e234">

**Resolved**

</td><td>

The arbitration is accepted and the outcome is resolved.

</td></tr><tr><td id="d83011e243">

**Unresolved**

</td><td>

The issuer is not happy with the arbitration outcome and would go for an appeal. The **Create appeal** drop-down is displayed. An appeal can be created only if certain conditions are met. For more information, see [Allocation workflow](../concept/allocation-workflow.md).

-   Select **Yes** to create an appeal.
    1.  Enter the **Appeal amount**.
    2.  Provide the **Reason for appeal**.
    3.  Select **Continue**.
    4.  Select **Create appeal**.
-   Select **No** to continue without the appeal.


</td></tr></tbody>
</table>
## Result

After the request executes successfully, the transaction state moves to **Awaiting External Info**. The form is set to read-only mode while waiting on a response.

## What to do next

Visa confirms the appeal with an acknowledgment letter. Retrieve the letter by selecting `Get acknowledgement letter` in the **Review case filing appeal** activity.

**Parent Topic:**[Allocation dispute workflow](../concept/allocation-dispute-work-flow.md)

