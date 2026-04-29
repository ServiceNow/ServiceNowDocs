---
title: Set Automatic Token Cleanup for Token Credentials
description: Use the com.snc.platform.security.token.auth.cleanup property to ensure that expired API keys and HMAC secrets are deleted, thereby limiting the potential for token reuse.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Architecture, design, and threat modeling, Hardening settings, Platform Security]
---

# Set Automatic Token Cleanup for Token Credentials

Use the **com.snc.platform.security.token.auth.cleanup** property to ensure that expired API keys and HMAC secrets are deleted, thereby limiting the potential for token reuse.

If the **com.snc.platform.security.token.auth.cleanup** system property is set to the insecure value of **false**, expired API keys and HMAC secrets will not be deleted. This creates a potential for token reuse. If the token was expired due to leakage or compromise, reuse exposes the instance to anyone possessing the leaked token. Expired tokens are kept for the number of days defined by the **com.snc.platform.security.token.auth.days.expired.hmac\_secret.is.kept** and **com.snc.platform.security.token.auth.days.expired.api\_key.is.kept** system properties. Integer values of `0` and greater are valid values. A value of 0 causes the expired tokens to be deleted in the same day. The default of 7 days, or fewer, is recommended.

Ensure the property **com.snc.platform.security.token.auth.cleanup** does not exist in the System Properties \[sys\_properties\] table or is set to **true**. Ensure that the properties **com.snc.platform.security.token.auth.days.expired.api\_key.is.kept** and **com.snc.platform.security.token.auth.days.expired.hmac\_secret.is.kept** do not exist in the System Properties \[sys\_properties\] table or are set to 7 or less.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

-   **com.snc.platform.security.token.auth.cleanup**
-   **com.snc.platform.security.token.auth.days.expired.hmac\_secret.is.kept**
-   **com.snc.platform.security.token.auth.days.expired.api\_key.is.kept**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

Integer

</td></tr><tr><td>

Recommended value

</td><td>

-   true
-   Less than or equal to 7
-   Less than or equal to 7

</td></tr><tr><td>

Default value

</td><td>

&lt;none&gt;

</td></tr><tr><td>

Fallback value

</td><td>

-   true
-   7
-   7

</td></tr><tr><td>

Category

</td><td>

[Architecture, design, and threat modeling](sc-architecture-design-threat-molding.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 5.1
-   CVSS score: Medium
-   Security risk details: A high number of days increases the exposure period for token reuse.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Architecture, design, and threat modeling](sc-architecture-design-threat-molding.md)

