---
title: Review the pre-arbitration response and create a case filing
description: Review the merchant’s response to the pre-arbitration and create a case filing.
locale: en-US
release: australia
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Collaboration workflow, Initiate chargeback, Processing a Visa dispute, Resolving disputes with Visa, Processing, Use, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Review the pre-arbitration response and create a case filing

Review the merchant’s response to the pre-arbitration and create a case filing.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector

## About this task

After you receive the merchant’s response for pre-arbitration, the response is updated in the system and the task is moved to closure automatically.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon](../../../use/reporting/image/inline-data-vis-96px-list.png)\).

3.  In the **Lists** tab under **Card disputes service cases**, open the case list.

    -   For your assigned cases, select **Assigned to me**.
    -   For all dispute cases, select **All**.
4.  In the list, select which case you want to work on.

    If you want to work on a case that isn't assigned to you yet, you can assign it to yourself by selecting **Assign to me**.

5.  Select the **Playbook** tab.

6.  In the transaction level playbook of the **Processing** tab, select the transaction ID.

7.  The **Chargeback** stage is initiated for the transaction.

8.  Select the **Review pre arbitration response and create case filing** activity.

9.  Review the acquirer’s pre-arbitration response details in the **Pre arbitration response received** field of the record.

    You can also view the merchant response as an attachment in the activity stream.

    **Note:** If Card Data Security is installed and configured, **Attachments** in the contextual side panel will handle files differently in transaction records. For more information, see [Manage attachments in Card Data Security](../../fso-card-data-security/concept/manage-attachments-in-card-data-security.md).

10. In the **Pre arbitration outcome** field, select **Resolved** or **Unresolved**.

<table id="choicetable_inv_t2g_2fc"><thead><tr><th align="left" id="d123223e236">

Selection

</th><th align="left" id="d123223e239">

Result

</th></tr></thead><tbody><tr><td id="d123223e245">

**Unresolved**

</td><td>

the field **Do you want to create case filing?** is displayed.1.  Create a case filing by selecting **Yes**
2.  Specify the amount for the case filing and the reason for the case filing.
3.  In the **Description**, **Remarks**, and **Work notes** fields, enter additional details as necessary.
4.  Select **Continue**.
5.  Select **Submit dispute filing**.


</td></tr><tr><td id="d123223e291">

**Resolved**

</td><td>

 

</td></tr></tbody>
</table>
## Result

After the request executes successfully, the transaction state changes to **Awaiting External Info**. The form is set to read-only mode while you wait on a response. Visa confirms the case filing with an acknowledgment letter.

## What to do next

Retrieve the letter by selecting `Get acknowledgement letter`. The letter can be viewed in the activity stream. You can withdraw the case filing by selecting **Withdraw case**.

1.  After a decision by Visa is available, you can access it by selecting **Get case filing response**.
2.  The task is automatically closed and the **Review case filing response** activity and appeal is available.

**Parent Topic:**[Collaboration dispute workflow](../concept/collaboration-dispute-workflow.md)

