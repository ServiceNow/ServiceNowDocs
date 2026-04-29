---
title: Create an insurance policy
description: Create a policy record in the system that represents the agreement between the insurance provider and the customer by using the Insurance claims application.
locale: en-US
release: australia
product: Insurance Claims
classification: insurance-claims
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setting up an insurance policy for Insurance claims, Setting up the policy data for Insurance claims, Configure, Insurance claims, Claims applications, Insurance applications, Financial Services Operations \(FSO\)]
---

# Create an insurance policy

Create a policy record in the system that represents the agreement between the insurance provider and the customer by using the Insurance claims application.

## Before you begin

An insurance product model, a coverage specification, and an insurance policy table that extends the Insurance Policy \(sn\_bom\_ins\_policy\) table are required. For more information, see the following topics:

-   [Insurance product models](../concept/insurance-product-models.md)
-   [Coverage specification](../concept/coverage-specification.md)
-   [Create an insurance policy table](create-an-insurance-policy-table.md)

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

2.  Open the list view of the insurance policy table that you want to create a policy for.

3.  Select **New**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Product|Insurance product model.|
    |Name|Name of the insurance policy.|
    |Policy number|Unique identifier of the policy.|
    |Policy holder|Customer that owns the policy.|
    |Effective date|Effective date of the policy. The date is set to either the current date or the past.|
    |Expiration date|Date when the policy expires.|
    |Status|Status of the policy. Active policies are set to In Force. Policies that aren’t In Force are ignored when creating a case.|

5.  Select **Update**.


## What to do next

Apply coverage to an insurance policy. For more information, see [Apply coverages to an insurance policy](apply-coverage-to-an-insurance-policy.md).

**Parent Topic:**[Setting up an insurance policy for Insurance claims](../concept/set-up-an-insurance-policy.md)

