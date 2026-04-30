---
title: Contextual Security Manager
description: Contextual Security Manager protects your data by controlling read, write, create, and delete authorization.
locale: en-US
release: xanadu
product: Access Control
classification: access-control
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Access Control List Rules, Access Management]
---

# Contextual Security Manager

Contextual Security Manager protects your data by controlling read, write, create, and delete authorization.

## Key advantages

The Contextual Security Manager is aware of the system table hierarchy, enabling you to create specific security rules for a field based on where in the hierarchy it is displayed. Benefits of the Contextual Security Manager include:

-   **Contextual security**: Secure a record based on the contents of the record.
-   **Hierarchical security**: Apply security rules to any level in the object hierarchy.

## Securing fields and tables

With the legacy Simple Security Manager, you could secure fields and tables by adding roles to the appropriate dictionary entry. With the Contextual Security Manager, these dictionary roles are no longer tested. Instead, the system looks for ACL rules on fields and tables.

**Warning:** After you install the Contextual Security Manager, you must secure fields and tables via ACL rules. Even if you [Configuring the form layout](https://www.servicenow.com/docs/access?context=configure-form-layout&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) the dictionary form and add roles to a dictionary entry, no change in rights occurs.

## Contextual security and roles

You can grant roles to users or groups. However, after installing the Contextual Security Manager, the **roles** field on the user record is no longer checked and no longer appears on your user and group forms. Instead, you must add roles to the Roles related list instead of to the user or group record.

Applications and modules contain lists of the roles required to view them. For example, to view the System Definition application, the admin role is required. Security rights for applications and modules are still defined using role arrays.

Both catalog items and catalog variables contain lists of the roles required to view them. Security rights for catalog items and catalog variables are still defined via these role arrays.

Under the Contextual Security Manager, a group still automatically inherits any role granted to the group when the inherits flag for the role is set to true.

## Activating the Contextual Security Manager

The Contextual Security Manager is active in the base system. If there are many duplicate entries in the User Roles table, you may need to upgrade to Contextual Security: Role Management V2 to eliminate duplicate roles. Plugins include:

-   **Contextual Security: Role Management \[com.glide.role\_management\]**

    Provides contextual security functionality. This plugin is automatically installed.

-   **Contextual Security: Role Management V2 \[com.glide.role\_management.inh\_count\]**

    Prevents duplicate entries caused by inherited roles in the User Roles \[sys\_user\_has\_role\] table. This plugin is automatically installed on new instances and can be activated for upgrades. The Contextual Security: Role Management Enhancements plugin is a previous version of this plugin. The Role Management Enhancements plugin does not include the RoleManagementVerify\(\) script. This script returns a list of changes that an upgrade will perform, enabling you to monitor changes made by the plugin.


**Note:** After activating Role Management V2, you must set the glide.role\_management.v2.audit\_roles system property to allow the Audit Roles table to create audit records related to user roles. To learn more about setting this property and about the Audit Roles table, see:

-   [Enable role auditing with Contextual Security: Role Management V2](../task/enable-audit-roles.md).
-   [Hardening settings](../../security-center/reference/security-hardening-settings.md) in Instance Security Hardening Settings.
-   [Audit user roles](https://www.servicenow.com/docs/access?context=audit-user-roles&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)

