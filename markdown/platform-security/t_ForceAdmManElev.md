---
title: Force administrators to manually elevate
description: A property is available to force all users with the administrator role to manually select the role that they want to elevate to.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Elevated privilege roles, Security Roles, Access Management]
---

# Force administrators to manually elevate

A property is available to force all users with the administrator role to manually select the role that they want to elevate to.

## Before you begin

Role required: security\_admin

## Procedure

1.  Log in as admin.

2.  Elevate your role to security\_admin.

3.  Navigate to **sys\_properties.list**.

4.  Search for and select the **glide.security.strict\_elevate\_privilege** property.

5.  Set the Value field to **true** and click **Submit**.


## Result

When the user logs in, they are presented with a dialog window to select the role to which they can elevate.

**Parent Topic:**[Elevated privilege roles](../concept/c_ElevatedPrivilege.md)

**Related topics**  


[Security\_admin role](../concept/security-admin-role.md)

[Elevate to a privileged role](t_ElevateToAPrivilegedRole.md)

