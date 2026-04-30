---
title: Check impersonation on ACL evaluation in HR App \[New in Security Center 1.3 and updated in 1.5\]
description: Use the sn\_hr\_core.impersonateCheck property to prevent a user from impersonating another user and accessing their HR information.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Architecture, design, and threat modeling, Hardening settings, Platform Security]
---

# Check impersonation on ACL evaluation in HR App \[New in Security Center 1.3and updated in 1.5\]

Use the **sn\_hr\_core.impersonateCheck** property to prevent a user from impersonating another user and accessing their HR information.

A secure setting prevents an admin from seeing another user's HR information while using impersonation. An insecure setting for this property allows an admin to impersonate a user and access HR data such as survey results or audit records with the impersonated user's access. Due to the nature of this type of data, such as information which should be available only to the user themselves like email, this is not recommended. Setting **sn\_hr\_core.impersonateCheck** to true only allows access to HR information when the user is not impersonating any others.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**sn\_hr\_core.impersonateCheck**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

boolean

</td></tr><tr><td>

Recommended value

</td><td>

true

</td></tr><tr><td>

Default value

</td><td>

false

</td></tr><tr><td>

Category

</td><td>

[Architecture, design, and threat modeling](sc-architecture-design-threat-molding.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 2.7
-   CVSS score: Low
-   Security risk details: An insecure setting for this property allows an admin to impersonate a user and access HR data such as survey results or audit records with the impersonated user's access.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

Functional impact

</td><td>

When this property set to true, it prevents an admin from seeing another user's HR information while using impersonation. When set to false, it allows an admin to impersonate a user and access HR data such as survey results or audit records with the impersonated user's access. Due to the nature of this type of data, such as information which should available only to the user themselves like an email, this is not recommended. Setting sn\_hr\_core.impersonateCheck to true only allows access to HR information when the user is not impersonating any others.

</td></tr></tbody>
</table>**Parent Topic:**[Architecture, design, and threat modeling](sc-architecture-design-threat-molding.md)

