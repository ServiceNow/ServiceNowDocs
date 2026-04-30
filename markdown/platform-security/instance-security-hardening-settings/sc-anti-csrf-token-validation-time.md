---
title: Anti-CSRF token validation time \[New in Security Center 1.3\]
description: The glide.security.csrf\_previous.time\_limit property specifies the time in seconds for a secure token to expire.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Anti-CSRF token validation time \[New in Security Center 1.3\]

The **glide.security.csrf\_previous.time\_limit** property specifies the time in seconds for a secure token to expire.

When a user session expires, the secure token expires with it unless the **allowing reuse of expired tokens are allowed** property is enabled, and it is within the time frame described by this property. This token is used to prevent cross site request forgery attacks.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.security.csrf\_previous.time\_limit**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

integer

</td></tr><tr><td>

Recommended value

</td><td>

86400 seconds or 1 day

</td></tr><tr><td>

Default value

</td><td>

86400 seconds or 1 day

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 5.3
-   CVSS score: Medium
-   Security risk details: Not setting this property to the recommended value disables the token validation used to prevent cross site request forgery attacks.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

Functional impact

</td><td>

This property determines the duration in seconds for a secure token to remain valid. The secure token expires when the user session expires unless the **allowing reuse of expired tokens** property is enable, and the token is within the time frame specified in this property. This token prevents cross-site request forgery attacks. It has a default value of 86400 seconds or 1 day.

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

