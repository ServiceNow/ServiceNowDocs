---
title: Create an insurance policy table
description: Create a table that extends the Insurance Policy \(sn\_bom\_ins\_policy\) table in the Insurance claims application. You use this table to hold all the information about insurance policies of a particular type that you sold to your customers. Creating tables helps to ensure that each type of policy is properly organized and maintained within the system.
locale: en-US
release: australia
product: Insurance Claims
classification: insurance-claims
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setting up an insurance policy for Insurance claims, Setting up the policy data for Insurance claims, Configure, Insurance claims, Claims applications, Insurance applications, Financial Services Operations \(FSO\)]
---

# Create an insurance policy table

Create a table that extends the Insurance Policy \(sn\_bom\_ins\_policy\) table in the Insurance claims application. You use this table to hold all the information about insurance policies of a particular type that you sold to your customers. Creating tables helps to ensure that each type of policy is properly organized and maintained within the system.

## Before you begin

Set the application scope in your instance to **Financial Services Operations Core**.

Role required: admin

## About this task

Each type of insurance policy requires a table that extends the Insurance Policy \(sn\_bom\_ins\_policy\) table.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

2.  Select **New**.

3.  In the **Label** field, enter the name of the insurance policy.

4.  In the **Extends table** field, select **Insurance Policy**.

5.  Select **Submit**.

    You created a table that inherits all the fields from the Insurance Policy \(sn\_bom\_ins\_policy\) table.


## What to do next

Set up the roles, establish read-and-write access control lists \(ACLs\), and then grant access to the table. For more information, see [Create a role to access insurance policy tables](create-roles-acls-and-grant-access.md).

**Parent Topic:**[Setting up an insurance policy for Insurance claims](../concept/set-up-an-insurance-policy.md)

