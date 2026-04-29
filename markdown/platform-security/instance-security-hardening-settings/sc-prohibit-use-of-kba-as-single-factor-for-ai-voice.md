---
title: Prohibit Use of KBA as Single Factor for AI Voice
description: Use a system property to prevent Knowledge Based Authentication \(KBA\) from being the only factor of authentication required to authenticate to the platform for AI voice.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Prohibit Use of KBA as Single Factor for AI Voice

Use a system property to prevent Knowledge Based Authentication \(KBA\) from being the only factor of authentication required to authenticate to the platform for AI voice.

Use the **glide.voice.authenticate.allow\_kba\_as\_only\_factor** system property to prevent security questions from being the only factor of authentication required to authenticate to the platform in the AI voice agent authentication feature. Knowledge Based Authentication \(KBA\) allows users to answer security questions as an authentication factor. Learn more about authentication factors for AI voice agents at [Explore authentication factors for AI voice agents](../../../integrate/authentication/concept/explore-authentication-factors.md).

Ensure that the **glide.voice.authenticate.allow\_kba\_as\_only\_factor** system property is set to `false`.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.voice.authenticate.allow\_kba\_as\_only\_factor**

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

false

</td></tr><tr><td>

Category

</td><td>

[Authentication](sc-authentication.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 3.3
-   CVSS score: Low
-   Security risk details: Allowing users to authenticate with a single factor increases the risk of account compromise if that factor is compromised. Enforcing Multi-factor Authentication \(MFA\) is recommended. If single-factor access is allowed, then KBA security questions aren't recommended as the single factor. Security questions can be guessed, learned through social engineering, or obtained from public records, increasing the risk of account compromise.

</td></tr><tr><td>

Functional impact

</td><td>

If KBA can’t be used as a single factor of authentication, then users must use another form to authenticate to the platform for the Voice Authentication feature, such as SoftPin or SMS OTP.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

AI voice agent authentication feature is setup and enabled.

</td></tr></tbody>
</table>**Parent Topic:**[Authentication](sc-authentication.md)

