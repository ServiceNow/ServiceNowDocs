---
title: Create a debit approval case for an internal refund
description: Create a debit approval case for a claim so that you can request a refund internally from one of your banks or a customer.
locale: en-US
release: yokohama
product: Financial Services Payment Operations
classification: financial-services-payment-operations
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Work on a claim with an internal refund, Managing payment claims and debit approvals, Payment Operations, Using banking applications, Financial Services Operations \(FSO\)]
---

# Create a debit approval case for an internal refund

Create a debit approval case for a claim so that you can request a refund internally from one of your banks or a customer.

## Before you begin

Role required: sn\_bom\_payment.claim\_agent or sn\_bom\_payment.claim\_agent\_connector

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Click the lists icon \(![lists icon](../../fso-card-operations/image/list-icon.png)\).

3.  In the **Lists** tab, under **Claims**, click **Assigned to me**.

4.  In the list, click the case that you want to open.

5.  On the claim form, fill in these fields:

    -   Error type
    -   Error category
    -   Error subcategory
    -   Requested treatment
    -   Claim bank
    -   Transaction ID
    -   Refund bank
    -   Debit customer or Debit account
    -   Debit financial account
    -   Receiving transaction
    For information on the Claim form field descriptions, see [Field descriptions for a claim case](../reference/claim-form-fields.md).

6.  Click **Create Debit Approval**.


## Result

-   A payment service case for debit approval is created and is assigned to the claim agent that is working on the claim.
-   The state of the claim case updates to Awaiting Refund.
-   The debit customer gets a pre-configured email notification about the debit approval case.
-   If there's a Customer or Consumer Service Portal available for customers, they get a notification for the debit approval case on the portal. Buttons for accepting or rejecting the debit approval appear in the section of the form that shows the customer actions on the portal. For more information, see:

    -   [View a case from the Consumer Service Portal](https://www.servicenow.com/docs/access?context=view-cases-consumer-portal&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)
    -   [Accept or reject a case solution from the Consumer Service Portal](https://www.servicenow.com/docs/access?context=resolve-cases-consumer-portal&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)
    **Note:** To use the Consumer Service Portal, activate the Consumer Service Portal plugin \(com.glide.service-portal.consumer-portal\).


## What to do next

-   If the refund amount should be debited from multiple financial accounts, set up instructions for each debit account in the Debit instructions tab.
-   Get an acceptance for the debit from the debit customer or the refund bank.
-   Update the debit approval case fields as required to complete the refund and close this case. For more information, see [Work on a debit approval case to complete a refund](work-debit-approval-case-internal-refund.md).
-   If the debit customer or the bank rejects the debit, move the claim case back to the **Open** state. If the customer rejected the debit from the Customer or Consumer Service Portal, the state of the claim case automatically updates to Open.

**Parent Topic:**[Work on a claim with an internal refund](work-claim-with-internal-refund.md)

