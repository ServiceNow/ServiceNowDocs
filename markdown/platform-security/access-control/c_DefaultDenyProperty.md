---
title: Default deny property
description: The default deny property \(glide.sm.default\_mode\) controls the security manager default behavior when the only matching ACL rules are the wildcard table ACL rules.
locale: en-US
release: australia
product: Access Control
classification: access-control
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Contextual Security Manager, Access Control List Rules, Access Management]
---

# Default deny property

The default deny property \(`glide.sm.default_mode`\) controls the security manager default behavior when the only matching ACL rules are the wildcard table ACL rules.

A set of wildcard table ACL rules for the most common record-based operations are available: read, write, create, and delete. A significant number of ACLs to provide role-based access to system tables are also available. For example, there are ACLs that grant sys\_script access to the business\_rule\_admin role because that role is documented as being able to manage business rules.

Use the `glide.sm.default_mode` property to deny or allow these operations on all tables:

-   **Deny Access**: The wildcard table ACL rules restrict the read, write, create, and delete operations on all tables unless the user has the admin role or meets the requirements of another table ACL rule. Other operations, such as report\_on and personalize\_choices, are unaffected by this setting.
-   **Allow Access**: The wildcard table ACL rules allow the read, write, create, and delete operations on all tables unless there are specific table ACL rules in place to restrict such operations.

You cannot reset `glide.sm.default_mode` to **Allow Access** once it has been set to **Deny Access**.

**Note:** By default, the wildcard table ACL rules are the only ACL rules that check for the value of the `glide.sm.default_mode` property. If you want to control other operations with this setting, create your own ACL rules to check for this property value.

To learn more about this property, see [Deny by default with empty ACLs \[Updated in Security Center 1.3\]](../../security-center/reference/sc-security-manager-default-deny.md) in Instance Security Hardening Settings.

