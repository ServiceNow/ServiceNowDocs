---
title: Invalidate Session After OAuth Token Expiration \[New in Security Center 2.0\]
description: Use a system property to the secure value to prevent users from continuing to use a session via cookies after the OAuth token used to create the session expires.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Session management, Hardening settings, Platform Security]
---

# Invalidate Session After OAuth Token Expiration \[New in Security Center 2.0\]

Use a system property to the secure value to prevent users from continuing to use a session via cookies after the OAuth token used to create the session expires.

When an OAuth access token is issued, the response includes a cookie. Users can use this cookie to continue using a session even after the OAuth token used to create that session expires. Use the **glide.authenticate.oauth.post.token.expiration.cookie\_auth.disabled** system property to prevent this.

Ensure the **glide.authenticate.oauth.post.token.expiration.cookie\_auth.disabled** system property exists in the System Properties \[sys\_properties\] table, and is set to a value of `true`.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.authenticate.oauth.post.token.expiration.cookie\_auth.disabled**

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

false

</td></tr><tr><td>

Category

</td><td>

[Session management](sc-session-management.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 6.8
-   CVSS score: Medium
-   Security risk details: If an OAuth token is leaked or compromised, the lack of expiration would allow an attacker to use and extend the session via the created cookie. Malicious users can use sessions to access unauthorized resources and take unauthorized actions. Set this property to the secure value to eliminate this hidden session extension mechanism and reduce replay risk by enforcing token expiration.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

Functional impact

</td><td>

Impact when set to true:

-   Sessions end immediately when the access token expires.
-   Cookies no longer refresh session validity.
-   Clients must use refresh tokens or re-authenticate to obtain a new access token.

 Potential Breakage:

-   Legacy clients or custom integrations relying on cookie-based session extension fail after token expiry.
-   Long-running jobs without token renewal logic may encounter 401 errors.

 What Continues to Work:

-   Standard OAuth flows with refresh tokens.
-   Properly designed integrations that renew tokens proactively.

</td></tr></tbody>
</table>**Parent Topic:**[Session management](sc-session-management.md)

