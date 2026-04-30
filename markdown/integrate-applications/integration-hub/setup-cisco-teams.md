---
title: Set up the Cisco Webex Teams Spoke
description: Integrate the ServiceNow instance and Cisco Webex Teams by creating a custom OAuth application in Cisco Webex Teams or using the custom Cisco Webex Credentials to authenticate ServiceNow requests.Use the information generated during the Cisco Webex Teams application configuration to register Cisco Webex Teams as an OAuth provider and allow the ServiceNow instance to request OAuth 2.0 tokens.Create a credential record for the Cisco Webex Teams account. The Cisco Webex Teams Spoke connection and credential alias uses these credentials to authorize actions.Create a credential record for the Cisco Webex Teams account. The Cisco Webex Teams Spoke connection and credential alias uses these credentials to authorize actions.Modify the short description to provide spoke specific information.Create a connection record for your Specify whether the record is for a host, instance, custom application, or account.. The Visa spoke connection and credential aliases use these connections to perform actions in .
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Cisco Webex Teams Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Set up the Cisco Webex Teams Spoke

Integrate the ServiceNow instance and Cisco Webex Teams by creating a custom OAuth application in Cisco Webex Teams or using the custom Cisco Webex Credentials to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate Cisco Webex Teams Spoke.
-   Role required: admin

You can choose to use either OAuth 2.0 or the custom credentials, Cisco Webex Credentials, for authentication.

## Register Cisco Webex Teams as an OAuth provider

Use the information generated during the Cisco Webex Teams application configuration to register Cisco Webex Teams as an OAuth provider and allow the ServiceNow instance to request OAuth 2.0 tokens.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

2.  Click **New**.

    The system displays this message: `What kind of OAuth application?`.

3.  Select **Connect to a third party OAuth Provider**.

4.  On the form, fill these values.

<table id="table_ol2_bg4_ymb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to uniquely identify the record. For example, enter: `Cisco Webex Teams OAuth`

</td></tr><tr><td>

Client ID

</td><td>

Client ID created during the Cisco Webex Teams application configuration.

</td></tr><tr><td>

Client Secret

</td><td>

Client Secret created during the Cisco Webex Teams application configuration.

</td></tr><tr><td>

Authorization URL

</td><td>

OAuth authorization code endpoint. Enter: `https://webexapis.com/v1/authorize`

</td></tr><tr><td>

Token URL

</td><td>

OAuth server token endpoint. Enter: `https://webexapis.com/v1/access_token`

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

Script to customize the request and response. Select **OauthCiscoWebexTeamsUtils**.

</td></tr><tr><td>

Logo URL

</td><td>

URL that contains an image to use as the application logo.

</td></tr><tr><td>

Default Grant Type

</td><td>

Grant type used to establish the token. Select **Authorization Code**.

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

</td></tr></tbody>
</table>5.  Right-click the form header, and click **Save**.


### What to do next

Ensure that the OAuth entity profile has these permissions:![OAuth entity profile scopes.](../image/cisco-teams-entity-profiles.png)

## Create a OAuth credential record for the Cisco Webex Teams Spoke

Create a credential record for the Cisco Webex Teams account. The Cisco Webex Teams Spoke connection and credential alias uses these credentials to authorize actions.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **IntegrationHub** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Click **New**.

    The system displays this message: `What type of Credentials would you like to create?`

3.  Select **OAuth 2.0 Credentials**.

4.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Name|Name to uniquely identify the record. For example, Cisco Webex Teams Cred.|
    |Active|Option to actively use the credential record.|
    |OAuth Entity Profile|OAuth profile created during the registration of Cisco Webex Teams as an OAuth provider. For example, Cisco Webex Teams OAuth Profile.|
    |Applies to|Option to specify if the credential applies to all MID Servers in your network, or to one or more **Specific MID servers**. Specify the MID Servers that should use this credential in the **MID servers** field.|
    |Order|Order to apply this credential. For example, `100`.|
    |Credential alias|Credential alias associated with the spoke.|

5.  Right-click the form header and click **Submit**.

6.  To generate the OAuth token, click the **Get OAuth Token** related link.


## Create a connection and credential alias record for the Cisco Webex Teams Spoke

Create a credential record for the Cisco Webex Teams account. The Cisco Webex Teams Spoke connection and credential alias uses these credentials to authorize actions.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **IntegrationHub** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Open the **CiscoWebexTeams** record.

    ![Cisco Teams Webex connection and credential alias](../image/cisco_webex_teams_conn-credential.png)

    The **CiscoWebexTeams** Connection &amp; Credential Aliases display.

3.  Click **New** under **Connections** tab.

    ![New connection and credentials for Cisco Webex Teams](../image/new_connection_credential_cisco_webex_teams.png)

4.  On the form, fill these values.

<table id="table_ctx_plw_xqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the HTTPS connection record for Cisco Webex Teams spoke

</td></tr><tr><td>

Credentials

</td><td>

Name of the credential created for Cisco Webex Teams spoke

 Provide the value ceated in “Create a OAuth credential record for the Cisco Webex Teams spoke”.

</td></tr><tr><td>

Connection URL

</td><td>

Option to provide the connection URL.

 Provide the value as https://webexapis.com

</td></tr></tbody>
</table>    ![Connection record for Cisco Webex Teams](../image/connection_record_cisco_webex_teams.png)

5.  Right-click the form header and click **Submit**.


## Create a Connection &amp; Credentials alias for Visa Spoke

Create a connection record for your  . The Visa spoke connection and credential aliases use these connections to perform actions in .

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connections &amp; Credentials Aliases**.

2.  Open the alias record for ****.

3.  From the **Connections** tab, click **New**.

4.  On the form, fill these fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name to uniquely identify the record. For example, `<Application-Name> Connection`.|
    |Credential|Credential record created for Visa spoke. For example, `<Application-Name> Cred`.|
    |Connection alias|Alias record associated with this connection.|
    |Host|Fully qualified domain name of the target host where the **** server is installed. For example, `<host>.<domain>.com`.|
    |Connection URL|Base URL to connect to ****. Enter: ``|
    |Active|Option to actively use the connection record.|
    |Domain|Domain that the action runs in.|
    |Override default port|Target port used by the connection. If blank, the system uses the default port.|
    |Use MID server|Option to use a MID Servers for this connection. If the check box is selected, define the fields in the Advanced MID Server Configuration related list.|

5.  Click **Submit**.


