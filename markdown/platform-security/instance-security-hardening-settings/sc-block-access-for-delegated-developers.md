---
title: Block access for delegated developers
description: This configuration affects access for delegated developers that are updating user roles through script. When the configuration is compliant, the developer will not be able to update or insert records into the sys\_user\_has\_role table without also having the user\_admin role.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Block access for delegated developers

This configuration affects access for delegated developers that are updating user roles through script. When the configuration is compliant, the developer will not be able to update or insert records into the sys\_user\_has\_role table without also having the user\_admin role.

This property determines whether a delegated developer can give assign roles to users through scripts. If **com.glide.sys.security.delegateddev.block\_grant\_roles** is not set to the recommended value of **true**, then a delegated developer could assign roles to any user. This could lead to unapproved privilege escalation.

Ensure that the property **com.glide.sys.security.delegateddev.block\_grant\_roles** is set to **true**.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**com.glide.sys.security.delegateddev.block\_grant\_roles**

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
-   CVSS rating: Medium
-   Security risk details: Delegated developers may assign roles to any user via scripts, posing a significant security risk of unauthorized privilege escalation.

</td></tr><tr><td>

Functional impact

</td><td>

When a user with the delegated\_developer role is attempting to modify a record in the User Roles \[sys\_user\_has\_role\] table, this property enables additional security checks against the operation. The additional security checks validate that the user has been granted the user\_admin role if they're trying to create or update the User Roles \[sys\_user\_has\_role\] table. If they do not have the user\_admin role, the access will be denied. When the property is false, these additional checks are not validated.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

