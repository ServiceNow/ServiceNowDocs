---
title: Review a case filing response and appeal the decision
description: An appeal can be created by the issuer or acquirer if either party isn’t satisfied with the arbitration ruling from Visa. Review the case filing response and receive the decision letter from Visa.
locale: en-US
release: yokohama
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2025-03-02"
reading_time_minutes: 2
breadcrumb: [Collaboration dispute workflow, Chargeback stage, Processing a dispute case with the Card Dispute Transaction playbook, Working on a dispute case integrated with Visa, Managing dispute service requests, Dispute Management, Using banking applications, Financial Services Operations \(FSO\)]
---

# Review a case filing response and appeal the decision

An appeal can be created by the issuer or acquirer if either party isn’t satisfied with the arbitration ruling from Visa. Review the case filing response and receive the decision letter from Visa.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector

## About this task

After reviewing the case filing response, Visa issues a decision letter that supports either the acquirer or the issuer. If either party isn’t satisfied with the decision, they can file an appeal.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon.](../image/list-icon.png)\).

3.  In the **Lists** tab, under **Card disputes service cases**, open the case list.

4.  In the list, select the case that you want to work on.

    If you want to work on a case that isn't assigned to you yet, you can assign it to yourself by selecting **Assign to me**.

5.  Select the **Playbook** tab.

6.  In the transaction level playbook of the **Processing** tab, select the transaction ID.

7.  The **Chargeback** stage is initiated for the transaction.

8.  Select the **Review case filing response and appeal** activity.

9.  Retrieve the decision letter from Visa by selecting **Get case filing response**.

    The letter can also be viewed in the activity stream.

10. In the **Response outcome** field, either accept or appeal the decision.

<table id="choicetable_lqj_tw4_mfc"><thead><tr><th align="left" id="d27948e192">

Option

</th><th align="left" id="d27948e195">

Result

</th></tr></thead><tbody><tr><td id="d27948e201">

**Unresolved**

</td><td>

Either of the following scenarios appear:-   If the appeal amount is less than a certain amount, the **Reverse provisional credit** drop-down is displayed. Select **Yes** or **No**
-   In the **Create appeal** drop-down list, select **Yes**.

**Note:** Certain conditions must be met to create an appeal. For more information, see [Collaboration workflow](../concept/collaboration-workflow.md).

    1.  In the **Appeal amount** field, enter the amount for the appeal.
    2.  In the **Reason for appeal** field, explain why you want to appeal the decision.
    3.  In the **Description**, **Remarks**, and **Work notes** fields, enter additional details as necessary.
    4.  Select **Continue**.
    5.  Select **Create appeal**.
-   In the **Create appeal** drop-down list, select **No**.
    1.  Select **Yes** or **No** in the **Reverse provisional credit** drop-down.
    2.  Select **Continue**.


</td></tr><tr><td id="d27948e309">

**Resolved**

</td><td>

Select to indicate the case is resolved.

</td></tr></tbody>
</table>
## Result

After the request executes successfully, the transaction state changes to **Awaiting External Info**. The form is set to read-only mode while waiting on a response. Visa confirms the appeal with an acknowledgment letter. Retrieve the letter by selecting **Get acknowledgment letter** in the [Review the case filing appeal](review-case-filing-appeal.md) activity.

**Parent Topic:**[Collaboration dispute workflow](../concept/collaboration-dispute-workflow.md)

