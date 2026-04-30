---
title: Set up the Guidewire spoke
description: Integrate the ServiceNow instance and Guidewire using basic Auth or OAuth 2.0 authentication to authenticate ServiceNow requests.Use the information generated during the Guidewire application configuration to register Guidewire as an OAuth provider. OAuth provider registration enables the ServiceNow instance to request OAuth 2.0 tokens.Create credential records to the Guidewire custom OAuth application you created during Guidewire account configuration. The Guidewire spoke connection and credential aliases use these credentials to authorize actions in Guidewire application. The Guidewire connection and credential alias uses these credentials to authorize actions.Create a Basic Auth credential record for the Guidewire application. The Guidewire connection and credential alias uses these credentials to authorize actions in Guidewire PolicyCenter, Guidewire ContactManager, and Guidewire ClaimCenter.You can choose to switch between implemented basic Auth and OAuth 2.0 authentication based on your event or security needs.Create a connection record for your Guidewire application. The Guidewire connection and credential aliases use these connections to perform actions in Guidewire PolicyCenter, Guidewire ContactManager, and Guidewire ClaimCenter.Generate the Guidewire access token.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Guidewire Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Set up the Guidewire spoke

Integrate the ServiceNow instance and Guidewire using basic Auth or OAuth 2.0 authentication to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Guidewire spoke.
-   Choose and implement the Guidewire authentication approach appropriate for your application. See the Guidewire documentation for [Choosing an authentication flow](https://docs.guidewire.com/cloud/cc/202205/cloudapica/cloudAPI/topics/71_Authentication/p_choosing-an-authentication-flow.html) for details.
-   Ensure that the dependent plugins are activated.
-   Role required: admin.

## Register Guidewire as an OAuth provider

Use the information generated during the Guidewire application configuration to register Guidewire as an OAuth provider. OAuth provider registration enables the ServiceNow instance to request OAuth 2.0 tokens.

### Before you begin

-   Role required: admin
-   Client ID and client secret generated from configuration of the third-party Guidewire application

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

Name to uniquely identify the record. For example, enter: `Guidewire OAuth`

</td></tr><tr><td>

Client ID

</td><td>

&lt;Client ID&gt; created during the Guidewire account configuration.

</td></tr><tr><td>

Client Secret

</td><td>

&lt;Client Secret&gt; created during the Guidewire account configuration.

</td></tr><tr><td>

Authorization URL

</td><td>

OAuth authorization code endpoint.

</td></tr><tr><td>

Token URL

</td><td>

OAuth server token endpoint.

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

Grant type used to establish the token..

</td></tr><tr><td>

Refresh Token Lifespan

</td><td>

Time, in seconds, that the refresh token is valid. The default time is 8,640,0000 seconds.

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

Option for whether or how to send authentication information identifying the application and its authorized users to the OAuth server.

</td></tr></tbody>
</table>5.  On the form header, select **Submit**.


## Create OAuth 2.0 credential record for the Guidewire spoke

Create credential records to the Guidewire custom OAuth application you created during Guidewire account configuration. The Guidewire spoke connection and credential aliases use these credentials to authorize actions in Guidewire application. The Guidewire connection and credential alias uses these credentials to authorize actions.

### Before you begin

Role required: admin

The following example shows the steps for creating a credential record for Guidewire PolicyCenter, Guidewire ContactManager, or Guidewire ClaimCenter.

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Select **New**.

    The system displays this message: `What type of Credentials would you like to create?`

3.  Select **OAuth 2.0 Credentials**.

    The pop-up window displays a blank OAuth 2.0 Credentials form.

4.  Enter these values.

    |Field|Value required|
    |-----|--------------|
    |Name|Enter any name to uniquely identify the record. For example, enter `Guidewire OAuth2.0 API Credentials`.|
    |Active|Enable|
    |OAuth Entity Profile|Select the OAuth profile you created when you registered the custom Equifax application as an OAuth provider. For example, select **Equifax OAuth default profile**.|
    |Applies to|Select the MID Servers that can use this credential. For example, select **All MID Servers**.|
    |Order|Select the order to apply this credential. For example, enter `100`.|

5.  Select **Submit**.

6.  To generate the OAuth token, select the **Get OAuth Token** related link.


## Create Basic Auth credential record for the Guidewire spoke

Create a Basic Auth credential record for the Guidewire application. The Guidewire connection and credential alias uses these credentials to authorize actions in Guidewire PolicyCenter, Guidewire ContactManager, and Guidewire ClaimCenter.

### Before you begin

Role required: admin

The following example shows the steps for creating a basic Auth credential record for Guidewire PolicyCenter, Guidewire ContactManager, and Guidewire ClaimCenter.

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Select **New**.

    The system displays this message: `What type of Credentials would you like to create?`

3.  Select Basic Auth Credentials.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name to uniquely identify the record. For example, Guidewire.|
    |User name|User name to be entered as credential.|
    |Password|Password to be entered as credential.|
    |Active|Option to actively use the credential record. Select the option.|
    |Order|Order that the credentials are used. For example, enter `100`.|

5.  Right-click the form header and select **Submit**.


## Switch between basic Auth and OAuth 2.0 credential

You can choose to switch between implemented basic Auth and OAuth 2.0 authentication based on your event or security needs.

### Before you begin

-   Role required: admin
-   [Create Basic Auth credential record for the Guidewire spoke](set-up-guidewire-spoke.md#)
-   [Register Guidewire as an OAuth provider](set-up-guidewire-spoke.md#)

The following example shows the steps for switching from basic auth to OAuth 2.0 for the Guidewire ClaimCenter application.

### Procedure

1.  Navigate to **All****Connections &amp; Credentials****Connection &amp; Credential Aliases**.

2.  Select the Guidewire ClaimCenter record you want to re-configure.

3.  From the **Connections** tab, open the existing target connection record.

4.  In the **Credential** field, select the reference lookup icon.

5.  Select the credential record.

6.  -   If switching the authentication method from basic auth to OAuth 2.0, select the credential record created during OAuth setup.
-   If switching the authentication method from OAuth 2.0 to basic auth, select the credential record created during basic Auth setup.
7.  Save the record.


### What to do next

[Get Guidewire OAuth token](set-up-guidewire-spoke.md#)

## Create connection record for the Guidewire spoke

Create a connection record for your Guidewire application. The Guidewire connection and credential aliases use these connections to perform actions in Guidewire PolicyCenter, Guidewire ContactManager, and Guidewire ClaimCenter.

### Before you begin

Role required: admin

The following example shows the steps for creating a connection record for Guidewire PolicyCenter, Guidewire ContactManager, or Guidewire ClaimCenter.

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connections &amp; Credentials Aliases**.

2.  Open the alias record, for example, **Guidewire ClaimCenter**.

3.  From the **Connections** tab, select **New**.

4.  On the form, fill these fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name to uniquely identify the record. For example, `Guidewire Connection`.|
    |Credential|Basic Auth or OAuth 2.0 credential record created for Guidewire. For example, `Guidewire OAuth2.0 API Credentials`.|
    |Connection alias|Alias record associated with this connection.|
    |Connection URL|Base URL to connect to **Guidewire**.|
    |Active|Option to actively use the connection record.|
    |Domain|Domain that the action runs in.|

5.  Select **Submit**.


## Get Guidewire OAuth token

Generate the Guidewire access token.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Select the Guidewire spoke OAuth Credential record.

    For example, select **Guidewire OAuth2.0 Credentials**.

3.  From Related Links, select **Get OAuth Token**.


### Result

The Guidewire spoke receives a new OAuth access token.

