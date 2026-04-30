---
title: Create a claim for a payment inquiry case
description: Create a claim for an internal payment inquiry case when its investigation indicates that it's a valid claim and the customer is entitled to a refund.
locale: en-US
release: xanadu
product: Financial Services Payment Operations
classification: financial-services-payment-operations
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Investigate a payment inquiry case, Managing payment inquiries, Financial Services Payment Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Create a claim for a payment inquiry case

Create a claim for an internal payment inquiry case when its investigation indicates that it's a valid claim and the customer is entitled to a refund.

## Before you begin

Role required: sn\_bom\_payment.inquiry\_agent or sn\_bom\_payment.inquiry\_agent\_connector

## About this task

Set the case as **Valid claim** and create a claim for the inquiry.

You can set a case as a valid claim and create a claim for it only if it's an internal payment inquiry case such as a Beneficiary Claim Non-Receipt - Internal and Payment made In Error.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Click the lists icon \(![lists icon](../../fso-card-operations/image/list-icon.png)\).

3.  In the **Lists** tab, under **Payment Inquiry Cases**, click **Assigned to me**.

4.  In the list, select the case that you want to open.

5.  Set the inquiry case as a valid claim.

    1.  Select the **Valid claim** check box.

    2.  In the **Payment processor** field, select a payment processor.

    3.  In the **Transaction ID** field, enter the transaction ID.

    4.  In the **Additional comments** field, enter your comments.

    5.  Click **Update**.

6.  In the **Additional comments** field, enter your comments regarding the claim and click **Create Claim**.


## Result

-   A claim case for the payment inquiry case is created and assigned to an assignment group or a claim agent based on the configured assignment rules. The payment inquiry is now tracked via the claim case.

    You can view the case details by clicking the link in the case creation message. For more information on claims, see [Managing payment claims and debit approvals](../concept/managing-payment-claims.md).

-   The customer gets a pre-configured email notification about the new claim case.
-   If there's a Customer or Consumer Service Portal available for customers, the new claim case appears on the portal.

    For more information, see [View a case from the Consumer Service Portal](https://www.servicenow.com/docs/access?context=view-cases-consumer-portal&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US).

    **Note:** To use the Consumer Service Portal, activate the Consumer Service Portal plugin \(com.glide.service-portal.consumer-portal\).


## What to do next

You can close the associated inquiry case as the request is now tracked via the claim case. For more information, see [Close a payment inquiry case](close-payment-inquiry-case.md).

**Parent Topic:**[Investigate a payment inquiry case](investigate-payment-inquiry-case.md)

