---
title: Multi-Provider single sign-on \(SSO\)
description: External SSO allows organizations to use several SSO identity providers \(IdPs\) to manage authentication as well as retain local database \(basic\) authentication.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Authentication, Access Management]
---

# Multi-Provider single sign-on \(SSO\)

External SSO allows organizations to use several SSO identity providers \(IdPs\) to manage authentication as well as retain local database \(basic\) authentication.

Multi-Provider Single sign-on \(SSO\) is an authentication method that enables users to access multiple applications with one login and one set of credentials.

For using SSO, you must understand the following:

-   **Service Providers**: When users trying to access the ServiceNow instance are redirected to an Identity Providers \(IdP\) to validate their credentials after successful validation users are allowed to access the instance. Here, ServiceNow acts as a service provider and relies on an Identity Provider \(IdP\) for handling user authentication and granting access to the instance.
-   Identity Providers: IdPs are external systems that validates the users identity and credentials to access a system.

To establish an SSO with to access ServiceNow, you must activate Multi-Provider Single sing-on \(SSO\) you must install the **Integration - Multiple Provider Single Sign-On Installer \(com.snc.integration.sso.multi.installer\)** plugin. For more information, see [Activate Multi-Provider SSO plugin](../task/t_ActivateMultipleProviderSSO.md).

After successful installation of the plugin, you can customize the SSO properties, access tables and scripts that are shipped along with the plugin. For more information, see [Multi-Provider SSO properties, tables, and scripts](../reference/r_InstalledWithMultiProviderSSO.md).

ServiceNow supports the following SSO methods:

-   [OpenID Connect](OIDC-SSO-overview.md)
-   [SAML 2.0](../../saml/concept/c_SAML2.0WebBrowserSSOProfile.md)
-   [Digest Authentication](c_DigestTokenAuthentication.md) \(Token based authentication\).

Choose the SSO method based on your requirement and learn more about how you need to prepare for configuring SSO. You must perform several steps to set up Multi-Provider SSO, including configuring properties, creating identity providers \(IdPs\), and configuring users to use SSO. For more information, see [Multi-Provider SSO configurations](sso-configurations.md).

After a successful configuration, the active IdPs in the instance are listed on the ServiceNow. You can list various SAML or OIDC Identity Providers \(IdPs\).

**Note:** A maximum of 10 IdPs can be listed on the login page. The IdP options won't be visible if the instance has Domain Support - Domain Extensions Installer \(**com.glide.domain.msp\_extensions.installer**\) plugin installed and enabled.

The Zurich release of ServiceNow include the following enhancements on SSO:

-   **List SAML IdPs on login page**: Log in using SAML and OIDC IdPs that are listed on the login experience on both the platform and portal login pages, making it easier for users to select their preferred IdP. Earlier only OIDC IdPs were listed.
-   **Select group for Auto-Provisioning**: Select specific groups during the auto-provisioning configuration for SAML and OIDC, ensuring users are assigned to the correct groups automatically.
-   **Configure multiple OIDC record using the same well-known URL**: Simplify OIDC setup by allowing the creation of OIDC records using the same well-known URL, streamlining the configuration process.
-   **Enhanced External logout complete page**: Display of login failure reason to the user. Provision to log in again to ServiceNow on the external logout complete page in case of successful logout.
-   **Enhanced error message**: Display of generic error message when Single Logout \(SLO\) is unsuccessful, ensuring consistent and secure communication.
-   **Notification enhancements for SAML Certificate and Encryption Keystore**: Receive timely notifications to the admins for SAML certificate and Encryption Keystore updates expiry, ensuring that your SSO configurations remain secure and up-to-date.

## Why organization needs SSO

A globally dispersed corporation might require one SSO provider for their employees, a different one for their vendors, and local database authentication for their administrators. Alternatively, a company might implement SAML 2.0 and a digest token authentication solutions on the same instance.

