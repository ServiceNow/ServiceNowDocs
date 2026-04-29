---
title: Block Expired Anti-CSRF Tokens
description: Block expired CSRF tokens to prevent cross-site request forgery attacks.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Block Expired Anti-CSRF Tokens

Block expired CSRF tokens to prevent cross-site request forgery attacks.

The **glide.security.csrf\_previous.allow** system property enables use of an expired secure token to identify and validate incoming requests. This token is used to prevent cross-site request forgery attacks.

Ensure that the property **glide.security.csrf\_previous.allow** is set to **false**.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.security.csrf\_previous.allow**

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

false

</td></tr><tr><td>

Default value

</td><td>

false

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

-   Severity score: 6.5
-   CVSS rating: Medium
-   Security risk details: Allowing the use of previous or expired CSRF tokens exposes the application to replay attacks, enabling attackers to reuse valid requests and potentially perform unauthorized actions on behalf of legitimate users.

</td></tr><tr><td>

Functional impact

</td><td>

None

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

