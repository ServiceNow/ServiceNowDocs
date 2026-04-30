---
title: Add a policy participant to an insurance policy
description: Add a customer to an insurance policy as the insured entity by using the Insurance claims application.
locale: en-US
release: yokohama
product: Insurance Claims
classification: insurance-claims
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Setting up an insurance policy for Insurance claims, Setting up the policy data for Insurance claims, Setting up Insurance claims, Insurance claims, Claims applications, Using insurance applications, Financial Services Operations \(FSO\)]
---

# Add a policy participant to an insurance policy

Add a customer to an insurance policy as the insured entity by using the Insurance claims application.

## Before you begin

Create an insurance policy. For more information, see [Create an insurance policy](create-an-insurance-policy-for-a-consumer.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

2.  Open an insurance policy table.

3.  Open an insurance policy record in the table.

4.  Select the **Policy Participants** tab, and select **New**.

5.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Consumer \(for Personal insurance policies\)|Consumer record that is the insured entity.|
    |Account \(for Commercial insurance policies\)|Account record that is the insured entity.|

6.  Select **Save**.

7.  In the Policy Participant Role related list, select **New**.

8.  Enter the following field values.

    |Field|Value|
    |-----|-----|
    |Policy participant|&lt;customer record&gt;|
    |Role|&lt;insured&gt;|

9.  Select **Save**.


## What to do next

Add a related list to the insurance model's financial model view to see all the policies for that insurance product. For more information, see [Add a related list to an insurance product model](add-related-list-to-insurance-product-model.md).

**Parent Topic:**[Setting up an insurance policy for Insurance claims](../concept/set-up-an-insurance-policy.md)

