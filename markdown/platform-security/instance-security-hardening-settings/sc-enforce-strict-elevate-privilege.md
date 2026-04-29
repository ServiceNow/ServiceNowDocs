---
title: Enforce strict elevate privilege
description: Use the glide.security.strict\_elevate\_privilege property to control whether roles marked as privileged must be manually elevated for the user to be granted the role's capabilities.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Enforce strict elevate privilege

Use the **glide.security.strict\_elevate\_privilege** property to control whether roles marked as privileged must be manually elevated for the user to be granted the role's capabilities.

When the **glide.security.strict\_elevate\_privilege** system property is set to **true**, roles marked as privileged must always be manually elevated by an admin user upon new session creation in order for the user to be granted the role's capabilities. When **false**, roles marked as privileged are automatically elevated upon an admin user new session, and do not need to be manually elevated \(with exception of security\_admin\). Setting this property to secure value adds an extra layer of security validation to role elevation by privileged user.

Ensure that **glide.security.strict\_elevate\_privilege** is set to **true** as it allows a user with admin to manually elevate to a role they want.

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

&lt;none&gt;

</td></tr><tr><td>

Fallback value

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
-   Security risk details: This risks potential privilege misuse or accidental execution of high-impact actions. Requiring manual elevation adds a deliberate security checkpoint that helps prevent unauthorized or unintended access to sensitive capabilities.

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

