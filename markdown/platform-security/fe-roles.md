---
title: Role requirements for Field Encryption
description: Learn about the roles required to configure Field Encryption.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-28"
reading_time_minutes: 1
breadcrumb: [Configuring Field Encryption, Field Encryption, Encryption]
---

# Role requirements for Field Encryption

Learn about the roles required to configure Field Encryption.

Managing requires the following roles. Since is based on the Key Management Framework, there are roles common to both.

-   Admin
-   Security Admin
-   KMF Admin
-   KMF Cryptographic Manager

For complete details on details on roles, see [Roles installed with Key Management Framework](../../key-management-framework/reference/kmf-roles.md#).

## Admin and Security Admin

Users must have the admin role to elevate to the Security Admin role. You need the Security Admin role to perform high Security Tasks, such as configuring encrypted field configurations and configuring Access Observer.

Admins can elevate to Security admin using this procedure.

1.  Select on your profile picture at the top right of the screen.
2.  In the drop-down menu, select **Elevate Role**.
3.  Select **Security Admin**.
4.  Select **Save**.

## KMF Admin

Users with the Admin role can assign users to the KMF admin role using this process:

1.  Navigate to **All** &gt; **System Security** &gt; **Key Management Administration**.
2.  From the **Available Users** list, move a user who needs the KMF Admin role over to the **Selected User\(s\)** list.
3.  Select **Save**.

**Important:** For help prevent security issues, avoid granting the KMF Admin role to more than one users. Avoid assigning this role to users when more specialized roles are available.

## KMF Cryptographic Manager

Users with the KMF Cryptographic Manager role can create and update operations on cryptographic modules and module access policies. KMF cryptographic managers can also perform key management and life cycle operations.

Use the following process to assign this role to a user.

1.  Navigate to **All** &gt; **System Security** &gt; **Users**.
2.  Select a user that needs to configure Field Encryption.
3.  In the **Roles** related list, select **Edit**.
4.  Search for `sn_kmf.cryptographic manager` and add the role the selected user.
5.  Select **Save**.

**Parent Topic:**[Configuring Field Encryption](configuring-column-level-encryption.md)

