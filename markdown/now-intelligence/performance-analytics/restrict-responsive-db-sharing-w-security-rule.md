---
title: Restrict responsive dashboard sharing with security rules
description: You can configure the users, roles, and groups that users can see on the Share panel when they share a responsive dashboard.
locale: en-US
release: zurich
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Restrict responsive dashboard access to specific roles, Dashboard permissions, Administering dashboards, Responsive dashboards in the Core UI, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Restrict responsive dashboard sharing with security rules

You can configure the users, roles, and groups that users can see on the **Share** panel when they share a responsive dashboard.

## Before you begin

Role required: admin. To modify the Access Control List, the admin must elevate to the security\_admin role. For information, see [Elevate to a privileged role](https://www.servicenow.com/docs/access?context=t_ElevateToAPrivilegedRole&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

## About this task

Users who can see the **Share** icon based on the configuration of **List of roles \(comma-separated\) that can share their own dashboards** may not see content in the **Share** panel based on the configuration of the property **Apply security rules to the list of users, user groups, and roles that are visible when sharing dashboards**.

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **Dashboard Properties**.

2.  Select the box labeled **Apply security rules to the list of users, user groups, and roles that are visible when sharing dashboards** to apply security rules to what is visible in the **Share** panel.

    The existing security rule configuration for users, user groups and roles is described in their associated read access control list at the platform level. For more information, see [Access control list rules](https://www.servicenow.com/docs/access?context=access-control-rules&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).


## Result

Only users whose roles are specified in the field labeled **List of roles \(comma-separated\) that can share their own dashboards** can share their dashboards. If this property is configured and a user's role is not specified in the property, the user does not see the **Share** panel. When **Apply security rules to the list of users, user groups, and roles that are visible when sharing dashboards** is enabled, security rules are applied to the list of users, groups, and roles that the user can share their dashboards with in the **Share** panel.

**Related topics**  


[Share a responsive dashboard](t_ControlAccessToADashboard.md)

