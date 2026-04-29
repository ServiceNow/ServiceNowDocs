---
title: Configure Private Key JWT for OIDC based SSO
description: Configure Private Key JWT for OIDC based SSO integrations.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Private Key JWT Support for OAuth 2.0 Client Authentication, OAuth Outbound, OAuth authentication, Authentication, Access Management]
---

# Configure Private Key JWT for OIDC based SSO

Configure Private Key JWT for OIDC based SSO integrations.

## Before you begin

Role required: oauth\_admin

You must perform the following tasks before choosing Private Key JWT for OIDC based SSO.

-   [Upload Java Key Store certificate](../../../administer/security/task/JWT-Bearer-token-support.md#): Attach a JKS certificate to your instance to use to enable the JWT client authentication.
-   [Configure a JWT signing key](../../../administer/security/task/JWT-Bearer-token-support.md#): Create a JWT signing key to assign to your Java KeyStore \(JKS\) certificate.

    **Note:** If you want to add **X.509 Certificate SHA-1 Thumbprint int \(x5t\)** to the header as part of the JWT Key, you must configure the form and add the **X.509 Certificate SHA-1 Thumbprint int \(x5t\)** field.

-   [Create a JWT provider with a JWT signing key](../../../administer/security/task/JWT-Bearer-token-support.md#): Add a JWT provider to your ServiceNow instance.

To include a JWT Key for OIDC based Identity Provider, you must:

-   Install the **Integration - Multiple Provider Single Sign-On Installer** \(`com.snc.integration.sso.multi.installer`\) plugin.
-   Enable the properties for **Multiple Provider SSO Properties**. For more information, see [Multi-Provider SSO properties, tables, and scripts](../../single-sign-on/reference/r_InstalledWithMultiProviderSSO.md).
-   Create an OIDC Identity Provider. For more information, see [Create an OpenID Connect \(OIDC\) configuration for Single Sign-On \(SSO\)](../../single-sign-on/task/create-OIDC-configuration-SSO.md).

## Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

2.  Select the OIDC Identity Provider that you had created.

3.  On top of the form, select **Configure** &gt; **Form Design**.

    **Note:** You must add **Send Credentials** and **JWT Provider** fields to the form to use the Private Key JWT for OIDC based Identity Provider authentication requests.

4.  Choose the **As Private Key JWT** for Send Credentials.

5.  Select the **JWT Provider**.

    ![](../images/jwt-oidc-sso.png)

    When the user authenticates, the authentication page has options to login through Okta.


