---
title: Review a dispute response and initiate pre-arbitration
description: Review a merchant’s response for the dispute and initiate pre-arbitration, if necessary for the collaboration dispute workflow for the Chargeback stage.
locale: en-US
release: zurich
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Collaboration workflow, Chargeback, Processing a Visa dispute, Resolving disputes with Visa, Processing, Use, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Review a dispute response and initiate pre-arbitration

Review a merchant’s response for the dispute and initiate pre-arbitration, if necessary for the collaboration dispute workflow for the Chargeback stage.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector

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

    The **Chargeback** stage is initiated for the transaction.

7.  Select the **Review dispute response and create pre-arbitration** activity.

8.  Review the merchant response in the **Dispute response** field of the record.

    The response might include the amount accepted for the chargeback or reasons the dispute wasn't accepted. You can also view the merchant response as an attachment in the activity stream.

9.  In the **Response outcome** field, select **Resolved** or **Unresolved**.

10. Select one of the following options.

<table id="choicetable_sh5_nr3_f5b"><thead><tr><th align="left" id="d53790e220">

Selection

</th><th align="left" id="d53790e223">

Result

</th></tr></thead><tbody><tr><td id="d53790e231">

**Unresolved**

</td><td>

1.  Based on the policy rule, the **Reverse Provisional Credit** field appears only for the IPC policy.
2.  The Reverse Provisional Credit field does not appear for the Immediate Final Credit \(IFC\) policy.
3.  The **Final Credit** field appears for **No Credit**.
4.  When pre-arbitration is created, reject the dispute response from the merchant.
5.  If you want to continue with pre-arbitration, select `Continue`.
6.  A **Fill questionnaire link** is displayed. This questionnaire is associated with the issuer’s pre-arbitration case.
7.  Enter the details in the questionnaire.
8.  Select **Submit**.


</td></tr><tr><td id="d53790e295">

**Resolved**

</td><td>

Accept the dispute response and resolve the dispute.1.  Provide the **Description**, **Remarks**, and **Work Notes**.
2.  Select **Continue**.


</td></tr></tbody>
</table>11. In the **Description** field, enter any comments.

12. Select **Update** to save your changes.

13. Initiate pre-arbitration by selecting **Create pre-arbitration**.

    The activity stream updates with the result of the request.


## Result

After the request executes successfully, the transaction state changes to **Awaiting External Info**. The form is set to read-only mode while you wait on a response. You can recall the request if you're within three days from the submission date and you haven't received a response yet.

request if you're within three days from the submission date and you haven't received a response yet. To recall the request, select **Recall**. When a response is received, the **Pre arbitration response received** value changes to **Yes** and the transaction state moves to **Work to Progress**.

## What to do next

To recall the request, select **Recall**. When a response is received, the **Pre arbitration response received** value changes to **Yes** and the transaction state moves to **Work to Progress**.

**Parent Topic:**[Collaboration dispute workflow](../concept/collaboration-dispute-workflow.md)

