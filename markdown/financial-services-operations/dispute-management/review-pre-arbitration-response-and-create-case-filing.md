---
title: Review the pre-arbitration response and create a case filing
description: Review the merchant’s response to the pre-arbitration and create a case filing.
locale: en-US
release: yokohama
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2025-03-02"
reading_time_minutes: 2
breadcrumb: [Collaboration dispute workflow, Chargeback stage, Processing a dispute case with the Card Dispute Transaction playbook, Working on a dispute case integrated with Visa, Managing dispute service requests, Dispute Management, Using banking applications, Financial Services Operations \(FSO\)]
---

# Review the pre-arbitration response and create a case filing

Review the merchant’s response to the pre-arbitration and create a case filing.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector

## About this task

After you receive the merchant’s response for pre-arbitration, the response is updated in the system and the task is moved to closure automatically. Review the pre arbitration response and decide to create an appeal.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon.](../image/list-icon.png)\).

3.  In the **Lists** tab, under **Card disputes service cases**, open the case list.

4.  In the list, select the case that you want to work on.

    If you want to work on a case that isn't assigned to you yet, you can assign it to yourself by selecting **Assign to me**.

5.  Select the **Playbook** tab.

6.  In the transaction level playbook of the **Processing** tab, select the transaction ID.

7.  The **Chargeback** stage is initiated for the transaction.

8.  Select the **Review pre arbitration response and create case filing** activity.

9.  Review the acquirer’s pre-arbitration response details in the **Pre arbitration response** field of the record.

    You can also view the merchant response as an attachment in the activity stream.

10. In the **Pre arbitration outcome** drop-down, select **Resolved** or **Unresolved**.

<table id="choicetable_inv_t2g_2fc"><thead><tr><th align="left" id="d101718e184">

Selection

</th><th align="left" id="d101718e187">

Result

</th></tr></thead><tbody><tr><td id="d101718e193">

**Unresolved**

</td><td>

The field **Do you want to create case filing?** is displayed.-   Select **Yes**.
    1.  Specify the amount for the case filing and the reason for the case filing in **Case filing amount** and **Reason for filing**.
    2.  In the **Description**, **Remarks**, and **Work notes** fields, enter additional details as necessary.
    3.  Select **Continue**.
    4.  Select **Close task**.
    5.  Select **Submit dispute filing**.
-   Select **No**.
-   The **Reverse provisional credit** drop-down is displayed.
-   Select **Yes** or **No** and click **Continue**.


</td></tr><tr><td id="d101718e278">

**Resolved**

</td><td>

Option to resolve the dispute.

</td></tr></tbody>
</table>
## Result

After the request executes successfully, the transaction state changes to **Awaiting External Info**. The form is set to read-only mode while you wait on a response. Visa confirms the case filing with an acknowledgment letter.

## What to do next

Retrieve the letter by selecting `Get acknowledgement letter`. The letter can be viewed in the activity stream. You can also withdraw the case filing by selecting **Withdraw case**. After a decision from Visa is available, the task is automatically closed and the [Review a case filing response and appeal the decision](review-case-filing-response-and-appeal.md) activity is available.

**Parent Topic:**[Collaboration dispute workflow](../concept/collaboration-dispute-workflow.md)

