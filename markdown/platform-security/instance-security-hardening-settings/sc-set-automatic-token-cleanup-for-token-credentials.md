---
title: Set Automatic Token Cleanup for Token Credentials \[New in Security Center 2.0\]
description: Use the com.snc.platform.security.token.auth.cleanup property to ensure that expired API keys and HMAC secrets are deleted, thereby limiting the potential for token reuse.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Architecture, design, and threat modeling, Hardening settings, Platform Security]
---

# Set Automatic Token Cleanup for Token Credentials \[New in Security Center 2.0\]

Use the **com.snc.platform.security.token.auth.cleanup** property to ensure that expired API keys and HMAC secrets are deleted, thereby limiting the potential for token reuse.

If the **com.snc.platform.security.token.auth.cleanup** property is set to the insecure value of false, expired API keys and HMAC secrets will not be deleted, creating a potential for token reuse. If a token was expired due to leakage or compromise, its reuse could expose the instance to anyone possessing the leaked token.

Expired tokens are retained for the number of days defined by **com.snc.platform.security.token.auth.days.expired.hmac\_secret.is.kept** and **com.snc.platform.security.token.auth.days.expired.api\_key.is.kept**. Valid values for these settings are integers of 0 or greater. A value of 0 results in the expired tokens being deleted on the same day, while a higher number of days increases the exposure period. A default value of 7 days or fewer is recommended.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**com.snc.platform.security.token.auth.cleanup, com.snc.platform.security.token.auth.days.expired.hmac\_secret.is.kept,com.snc.platform.security.token.auth.days.expired.api\_key.is.kept**

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

The recommended values are true, and any integer less than or equal to 7.

</td></tr><tr><td>

Default value

</td><td>

7

</td></tr><tr><td>

Category

</td><td>

[Architecture, design, and threat modeling](sc-architecture-design-threat-molding.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 5.1
-   CVSS score: Medium
-   Security risk details: Not configuring this property to the recommend value of true could prevent expired API keys and HMAC secrets from being deleted which increases the likelihood for token reuse.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Architecture, design, and threat modeling](sc-architecture-design-threat-molding.md)

