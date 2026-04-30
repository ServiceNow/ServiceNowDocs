---
title: Set up the Microsoft Intune spoke
description: Integrate your ServiceNow instance with the Microsoft Intune account by creating a custom OAuth application in Microsoft Intune.Provide authorization to the ServiceNow instance by registering an application on Microsoft Entra ID.Use the information generated during the application configuration in Microsoft Azure portal to register Microsoft Intune as the OAuth provider so that the ServiceNow instance can request OAuth 2.0 tokens.Authorize the Microsoft Intune spoke actions by creating credential records for the application registered in the Microsoft Azure portal. The Microsoft Intune connection and credential alias uses these credentials to authorize actions.Modify the short description to provide spoke specific information.Perform actions in Microsoft Intune by creating connection records for your Microsoft Intune account. The Microsoft Intune connection and credential alias uses these connections to perform actions.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Microsoft Intune Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Set up the Microsoft Intune spoke

Integrate your ServiceNow instance with the Microsoft Intune account by creating a custom OAuth application in Microsoft Intune.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Microsoft Intune plugin.
-   Role required: admin.

## Register OAuth application using the Microsoft Azure portal

Provide authorization to the ServiceNow instance by registering an application on Microsoft Entra ID.

### Before you begin

Role required: Azure Active Directory admin

### About this task

Complete these steps from the Microsoft Azure portal.

### Procedure

1.  Log in to the Microsoft Azure portal.

    For instructions on registering an application, see [Tutorial: Register an app with Azure Active Directory](https://docs.microsoft.com/en-us/powerapps/developer/common-data-service/walkthrough-register-app-azure-active-directory) in the [Microsoft Azure documentation](https://docs.microsoft.com/en-gb/).

2.  In the Azure portal, add the **Redirect URIs**.

    The Redirect URI should be in the format `https://<instance-name>.service-now.com/oauth_redirect.do`. For more information, see [Authentication and authorization for Azure Time Series Insights API](https://docs.microsoft.com/en-us/azure/time-series-insights/time-series-insights-authentication-and-authorization).

3.  For the **Required Permissions**, ensure that you provide these permissions:

    ![API permissions](../image/api-permission-ms-intune.png)

    Depending on your requirement, the permissions can be of the type, **Application**, or **Delegated**. For more information, see [Quickstart: Configure a client application to access a web API](https://docs.microsoft.com/en-us/azure/active-directory/develop/quickstart-configure-app-access-web-apis) in [Microsoft Docs](https://docs.microsoft.com/en-us/).

4.  In the Azure portal, create a client secret.

    For more information, see [Option 2: Create a new application secret](https://docs.microsoft.com/en-us/azure/active-directory/develop/howto-create-service-principal-portal).

5.  Copy the client secret for later reference.


### Result

The ServiceNow application is created with Microsoft Azure AD.

## Register Microsoft Intune as an OAuth provider

Use the information generated during the application configuration in Microsoft Azure portal to register Microsoft Intune as the OAuth provider so that the ServiceNow instance can request OAuth 2.0 tokens.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

2.  Open for the record, **Microsoft Intune**.

3.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Client ID|Application ID created during application registration.|
    |Client Secret|Client secret created during application registration.|
    |Active|Option to actively use the application registry.|
    |Authorization URL|OAuth authorization code endpoint. Enter `https://login.microsoftonline.com/<Directory-ID>/oauth2/v2.0/authorize`.|
    |Token URL|OAuth server token endpoint. Enter `https://login.microsoftonline.com/<Directory-ID>/oauth2/v2.0/token`.|
    |Token Revocation URL|OAuth server token revocation endpoint.|
    |Redirect URL|OAuth callback endpoint. Enter `https://<instance-name>.service-now.com/oauth_redirect.do`.|

4.  Right-click the form header, and click **Save**.


## Create a credential record for the Microsoft Intune spoke

Authorize the Microsoft Intune spoke actions by creating credential records for the application registered in the Microsoft Azure portal. The Microsoft Intune connection and credential alias uses these credentials to authorize actions.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Click **New**.

    The system displays this message: `What type of Credentials would you like to create?`

3.  Select **OAuth 2.0 Credentials**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name to uniquely identify the record. For example, `MS Intune Cred`.|
    |Active|Option to actively use the credential record.|
    |OAuth Entity Profile|OAuth profile created during the registration of Microsoft Intune as an OAuth provider. For example, `Microsoft Intune default_profile`.|

5.  Right-click the form header and click **Submit**.

6.  To generate the OAuth token, click the **Get OAuth Token** related link.


## Create a connection record for the Microsoft Intune spoke

Perform actions in Microsoft Intune by creating connection records for your Microsoft Intune account. The Microsoft Intune connection and credential alias uses these connections to perform actions.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connections &amp; Credentials Aliases**.

2.  Open the alias record, **Microsoft\_Intune**.

3.  From the **Connections** tab, click **New**.

4.  On the form, fill in the fields.

<table id="table_c4p_lzg_2hb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to uniquely identify the record. For example, `MS Intune Connection`.

</td></tr><tr><td>

Credential

</td><td>

Credential record created for Microsoft Intune spoke. For example, `MS Intune Cred`.

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

Active

</td><td>

Option to actively use the connection.

</td></tr><tr><td>

Domain

</td><td>

Domain that the action or activity runs in.

</td></tr></tbody>
</table>5.  In the **Attributes** tab, specify `v1.0` for **u\_version**.

6.  Click **Submit**.


### Result

The Microsoft Intune spoke is set up and Microsoft Intune is integrated with the ServiceNow instance.

