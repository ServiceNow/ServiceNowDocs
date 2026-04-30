---
title: Roles installed with Key Management Framework
description: The Key Management Framework \(KMF\) introduces specific roles for cryptographic module and key management-related configurations.Assigns roles to other users to perform operations around the ServiceNow Key Management Framework.Create, read, and update operations on cryptographic modules \(association of keys to cryptographic usage and algorithm configurations\) and module access policies. Also, KMF cryptographic managers can perform key management \(generate, rotate, revoke\) and life cycle operations.View cryptographic module information, key metadata, and life cycle-related details, as well as module access policy \(MAP\) information.Integrate Key Management Framework with external keystores or systems.Access part of the ServiceNow Key Management Framework key lifecycle: renewal, rotation, revocation.Assign KMF roles to admins, who in turn can assign other KMF roles.
locale: en-US
release: yokohama
product: Platform Encryption
classification: platform-encryption
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Key Management Framework Reference, Key Management Framework, Encryption]
---

# Roles installed with Key Management Framework

The Key Management Framework \(KMF\) introduces specific roles for cryptographic module and key management-related configurations.

**Important:**

KMF roles are required to use the Key Management Framework. Users without KMF roles are not be able to access lists, tables and modules used to configure key management.

To assign the KMF admin role, you must have the admin, security\_admin, and sn\_kmf\_admin roles. Use the KMF admin role to assign other KMF roles. For details on assigning KMF roles, see [Assign KMF roles](kmf-roles.md#).

![KMF roles](../image/kmf-roles.png)

**Parent Topic:**[Key Management Framework Reference](../concept/understanding-kmf.md)

**Related topics**  


[Key Management Framework key life-cycle states](key-life-cycle-states.md)

[Module access policy visualization](../concept/map-vis-concept.md)

[Module access policy debugger](../concept/map-debugger.md)

[Encryption and Key Management subscription bundle](../../encryption/reference/encryption-sku.md)

## KMF admin \[sn\_kmf.admin\]

Assigns roles to other users to perform operations around the ServiceNow Key Management Framework.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

**Important:** Avoid granting an admin role when more specialized roles are available.

-   This role is assigned via the process shown in [Assign KMF roles](kmf-roles.md#).
-   You must have this role to assign  KMF roles, and in addition can perform all the capabilities of the KMF cryptographic manager.

## KMF cryptographic manager \[sn\_kmf.cryptographic\_manager\]

Create, read, and update operations on cryptographic modules \(association of keys to cryptographic usage and algorithm configurations\) and module access policies. Also, KMF cryptographic managers can perform key management \(generate, rotate, revoke\) and life cycle operations.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

## KMF cryptographic auditor \[sn\_kmf.cryptographic\_auditor\]

View cryptographic module information, key metadata, and life cycle-related details, as well as module access policy \(MAP\) information.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

## KMF cryptographic integrator \[sn\_kmf.cryptographic\_integrator\]

Integrate Key Management Framework with external keystores or systems.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

## KMF cryptographic operator \[sn\_kmf.cryptographic\_operator\]

Access part of the ServiceNow Key Management Framework key lifecycle: renewal, rotation, revocation.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

## Assign KMF roles

Assign KMF roles to admins, who in turn can assign other KMF roles.

### Before you begin

Role required: admin and security\_admin

You must elevate to the security\_admin role before assigning the KMF admin role. For instructions, see [Elevate to a privileged role](../../security/task/t_ElevateToAPrivilegedRole.md)

### Procedure

1.  Elevate to the security admin role.

2.  Navigate to **User Administration** &gt; **Users** and select the user you want to be the KMF admin.

3.  Verify that the user already has the admin and security\_admin roles.

    If not, select **Edit** under the Roles related list and add **admin** and **security \_admin**.

4.  Navigate to **System Security** &gt; **Key Management Administration**.

5.  Select the user that you want to be KMF admin in the **Available Users** column and move them to the **Selected User\(s\)** column.

    ![KMF admin role](../../encryption/image/kmf-admin-select-user.png)

6.  Select **Save**.

7.  Navigate to **User Administration** &gt; **Users** and select the user you just gave the sn\_kmf.admin role to.

    The user has the sn\_kmf.admin role in the **Roles** related list, and can assign other KMF roles.

    ![KMF admin role in the Roles related list](../../encryption/image/sn-kmf-admin-role.png)


### What to do next

If you have the KMF admin role, follow these steps for assigning other KMF roles:

1.  Navigate to **User Administration** &gt; **Users** and select the user you want to have another KMF role, such as KMF Cryptographic Manager.
2.  In the Roles related list, select **Edit** and select the KMF roles you want to assign the users. All KMF roles start with `sn_kmf`.

    ![Assigning other KMF roles](../../encryption/image/kmf-roles-assignments.png)


