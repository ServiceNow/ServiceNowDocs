---
title: Require Multi-Factor Authentication for AI Voice Agent
description: Use a system property to control whether Multi-Factor Authentication \(MFA\) is required for the AI voice agent authentication feature.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Require Multi-Factor Authentication for AI Voice Agent

Use a system property to control whether Multi-Factor Authentication \(MFA\) is required for the AI voice agent authentication feature.

Use the **glide.voice.authenticate.mfa\_mandatory** system property to control whether Multi-Factor Authentication \(MFA\) is required for the AI voice agent authentication feature. MFA requires users to provide two or more different verification factors to access a service or account. Examples of factors are SoftPIN or time-based one-time password \(TOTP\). More information about authentication factors for AI voice agents can be found at [Explore authentication factors for AI voice agents](../../../integrate/authentication/concept/explore-authentication-factors.md).

Ensure the **glide.voice.authenticate.mfa\_mandatory** system property is set to `true`.

**Important:** The sys\_id of this System Properties \[sys\_properties\] record should be e0f4e8bd70103210f87732f6ceab0a2f.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.voice.authenticate.mfa\_mandatory**

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

-   Severity score: 3.3
-   CVSS score: Low
-   Security risk details: Enforcing MFA reduces the risk of account compromise if a single factor is leaked or compromised.

</td></tr><tr><td>

Functional impact

</td><td>

Users must configure multiple factors of authentication to use voice authentication. This is the default behavior.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

AI voice agent authentication feature is set up and enabled.

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

