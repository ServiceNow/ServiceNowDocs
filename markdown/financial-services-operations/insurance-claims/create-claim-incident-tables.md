---
title: Create a Claim Incident table
description: Create a Claim Incident \[sn\_ins\_claim\_property\] table for your business needs and the type of claims that you’re processing by using the Insurance claims application.
locale: en-US
release: australia
product: Insurance Claims
classification: insurance-claims
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Claim incidents, Configure, Insurance claims, Claims applications, Insurance applications, Financial Services Operations \(FSO\)]
---

# Create a Claim Incident table

Create a Claim Incident \[sn\_ins\_claim\_property\] table for your business needs and the type of claims that you’re processing by using the Insurance claims application.

## Before you begin

Set the application scope of your instance to **Insurance Claims Core**.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Label|Display label of the table.|
    |Name|Name of the table in snake case.|
    |Extends table|Option to extend the table. In this field, choose the base table Claim Incident.|

4.  Select **Submit**.


## What to do next

Create roles for the new Claim Incident \[sn\_ins\_claim\_property\] table. For more information, see [Create roles for a claim incident table](create-roles-for-a-claim-incident-table.md).

You can add script includes for the new incident table, including the code for getting the reference qualifier strings.

You can also create a workspace view for this new incident table if necessary.

