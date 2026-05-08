---
title: Configuring authentication settings for ServiceNow services and components in AEM
description: Enable logging in to both the Adobe Experience Manager \(AEM\) instance of your website and the ServiceNow instance using a third-party OpenID Connect \(OIDC\) provider that supports both OIDC and single sign-on \(SSO\) protocols.Register ServiceNow as a web application with a third-party OIDC provider to validate the identity of a user using a JSON Web Token \(JWT\).Add a third-party OIDC provider service to your ServiceNow instance to verify the identity of end users.Configure the third-party OIDC provider details in your Adobe Experience Manager \(AEM\) instance to access the ServiceNow components as an authenticated user.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Integrating with Adobe Experience Manager, Integrate, Customer Service Management]
---

# Configuring authentication settings for ServiceNow services and components in AEM

Enable logging in to both the Adobe Experience Manager \(AEM\) instance of your website and the ServiceNow instance using a third-party OpenID Connect \(OIDC\) provider that supports both OIDC and single sign-on \(SSO\) protocols.

You can select Okta or Microsoft Azure as the third-party OIDC provider that supports both OIDC and single sign-on \(SSO\) protocols.

**Note:** Your AEM instance must use the selected third-party OIDC provider as the SSO provider.

## Register ServiceNow with a third-party OIDC provider

Register ServiceNow as a web application with a third-party OIDC provider to validate the identity of a user using a JSON Web Token \(JWT\).

### Before you begin

ServiceNow identifies an end user by sending the JWT token containing the end user information to the OIDC provider. The process to register ServiceNow with the OIDC provider varies depending on the provider.

**Note:**

This topic uses Okta as an example, but you can substitute the details of your own OIDC provider.

Role required: Okta account \(Third-party OIDC provider account\)

### Procedure

1.  Log in to your Okta account.

2.  Select the Applications menu.

3.  On the Applications page, click **Add Application**.

4.  On the Create New Application page, select **Web**.

5.  Fill in the fields.

<table id="table_y5k_pxj_vkb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Application label

</td><td>

Unique application name for your ServiceNow instance.

</td></tr><tr><td>

Authorization Code

</td><td>

Selected

</td></tr><tr><td>

Refresh Token

</td><td>

Selected

</td></tr><tr><td>

Login redirect URIs

</td><td>

Callback URL of your AEM instance.The URL structure is: `https://<AEM-instance>:<AEM_port>/bin/now/auth/callback`

</td></tr><tr><td>

Login initiated

</td><td>

App Only

</td></tr></tbody>
</table>6.  Click **Done**.


### What to do next

In the Client Credentials section, record the Client ID and Client secret values for when you set up Okta as an OAuth provider in your ServiceNow and AEM instances.

## Add an OIDC provider to the ServiceNow instance

Add a third-party OIDC provider service to your ServiceNow instance to verify the identity of end users.

### Before you begin

You must have configured the third-party OIDC provider service as an OAuth provider and recorded your **Client ID** and **Client secret** values. For more information, see [Register ServiceNow with a third-party OIDC provider](aem-setup-servicenow-authentication.md#).

Role required: oauth\_admin

### Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

2.  Set up OAuth for your ServiceNow instance.

    -   Click **New**, select **Configure an OIDC provider to verify ID tokens**, and then fill in the Application Registries form.
    -   Select an existing template for your OIDC provider \(Okta or Microsoft Azure\), and then either accept the default values in the Application Registries form or modify them.

        **Note:** OIDC provider templates are available after loading demo data with the OAuth 2.0 plugin. For more information, see Configure an OAuth OIDC provider.

<table id="table_zfw_cyj_vkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the OAuth provider.

</td></tr><tr><td>

Client ID

</td><td>

Client ID you recorded earlier for your ServiceNow instance registered in the third-party OIDC server. The ServiceNow instance uses the client ID when requesting an access token.

</td></tr><tr><td>

Client Secret

</td><td>

Client secret you recorded earlier for your ServiceNow instance registered in the third-party OIDC server.

</td></tr><tr><td>

OAuth OIDC Provider Configuration

</td><td>

OIDC provider with which you registered your ServiceNow instance.

**Note:** Select the record of your OIDC provider configuration or create another configuration, if not available, to ensure that the **OIDC Metadata URL** field value is correct and the **User Claim** and **User Field** fields are mapped correctly.

</td></tr></tbody>
</table>3.  Save your changes.

    -   For an existing template, click **Update**.
    -   For a new template, click **Submit**.

## Configure OIDC provider details in Adobe Experience Manager

Configure the third-party OIDC provider details in your Adobe Experience Manager \(AEM\) instance to access the ServiceNow components as an authenticated user.

### Before you begin

You must have configured the third-party OIDC provider service as an OAuth provider and recorded your **Client ID** and **Client secret** values \(see [Register ServiceNow with a third-party OIDC provider](aem-setup-servicenow-authentication.md#)\).

Role required: AEM administrator

### About this task

Configure the OIDC provider details in AEM to enable the AEM users to access the ServiceNow instance as authenticated users. If you don't configure the OIDC provider details in AEM, an AEM user is considered as a public user when accessing the ServiceNow instance.

### Procedure

1.  Access the web console in AEM with a URL in the following format: `https://<AEM_hostname>:<AEM_port>/system/console/configMgr`.

2.  Search for `ServiceNow OAuth Configuration`.

3.  In the **Name** column, click the **ServiceNow OAuth Configuration** link.

4.  Provide values for the configuration settings.

<table id="table_z3l_4zj_vkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ServiceNow Client ID

</td><td>

Client ID you recorded when setting up the OAuth for your ServiceNow instance.

</td></tr><tr><td>

ServiceNow Client Secret

</td><td>

Client secret you recorded when setting up the OAuth for your ServiceNow portal.

</td></tr><tr><td>

OAuth Provider Auth URL

</td><td>

Authorization server end point used for obtaining the authorization code. In the following URL structure, substitute the domain name of the authorization server of your third-party OIDC provider.Example: `https://<auth_server_domain>/oauth2/authorize`

</td></tr><tr><td>

OAuth Provider Access Token URL

</td><td>

Authentication server endpoint used for exchanging the authorization code for an access token. In the following URL structure, substitute the domain name of the authorization server of your third-party OIDC provider.Example: `https://<auth_server_domain>/oauth2/token`

</td></tr><tr><td>

Authorization request scope

</td><td>

List of scopes for limiting the authorization access. **Note:** The default value `openid email profile offline_access` works for most OIDC providers \(for example, Okta\).

</td></tr><tr><td>

User property to store refresh token

</td><td>

Name of the user property to store the authentication refresh token. **Note:** Once filled, this token is used to obtain access tokens for that user in all future requests.

</td></tr></tbody>
</table>5.  Click **Save**.


