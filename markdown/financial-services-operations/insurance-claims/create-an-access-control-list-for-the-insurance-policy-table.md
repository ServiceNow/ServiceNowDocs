---
title: Create an access control list for an insurance policy table
description: Create an access control list \(ACL\) for a table that extends the Insurance Policy \(sn\_bom\_ins\_policy\) table by using the Insurance claims application. By creating an ACL, you ensure that users with specific roles can interact with tables for a particular insurance policy.
locale: en-US
release: zurich
product: Insurance Claims
classification: insurance-claims
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Setting up an insurance policy for Insurance claims, Setting up the policy data for Insurance claims, Configure, Insurance claims, Claims applications, Insurance applications, Financial Services Operations \(FSO\)]
---

# Create an access control list for an insurance policy table

Create an access control list \(ACL\) for a table that extends the Insurance Policy \(sn\_bom\_ins\_policy\) table by using the Insurance claims application. By creating an ACL, you ensure that users with specific roles can interact with tables for a particular insurance policy.

## Before you begin

Create a role to assign access to a table that extends the Insurance Policy \(sn\_bom\_ins\_policy\) table. For more information, see [Create a role to access insurance policy tables](create-roles-acls-and-grant-access.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

2.  Open the table definition of the insurance policy.

3.  In the Access Controls related list, select **New**.

    Elevate your role to security\_admin to create an ACL.

4.  In the Requires role list, assign the role and sn\_bom.admin to the new ACL.

    For example, if you created a viewer role, you would create a read operation ACL and assign the viewer role that you created, and add the sn\_bom.admin role to the Requires role list.

    **Note:** Adding the sn\_bom.admin role enables you as the application administrator to manage access to the insurance policy table more effectively. You can then grant, revoke, or modify access without needing system-level permissions. This role provides you with greater flexibility while enabling you to maintain control over the table.


## Result

The insurance policy table contains the ACLs for the roles in your workflow, providing them with the appropriate level of access. The sn\_bom.admin role is also added to the table so that you, as the application administrator, can manage access.

## What to do next

Grant the Insurance claims contributor \(sn\_ins\_gen\_claim.fnol\_representative\) and agent \(sn\_ins\_gen\_claim.processor\) roles so that they can access the insurance policy table. For more information, see [Grant the Insurance claims roles access to an insurance policy table](grant-insurance-claims-roles-access-to-the-insurance-policy-table.md).

**Parent Topic:**[Setting up an insurance policy for Insurance claims](../concept/set-up-an-insurance-policy.md)

