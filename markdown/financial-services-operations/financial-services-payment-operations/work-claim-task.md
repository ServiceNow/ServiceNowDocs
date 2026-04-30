---
title: Work on a claim task for an external refund
description: Using a claim task, follow up with the third-party bank for a claim refund.
locale: en-US
release: yokohama
product: Financial Services Payment Operations
classification: financial-services-payment-operations
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Work on a claim with an external refund, Managing payment claims and debit approvals, Payment Operations, Using banking applications, Financial Services Operations \(FSO\)]
---

# Work on a claim task for an external refund

Using a claim task, follow up with the third-party bank for a claim refund.

## Before you begin

Role required: sn\_bom\_payment.claim\_agent or sn\_bom\_payment.claim\_agent\_connector

## About this task

A claim task is automatically generated for a claim with an external refund and is assigned to the claim agent that is working on the case. However, for any internal follow-up, you can also create an ad hoc claim task for any type of claim.

You can create an ad hoc claim task by navigating to the **Claim Tasks** tab of the case and clicking **New**.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Click the lists icon \(![lists icon](../../fso-card-operations/image/list-icon.png)\).

3.  Open the claim task from a claim case or from the Claim Tasks list.

<table id="choicetable_lgv_1db_hmb"><thead><tr><th align="left" id="d108413e93">

Option

</th><th align="left" id="d108413e96">

Steps

</th></tr></thead><tbody><tr><td id="d108413e102">

**From a claim case**

</td><td>

1.  In the **Lists** tab, under **Claims**, click **Assigned to me**.
2.  In the list, click the case that you want to open.
3.  In the case, click the **Claim Tasks** tab and click the claim task.


</td></tr><tr><td id="d108413e135">

**From the Claim Tasks list**

</td><td>

1.  In the **Lists** tab, under **Claim Tasks**, click **Assigned to me**.
2.  In the list, click the task that you want to open.


</td></tr></tbody>
</table>4.  In the **State** field, change the state of the task to **Work in Progress** and send an email to the refund bank to follow up on the refund status for the claim.

5.  If you've received the information from the refund bank via emails or any other interactions, attach these artifacts to the case.

6.  In the **Work notes** field, enter any comments or received information.

7.  In the **State** field, change the state of the task to **Closed Complete** to close the task.

8.  Click **Save**.


## What to do next

Update the associated claim case as per the refund or information that you receive from the refund bank.

**Note:** If the claim is not closed within the number of days mentioned in the **sn\_bom\_payment.claim\_follow \_up\_interval\_in\_days** [payment property](../reference/properties-installed-with-payment-operations.md), the system creates another follow-up claim task for the claim.

**Parent Topic:**[Work on a claim with an external refund](work-claim-with-external-refund.md)

