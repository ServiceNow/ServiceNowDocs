---
title: Insurance policies in Insurance claims
description: In Financial Services Operations, the Insurance Policy \(sn\_bom\_ins\_policy\) table is the base table for all insurance policies. Whenever a new type of policy is introduced in Insurance claims, you create a dedicated table for that insurance policy type.
locale: en-US
release: xanadu
product: Insurance Claims
classification: insurance-claims
topic_type: concept
last_updated: "2024-10-09"
reading_time_minutes: 1
breadcrumb: [Setting up an insurance policy for Insurance claims, Setting up the policy data for Insurance claims, Setting up Insurance claims, Insurance claims, Claims applications, Insurance applications, Financial Services Operations \(FSO\)]
---

# Insurance policies in Insurance claims

In Financial Services Operations, the Insurance Policy \(sn\_bom\_ins\_policy\) table is the base table for all insurance policies. Whenever a new type of policy is introduced in Insurance claims, you create a dedicated table for that insurance policy type.

The Insurance claims application includes a personal travel policy and a commercial travel policy as offerings from the base system. Each policy has a separate table that you use to manage these specific policies. This structured approach helps to ensure that each type of policy is properly organized and maintained within the system.

You can grant specific agents access to read particular policies. By creating separate tables and read or write roles for different insurance policy types or tables, you can control the permissions more effectively by ensuring that only authorized agents can view the policies that are relevant to their roles.

**Parent Topic:**[Setting up an insurance policy for Insurance claims](../../fso-insurance-claims-flow/concept/set-up-an-insurance-policy.md)

**Related topics**  


[Create an insurance policy table](../../fso-insurance-claims-flow/task/create-an-insurance-policy-table.md)

[Create a role to access insurance policy tables](../../fso-insurance-claims-flow/task/create-roles-acls-and-grant-access.md)

[Create an insurance policy](../../fso-insurance-claims-flow/task/create-an-insurance-policy-for-a-consumer.md)

