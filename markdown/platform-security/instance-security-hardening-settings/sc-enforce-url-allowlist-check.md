---
title: Enforce URL allowlist check \[Updated in Security Center 1.3, 1.5, and 2.0\]
description: Use the glide.security.url.whitelist system property to add extra layer of validation to ensure whether any external URL introduced should be a part of inclusion listed URLs.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Enforce URL allowlist check \[Updated in Security Center 1.3, 1.5, and 2.0\]

Use the **glide.security.url.whitelist** system property to add extra layer of validation to ensure whether any external URL introduced should be a part of inclusion listed URLs.

Protect your users from client-side open redirection, which enable attackers to redirect your users to untrusted and malicious pages.

If **glide.security.url.whitelist.strict\_check** is not set to the recommended value of **true**, all external URLs are allowed for redirection as long as the **glide.security.url.whitelist** system property is empty. If **glide.security.url.whitelist** is not empty, then only external URLs listed in that property are allowed.

Set **glide.security.url.whitelist.strict\_check** to **true** or ensure that **glide.security.url.whitelist** is configured with the allowed external URLs to help secure your instance from open redirection attacks.

This property is applicable in the following cases:

-   `/logout.do?sysparm_goto_url={External URL}`
-   `/cms_login_redirect.do?sysparm_goto_url={External URL}`

Users are directed to an external trusted site after they log out of the instance:

-   `/logout_redirect.do?sysparm_url={External URL}`
-   `/saml_redirector.do?sysparm_uri={External URL}`
-   `/logout_success.do?RelayState={External URL}`

When SAML is enabled, it invokes an identity provider \(IDP\) logout URL.

Ensure the property **glide.security.url.whitelist.strict\_check** is set to true or the property **glide.security.url.whitelist** is set to a value.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Property name

</td><td>

**glide.security.url.whitelist**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Category

</td><td>

[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

</td></tr><tr><td>

Purpose

</td><td>

To implement safe URL redirect during login, logout, or other redirects. This property mitigates one of the OWASP top 10 attacks called Invalidated Redirects and forwards.

</td></tr><tr><td>

Type

</td><td>

String

</td></tr><tr><td>

Default value

</td><td>

true

</td></tr><tr><td>

Recommended value

</td><td>

true

</td></tr><tr><td>

Value

</td><td>

Your organization's approved URLs \[Some Defined FQDN \(Fully Qualified Domain Name\) Ex. http://www.servicenow.com\]

</td></tr><tr><td>

Security risk rating

</td><td>

6.3

</td></tr><tr><td>

Functional impact

</td><td>

This remediation enforces validation on logout page. It might have a functional impact on a user of an instance with an SSO/SAML configuration.

</td></tr><tr><td>

Security risk

</td><td>

\(High\) Client-side open redirection can enable attacker to redirect victims/users to attacker-controlled website and is viewed as a security risk.

</td></tr><tr><td>

References

</td><td>

[Multi-SSO \(SAML 2.0\) errors and fixes](../../../integrate/saml/reference/saml-errors.md)

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

