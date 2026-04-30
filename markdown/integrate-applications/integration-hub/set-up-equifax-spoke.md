---
title: Set up Equifax spoke
description: Integrate the ServiceNow instance and Equifax spoke by using basic Auth or OAuth 2.0 authentication to authenticate ServiceNow requests.Use the information generated during the application configuration to register Equifax as an OAuth provider. OAuth provider registration enables the ServiceNow instance to request OAuth 2.0 tokens.Create credential records to the Equifax custom OAuth application you created during Equifax account configuration. The Equifax spoke connection and credential aliases use these credentials to authorize actions in Equifax application.Create a connection record for your Equifax application with the credential aliases provided. You need to select the credential record to the Equifax custom OAuth application you created during Equifax account configuration.Generate the Equifax access token.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Equifax Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Set up Equifax spoke

Integrate the ServiceNow instance and Equifax spoke by using basic Auth or OAuth 2.0 authentication to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Equifax spoke.
-   Ensure that the dependent plugins are activated.
-   Role required: admin.

## Register Equifax as an OAuth provider

Use the information generated during the application configuration to register Equifax as an OAuth provider. OAuth provider registration enables the ServiceNow instance to request OAuth 2.0 tokens.

### Before you begin

-   Role required: admin
-   Client ID and client secret generated from configuration of the third-party Equifax application

### Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

2.  Select **New**.

    The system displays this message: `What kind of OAuth application?`.

3.  Select **Connect to a third party OAuth Provider**.

4.  On the form, fill these values.

<table id="table_jqc_hgn_swb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to uniquely identify the record. For example, enter: `Equifax OAuth`

</td></tr><tr><td>

Client ID

</td><td>

&lt;Client ID&gt; created during the Equifax account configuration.

</td></tr><tr><td>

Client Secret

</td><td>

&lt;Client Secret&gt; created during the Equifax account configuration.

</td></tr><tr><td>

Authorization URL

</td><td>

OAuth Server's authorization code flow endpoint. Required only for Authorization Code grant type.

</td></tr><tr><td>

Token URL

</td><td>

OAuth Server's token endpoint. For example, `xxx.equifax.com`.

</td></tr><tr><td>

Token Revocation URL

</td><td>

OAuth server token revocation endpoint.

</td></tr><tr><td>

Redirect URL

</td><td>

OAuth callback endpoint in this format: `https://<instance>.service-now.com/oauth_redirect.do`

</td></tr><tr><td>

OAuth API Script

</td><td>

Script to customize the request and response.

</td></tr><tr><td>

Logo URL

</td><td>

URL that contains an image to use as the application logo.

</td></tr><tr><td>

Default Grant Type

</td><td>

Grant type used to establish the token. Select **Client Credentials**.

</td></tr><tr><td>

Refresh Token Lifespan

</td><td>

Time, in seconds, that the refresh token is valid. The default time is 1430 seconds.

</td></tr><tr><td>

PKCE required

</td><td>

Option to enable public clients to require PKCE for an authorization.**Note:** You can use only **Authorization Code** as the **Default Grant type** when **PKCE** is enabled.

</td></tr><tr><td>

Application

</td><td>

Application scope that contains this record.

</td></tr><tr><td>

Accessible from

</td><td>

Application scope that this registry is accessible from.

</td></tr><tr><td>

Active

</td><td>

Option to actively use the application registry.

</td></tr><tr><td>

Use mutual authentication

</td><td>

Option to use mutual authentication for token request and revocation. This option requires a mutual authentication profile to be specified.

</td></tr><tr><td>

Send credentials

</td><td>

Option for whether or how to send authentication information identifying the application and its authorized users to the OAuth server. Select **In Request Body**.

</td></tr></tbody>
</table>5.  On the form header, select **Submit**.


## Create OAuth 2.0 credential record for the Equifax spoke

Create credential records to the Equifax custom OAuth application you created during Equifax account configuration. The Equifax spoke connection and credential aliases use these credentials to authorize actions in Equifax application.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Select **New**.

    The system displays this message: `What type of Credentials would you like to create?`

3.  Select **OAuth 2.0 Credentials**.

    The pop-up window displays a blank OAuth 2.0 Credentials form.

4.  Enter these values.

    |Field|Value required|
    |-----|--------------|
    |Name|Enter any name to uniquely identify the record. For example, enter `Equifax OAuth2.0 API Credentials`.|
    |Active|Enable|
    |OAuth Entity Profile|Select the OAuth profile you created when you registered the custom Equifax application as an OAuth provider. For example, select **Equifax OAuth default profile**.|
    |Applies to|Select the MID Servers that can use this credential. For example, select **All MID Servers**.|
    |Order|Select the order to apply this credential. For example, enter `100`.|

5.  Select **Submit**.

6.  To generate the OAuth token, select the **Get OAuth Token** related link.


## Create connection record for the Equifax spoke

Create a connection record for your Equifax application with the credential aliases provided. You need to select the credential record to the Equifax custom OAuth application you created during Equifax account configuration.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connections &amp; Credentials Aliases**.

2.  Open the alias record, for example, **Equifax.**.

3.  From the **Connections** tab, select **New**.

4.  On the form, fill these fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name to uniquely identify the record. For example, `Equifax Connection`.|
    |Credential|Basic Auth or OAuth 2.0 credential record created for Equifax. For example, `Equifax OAuth2.0 API Credentials`.|
    |Connection alias|Alias record associated with this connection. For example, `sn_equifax_spoke.Equifax`|
    |Connection URL|Base URL to connect to **Equifax**.|
    |Active|Option to actively use the connection record.|
    |Domain|Domain that the action runs in.|

5.  Select **Submit**.


## Get Equifax OAuth token

Generate the Equifax access token.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Select the Equifax spoke OAuth Credential record.

    For example, select **Equifax OAuth2.0 Credentials**.

3.  From Related Links, select **Get OAuth Token**.


