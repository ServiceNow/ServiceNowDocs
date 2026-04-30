---
title: Rotate HTTP session identifiers
description: Use the glide.ui.rotate\_sessions property to enable rotation of the HTTP session identifiers to reduce security vulnerabilities.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Session management, Hardening settings, Platform Security]
---

# Rotate HTTP session identifiers

Use the **glide.ui.rotate\_sessions** property to enable rotation of the HTTP session identifiers to reduce security vulnerabilities.

If an unauthenticated user's session ID doesn't change after authentication, a web application is vulnerable to a [session fixation attack](https://www.owasp.org/index.php/Session_fixation). A malicious user could start an unauthenticated session and give the associated session ID to the victim. Once the victim authenticates, the malicious user now shares that authenticated session.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Property name

</td><td>

**glide.ui.rotate\_sessions**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Category

</td><td>

[Session management](sc-session-management.md)

</td></tr><tr><td>

Purpose

</td><td>

To achieve more secure session authentication.

</td></tr><tr><td>

Recommended value

</td><td>

true

</td></tr><tr><td>

Default value

</td><td>

true

</td></tr><tr><td>

Security risk rating

</td><td>

8.8

</td></tr><tr><td>

Functional impact

</td><td>

This remediation modified the SessionID when user navigates from unauthenticated page to authenticated pages. -   If you are using a proxy or hardcoding the SessionID when a user first logs in, or for any purpose, then there can be a potential functionality impact.
-   If you are using the SAML 2.0 plugin for Single Sign-on authentication, it might interfere with the session information sharing between the instance and the Identity Provider. In such case, you can set this property to false.

</td></tr><tr><td>

Security risk

</td><td>

\(Moderate\) SessionID is used to process and authenticate the instance user by maintaining the session state on the browser. Thus, SessionID is deemed as sensitive data and should be secure by default. Session Rotation is a security control that enforces the alteration of sessionID whenever the user navigates from unauthenticated pages to authenticate pages.

</td></tr><tr><td>

References

</td><td>

[Authentication with SAML](../../../integrate/saml/concept/c_SAML2.0WebBrowserSSOProfile.md)

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Session management](sc-session-management.md)

