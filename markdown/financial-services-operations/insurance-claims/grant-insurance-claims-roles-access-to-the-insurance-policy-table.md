---
title: Grant the Insurance claims roles access to an insurance policy table
description: Grant the Insurance claims contributor \(sn\_ins\_gen\_claim.fnol\_representative\) and agent \(sn\_ins\_gen\_claim.processor\) roles with access to an insurance policy table by using the Insurance claims application. This way, the users with these roles can view the policy details when they’re processing claims.
locale: en-US
release: yokohama
product: Insurance Claims
classification: insurance-claims
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Setting up an insurance policy for Insurance claims, Setting up the policy data for Insurance claims, Setting up Insurance claims, Insurance claims, Claims applications, Using insurance applications, Financial Services Operations \(FSO\)]
---

# Grant the Insurance claims roles access to an insurance policy table

Grant the Insurance claims contributor \(sn\_ins\_gen\_claim.fnol\_representative\) and agent \(sn\_ins\_gen\_claim.processor\) roles with access to an insurance policy table by using the Insurance claims application. This way, the users with these roles can view the policy details when they’re processing claims.

## Before you begin

Create a role that can access a table that extends the Insurance Policy \(sn\_bom\_ins\_policy\) table. For more information, see [Create a role to access insurance policy tables](create-roles-acls-and-grant-access.md).

Role required: admin

## Procedure

1.  Set the application scope in your instance to **Insurance claims**.

2.  Navigate to **All** &gt; **System Security** &gt; **Users and Groups** &gt; **Roles**.

3.  Search for sn\_ins\_gen\_claim.fnol\_representative and open the record.

4.  In the Contains Roles related list, select **Edit**.

5.  Add the role that can access the Insurance Policy \(sn\_bom\_ins\_policy\) table.

6.  Repeat this procedure for the sn\_ins\_gen\_claim.processor role.


## Result

The Insurance claims contributor \(sn\_ins\_gen\_claim.fnol\_representative\) and agent \(sn\_ins\_gen\_claim.processor\) roles have access to the insurance policy table. These roles can now interact with the table in an Insurance claims workflow.

## What to do next

Create an instance of the insurance policy by creating a policy record. For more information, see [Create an insurance policy](create-an-insurance-policy-for-a-consumer.md).

**Parent Topic:**[Setting up an insurance policy for Insurance claims](../concept/set-up-an-insurance-policy.md)

