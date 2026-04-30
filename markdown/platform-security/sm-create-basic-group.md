---
title: Create a basic secret group
description: Create a basic secret group to group any secrets, regardless of their criteria.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Secrets management dashboard, Secrets Management, Platform Security]
---

# Create a basic secret group

Create a basic secret group to group any secrets, regardless of their criteria.

## Before you begin

Role required: admin

Basic secret groups can contain any secret you add to them, regardless of their table, scope, or application. After creating it, you manually add secrets to the group. To create a group specifically for all secrets that share a common attribute such as those, create a secret group with criteria using the instructions in [Create a secret group with criteria](sm-create-criteria-group.md).

## Procedure

1.  Navigate to **All** &gt; **Secrets Management** &gt; **Secret Groups**.

2.  Select **New**.

3.  At the **What type of Secret Group would you like to create?** select **Basic Secret Group**.

4.  In the **Secret Group** form, fill in the fields.

<table id="table_tgr_xp5_4tb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Group Name

</td><td>

Name for the group**Note:** Secret group names can only contain lowercase characters, numbers, and underscores\( \_ \)

</td></tr><tr><td>

Secret Type

</td><td>

Whether the group is **Instance accessible** or **Client accessible**.

</td></tr><tr><td>

Autogen Module

</td><td>

Generates a new cryptographic module for this secret group. This module encrypts and decrypts your data. This field is enabled by default.

</td></tr><tr><td>

Application

</td><td>

Scoped application for this record. This read-only field is automatically populated with the current scope.

</td></tr><tr><td>

Short Description

</td><td>

Description of the group

</td></tr><tr><td>

Crypto Module

</td><td>

Select the cryptographic module to use with this group. This module encrypts and decrypts your data. This field is only visible when **Autogen Module** isn’t selected. For details on module access policies, see [Module access policy overview](../../key-management-framework/concept/module_access_policy_overview.md) **Note:** You can review the module access policies related to your secret group using the **Manage instance access** button.

</td></tr></tbody>
</table>5.  Click **Submit**.

    **Note:** When created, a secret group is inactive by default. Return to the group record and select **Active** to activate the group.


**Parent Topic:**[Secrets management dashboard](../concept/secrets-dashboard.md)

