---
title: Create a role to access insurance policy tables
description: Create a role to enable an authorized agent to access tables that extend the Insurance Policy \(sn\_bom\_ins\_policy\) table by using the Insurance claims application. By creating a role, you ensure that only authorized agents can view the policies that are relevant to their roles.
locale: en-US
release: xanadu
product: Insurance Claims
classification: insurance-claims
topic_type: task
last_updated: "2024-10-09"
reading_time_minutes: 1
breadcrumb: [Setting up an insurance policy for Insurance claims, Setting up the policy data for Insurance claims, Setting up Insurance claims, Insurance claims, Claims applications, Insurance applications, Financial Services Operations \(FSO\)]
---

# Create a role to access insurance policy tables

Create a role to enable an authorized agent to access tables that extend the Insurance Policy \(sn\_bom\_ins\_policy\) table by using the Insurance claims application. By creating a role, you ensure that only authorized agents can view the policies that are relevant to their roles.

## Before you begin

Create a table that extends the Insurance Policy \(sn\_bom\_ins\_policy\) table for a particular type of policy. For more information, see [Create an insurance policy table](create-an-insurance-policy-table.md).

Role required: admin

## Procedure

1.  Set the application scope in your instance to **Financial Services Operations Core**.

2.  Navigate to **All** &gt; **System Security** &gt; **Users and Groups** &gt; **Roles**.

3.  Select **New**.

4.  In the **Suffix** field, enter the name of the role.

5.  In the **Assignable by** field, select **sn\_bom.admin**.

    This role is an admin role of the Financial Services Operations Core application.

6.  In the **Description** field, enter a description of the role.

7.  Select **Submit**.


## What to do next

Create an access control list \(ACL\) to define which roles can access an insurance policy table. For more information, see [Create an access control list for an insurance policy table](create-an-access-control-list-for-the-insurance-policy-table.md).

**Parent Topic:**[Setting up an insurance policy for Insurance claims](../concept/set-up-an-insurance-policy.md)

