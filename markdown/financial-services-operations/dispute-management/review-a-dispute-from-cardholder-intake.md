---
title: Review a dispute from portal or workspace intake
description: Review dispute cases that customers submit through the dispute intake portal, or that contributors create in the intake workspace.
locale: en-US
release: zurich
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Use, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Review a dispute from portal or workspace intake

Review dispute cases that customers submit through the dispute intake portal, or that contributors create in the intake workspace.

## About this task

You can verify disputed and associated transactions, update the dispute reason, change dispute category, fill out a transaction-level questionnaire in cases with multiple transactions, modify the dispute answers, and submit the case for investigation.

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

    The case playbook guides fulfillers through the steps that are involved in resolving a case.

6.  Under the **Review** playbook stage, review the submitted information and make any necessary adjustments.

<table id="choicetable_fwv_5cd_1cc"><thead><tr><th align="left" id="d104723e173">

Activity

</th><th align="left" id="d104723e176">

Description

</th></tr></thead><tbody><tr><td id="d104723e182">

**Review intake**

</td><td>

Review the disputed transactions and the reason for dispute.

 To modify the disputed transactions, select **Modify transactions**. Select or deselect the transactions and select **Modify** to save your changes.

 At least one transaction must be selected to continue. Multiple transactions can only be selected for Fraud dispute cases.

 To modify the dispute category and reason, select **Modify dispute reason**. Answer the questions presented, then select **Modify**.

 Each dispute can only address a single dispute category. If the reason code doesn’t match the dispute category for the case, you must cancel the case and create a new one.

**Note:** If the transaction is part of another dispute case, it will be flagged with a link to the case and information on the case outcome.

 **Note:** In case of integration with Visa and Mastercard APIs, if an error displays, refer to the **Activity stream** to see the error cause, resolve it and then select **Continue** to be able to proceed to the next activity.

</td></tr><tr><td id="d104723e239">

**Additional questions**

</td><td>

Provide answers to any additional questions not answered by the customer and update any additional questions as required. If the dispute category changes, the system will produce a questionnaire for the newly selected category, which you must fill out. Select **Continue** when you have finished the questionnaire.

</td></tr><tr><td id="d104723e251">

**Customer signature required**

</td><td>

For compliance purposes, inform the customer to sign a written statement for the unauthorized ACH debit and submit the document emailed to them.

 According to NACHA guidelines, customer must send a signed acknowledgment to the bank acknowledging they are disputing an unauthorized ACH debit transaction under certain reason codes.

 A pre-written email template is sent to the customer. This email can be e-signed and can be amended by your organization as needed.

 Once the customer completes this, the signed statement is added as an attached document on the Document verification task created for the case.

 **Note:** In order for users to view the Written Statement of Unauthorized Debit \(WSUD\) document, the Document Templates \[sn\_doc\] plugin must be activated.

</td></tr><tr><td id="d104723e278">

**Submit for investigation**

</td><td>

Review the dispute amount and add any comments or descriptions for the dispute transactions, then select **Submit**.

</td></tr></tbody>
</table>
**Parent Topic:**[Managing dispute service requests](../concept/managing-card-disputes.md)

