---
title: Grant Insurance claims roles access to a claim incident table
description: Grant the sn\_bom.fnol\_representative and sn\_ins\_gen\_claim.processor roles with access to a claim incident table by using the Insurance claims application. This way, the users with these roles can read and write entries in a claim incident table during the claim creation process.
locale: en-US
release: xanadu
product: Insurance Claims
classification: insurance-claims
topic_type: task
last_updated: "2024-10-29"
reading_time_minutes: 1
breadcrumb: [Claim incidents, Setting up Insurance claims, Insurance claims, Claims applications, Insurance applications, Financial Services Operations \(FSO\)]
---

# Grant Insurance claims roles access to a claim incident table

Grant the sn\_bom.fnol\_representative and sn\_ins\_gen\_claim.processor roles with access to a claim incident table by using the Insurance claims application. This way, the users with these roles can read and write entries in a claim incident table during the claim creation process.

## Before you begin

Set the application scope of your instance to **Financial Services Operations Core**.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Users and Groups** &gt; **Roles**.

2.  Search for the role sn\_bom.fnol\_representative and open the record.

3.  In the Contains Roles related list, select **Edit**.

4.  Add the reader and writer roles for the claim incident table to the Contains Roles List.

5.  Select **Save**.

6.  Select **Update**.


## What to do next

Repeat these steps for the sn\_ins\_gen\_claim.processor role. Ensure that the application scope of your instance is set correctly.

