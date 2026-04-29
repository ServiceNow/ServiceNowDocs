---
title: Assign Key Management Framework roles
description: Administrators with the security\_admin role can assign Key Management Framework \(KMF\) admins, who in turn can assign other Key Management Framework roles.
locale: en-US
release: australia
product: Platform Encryption
classification: platform-encryption
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring the Key Management Framework, Key Management Framework, Encryption]
---

# Assign Key Management Framework roles

Administrators with the security\_admin role can assign Key Management Framework \(KMF\) admins, who in turn can assign other Key Management Framework roles.

## Before you begin

Role required: admin and security\_admin

You must elevate to the security\_admin role before assigning the KMF admin role. For instructions, see [Elevate to a privileged role](../../security/task/t_ElevateToAPrivilegedRole.md).

**Important:** KMF roles are required to use the Key Management Framework. Users without KMF roles aren’t be able to access lists, tables, and modules used to configure key management.

## Procedure

1.  Elevate to the security admin role.

2.  Navigate to **User Administration** &gt; **Users** and select the user you want to be the KMF admin.

3.  If the user doesn’t already have the admin and security\_admin roles, select **Edit** under the Roles related list and add **admin** and **security \_admin**.

4.  Navigate to **System Security** &gt; **Key Management Administration**.

5.  Select the user that you want to be KMF admin in the **Available Users** column and move them to the **Selected User\(s\)** column.

    ![User selection list](../image/kmf-admin-select-user.png)

6.  Select **Save**.

7.  Navigate to **User Administration** &gt; **Users** and select the user you just gave the KMF admin role to.

    That user now has the sn\_kmf.admin role in the Roles related list. That user can now assign other KMF roles.

    ![KMF admin role in the roles related list](../image/sn-kmf-admin-role.png)


## What to do next

If you have the KMF admin role, follow these steps for assigning other KMF roles:

1.  Navigate to **User Administration** &gt; **Users** and select the user you want to have another KMF role, such as KMF Cryptographic Manager.
2.  In the Roles related list, click **Edit** and select the KMF roles you want to assign the users. All KMF roles start with `sn_kmf`.

    ![Assigning other KMF roles](../image/kmf-roles-assignments.png)


## What to do next

To learn more about the available KMF roles, see [Roles installed with Key Management Framework](../../key-management-framework/reference/kmf-roles.md#).

**Parent Topic:**[Configuring the Key Management Framework](../concept/configure-kmf.md)

