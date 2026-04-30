---
title: Set up Microsoft OneDrive spoke
description: Integrate the ServiceNow instance and Microsoft OneDrive spoke by using OAuth 2.0 credentials to authenticate ServiceNow requests.Create a custom OAuth application from your Microsoft OneDrive account to enable OAuth 2.0 authentication with the Microsoft OneDrive spoke.Use the information generated during Microsoft OneDrive account configuration to register Microsoft OneDrive as an OAuth provider and allow the instance to request OAuth 2.0 tokens.Create Connection records to your Microsoft OneDrive account. The Microsoft OneDrive spoke connection and credential aliases use these connections to perform actions in the Microsoft OneDrive.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Microsoft OneDrive Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Set up Microsoft OneDrive spoke

Integrate the ServiceNow instance and Microsoft OneDrive spoke by using OAuth 2.0 credentials to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Microsoft OneDrive spoke.
-   Role required: admin.

## Configure Microsoft OneDrive application

Create a custom OAuth application from your Microsoft OneDrive account to enable OAuth 2.0 authentication with the Microsoft OneDrive spoke.

### Before you begin

Microsoft OneDrive requirements:

-   Microsoft OneDrive account
-   [Microsoft Azure](https://portal.azure.com) account
-   Role required: Microsoft OneDrive tenant administrator credentials

### About this task

Complete these steps from your Azure Developer account. See the [Azure](https://docs.microsoft.com/en-us/azure/) product documentation for instructions on creating and configuring custom applications.

### Procedure

1.  Log in to the [Microsoft Azure App registration portal](https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationsListBlade) with your organization credentials.

2.  Register a new custom application.

    Fill in the application name, the supported account type, and the redirect URI, and then click **Register**.

    An overview of the application's basic information is shown.

    **Note:** Ensure that you enter the redirect URI in this format: `https://<instance>.service-now.com/oauth_redirect.do`.

3.  Copy the application ID to a text file.

    You will use this ID and the client secret generated in the next step to register the app as a third-party OAuth provider on your ServiceNow instance. You use the application ID as the client ID when you connect the application to ServiceNow.

4.  Add a client secret.

    1.  In Microsoft Azure, navigate to **Manage** &gt; **Certificates &amp; secrets**.

    2.  Provide a description and an expiration date and click **Add**.

        **Note:** The client secret is only displayed in plain text for a short time. You use the client secret when you connect the application to ServiceNow.

5.  Enable the permissions you want the application to support.

    For more information, see the [Microsoft Graph permissions reference](https://docs.microsoft.com/en-us/graph/permissions-reference).

    1.  In Microsoft Azure, navigate to **Manage** &gt; **API permissions**.

    2.  Click the Microsoft Graph tile.

    3.  Select the Delegated or Application permissions that the application supports.

        Delegated permissions enable the application to access the API as a signed-in user. Application permissions enable the application to run as a background service or daemon without a signed-in user. You must mention these API permissions in the **OAuth Entity scopes** tab while configuring the [application registry](setup-msonedrive.md#).

        **Note:** You must ensure that these API permissions are provided for your custom app.

        |Name|OAuth scope|
        |----|-----------|
        |Calendars.ReadWrite|Calendars.ReadWrite|
        |Calendars.ReadWrite.Shared|Calendars.ReadWrite.Shared|
        |email|email|
        |Files.Read|Files.Read|
        |Files.Read.All|Files.Read.All|
        |offline\_access|offline\_access|

    4.  Click **Add permissions**.


## Register Microsoft OneDrive as OAuth provider

Use the information generated during Microsoft OneDrive account configuration to register Microsoft OneDrive as an OAuth provider and allow the instance to request OAuth 2.0 tokens.

### Before you begin

-   Request Integration Hub subscription.
-   Activate Microsoft OneDrive spoke.
-   Create Microsoft OneDrive application.
-   If you are using a single tenant app registration, obtain the value of **Directory \(tenant\) ID** from the Azure portal.

Role required: admin

### Procedure

1.  In ServiceNow, navigate to **System OAuth** &gt; **Application Registry**.

2.  Click **New**.

3.  On the screen titled **What kind of OAuth application**, select **Connect to a third-party OAuth Provider**.

4.  Enter these values in the Application Registries form:

<table id="table_alw_kq3_gfb"><thead><tr><th>

Field

</th><th>

Value required

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter any name to uniquely identify the record, for example `OneDrive OAuth profile`.

</td></tr><tr><td>

Client ID

</td><td>

Enter the Application ID of the OneDrive application you created in Azure.

</td></tr><tr><td>

Client Secret

</td><td>

Enter the Client Secret you generated when you created the application in Azure.

</td></tr><tr><td>

Default Grant type

</td><td>

Select **Authorization Code**.

</td></tr><tr><td>

Authorization URL

</td><td>

-   If you are using a multi-tenant app registration, click the lock icon![Lock icon](../../../common/image/icon-lock.png), enter `https://login.microsoftonline.com/common/oauth2/v2.0/authorize`, and then click the lock icon again.
-   If you are using a single tenant app registration, click the lock icon![Lock icon](../../../common/image/icon-lock.png), enter `https://login.microsoftonline.com/<Directory-ID>/oauth2/v2.0/authorize`, and then click the lock icon again.

In the URL, replace `<Directory-ID>` with the value of **Directory \(tenant\) ID** obtained from the Azure portal.

</td></tr><tr><td>

Token URL

</td><td>

Click the lock icon ![Lock icon](../../../common/image/icon-lock.png), enter `https://login.microsoftonline.com/common/oauth2/v2.0/token`, and then click the lock icon again.

</td></tr><tr><td>

Redirect URL

</td><td>

Click the lock icon ![Lock icon](../../../common/image/icon-lock.png), enter `https://<instance>.service-now.com/oauth_redirect.do`, and then click the lock icon again.

</td></tr></tbody>
</table>5.  In the **OAuth Entity Scopes** related list, add scopes to match the permissions you defined when you configured the Microsoft OneDrive application.

    Click **Insert a new row** and enter the name and the OAuth scope of the permission. The name and the OAuth scope are often the same string. Ensure that these scopes are provided.

    |Name|OAuth scope|
    |----|-----------|
    |Calendars.ReadWrite|Calendars.ReadWrite|
    |Calendars.ReadWrite.Shared|Calendars.ReadWrite.Shared|
    |email|email|
    |Files.Read|Files.Read|
    |Files.Read.All|Files.Read.All|
    |offline\_access|offline\_access|

    **Note:** The scopes mentioned here must be same as the API permissions provided during the [custom app configuration](setup-msonedrive.md#).

6.  Right-click the form header, and click **Save**.

    The system validates the OAuth credentials.


## Create Connection and Credential Alias for Microsoft OneDrive spoke

Create Connection records to your Microsoft OneDrive account. The Microsoft OneDrive spoke connection and credential aliases use these connections to perform actions in the Microsoft OneDrive.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **IntegrationHub** &gt; **Connections &amp; Credentials** &gt; **OneDrive**.

2.  From **Related Links**, click **Create New Connection &amp; Credential**.

3.  On the form, fill in these fields:

    |Field|Value required|
    |-----|--------------|
    |Connection Name|Name to identify the connection. This field is automatically set to Microsoft Onedrive Spoke Connection|
    |Connection URL|The URL to make connection to the spoke. This field is automatically set to https://graph.microsoft.com|
    |OAuth Entity Name|Name of the OAuth entity profile. This field is automatically set to Microsoft Onedrive Spoke Auth.|
    |OAuth Client ID|Client ID of the OneDrive application you registered in Microsoft Azure App registration portal.|
    |OAuth Client Secret|Client Secret generated when you registered the application in Microsoft Azure portal.|
    |OAuth Redirect URL|The redirect URL. The format of the URL is https://&lt;your-instance&gt;.service-now.com/oauth\_redirect.do|

4.  Click Create and Get OAuth Token.


### Result

The Microsoft OneDrive spoke is set up and integrated with the ServiceNow instance.

