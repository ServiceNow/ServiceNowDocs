---
title: Set up the Microsoft Azure Blob Storage Spoke
description: Configure the Microsoft Azure Blob Storage connection alias record on your ServiceNow instance. This enables the authentication of connection requests from the ServiceNow instance by the Microsoft Azure portal.Create an OAuth application on Microsoft Azure that authenticates requests for OAuth tokens from your ServiceNow instance.Configure the connection and credential alias record of the Microsoft Azure Blob Storage to send a request for an OAuth token from your ServiceNow instance and have it authenticated by the Microsoft Azure portal. After authentication, an OAuth token is available to your instance to access the Microsoft Azure Blob Storage.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2023-08-03"
reading_time_minutes: 3
breadcrumb: [Microsoft Azure Blob Storage Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Set up the Microsoft Azure Blob Storage Spoke

Configure the Microsoft Azure Blob Storage connection alias record on your ServiceNow instance. This enables the authentication of connection requests from the ServiceNow instance by the Microsoft Azure portal.

## Before you begin

-   Request Integration Hub subscription.
-   Activate the Azure Blob Storage spoke.
-   Role required: admin

## Register Microsoft Azure Blob Storage as an OAuth provider

Create an OAuth application on Microsoft Azure that authenticates requests for OAuth tokens from your ServiceNow instance.

### Before you begin

Role required: admin

### Procedure

1.  Log in to [https://portal.azure.com/](https://portal.azure.com/).

2.  Select **App registrations**.

3.  Select **New registration**.

4.  Fill the form.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the OAuth application.|
    |Supported account types|Option to specify who can use the OAuth application that you're creating to access Microsoft Azure Blob Storage.|
    |Redirect URI \(optional\)|Option to provide the redirect URI. The redirect URI format is https://&lt;instance-name&gt;.service-now.com/oauth\_redirect.do. From the Select a platform list, select **Web**.|

5.  Select **Register**.

    The OAuth application is registered.

6.  Copy the values from the following fields under the Essentials heading:

    -   Application \(client\) ID
    -   Directory \(tenant\) ID
7.  In the Client credentials field, select **Add a certificate or secret**.

8.  Under the Client secrets heading, select **New client secret**.

9.  In the Add a client secret window, do the following actions.

    1.  In the Description field, enter a description of the client secret.

    2.  In the Expires field, enter the expiry period of the client secret.

    3.  Select **Add**.

        The client secret is generated.

10. Under the Value heading, copy and store the client secret at a secure place.

11. Add the API permission.

    1.  On the left panel, select **API permissions**.

    2.  Select **Add a permission**.

    3.  On the Request API permissions window, select **Azure Storage**.

    4.  Select **Delegated permissions**.

    5.  Under Permissions, select **Access Azure Storage**.

    6.  Select **Add permissions**.

        The permission is added and visible under the API / Permissions name heading.

    7.  Select **Grant admin consent for ServiceNow**.

    8.  Select **Yes**.

    Microsoft Azure Blob Storage is registered as an OAuth service provider.


## Configure a connection to Microsoft Azure

Configure the connection and credential alias record of the Microsoft Azure Blob Storage to send a request for an OAuth token from your ServiceNow instance and have it authenticated by the Microsoft Azure portal. After authentication, an OAuth token is available to your instance to access the Microsoft Azure Blob Storage.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Select the **Integrations** tab.

3.  In the Search all connections field, enter Microsoft Azure Blob Storage.

    The **Outbound** tab is enabled by default. If the tab isn’t enabled, toggle-select to enable.

4.  On the Microsoft Azure Blob Storage tile, select **View Details**.

5.  Select **Configure**.

6.  Fill the form.

<table id="table_usv_xlj_zcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

Name of the connection alias record. The default name of the first connection record is the same as the alias. You can't update the name.

</td></tr><tr><td>

Authorization URL

</td><td>

URL that your ServiceNow instance uses to request OAuth tokens from the Microsoft Azure portal. The URL must in the following format: `https://login.microsoftonline.com/{tenant ID}/oauth2/v2.0/authorize`. Use the tenant ID that you generated when you registered the OAuth application.

</td></tr><tr><td>

Token URL

</td><td>

URL that your ServiceNow instance uses to get the OAuth token. The URL must in the following format: `https://login.microsoftonline.com/{tenant ID}/oauth2/v2.0/token`. Use the tenant ID that you generated when you registered the OAuth application.

</td></tr><tr><td>

Token Revocation URL

</td><td>

URL that your ServiceNow instance uses to cancel the OAuth token. The URL must in the following format: `https://login.microsoftonline.com/{tenant ID}/oauth2/v2.0/revoke`. Use the tenant ID that you generated when you registered the OAuth application.**Note:** This field isn't required.

</td></tr><tr><td>

Client ID

</td><td>

Unique ID of the OAuth application that you created on the Microsoft Azure portal. The Microsoft Azure portal uses this ID to authenticate your ServiceNow instance requests.

</td></tr><tr><td>

Client Secret

</td><td>

The secret that Microsoft Azure portal uses to authenticate your ServiceNow instance requests. You generate the client secret when you create the OAuth application on Microsoft Azure portal.

</td></tr><tr><td>

Redirect URL

</td><td>

Specific address where the third-party application sends your ServiceNow instance back after the request is authenticated. The format of the redirect URL is `https://<instance-name>.service-now.com/oauth_redirect.do`.

</td></tr></tbody>
</table>7.  Select **Configure and Get OAuth Token**.

    You're required to log in to [https://portal.azure.com/](https://portal.azure.com/) before the OAuth token is provided.

    On successful authentication, the request is authenticated and the OAuth token is available.


