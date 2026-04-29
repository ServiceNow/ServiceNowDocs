---
title: Apply coverages to an insurance policy
description: Define the coverages for an insurance policy by using the Insurance claims application. You can define what coverages types and coverage options apply to a customer's insurance policy.
locale: en-US
release: australia
product: Insurance Claims
classification: insurance-claims
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setting up an insurance policy for Insurance claims, Setting up the policy data for Insurance claims, Configure, Insurance claims, Claims applications, Insurance applications, Financial Services Operations \(FSO\)]
---

# Apply coverages to an insurance policy

Define the coverages for an insurance policy by using the Insurance claims application. You can define what coverages types and coverage options apply to a customer's insurance policy.

## Before you begin

Create a coverage specification with the coverage types and coverage options. For more information, see [Coverage specification](../concept/coverage-specification.md).

Create an insurance policy. For more information, see [Create an insurance policy](create-an-insurance-policy-for-a-consumer.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

2.  Open the list view of an insurance policy table.

3.  Open an insurance policy record in the table.

4.  Select and hold \(or right-click\) the header and navigate to **Configure** &gt; **Related Lists**.

5.  Confirm that only the following related lists are present:

    -   Policy Coverage-&gt;Insurance policy
    -   Policy Participant-&gt;Insurance policy
6.  Select **Save**.

7.  In the Policy Coverages related list, select **New**.

8.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Coverage type|Coverage type record.|
    |Coverage value|Coverage type option record.|

9.  Repeat steps 7 through 8 for each policy coverage that you want to add.


## What to do next

Add a policy participant as the insured entity to the policy. For more information, see [Add a policy participant to an insurance policy](add-a-policy-participant-to-an-insurance-policy.md).

**Parent Topic:**[Setting up an insurance policy for Insurance claims](../concept/set-up-an-insurance-policy.md)

