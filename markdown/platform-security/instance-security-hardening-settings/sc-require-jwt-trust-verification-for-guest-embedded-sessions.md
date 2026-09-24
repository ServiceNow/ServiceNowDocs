---
title: Require JWT trust verification for guest embedded sessions
description: The glide.embedded.session.trust.verification.enabled property determines whether guest embeddable sessions require JSON Web Tokens \(JWT\) validation for third-party origin verification.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-require-jwt-trust-verification-for-guest-embedded-sessions.html
release: brazil
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [JWT, guest embedded sessions, web embeddables, security]
breadcrumb: [Session management, Hardening settings, Platform Security]
---

# Require JWT trust verification for guest embedded sessions

The **glide.embedded.session.trust.verification.enabled** property determines whether guest embeddable sessions require JSON Web Tokens \(JWT\) validation for third-party origin verification.

This property requires JWT validation to confirm that guest embeddable session requests come from trusted third-party websites.

To configure this property:

1.  Navigate to `/sys_properties_list.do` on the instance.
2.  Verify **glide.embedded.session.trust.verification.enabled** exists and is set to **true**.

## More information

<table id="table_ajc_y23_3ik"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.embedded.session.trust.verification.enabled**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \( `/sys_properties_list.do`\)

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

[Session management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-session-management.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 5.3
-   CVSS rating: Medium
-   Security risk details:

When this property is inactive, the platform establishes guest embedded sessions for Web embeddables components without JWT verification. The JWT is designed to confirm that requests originate from trusted third party websites.


</td></tr><tr><td>

Functional impact

</td><td>

When enabled, any third-party website embedding guest components must implement the JWT-based token callback in its global code. See the [Web embeddables](https://www.servicenow.com/docs/r/customer-relationship-management/crm-web-embeddables.html) guest user documentation for more details.

 Sites that follow the documented setup are unaffected. JWT verification is the default behavior for this feature. Sites relying on the undocumented fallback behavior \(proceeding without a token\) must implement the callback before its embedded guest sessions can be established once enforcement begins.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

Only applicable when the web components for guest embeddables \(com.sn\_guest\_components\) plugin is active. This property has no effect, and this control does not evaluate it, on instances where the plugin is not installed and active.

</td></tr></tbody>
</table>**Parent Topic:**[Session management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-session-management.md)

