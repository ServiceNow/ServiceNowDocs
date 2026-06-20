---
title: Authentication
description: ServiceNow's authentication validates the identity of a user who accesses an instance, and then authorizes the user to features that match the user's role or job function.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/platform-security/authentication/c\_Authentication.html
release: xanadu
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Access Management]
---

# Authentication

ServiceNow®'s authentication validates the identity of a user who accesses an instance, and then authorizes the user to features that match the user's role or job function.

## Get started

<table id="table_vcy_yrq_dsb" class="nav-card"><tbody><tr><td>

[\[Omitted image "bus-security.svg"\] Alt text:Multi-Provider Single Sign-on \(SSO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-security/authentication/c_MultipleProviderSingleSignOn.md)

 [Username and password configured in identity providers, which have a matching user account in the database.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-security/authentication/c_MultipleProviderSingleSignOn.md)

</td><td>

[\[Omitted image "bus-password-reset.svg"\] Alt text: OAuth Inbound and Outbound](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-security/authentication/api-inbound-and-outbound.md)

 [OAuth based authentication validates the identity of the client that attempts to establish a trust on the system by using an authentication protocol.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-security/authentication/api-inbound-and-outbound.md)

</td></tr><tr><td>

[\[Omitted image "bus-whitepaper.svg"\] Alt text: API Access Policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-security/authentication/api-access-policy.md)

 [API access policy defines the permissions and access to an API that can be controlled through a policy.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-security/authentication/api-access-policy.md)

</td><td>

[\[Omitted image "bus-endpoint.svg"\] Alt text: Digest Token Authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-security/authentication/c_DigestTokenAuthentication.md)

 [Username and the secret in the table, perform an hash operation that is user-specific such as SHA1, SHA 256, or MD5. This value has to be appended as part of the URL suffix, which works on the query param.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-security/authentication/c_DigestTokenAuthentication.md)

</td></tr><tr><td>

[\[Omitted image "bus-sla.svg"\] Alt text:Time Limited Authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-security/authentication/time-limited-authentication.md)

 [Configure link based authentication on the ServiceNow instance. The configured link can be shared with the user through Email or SMS and user can use those links to login to instance.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-security/authentication/time-limited-authentication.md)

</td><td>

\[Omitted image "bus-manager.svg"\] Alt text:Multi-factor Authentication \(MFA\)

 MFA enables you to provide second level of authentication that includes using passcode from an authentication app, hardware key, biometric authenticator, SMS, or Email.

</td></tr><tr><td>

[\[Omitted image "bus-get-certified.svg"\] Alt text:Certificate based authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-security/certificate-based-authentication/certificate-based-authentication.md)

 [Unique PEM encoded certificates mapped to users instead of user name and password for certificate based authentication.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-security/certificate-based-authentication/certificate-based-authentication.md)

</td><td>

[\[Omitted image "bus-contract.svg"\] Alt text:Self Registration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-security/authentication/external-user-self-registration.md)

 [Use external user self-registration to on-board a large volume of external users to your instance.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-security/authentication/external-user-self-registration.md)

</td></tr><tr><td>

[\[Omitted image "bus-profile.svg"\] Alt text:LDAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-security/ldap-integration/c_LDAPIntegration.md)

 [Integrate with a Lightweight Directory Access Protocol \(LDAP\) directory to streamline the user login process](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-security/ldap-integration/c_LDAPIntegration.md)

</td><td>

 

</td></tr></tbody>
</table>You can use several different methods to authenticate users. User credentials are matched to different saved credentials for each method.

**Note:**

-   The Okta SSO plugin is deprecated.
-   To learn more about the security properties that affect authorization processing, see [Access control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-security/instance-security-hardening-settings/sc-access-control.md) in Instance Security Hardening Settings.
-   You can use SAML and Digest Authentication through the Multiple Provider SSO application.

