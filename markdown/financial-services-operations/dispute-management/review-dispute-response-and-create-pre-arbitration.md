---
title: Review dispute response and create pre-arbitration
description: Review a merchant’s response for the dispute and initiate pre-arbitration, if necessary for the collaboration dispute workflow of the Chargeback stage.
locale: en-US
release: yokohama
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2025-03-01"
reading_time_minutes: 2
breadcrumb: [Collaboration dispute workflow, Chargeback stage, Processing a dispute case with the Card Dispute Transaction playbook, Working on a dispute case integrated with Visa, Managing dispute service requests, Dispute Management, Using banking applications, Financial Services Operations \(FSO\)]
---

# Review dispute response and create pre-arbitration

Review a merchant’s response for the dispute and initiate pre-arbitration, if necessary for the collaboration dispute workflow of the Chargeback stage.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon.](../image/list-icon.png)\).

3.  In the **Lists** tab, under **Card disputes service cases**, open the case list.

4.  In the list, select the case that you want to work on.

    If you want to work on a case that isn't assigned to you yet, you can assign it to yourself by selecting **Assign to me**.

5.  Select the **Playbook** tab.

6.  In the transaction level playbook of the **Processing** tab, select the transaction ID.

    The **Chargeback** stage is initiated for the transaction.

7.  Select the **Review dispute response and create pre-arbitration** activity.

8.  Review the merchant response in the **Dispute response** field of the record.

    The response might include the amount accepted for the chargeback or reasons the dispute wasn't accepted. You can also view the merchant response as an attachment in the activity stream.

9.  In the **Response outcome** field, select **Resolved** or **Unresolved**.

10. Select one of the following options.

<table id="choicetable_sh5_nr3_f5b"><thead><tr><th align="left" id="d48175e186">

Selection

</th><th align="left" id="d48175e189">

Result

</th></tr></thead><tbody><tr><td id="d48175e197">

**Unresolved**

</td><td>

-   Select **Yes** in the **Create pre arbitration** drop-down to continue with pre-arbitration.
    1.  Select `Continue`.
    2.  A **Fill questionnaire link** is displayed. This questionnaire is associated with the issuer’s pre-arbitration case.
    3.  Enter the details in the questionnaire.
    4.  Select **Submit**.
    5.  Provide the **Description**, **Remarks**, and **Work Notes**.
    6.  Select **Create pre-arbitration** to create pre-arbitration.
    -   Based on the policy rule, the **Reverse Provisional Credit** field appears only for the IPC policy.
    -   The Reverse Provisional Credit field does not appear for the Immediate Final Credit \(IFC\) policy.
    -   The **Final Credit** field appears for **No Credit**.
-   Select **No** in the **Create pre arbitration** drop-down to accept the dispute.
    1.  The **Reverse provisional credit** drop-down is displayed.
    2.  Select **Yes** or **No** and click **Continue**.


</td></tr><tr><td id="d48175e318">

**Resolved**

</td><td>

Accept the dispute response and resolve the dispute.1.  Provide the **Description**, **Remarks**, and **Work Notes**.
2.  Select **Continue**.


</td></tr></tbody>
</table>
## Result

After the request executes successfully, the transaction state changes to **Awaiting External Info**. The activity stream updates with the result of the request. The form is set to read-only mode while you wait on a response. You can recall the request if you're within three days from the submission date and you haven't received a response yet.

To recall the request, select **Recall**. When a response is received, the **Pre arbitration response received** value changes to **Yes** and the transaction state moves to **Work to Progress**.

## What to do next

To recall the request, select **Recall**. When a response is received, the **Pre arbitration response received** value changes to **Yes** and the transaction state moves to **Work to Progress**. You will be redirected to the next activity [Review the pre-arbitration response and create a case filing](review-pre-arbitration-response-and-create-case-filing.md).

**Parent Topic:**[Collaboration dispute workflow](../concept/collaboration-dispute-workflow.md)

