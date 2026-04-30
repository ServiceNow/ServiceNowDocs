---
title: Set up Microsoft Exchange Online spoke
description: Integrate the ServiceNow instance and Microsoft Exchange Online account by creating a custom OAuth application in Microsoft Exchange Online to authenticate ServiceNow requests.Provide authorization to the ServiceNow instance by registering an application with Azure AD.Register Microsoft Exchange Online as the OAuth provider so that the ServiceNow instance can request OAuth 2.0 tokens.Authorize the Microsoft Exchange Online spoke actions by creating credential records for the application registered in the Microsoft Azure portal. The Microsoft Exchange Online connection and credential alias uses these credentials to authorize actions.Create a credential record for the Microsoft Exchange Online spoke Mailbox actions. The Microsoft Exchange Online spoke connection and credential alias uses these credentials to authorize Mailbox actions.Perform actions in Microsoft Exchange Online by creating connection records for your Microsoft Exchange Online account. The Microsoft Exchange Online spoke connection and credential alias uses these connections to perform actions.Modify the short description to provide spoke specific information.Create a connection record for your Microsoft Exchange Online spoke Mailbox actions. The Microsoft Exchange Online spoke connection and credential aliases use these connections to perform only Mailbox actions.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 8
breadcrumb: [Microsoft Exchange Online Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
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

    ![Permissions required for Microsoft Exchange Online spoke](../image/ms-exchange-online-spoke-permissions.png)

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

## Create connection records for the Microsoft Exchange Online spoke

Perform actions in Microsoft Exchange Online by creating connection records for your Microsoft Exchange Online account. The Microsoft Exchange Online spoke connection and credential alias uses these connections to perform actions.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Open the record, **Microsoft\_Exchange\_Online**.

3.  In the Connections related list, click **New**.

4.  On the form, fill in the fields.

<table id="table_c4p_lzg_2hb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to uniquely identify the record. For example, `Exchange_Online_Connection`.

</td></tr><tr><td>

Credential

</td><td>

Credential record created for Microsoft Exchange Online. For example, `Exchange_Online_Credentials`.

</td></tr><tr><td>

Connection alias

</td><td>

Alias record associated with this connection.

</td></tr><tr><td>

URL builder

</td><td>

**Note:** Do not select the check box.

</td></tr><tr><td>

Connection URL

</td><td>

Connection URL. Enter `https://graph.microsoft.com`.

</td></tr><tr><td>

Use MID server

</td><td>

Option to use a MID Server. If the check box is selected, define the fields in the Advanced MID Server Configuration related list.

</td></tr><tr><td>

Active

</td><td>

Option to actively use the connection.

</td></tr><tr><td>

Domain

</td><td>

Domain that the action or activity runs in.

</td></tr></tbody>
</table>5.  Click **Update**.

6.  Navigate to **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

7.  Open the record, **Microsoft\_Exchange\_Online\_clientCred**.

8.  In the Connections related list, click **New**.

9.  On the form, fill in the fields.

<table id="table_vjd_1md_qnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to uniquely identify the record. For example, `Exchange_Online_Connection_clientCred`.

</td></tr><tr><td>

Credential

</td><td>

Credential record created for Microsoft Exchange Online. For example, `Exchange_Online_Credentials_clientCred`.

</td></tr><tr><td>

Connection alias

</td><td>

Alias record associated with this connection.

</td></tr><tr><td>

URL builder

</td><td>

**Note:** Do not select the check box.

</td></tr><tr><td>

Connection URL

</td><td>

Connection URL. Enter `https://graph.microsoft.com`.

</td></tr><tr><td>

Use MID server

</td><td>

Option to use a MID Server. If the check box is selected, define the fields in the Advanced MID Server Configuration related list.

</td></tr><tr><td>

Active

</td><td>

Option to actively use the connection.

</td></tr><tr><td>

Domain

</td><td>

Domain that the action or activity runs in.

</td></tr></tbody>
</table>10. Click **Update**.


### Result

The Microsoft Exchange Online spoke is set up and integrated with the ServiceNow instance.

## Create a connection record for the Microsoft Exchange Online spoke Mailbox actions

Create a connection record for your Microsoft Exchange Online spoke Mailbox actions. The Microsoft Exchange Online spoke connection and credential aliases use these connections to perform only Mailbox actions.

### Before you begin

-   Make sure that MID Server is setup and configured
-   Make sure that Power Shell with EXO V2 module is installed. This module is required for executing Mailbox management actions.
-   Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connections &amp; Credentials Aliases**.

2.  Open the **Microsoft Exchange Online MID** record.

3.  From the **Connections** tab, click **New**.

4.  On the form, fill these fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name to uniquely identify the record. For example, `MS Exchange Online Mailbox Connection`.|
    |Credential|Credential record created for Microsoft Exchange Online spoke Mailbox actions. For example, `MS Exchange Online spoke Mailbox Cred`.|
    |Connection alias|Alias record associated with this connection.|
    |Connection URL|Base URL to connect to **Microsoft Exchange Online**. Enter: `127.0.0.1`|
    |Active|Option to actively use the connection record.|
    |Domain|Domain that the action runs in.|
    |Override default port|Target port used by the connection. If blank, the system uses the default port.|
    |Use MID server|Option to use MID Servers for this connection. If the check box is selected, define the fields in the Advanced MID Server Configuration related list.|

5.  Click **Submit**.


### Result

A connection record is created for Microsoft Exchange Online spoke Mailbox actions.

