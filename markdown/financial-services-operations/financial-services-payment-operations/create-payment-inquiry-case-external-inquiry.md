---
title: Create a payment inquiry case for an external inquiry
description: As an inquiry agent, you can create an inquiry case for an external inquiry that you receive from a third-party bank.
locale: en-US
release: xanadu
product: Financial Services Payment Operations
classification: financial-services-payment-operations
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Managing payment inquiries, Financial Services Payment Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Create a payment inquiry case for an external inquiry

As an inquiry agent, you can create an inquiry case for an external inquiry that you receive from a third-party bank.

## Before you begin

Role required: sn\_bom\_payment.inquiry\_agent or sn\_bom\_payment.inquiry\_agent\_connector

## About this task

An external inquiry is the inquiry that comes from a third-party bank, which means that the payment recipient is always internal.

**Note:** There can never be a case where both the inquiry and the recipient are external.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Click the lists icon \(![lists icon](../../fso-card-operations/image/list-icon.png)\).

3.  In the **Lists** tab, under **Payment Inquiry Cases**, click **All**.

4.  Click **New**.

5.  In the New Payment Inquiry Case dialog box, select **Beneficiary Claim Non-Receipt - External** from the list.

6.  Click **Create**.

7.  On the form, fill in the required fields and any other information that is related to the request that you've received from the sender bank.

    For information on Payment Inquiry Case form field descriptions, see [Field descriptions for a payment inquiry case](../reference/payment-inquiry-case-form-fields.md).

8.  Click **Save**.


## Result

The payment inquiry case is created in the New state and is assigned to an assignment group or inquiry agent in the payment inquiry department. The assignment group or user to whom the case is assigned is based on the assignment rules.

## What to do next

-   As an inquiry agent, if the case is not assigned to you, you can assign the case to yourself and start investigating it. For more information on working on a payment inquiry case, see [Investigate a payment inquiry case](investigate-payment-inquiry-case.md).

-   You can also assign the case to any other inquiry agent. For more information, see [Assign a payment inquiry case](assign-payment-inquiry-case.md).

**Parent Topic:**[Managing payment inquiries](../concept/managing-payment-inquiries.md)

