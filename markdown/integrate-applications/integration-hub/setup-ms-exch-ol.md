---
title: Set up Microsoft Exchange Online spoke
description: Integrate the ServiceNow instance and Microsoft Exchange Online account by creating a custom OAuth application in Microsoft Exchange Online to authenticate ServiceNow requests.Provide authorization to the ServiceNow instance by registering an application with Azure AD.Register Microsoft Exchange Online as the OAuth provider so that the ServiceNow instance can request OAuth 2.0 tokens.Authorize the Microsoft Exchange Online spoke actions by creating credential records for the application registered in the Microsoft Azure portal. The Microsoft Exchange Online connection and credential alias uses these credentials to authorize actions.Create a credential record for the Microsoft Exchange Online spoke Mailbox actions. The Microsoft Exchange Online spoke connection and credential alias uses these credentials to authorize Mailbox actions.Perform actions in Microsoft Exchange Online by configuring connection records for your Microsoft Exchange Online account. The Microsoft Exchange Online spoke connection and credential alias uses these connections to perform actions.Configure a connection record for your Microsoft Exchange Online spoke Mailbox actions. The Microsoft Exchange Online spoke connection and credential aliases use these connections to perform only Mailbox actions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/integration-hub/setup-ms-exch-ol.html
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Microsoft Exchange Online Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up Microsoft Exchange Online spoke

Integrate the ServiceNow instance and Microsoft Exchange Online account by creating a custom OAuth application in Microsoft Exchange Online to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Microsoft Exchange Online spoke.
-   Role required: admin.

## Register an application using the Microsoft Azure portal

Provide authorization to the ServiceNow instance by registering an application with Azure AD.

### Before you begin

Role required: Azure Active Directory admin

### About this task

Complete these steps from the Microsoft Azure portal. For instructions on registering an application, see the [Microsoft Azure documentation](https://docs.microsoft.com/en-gb/).

### Procedure

1.  In the Microsoft Azure portal, add the **Redirect URIs** in this format: `https://<instance-name>.service-now.com/oauth_redirect.do`

2.  For the **Required Permissions**, select **Microsoft Graph**.

    \[Omitted image "ms-exchange-online-spoke-permissions.png"\] Alt text: Permissions required for Microsoft Exchange Online spoke

3.  Record the **Client Secret** for use in later configurations.


### Result

The ServiceNow application is created with Microsoft Azure AD.

## Register Microsoft Exchange Online as the OAuth provider

Register Microsoft Exchange Online as the OAuth provider so that the ServiceNow instance can request OAuth 2.0 tokens.

### Before you begin

Role required: admin

### About this task

Use the information generated during the registration of the application in the Microsoft Azure portal.

### Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

2.  Open the record, **Microsoft Exchange Online**.

3.  On the form, fill in the fields.

<table id="table_rn5_5md_qnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to uniquely identify the record. For example, `Microsoft Exchange Online`.

</td></tr><tr><td>

Client ID

</td><td>

Application ID created during application registration.

</td></tr><tr><td>

Client Secret

</td><td>

Client secret created during application registration.

</td></tr><tr><td>

OAuth API Script

</td><td>

Optional script to customize the request and response.

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

Authorization URL

</td><td>

OAuth authorization code endpoint. Enter `https://login.microsoftonline.com/<Directory-ID>/oauth2/v2.0/authorize`

</td></tr><tr><td>

Token URL

</td><td>

OAuth server token endpoint. Enter `https://login.microsoftonline.com/<Directory-ID>/oauth2/v2.0/token`

</td></tr><tr><td>

Token Revocation URL

</td><td>

OAuth server token revocation endpoint.

</td></tr><tr><td>

Redirect URL

</td><td>

OAuth callback endpoint. Enter `https://<instance-name>.service-now.com/oauth_redirect.do`

</td></tr><tr><td>

Use mutual authentication

</td><td>

Option to use mutual authentication for token request and revocation. This option requires a mutual authentication profile to be specified.

</td></tr><tr><td>

Send Credentials

</td><td>

Client credentials in the request.

</td></tr></tbody>
</table>4.  Right-click the form header, and click **Save**.

    A system-generated OAuth entity profile is created and displayed in the OAuth Entity Profiles related list. For example, `Microsoft Exchange Online default_profile`.

5.  Navigate to **System OAuth** &gt; **Application Registry**.

6.  Open the record, **Microsoft Exchange Online\_clientCredentials**.

7.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Client ID|Application ID created during application registration.|
    |Client Secret|Client secret created during application registration.|
    |Default Grant Type|Grant type used to establish the token. Select **Client Credentials**.|
    |Token URL|OAuth server token endpoint. Enter `https://login.microsoftonline.com/<Directory-ID>/oauth2/v2.0/token`|
    |Redirect URL|OAuth callback endpoint. Enter `https://<instance-name>.service-now.com/oauth_redirect.do`|

8.  Right-click the form header, and click **Save**.

    A system-generated OAuth entity profile is created and displayed in the OAuth Entity Profiles related list. For example, `Microsoft Exchange Online_clientCredentials default_profile`.


## Create credential records for the Microsoft Exchange Online spoke

Authorize the Microsoft Exchange Online spoke actions by creating credential records for the application registered in the Microsoft Azure portal. The Microsoft Exchange Online connection and credential alias uses these credentials to authorize actions.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Click **New**.

    The system displays the message, `What type of Credentials would you like to create?`

3.  Select **OAuth 2.0 Credentials**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name to uniquely identify the record. For example, `Exchange_Online_Credentials`.|
    |Active|Option to actively use the credential record.|
    |OAuth Entity Profile|OAuth profile created during the registration of Microsoft Exchange Online spoke as an OAuth provider with **Default Grant Type** as **Authorization Code**. For example, `Microsoft Exchange Online`.|
    |Applies to|MID Servers that can use this credential. For example, select **All MID Servers**.|
    |Order|Order that the credentials are used. For example, enter `100`.|

5.  Right-click the form header and click **Save**.

6.  To generate the OAuth token, click the **Get OAuth Token** related link.

7.  Navigate to **Connections &amp; Credentials** &gt; **Credentials**.

8.  Click **New**.

    The system displays the message, `What type of Credentials would you like to create?`

9.  Select **OAuth 2.0 Credentials**.

10. On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name to uniquely identify the record. For example, `Exchange_Online_Credentials_clientCred`.|
    |Active|Option to actively use the credential record.|
    |OAuth Entity Profile|OAuth profile created during the registration of Microsoft Exchange Online spoke as an OAuth provider with **Default Grant Type** as **Client Credentials**. For example, `Microsoft Exchange Online_clientCredentials default_profile`.|
    |Applies to|MID Servers that can use this credential. For example, select **All MID Servers**.|
    |Order|Order that the credentials are used. For example, enter `100`.|

11. Right-click the form header and click **Save**.

12. To generate the OAuth token, click the **Get OAuth Token** related link.


### Result

The credential records for the Microsoft Exchange Online spoke are created.

## Create a credential record for the Microsoft Exchange Online spoke Mailbox actions

Create a credential record for the Microsoft Exchange Online spoke Mailbox actions. The Microsoft Exchange Online spoke connection and credential alias uses these credentials to authorize Mailbox actions.

### Before you begin

-   Make sure that MID Server is setup and configured
-   Make sure that Power Shell with EXO V2 module is installed. This module is required for executing Mailbox management actions.
-   Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Click **New**.

    The system displays this message: `What type of Credentials would you like to create?`

3.  Select **Windows Credentials**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name to uniquely identify the record. For example, MS Exchange Online Mailbox Cred.|
    |Active|Option to actively use the credential record.|
    |User name|User name with access to the target Windows host.|
    |Password|Password for the account.|
    |Applies to|Option to specify if the credential applies to all MID Servers in your network, or to one or more **Specific MID servers**. Specify the MID Servers that should use this credential in the **MID servers** field.|
    |Order|Order to apply this credential. For example, `100`.|
    |Credential alias|Credential alias associated with the spoke.|

5.  Right-click the form header and click **Submit**.


### Result

A Windows Credential record is created for the Microsoft Exchange Online spoke Mailbox actions.

## Configure a connection for the Microsoft Exchange Online spoke

Perform actions in Microsoft Exchange Online by configuring connection records for your Microsoft Exchange Online account. The Microsoft Exchange Online spoke connection and credential alias uses these connections to perform actions.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click the **Integrations** tab.

3.  Under **Connections**, the **Outbound** connections are displayed by default.

4.  Locate the **Microsoft\_Exchange\_Online** connection alias and click **View Details**.

    -   To configure the default connection and credential alias record that is shipped along with the Microsoft Exchange Online spoke, click **View Details**.
    -   To manage more than one Microsoft Exchange Online spoke connection records, you should create a new child alias record by clicking **Add Connection**. For more information about using multiple connections, see [Supporting multiple connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/support-multiple-connections.md).
    If you are configuring the spoke for the first time, click **Configure**. Otherwise, click **Edit**.

5.  On the **Connection** form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Connection Information|
    |Name|Name to uniquely identify the connection. For example, `Microsoft_Exchange_Online`.|
    |Connection URL|Enter `https://graph.microsoft.com`.|
    |API Version|Enter `v1.0`.|
    |Credential Information|
    |Name|Name to identify the credential record. For example, `Exchange_Online Creds`.|
    |Authorization URL|OAuth authorization code endpoint. Enter `https://login.microsoftonline.com/<Directory-ID>/oauth2/v2.0/authorize`|
    |Token URL|OAuth server token endpoint. Enter `https://login.microsoftonline.com/<Directory-ID>/oauth2/v2.0/token`|
    |Token Revocation URL|OAuth server token revocation endpoint.|
    |OAuth Client ID|Application ID created during application registration.|
    |OAuth Client Secret|Client secret created during application registration.|
    |OAuth Redirect URL|OAuth callback endpoint. Enter `https://<instance-name>.service-now.com/oauth_redirect.do`|

6.  Click **Create and Get OAuth Token**.


### Result

The Microsoft Exchange Online spoke is set up and integrated with the ServiceNow instance.

## Configure a connection record for the Microsoft Exchange Online spoke Mailbox actions

Configure a connection record for your Microsoft Exchange Online spoke Mailbox actions. The Microsoft Exchange Online spoke connection and credential aliases use these connections to perform only Mailbox actions.

### Before you begin

-   Make sure that MID Server is setup and configured
-   Make sure that Power Shell with EXO V2 module is installed. This module is required for executing Mailbox management actions.
-   Role required: admin

### Procedure

1.  Navigate to **All** &gt; **IntegrationHub** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Locate the **Microsoft Exchange Online MID** connection alias and open it.

3.  For **Configuration Template**, ensure that **Microsoft Exchange Online Authorization Code** is selected.

4.  Click the Create New Connection &amp; Credential related link.

5.  On the form, fill the fields.

    |Field|Description|
    |-----|-----------|
    |Connection Information|
    |Name|Name to uniquely identify the connection. For example, `Microsoft_Exchange_Online_MID`.|
    |Connection URL|Enter `https://graph.microsoft.com`.|
    |API Version|Enter `v1.0`.|
    |Credential Information|
    |Name|Name to identify the credential record. For example, `Exchange_Online_MID Creds`.|
    |Authorization URL|OAuth authorization code endpoint. Enter `https://login.microsoftonline.com/<Directory-ID>/oauth2/v2.0/authorize`|
    |Token URL|OAuth server token endpoint. Enter `https://login.microsoftonline.com/<Directory-ID>/oauth2/v2.0/token`|
    |Token Revocation URL|OAuth server token revocation endpoint.|
    |OAuth Client ID|Application ID created during application registration.|
    |OAuth Client Secret|Client secret created during application registration.|
    |OAuth Redirect URL|OAuth callback endpoint. Enter `https://<instance-name>.service-now.com/oauth_redirect.do`|

6.  Click **Create and Get OAuth Token**.


### Result

A connection record is created for Microsoft Exchange Online spoke Mailbox actions.

