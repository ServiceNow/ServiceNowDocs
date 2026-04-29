---
title: Review and respond to a pre-arbitration request
description: Review and respond to the pre-arbitration request created by the acquirer.
locale: en-US
release: australia
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Allocation workflow, Initiate chargeback, Processing a Visa dispute, Resolving disputes with Visa, Processing, Use, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Review and respond to a pre-arbitration request

Review and respond to the pre-arbitration request created by the acquirer.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector

## About this task

The acquirer might choose to initiate pre-arbitration. You can review and respond to this pre-arbitration activity.

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

8.  Select the **Review and respond to pre arbitration** activity.

9.  Review the pre-arbitration request by opening the record under the **Pre arbitration request** field.

    You can also view the merchant response as an attachment in the activity stream.

    **Note:** If Card Data Security is installed and configured, **Attachments** in the contextual side panel will handle files differently in transaction records. For more information, see [Manage attachments in Card Data Security](../../fso-card-data-security/concept/manage-attachments-in-card-data-security.md).

10. Respond in one of the following ways.

<table id="choicetable_hxf_hdv_n2c"><thead><tr><th align="left" id="d74915e221">

Option

</th><th align="left" id="d74915e224">

Description

</th></tr></thead><tbody><tr><td id="d74915e230">

**Resolved**

</td><td>

Determine whether to reverse provisional credit using the **Reverse provisional credit** field. Select **Continue**, then select **Accept dispute**. Select **Close task**.

 As a result, the issuer accepts the pre-arbitration request of the acquirer. It reverses provisional credit or convert provisional credit to final credit.

</td></tr><tr><td id="d74915e257">

**Unresolved**

</td><td>

Select **Continue**. Select **Fill questionnaire** and provide all the information related to the pre-arbitration as a response.

 Select **Submit** for the questionnaire form. Select Create pre-arbitration response.

 As a result, the issuer refutes the pre-arbitration.

</td></tr></tbody>
</table>
## Result

After the request executes successfully, the transaction state changes to **Awaiting External Info**. The form is set to read-only mode while you wait on a response. Visa confirms the case filing with an acknowledgment letter.

## What to do next

You can recall the request if you're within three days from the submission date and you haven't received a response yet. To recall the request, select **Recall**. When an arbitration case filing is received, the **Incoming arbitration received** value changes to **Yes** and the transaction state moves to **Work to Progress**.

**Parent Topic:**[Allocation dispute workflow](../concept/allocation-dispute-work-flow.md)

