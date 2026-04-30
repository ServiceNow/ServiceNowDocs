---
title: Authentication
description: ServiceNow's authentication validates the identity of a user who accesses an instance, and then authorizes the user to features that match the user's role or job function.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Access Management]
---

# Authentication

ServiceNow's authentication validates the identity of a user who accesses an instance, and then authorizes the user to features that match the user's role or job function.

## Get started

<table id="table_vcy_yrq_dsb" class="nav-card"><tbody><tr><td>

[![](../../../reuse/icons/brand-icons/bus-security.svg)Multi-Provider single sign-on \(SSO\)](c_MultipleProviderSingleSignOn.md)

 [Username and password configured in identity providers, which have a matching user account in the database.](c_MultipleProviderSingleSignOn.md)

</td><td>

[![](../../../reuse/icons/brand-icons/bus-password-reset.svg) OAuth inbound and outbound](../../authentication/concept/api-inbound-and-outbound.md)

 [OAuth based authentication validates the identity of the client that attempts to establish a trust on the system by using an authentication protocol.](../../authentication/concept/api-inbound-and-outbound.md)

</td></tr><tr><td>

[![](../../../reuse/icons/brand-icons/bus-whitepaper.svg) API access policy](../../authentication/concept/api-access-policy.md)

 [API access policy defines the permissions and access to an API that can be controlled through a policy.](../../authentication/concept/api-access-policy.md)

</td><td>

[![Authentication factors](../../../reuse/icons/brand-icons/bus-security.svg)Authentication factors](../../authentication/concept/authentication-factors.md)

 [Secure your voice agent access by choosing from flexible authentication options such as app-based codes, push prompts, SMS, SoftPIN or knowledge-based checks.](../../authentication/concept/authentication-factors.md)

</td></tr><tr><td>

[![](../../../reuse/icons/brand-icons/bus-sla.svg)Time limited authentication](../../authentication/concept/time-limited-authentication.md)

 [Configure link based authentication on the ServiceNow instance. The configured link can be shared with the user through Email or SMS and user can use those links to login to instance.](../../authentication/concept/time-limited-authentication.md)

</td><td>

[![](../../../reuse/icons/brand-icons/bus-manager.svg)Multi-factor authentication \(MFA\)](../../authentication/concept/mfa-landing.md)

 [MFA enables you to provide second level of authentication that includes using passcode from an authentication app, hardware key, biometric authenticator, SMS, or Email.](../../authentication/concept/mfa-landing.md)

</td></tr><tr><td>

[![](../../../reuse/icons/brand-icons/bus-get-certified.svg)Certificate based authentication](../../authentication/concept/certificate-based-authentication.md)

 [Unique PEM encoded certificates mapped to users instead of user name and password for certificate based authentication.](../../authentication/concept/certificate-based-authentication.md)

</td><td>

[![](../../../reuse/icons/brand-icons/bus-endpoint.svg) Digest token authentication](c_DigestTokenAuthentication.md)

 [Username and the secret in the table, perform an hash operation that is user-specific such as SHA1, SHA 256, or MD5. This value has to be appended as part of the URL suffix, which works on the query param.](c_DigestTokenAuthentication.md)

</td></tr><tr><td>

[![](../../../reuse/icons/brand-icons/bus-profile.svg)LDAP](../../ldap/concept/c_LDAPIntegration.md)

 [Integrate with a Lightweight Directory Access Protocol \(LDAP\) directory to streamline the user login process](../../ldap/concept/c_LDAPIntegration.md)

</td><td>

[![](../../../reuse/icons/brand-icons/bus-contract.svg)Self-registration](../../authentication/concept/external-user-self-registration.md)

 [Use external user self-registration to on-board a large volume of external users to your instance.](../../authentication/concept/external-user-self-registration.md)

</td></tr></tbody>
</table>You can use several different methods to authenticate users. User credentials are matched to different saved credentials for each method.

**Note:**

-   The Okta SSO plugin is deprecated.
-   To learn more about the security properties that affect authorization processing, see [Access control](../../../administer/security-center/reference/sc-access-control.md) in Instance Security Hardening Settings.
-   You can use SAML and Digest Authentication through the Multiple Provider SSO application.

