---
title: Enforce strict elevate privilege \[New in Security Center 1.3\]
description: Use the glide.security.strict\_elevate\_privilege property to control whether roles marked as privileged must be manually elevated for the user to be granted the role's capabilities.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Enforce strict elevate privilege \[New in Security Center 1.3\]

Use the **glide.security.strict\_elevate\_privilege** property to control whether roles marked as privileged must be manually elevated for the user to be granted the role's capabilities.

Set this property to true to add an extra layer of security validation when a privileged user elevates their role.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.security.strict\_elevate\_privilege**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

Boolean

</td></tr><tr><td>

Recommended value

</td><td>

true

</td></tr><tr><td>

Default value

</td><td>

true

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 6.7
-   CVSS score: Medium
-   Security risk details: When **glide.security.strict\_elevate\_privilege** is set to false, roles marked as privileged are automatically elevated upon an admin user new session, and do not need to be manually elevated \(with the exception of security\_admin\).

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

Functional impact

</td><td>

This property strictly requires admin role users to elevate privileges when needed.

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

