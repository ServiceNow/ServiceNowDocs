---
title: CSRF enforcement for session-authenticated REST APIs
description: The glide.security.csrf.rest.public\_csrf.enabled property enables Cross-Site Request Forgery \(CSRF\) token validation for public REST APIs that use session-cookie authentication.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-csrf-enforcement-for-session-authenticated-rest-apis.html
release: brazil
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [CSRF, REST API, session authentication, security]
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# CSRF enforcement for session-authenticated REST APIs

The **glide.security.csrf.rest.public\_csrf.enabled** property enables Cross-Site Request Forgery \(CSRF\) token validation for public REST APIs that use session-cookie authentication.

A CSRF token is a unique, session-specific security token embedded in requests. The server validates that the token matches the one it issued, confirming the request's legitimacy and preventing attackers from performing unauthorized actions on behalf of users.

When the **glide.security.csrf.rest.public\_csrf.enabled** property is set to `true`, all public REST APIs using session-cookie authentication must include a valid CSRF token in their requests. Requests without a valid token are rejected.

You can exempt specific REST API paths from CSRF validation by adding them to the sys\_rest\_csrf\_allow\_list table. Paths on this allowlist will not require CSRF tokens.

When the **glide.security.csrf.rest.public\_csrf.enabled** property is set to `false`, CSRF token validation is turned off entirely.

## More information

<table id="table_property_details"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.security.csrf.rest.public\_csrf.enabled**

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

Security risk

</td><td>

-   Security rating: Medium
-   CVSS score: 4.3
-   Security risk details: Setting this property to `false` disables CSRF token validation for public REST APIs, exposing them to potential CSRF attacks when using session cookies for authentication. A CSRF attack is an attack that forces an end user to execute unwanted actions on a web application in which they are currently authenticated. Typically enabled by social engineering, an attacker may trick the users of a web application into executing actions of the attacker's choosing. If the victim is a normal user, a successful CSRF attack can force the user to perform state-changing requests like changing their email address. If the victim is an administrative account, CSRF can compromise the entire web application.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

Functional impact

</td><td>

Setting this property to `true` may cause some customer instance scripts and integrations to break. However, this is only if these scripts and integrations rely on session cookie authentication and make requests to public REST API endpoints without including a valid CSRF token. Integrations that use supported authentication methods \(such as OAuth or basic auth\) or correctly include the CSRF token will continue to work without changes.

</td></tr></tbody>
</table>**Parent Topic:**[Access control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-access-control.md)

