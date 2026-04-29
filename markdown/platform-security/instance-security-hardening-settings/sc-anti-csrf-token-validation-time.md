---
title: Anti-CSRF token validation time
description: The glide.security.csrf\_previous.time\_limit property specifies the time in seconds for a secure token to expire.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Anti-CSRF token validation time

The **glide.security.csrf\_previous.time\_limit** property specifies the time in seconds for a secure token to expire.

The **glide.security.csrf\_previous.time\_limit** system property determines the time in seconds for a secure token to expire. When the user session expires, the secure token expires with it, unless the **allowing reuse of expired tokens** property is enabled, and its within the time frame described by this property. This token is used to prevent cross site request forgery attacks.

Ensure that the **glide.security.csrf\_previous.time\_limit** property is set to `86400` seconds \(1 day\).

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

86400

</td></tr><tr><td>

Default value

</td><td>

&lt;none&gt;

</td></tr><tr><td>

Fallback value

</td><td>

86400

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 5.3
-   CVSS score: Medium
-   Security risk details: The time limit for a CSRF token to expire defines how long the token remains valid for verifying legitimate user requests; if set too long, it increases the risk that an attacker could reuse a stolen token to perform unauthorized actions, while a shorter expiration window reduces this risk by narrowing the attack window.

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

