---
title: Enable anti-CSRF token
description: Use the glide.security.use\_csrf\_token property to confirm the use of a secure token to identify and validates incoming requests, which in turn are used to prevent these attacks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-anti-csrf-token.html
release: brazil
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Enable anti-CSRF token

Use the **glide.security.use\_csrf\_token** property to confirm the use of a secure token to identify and validates incoming requests, which in turn are used to prevent these attacks.

Cross-Site Request Forgery \(CSRF\) is an attack that forces authenticated users to submit a request to a web application, exploiting the web application's trust in an authenticated user.

The **glide.security.use\_csrf\_token** property controls whether the platform embeds a token in rendered pages and validates that token on incoming requests. This allows the platform to distinguish requests that originated from its own pages from requests forged by a third-party site.

To configure this property:

1.  Confirm the current user has the security\_admin role or has elevated to that role.
2.  Navigate to /sys\_properties\_list.do on the instance.
3.  Confirm the **glide.security.use\_csrf\_token**property exists and is set to `true`.

## More information

<table><tbody><tr><td>

Attribute

</td><td>

Description

</td></tr><tr><td>

Property name

</td><td>

**glide.security.use\_csrf\_token**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Category

</td><td>

[Access control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-access-control.md)

</td></tr><tr><td>

Purpose

</td><td>

To protect the application from potential CSRF attack.

</td></tr><tr><td>

Fallback value

</td><td>

false

</td></tr><tr><td>

Recommended value

</td><td>

true

</td></tr><tr><td>

Default value

</td><td>

true

</td></tr><tr><td>

Functional impact

</td><td>

Requests with a missing, expired, or mismatched token are rejected and the user is redirected to a security warning page instead of having the action performed.

</td></tr><tr><td>

Security risk

</td><td>

-   Security risk rating: High
-   CVSS rating: 8.1
-   Security risk details: If this property is not set to `true`, the platform can't distinguish a forged request from one the user actually intended. An attacker can craft a malicious page that causes an authenticated victim's browser to submit a request to the instance without their knowledge. That request executes with the victim's session and privileges.

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see .

**Parent Topic:**[Access control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-access-control.md)

