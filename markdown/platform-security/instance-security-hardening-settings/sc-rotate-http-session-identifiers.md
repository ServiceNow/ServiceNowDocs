---
title: Rotate HTTP session identifiers
description: Use the glide.ui.rotate\_sessions property to enable rotation of the HTTP session identifiers to reduce security vulnerabilities.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Session management, Hardening settings, Platform Security]
---

# Rotate HTTP session identifiers

Use the **glide.ui.rotate\_sessions** property to enable rotation of the HTTP session identifiers to reduce security vulnerabilities.

If the **glide.ui.rotate\_sessions** system property is not set to the recommended value of **true**, then identifying information on a session is kept and not rotated between applications.

Ensure that the property **glide.ui.rotate\_sessions** is set to **true**.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.ui.rotate\_sessions**

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

&lt;none&gt;

</td></tr><tr><td>

Fallback value

</td><td>

true

</td></tr><tr><td>

Category

</td><td>

[Session management](sc-session-management.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 8.8
-   CVSS rating: High
-   Security risk details: This increases the risk of session hijacking, as attackers could reuse session identifiers to gain unauthorized access.

</td></tr><tr><td>

Functional impact

</td><td>

This remediation modified the SessionID when user navigates from unauthenticated page to authenticated pages. -   If you are using a proxy or hardcoding the SessionID when a user first logs in, or for any purpose, then there can be a potential functionality impact.
-   If you are using the SAML 2.0 plugin for Single Sign-on authentication, it might interfere with the session information sharing between the instance and the Identity Provider. In such case, you can set this property to false.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Session management](sc-session-management.md)

