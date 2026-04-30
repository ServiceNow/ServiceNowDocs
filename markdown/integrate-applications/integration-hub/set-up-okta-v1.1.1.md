---
title: Set up Okta spoke
description: Integrate the Okta spoke with Okta to automate various actions on Okta. For example, you can automate the activation of a user on Okta. To integrate, connect your ServiceNow instance and Okta using an API key or OAuth authentication.Integrate the ServiceNow instance and your Okta account using an API key to authenticate ServiceNow requests.Generate an API key on your Okta organization or developer account to have the connection record authenticated by the Okta developer's or organizational account.Create Credential records to the Okta application that you created. The Okta spoke connection and credential alias uses these credentials to authorize actions.Create a Connection record to the Okta API. The Okta spoke connection and credential alias uses these connections to perform actions in Okta.Integrate the ServiceNow instance and your Okta account by creating a custom OAuth application in Okta to authenticate the ServiceNow requests.Create a custom OAuth application in your Okta developer's account to enable OAuth 2.0 authentication of the requests from your ServiceNow instance.Create a connection record that contains the information to connect to the Okta server. Your ServiceNow instance uses this form to send authentication requests to the OAuth application.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Okta Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up Okta spoke

Integrate the Okta spoke with Okta to automate various actions on Okta. For example, you can automate the activation of a user on Okta. To integrate, connect your ServiceNow instance and Okta using an API key or OAuth authentication.

Set up the Okta spoke.

## Before you begin

-   Request Integration Hub subscription.
-   Activate the Okta spoke on your ServiceNow instance.
-   Account with the Okta developers portal.
-   Role required: admin.

## About this task

Depending on your requirement, you can set up the spoke using an API key or OAuth credentials. However, you can use only one alias at a time for a ServiceNow domain.

## Set up Okta spoke using API key

Integrate the ServiceNow instance and your Okta account using an API key to authenticate ServiceNow requests.

### Generate an API key to request authentication

Generate an API key on your Okta organization or developer account to have the connection record authenticated by the Okta developer's or organizational account.

#### Before you begin

Okta requirements:

-   Okta organization or developer account
-   Role required: Okta administrator

#### About this task

The API key enables the Okta organization or developer account to authenticate an access request from your ServiceNow instance.

#### Procedure

1.  Log in to [https://developer.okta.com/login/](https://developer.okta.com/login/).

2.  On the left panel, navigate to **Security** &gt; **API**.

3.  On the API page, select Tokens.

    ![Token tab.](../image/okta-spoke-token-menu.png)

4.  Select **Create token**.

5.  In the Create token window, enter a name for the token.

6.  Select **Create token**.

    The token is created.

    ![Token created.](../image/okta-spoke-token-created.png)

7.  Copy the API token and store at a secured place.

    Note the expiry date of the token.

    ![Token expiry date.](../image/okta-spoke-token-expiry-date.png)


### Create an API Key credential record for the Okta spoke

Create Credential records to the Okta application that you created. The Okta spoke connection and credential alias uses these credentials to authorize actions.

#### Before you begin

Role required: admin.

#### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Select **New**.

3.  Select **API Key Credentials**.

4.  Fill the form.

<table id="table_lwy_g1z_4fb"><thead><tr><th>

Field

</th><th>

Value required

</th></tr></thead><tbody><tr><td>

Name

</td><td>

A custom name that uniquely identifies the record. For example, `Okta Credentials`.

</td></tr><tr><td>

Active

</td><td>

Activates the credential record so that it's used to connect to the Okta account.

</td></tr><tr><td>

API Key

</td><td>

API token that you had generated in your Okta account in the format `SSWS <API token>`. Replace `<API token>` with the API token.To learn how to generate an API token, see [Generate an API key to request authentication](set-up-okta-v1.1.1.md#).

</td></tr><tr><td>

Applies to

</td><td>

MID Server that can use this credential. For example, select **All MID Servers**.

</td></tr><tr><td>

Order

</td><td>

Order \(sequence\) in which this credential is used as it attempts to access the Okta API. The smaller the number, the higher in the list this credential appears. Establish credential order when using large numbers of credentials or when security locks out users after three failed login attempts. If all the credentials have the same order number \(or none\), the instance tries the credentials in a random order. For example, enter `100`.

</td></tr><tr><td>

Credential alias

</td><td>

The credential alias for Okta spoke that resolves in runtime when connecting to the Okta API.

</td></tr></tbody>
</table>5.  Select **Submit**.


### Create a connection record for the Okta spoke

Create a Connection record to the Okta API. The Okta spoke connection and credential alias uses these connections to perform actions in Okta.

#### Before you begin

Role required: admin.

#### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Open for the record for **Okta**.

3.  From the **Connections** tab, select **New**.

4.  Fill the form.

    |Field|Value required|
    |-----|--------------|
    |Name|Enter any name to uniquely identify the connection record. For example, enter `Okta Connection`.|
    |Credential|Select the Credential record that you created for Okta. For example, select **Okta Credentials**.|
    |Connection URL|Enter your Okta organization URL. For example, `https://dev-418994.oktapreview.com`.|

5.  Select **Submit**.


## Set up Okta using OAuth credentials

Integrate the ServiceNow instance and your Okta account by creating a custom OAuth application in Okta to authenticate the ServiceNow requests.

### Before you begin

-   Access to the Okta Developer Console
-   Role required: admin

### Create an OAuth application in Okta

Create a custom OAuth application in your Okta developer's account to enable OAuth 2.0 authentication of the requests from your ServiceNow instance.

#### Before you begin

Role required: admin

Administrator access to Okta Developer's or Organization account

#### Procedure

1.  Log in to [https://developer.okta.com/login/](https://developer.okta.com/login/).

2.  On the left panel, select **Applications** &gt; **Applications** &gt; **.**

3.  On the Applications page, select **Create App Integration**.

    ![Create App Integration.](../image/okta-spoke-oauth-createappintegration-button.png)

4.  On the Create a new app integration window, select OIDC - OpenID Connect.

5.  Select

    -   OIDC - OpenID Connect
    -   Web Application
6.  Select **Next**.![OAuth app settings.](../image/okta-spoke-oauth-settings.png)

7.  Fill the form.

<table id="table_jwz_52h_wyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

App integration name

</td><td>

Custom name of the OAuth application.

</td></tr><tr><td>

Logo

</td><td>

Logo of the OAuth application. Uploading a logo is optional.

</td></tr><tr><td>

Grant type

</td><td>

The type of OAuth 2.0 flow to use depending on the type of application you're building. To learn how to select the appropriate option, see [https://developer.okta.com/docs/concepts/oauth-openid/\#openid-connect](https://developer.okta.com/docs/concepts/oauth-openid/#openid-connect). Select the options:-   Authorization Code
-   Refresh Token
-   Implicit \(Hybrid\)
    -   Allow ID Token with implicit grant type
    -   Allow access token with implicit grant type


</td></tr><tr><td>

Sign-in redirect URIs

</td><td>

The URI that receives the authentication response and ID token from Okta. Enter your ServiceNow instance URL in the format `https://<instance-name>.service-now.com/oauth_redirect.do`.

</td></tr><tr><td>

Sign-out redirect URIs

</td><td>

The URI that contacts Okta to close a user session. Enter your ServiceNow instance URL in the format `https://<instance-name>.service-now.com/oauth_redirect.do`

</td></tr><tr><td>

Base URIs

</td><td>

URI of the self-hosted Okta widget. Providing the base URI is optional.

</td></tr><tr><td>

Controlled access

</td><td>

Option to assign access to Okta integration in your organization. To assign access:-   To assign access to everyone in the organization, select **Allow everyone in your organization to access**.
-   To assign access to selected groups, select **Limit access to selected groups** and enter the group names in the Selected group\(s\) field.
-   To assign access after integration, select **Skip group assignment for now**.


</td></tr></tbody>
</table>8.  Select **Save**.

    The OAuth application is created.![Okta OAuth application created.](../image/okta-spoke-oauth-app-created.png)

9.  Grant permissions to access Okta APIs.

    1.  Select **Okta API Scopes**.

        ![Okta API Scopes tab.](../image/okta-spoke-okta-scope-tab.png)

    2.  Under **Actions**, select **Grant for the APIs**.

        **Note:** These are all the OAuth scopes required for all the spoke actions to work. If you are only using a subset of the available spoke actions, you can select only the scopes required, based on your own security requirements.

        -   okta.users.manage
        -   okta.apps.manage
        -   okta.logs.read
        -   okta.groups.read
        -   okta.groups.manage
        -   okta.users.read
        -   okta.apps.read
        -   okta.eventHooks.read
        -   okta.eventHooks.manage
        For more information about the API scopes, see [Define allowed scopes](https://developer.okta.com/docs/guides/implement-oauth-for-okta/define-allowed-scopes/) in [Okta Developer Documentation](https://developer.okta.com/docs/).


### Create a connection record for Okta Spoke

Create a connection record that contains the information to connect to the Okta server. Your ServiceNow instance uses this form to send authentication requests to the OAuth application.

#### Before you begin

**Important:** If you have configured different OAuth scopes as mentioned in step 9 of [Create an OAuth application in Okta](set-up-okta-v1.1.1.md#), do not perform this procedure. Instead, perform the steps outlined in [Connect to a third-party OAuth provider](https://www.servicenow.com/docs/access?context=connect-3rd-party-oauth-provider&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) and add the corresponding OAuth scopes that align with your Okta Web Application that are granted in step 9 of [Create an OAuth application in Okta](set-up-okta-v1.1.1.md#).

Role required: admin.

#### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Select the **Integrations** tab.

3.  In the Search all connections field, enter `Okta`.

    **Note:** The Outbound tab is enabled by default. Confirm that it's enabled.

    ![Outbound tab is enabled.](../image/outbound-tab.png)

4.  On the Okta spoke tile, select **View Details**.

    ![View Details button on Okta spoke alias.](../image/okta-spoketile.png)

5.  Select **Configure**.

6.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the connection established with the Okta instance. The first connection's default name is automatically assigned to match the name specified in the Connections and Credentials form on the Connection &amp; Credential Aliases page. To provide your custom name, create a connection record by selecting **Add Connection**.|
    |Connection URL|The URL to connect to the Okta server. The URL format is https://\[yourOktaDomain\].com.|
    |API Version|The version of the Okta APIs.|
    |Authorization URL|The URL that the OAuth application at Okta provides to seek authorization to access the Okta resource server. The format is `https://{youroktadomain}.com/oauth2/{API version}/authorize`.|
    |Token URL|The URL to obtain the access token. The format is `https://{youroktadomain}.com/oauth2/{API version}/token`.|
    |Token Revocation URL|The URL provided by the OAuth authorization server that enables a client application to request the revocation or cancellation of access tokens and refresh tokens that were previously issued. The format is `https://{youroktadomain}.com/oauth2/{API version}/revoke`.|
    |OAuth Client ID|The client ID generated in the Okta developer's account.|
    |OAuth Client Secret|The client secret generated in the Okta developer's account.|
    |OAuth Redirect URL|Redirect the URL to your ServiceNow instance. The format is `https://{instance-name}.service-now.com/oauth_redirect.do`.|

    ![Okta spoke connection form.](../image/okta-conn-form.png)

7.  Select **Configure and Get OAuth Token**.

    The OAuth Access token is generated for the Okta spoke.

    **Note:** You must log in to Okta before the OAuth access token is granted.


