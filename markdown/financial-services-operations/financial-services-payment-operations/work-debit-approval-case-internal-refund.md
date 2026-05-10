---
title: Work on a debit approval case to complete a refund
description: Work with your internal customer or bank to get the debit amount approved so that you can complete the claim refund.
locale: en-US
release: australia
product: Financial Services Payment Operations
classification: financial-services-payment-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Work on a claim with an internal refund, Managing payment claims and debit approvals, Use, Payment Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Work on a debit approval case to complete a refund

Work with your internal customer or bank to get the debit amount approved so that you can complete the claim refund.

## Before you begin

Ensure that the debit customer or the refund bank has approved the debit amount.

Role required: sn\_bom\_payment.claim\_agent or sn\_bom\_payment.claim\_agent\_connector

## About this task

If there's a Customer or Consumer Service Portal available for customers, they get notification for the debit approval case on the portal from where they can choose to accept or reject the requested debit amount. If the debit customer accepts the debit amount, the debit approval case state automatically changes to Closed. For more information, see:

-   [View a case from the Consumer Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/view-cases-consumer-portal.md)
-   [Accept or reject a case solution from the Consumer Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/resolve-cases-consumer-portal.md)

**Note:** To use the Consumer Service Portal, activate the Consumer Service Portal plugin \(com.glide.service-portal.consumer-portal\).

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon](../../../use/reporting/image/inline-data-vis-96px-list.png)\).

3.  Open the debit approval payment service case from a claim case or from the Debit Approvals list.

<table id="choicetable_lgv_1db_hmb"><thead><tr><th align="left" id="d128762e110">

Option

</th><th align="left" id="d128762e113">

Steps

</th></tr></thead><tbody><tr><td id="d128762e119">

**From a claim case**

</td><td>

1.  In the **Lists** tab, under **Claims**, click **Assigned to me**.
2.  In the list, click the claim case that you want to open.
3.  In the **Debit approval** field on the claim form, click the information icon \(![Information icon](../image/information-icon.png)\) next to the debit approval case number.


</td></tr><tr><td id="d128762e158">

**From the Debit Approvals list**

</td><td>

1.  In the **Lists** tab, under **Debit Approvals**, click **Assigned to me**.
2.  In the list, click the case that you want to open.


</td></tr></tbody>
</table>4.  If the total refund amount should be debited from multiple financial accounts in parts as per the customer's instructions, set up instructions for each debit account in the **Debit instructions** tab.

5.  Get an acceptance from the debit customer or debit account for each debit account listed in the **Debit instructions** tab and complete the refund.

6.  In the **Outcome** field, select an appropriate refund outcome.

7.  In the **Outcome notes** field, enter your comments that are related to the refund outcome.

8.  Click **Close**.


## Result

-   The debit approval case moves to the Close – Complete state.
-   The state of the associated claim case updates to Refund Complete.
-   The **Outcome**, **Outcome notes**, and **Refund amount** fields on the claim are updated from the debit approval case.
-   The debit customer gets a pre-configured email notification about the debit completion.

## What to do next

Update the claim case fields as required and [close the claim](close-claim-case.md).

**Parent Topic:**[Work on a claim with an internal refund](work-claim-with-internal-refund.md)

