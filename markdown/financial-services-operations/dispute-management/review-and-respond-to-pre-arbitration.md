---
title: Review and respond to a pre-arbitration request
description: Review and respond to the pre-arbitration request created by the acquirer.
locale: en-US
release: yokohama
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2025-03-02"
reading_time_minutes: 2
breadcrumb: [Allocation dispute workflow, Chargeback stage, Processing a dispute case with the Card Dispute Transaction playbook, Working on a dispute case integrated with Visa, Managing dispute service requests, Dispute Management, Using banking applications, Financial Services Operations \(FSO\)]
---

# Review and respond to a pre-arbitration request

Review and respond to the pre-arbitration request created by the acquirer.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector

## About this task

The acquirer might choose to initiate pre-arbitration. You can review and respond to this pre-arbitration request.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon.](../image/list-icon.png)\).

3.  In the **Lists** tab, under **Card disputes service cases**, open the case list.

4.  In the list, select the case that you want to work on.

    If you want to work on a case that isn't assigned to you yet, you can assign it to yourself by selecting **Assign to me**.

5.  Select the **Playbook** tab.

6.  In the transaction level playbook of the **Processing** tab, select the transaction ID.

7.  The **Chargeback** stage is initiated for the transaction.

8.  Select the **Review and respond to pre arbitration** activity.

9.  Review the pre-arbitration request by opening the record under the **Pre arbitration request** field.

    You can also view the merchant response as an attachment in the activity stream.

10. In the **Pre arbitration outcome** drop-down, select one of the options.

<table id="choicetable_hxf_hdv_n2c"><thead><tr><th align="left" id="d63030e172">

Option

</th><th align="left" id="d63030e175">

Description

</th></tr></thead><tbody><tr><td id="d63030e181">

**Resolved**

</td><td>

Decide whether to reverse provisional credit using the **Reverse provisional credit** drop-down. Select **Yes** and **Continue**. Select **Close task**.

 As a result, the issuer accepts the pre-arbitration request of the acquirer. It reverses provisional credit or convert provisional credit to final credit.

</td></tr><tr><td id="d63030e212">

**Unresolved**

</td><td>

Select **Continue**. A **Fill questionnaire** link is displayed at the top of the screen. Select **Fill questionnaire** and provide all the information related to the pre-arbitration as a response.

 Select **Submit** for the questionnaire form. Select **Create pre-arbitration response**.

 As a result, the issuer refutes the pre-arbitration.

</td></tr></tbody>
</table>
## Result

After the request executes successfully, the transaction state changes to **Awaiting External Info**. The form is set to read-only mode while you wait on a response. Visa confirms the case filing with an acknowledgment letter.

## What to do next

You can recall the request if you're within three days from the submission date and you haven't received a response yet. To recall the request, select **Recall**. When an arbitration case filing is received, the **Incoming arbitration received** value changes to **Yes** and the transaction state moves to **Work to Progress**. The next activity [Review incoming case filing and appeal](review-incoming-case-filing-and-appeal.md) is displayed.

**Parent Topic:**[Allocation dispute workflow](../concept/allocation-dispute-work-flow.md)

