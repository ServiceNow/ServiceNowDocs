---
title: Authentication release notes
description: The ServiceNow Authentication application supports many authentication mechanisms that enable you to validate the identity of users. Authentication was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
---

# Authentication release notes

The ServiceNow® Authentication application supports many authentication mechanisms that enable you to validate the identity of users. Authentication was enhanced and updated in the Xanadu release.

## Authentication highlights for the Xanadu release

-   Use the FIDO2 authenticator, passkeys, biometric authenticators, and hardware security keys as multi-factor authentication \(MFA\) factors without requiring an authenticator app setup.

See [Authentication](https://www.servicenow.com/docs/access?context=c_Authentication&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US) for more information.

## Changed in this release

-   **[Multi-factor Authentication \(MFA\)](https://www.servicenow.com/docs/access?context=mfa-config-landing&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

    Use the FIDO2 authenticator, passkeys, biometric authenticators, and hardware security keys as multi-factor authentication \(MFA\) factors without requiring an authenticator app setup.


## Deprecations

-   The MultiSSO v1 plugin is deprecated. Upgrade to MutliSSO v2 from MultiSSO v1. For more information on how to upgrade to MultiSSO v2, refer to the knowledge article [MultiSSO v2 upgrade instructions \[KB9756504\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0756504) in the Now Support Knowledge Base.
-   The SAML 1.1 and SAML 1.1 Single Sign-On - Update 1 plugin is deprecated. The SAML-based identity providers \(IdP\) have already migrated to SAML 2.0. To use SAML 2.0, you must activate the MultiSSO v2 plugin and configure your identity provider.
-   The OpenID SSO plugin is deprecated. To use OpenID Connect \(OIDC\), you must activate the MultiSSO v2 and configure your OIDC-based identity provider.

## Activation information

Authentication is a ServiceNow AI Platform product that is active by default.

## Related ServiceNow applications and features

-   **Platform Security**

    Platform Security is built into all levels of the ServiceNow AI Platform. Implement the security features that are appropriate for your organization. Manage failed logins and encrypted password protection, access control rules, and audit logs.


**Parent Topic:**[ServiceNow AI Platform security release notes](now-platform-security-rn-landing.md)

