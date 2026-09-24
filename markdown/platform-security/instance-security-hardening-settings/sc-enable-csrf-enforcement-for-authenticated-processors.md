---
title: Enable CSRF enforcement for authenticated processors
description: Enable Cross-Site Request Forgery \(CSRF\) enforcement to protect authenticated processor requests from CSRF attacks when session cookies are used for authentication.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-enable-csrf-enforcement-for-authenticated-processors.html
release: brazil
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [CSRF, Cross-Site Request Forgery, security, authenticated processors, session cookies]
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Enable CSRF enforcement for authenticated processors

Enable Cross-Site Request Forgery \(CSRF\) enforcement to protect authenticated processor requests from CSRF attacks when session cookies are used for authentication.

The **glide.security.csrf.processor.all.authenticated.enabled** property enables CSRF checks for authenticated processor requests. When set to `true`, the platform checks for CSRF violations after session cookie authentication succeeds. If a violation is detected and the processor is not allow-listed, the request is rejected with an HTTP 401 response. Rejection details are logged. This enforcement applies to POST, PUT, and DELETE requests. GET requests are allowed without a CSRF token.

The **glide.security.csrf.httpauth\_processor\_allowlist** property controls an exception list that allows specific processors extending HTTPAuthProcessor to bypass CSRF enforcement. When **glide.security.csrf.processor.all.authenticated.enabled** is active, requests to processors named in this allow-list bypass the HTTP 401 rejection for invalid or missing CSRF tokens.

**Note:** The **glide.security.csrf.processor.all.authenticated.enabled** property is a broader upstream gate that supersedes **glide.security.csrf.rest.public\_csrf.enabled** for cookie-auth REST traffic when both are enabled. The **glide.security.csrf.rest.public\_csrf.enabled** property is effectively the specific guard for public REST API pages that the **glide.security.csrf.processor.all.authenticated.enabled** property does not cover \(for example, public REST requests sent with a session cookie where the page does not require cookie authentication\).

## More information

<table id="table_csrf_enforcement"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.security.csrf.processor.all.authenticated.enabled**, glide.security.csrf.httpauth\_processor\_allowlist

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \( `/sys_properties_list.do`\)

</td></tr><tr><td>

Data type

</td><td>

Boolean, String

</td></tr><tr><td>

Recommended value

</td><td>

glide.security.csrf.processor.all.authenticated.enabled: true

 glide.security.csrf.httpauth\_processor\_allowlist: ""

</td></tr><tr><td>

Default value

</td><td>

glide.security.csrf.processor.all.authenticated.enabled: false

 glide.security.csrf.httpauth\_processor\_allowlist: ""

</td></tr><tr><td>

Fallback value

</td><td>

glide.security.csrf.processor.all.authenticated.enabled: false

 glide.security.csrf.httpauth\_processor\_allowlist: ""

</td></tr><tr><td>

Security risk

</td><td>

Setting the **glide.security.csrf.processor.all.authenticated.enabled** property to `false` disables CSRF token validation for authenticated processor requests, allowing CSRF attacks when session cookies are used for authentication.

 A CSRF attack tricks an authenticated user's browser into making requests to a web application on the attacker's behalf, without the user's knowledge. The browser automatically attaches session cookies to outbound requests. A malicious page can silently trigger state-changing actions \(password changes, record updates, privilege escalations\) on any site the victim is currently logged in.

 The impact scales with the victim's privileges. A regular user loses control of their own account. An administrator can expose the entire instance.

</td></tr><tr><td>

Functional impact

</td><td>

Changing the **glide.security.csrf.processor.all.authenticated.enabled** property directly affects whether requests that change state and are authenticated via session cookies to HTTPAuthProcessor-based endpoints must present a valid CSRF token.

 Enabling this property can cause previously working integrations, browser-driven calls, or custom clients to start receiving HTTP 401 responses. This occurs if they rely on session cookies but don't send a valid X-UserToken. Disabling it preserves backward compatibility for such clients but weakens CSRF protection.

</td></tr><tr><td>

Regression testing

</td><td>

Log in to establish a session and call an affected processor endpoint using POST, PUT, or DELETE in three ways: without a token, with an invalid token, and with a valid token.

 When the property is enabled, the requests without a token, and those with an invalid token are rejected. The requests with a valid token should succeed. Confirm GET requests continue to work without requiring a CSRF token.

</td></tr><tr><td>

Related property

</td><td>

**glide.security.csrf.httpauth\_processor\_allowlist**

</td></tr></tbody>
</table>**Parent Topic:**[Access control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-access-control.md)

