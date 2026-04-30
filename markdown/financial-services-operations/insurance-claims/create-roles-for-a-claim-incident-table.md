---
title: Create roles for a claim incident table
description: Create roles to access claim incident tables by using the Insurance claims application. This way, you can ensure that only authorized users can access the claim incidents that are relevant to their roles.
locale: en-US
release: zurich
product: Insurance Claims
classification: insurance-claims
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Claim incidents, Configure, Insurance claims, Claims applications, Insurance applications, Financial Services Operations \(FSO\)]
---

# Create roles for a claim incident table

Create roles to access claim incident tables by using the Insurance claims application. This way, you can ensure that only authorized users can access the claim incidents that are relevant to their roles.

## Before you begin

Set the application scope of your instance to **Insurance Claims Core**.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Users and Groups** &gt; **Roles**.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Suffix|Role that you are creating for the new claim incident table; that is, a writer or reader role.|
    |Description|Brief description of what the role is.|

    Refer to the writer and reader roles in the base system as an example, such as sn\_ins\_claim.trip\_writer and sn\_ins\_claim.trip\_reader.


## What to do next

Create access control lists for the claim incident table so that specific roles can interact with the claim incident table. For more information, see [Create an access control list for a claim incident table](create-acls-for-a-claim-incident-table.md).

