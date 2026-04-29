---
title: Create a case for an external claim
description: As a claim agent, you can create a case for a refund request that comes from a third-party bank.
locale: en-US
release: australia
product: Financial Services Payment Operations
classification: financial-services-payment-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Managing payment claims and debit approvals, Use, Payment Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Create a case for an external claim

As a claim agent, you can create a case for a refund request that comes from a third-party bank.

## Before you begin

Role required: sn\_bom\_payment.claim\_agent or sn\_bom\_payment.claim\_agent\_connector

## About this task

For an external claim, the refund type is always internal, which means that the refund is made by the bank internally.

With this procedure, you can also create cases for internal claims.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon](../../../use/reporting/image/inline-data-vis-96px-list.png)\).

3.  In the **Lists** tab, under **Claims**, click **All** and then click **New**.

4.  In the New Claim dialog box, select **External** from the list.

5.  Click **Create**.

6.  On the form, fill in the required fields and any other information that is related to the claim that you've received from the sender bank.

    For information on the Claim form field descriptions, see [Field descriptions for a claim case](../reference/claim-form-fields.md).

7.  Click **Save**.


## Result

A case is created for the claim in the New state. The case is then assigned to an assignment group or claim agent in the payment claim department. The assignment group or user to whom the case is assigned is based on the assignment rules.

## What to do next

-   As a claim agent, you can assign the case to yourself and start working on it. For more information, see [Work on a claim with an internal refund](work-claim-with-internal-refund.md).
-   You can also assign the case to any other claim agent. For more information, see [Assign a payment claim](assign-payment-claim.md).

**Parent Topic:**[Managing payment claims and debit approvals](../concept/managing-payment-claims.md)

