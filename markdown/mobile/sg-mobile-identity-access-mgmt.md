---
title: User authentication for ServiceNow mobile apps
description: ServiceNow mobile apps support platform authentication using OAuth 2.0. Authentication mechanisms include multi provider SSO, MFA, LDAP, Local DB, and Digest.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Identity and access management, Device security for ServiceNow Mobile apps, Mobile security, Configuring the Mobile Platform, Mobile Platform]
---

# User authentication for ServiceNow mobile apps

ServiceNow mobile apps support platform authentication using OAuth 2.0. Authentication mechanisms include multi provider SSO, MFA, LDAP, Local DB, and Digest.

## AppAuth authentication

The ServiceNow mobile apps use a new authentication methodology called AppAuth. AppAuth uses an external mobile browser to log the user in. The following steps detail login using AppAuth.

1.  The client creates and records a secret named the `code_verifier`, and derives a transformed version `t(code_verifier)` \(referred to as the `code_challenge`\). This `code_challenge` is sent in the OAuth 2.0 Authorization Request along with the transformation method `t_m`.
2.  The Authorization Endpoint responds as usual but records `t(code_verifier)` and the transformation method.
3.  The client then sends the authorization code in the Access Token Request as usual but includes the `code_verifier` secret generated in the previous steps.
4.  The authorization server transforms `code_verifier` and compares it to `t(code_verifier)` from the previous steps. Access is denied if they are not equal.

![Flow for the authentication process for logging in to a mobile app](../image/AppAuthArch.png "Abstract protocol flow")

## Single sign-on

ServiceNow mobile apps require multi-provider single sign-on in order to use external authentication. The multi providers SSO plugin \[com.snc.integration.sso.multi.installer\] provides SAML authentication support. The login process \(AppAuth\) uses this plugin to redirect the user to the IDP \(SAML provider\) login page when using SAML.

For more information on this plugin, see [External single sign-on \(SSO\)](https://www.servicenow.com/docs/access?context=c_MultipleProviderSingleSignOn&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

For more information on configuring multi provider SSO, see [Multi-Provider Single sign-on \(SSO\)](https://www.servicenow.com/docs/access?context=c_MultipleProviderSingleSignOn&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

## Multifactor authentication

Users can access the instance via Multifactor Authentication using the MFA plugin \[com.snc.integration.multifactor.authentication\]. Users are directed to their login page after selecting their instance in a mobile app.

![Multifactor login page in the Mobile Agent app.](../image/mobile-mfa-redirect.png "Multifactor login page in the Mobile Agent app")

For details on configuring Multi-factor Authentication, see [Multifactor authentication system properties](https://www.servicenow.com/docs/access?context=mfa-properties&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)

## LDAP

Use LDAP authentication to access using LDAP credentials. The user sees the same login page as the local login \(DB based\) but the back end to the LDAP server deletes the authentication. For more information on LDAP configuration, see [LDAP integration](https://www.servicenow.com/docs/access?context=c_LDAPIntegration&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

## Local DB

The user name and password in the user record in the instance database.

## Not officially supported

-   Kerberos
-   Certificate-based authentication \(AppAuth’s external browser may solve for some certificate based mechanisms\)

**Parent Topic:**[Identity and access management](sg-mobile-ID-access-mgmt.md)

