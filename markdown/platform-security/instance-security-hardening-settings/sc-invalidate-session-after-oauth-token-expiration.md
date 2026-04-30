---
title: Invalidate Session After OAuth Token Expiration \[New in Security Center 2.0\]
description: Configure the glide.authenticate.oauth.post.token.expiration.cookie\_auth.disabled property to the secure value to prevent users from continuing to use a session via cookies after the OAuth token used to create the session expires.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Session management, Hardening settings, Platform Security]
---

# Invalidate Session After OAuth Token Expiration \[New in Security Center 2.0\]

Configure the **glide.authenticate.oauth.post.token.expiration.cookie\_auth.disabled** property to the secure value to prevent users from continuing to use a session via cookies after the OAuth token used to create the session expires.

When the **glide.authenticate.oauth.post.token.expiration.cookie\_auth.disabled** property is not set to the secure value of true, a user may continue to use a session via cookies after the OAuth token used to create the session expires. This increases the risk of cookies being leaked and the session being hijacked by a malicious user to access unauthorized resources. Ensure that the glide property **glide.authenticate.oauth.post.token.expiration.cookie\_auth.disabled** is set to true. If the record does not exist in the sys\_properties table, the default value is false.

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

boolean

</td></tr><tr><td>

Recommended value

</td><td>

true

</td></tr><tr><td>

Default value

</td><td>

For zboot instances, the property is true. For the update instances, the property is false by default.

</td></tr><tr><td>

Category

</td><td>

[Session management](sc-session-management.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 5.4
-   CVSS score: Medium
-   Security risk details: When this property is not set to the secure value of true, a user may continue to use a session even after the OAuth token used to create the session has expired, increasing the likelihood of the session being hijacked by a malicious user.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

Functional impact

</td><td>

True: Cookie authentication is only honored until the OAuth access token expires; after the expiration, authentication is not honored.

 False: Cookie authentication is honored even after the OAuth access token expires.

</td></tr></tbody>
</table>**Parent Topic:**[Session management](sc-session-management.md)

