---
title: Set up Dropbox Business spoke
description: Set up an outbound integration between a ServiceNow instance and a Dropbox Business application by setting up the connection and credential records.Set up an OAuth 2.0 authentication between the Dropbox Business application and the ServiceNow instance by setting up a custom Dropbox Business application.Create connection records to a Dropbox Business account. A connection alias resolves your Dropbox connection and credential at runtime. Only one connection is active per Connection Alias at a time.Create connection records to a Dropbox Business account for the DropboxBusinessFileAccess alias. Connection aliases resolve your Dropbox connection and credential at runtime. Only one connection is active per Connection Alias at a time.Create connection records to a Dropbox Business account for the DropboxBusinessContent alias. Connection aliases resolve your Dropbox connection and credential at runtime. Only one connection is active per Connection Alias at a time.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2023-08-03"
reading_time_minutes: 7
breadcrumb: [Dropbox Business Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up Dropbox Business spoke

Set up an outbound integration between a ServiceNow instance and a Dropbox Business application by setting up the connection and credential records.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Dropbox Business spoke.
-   Role required: admin.

Setting up the Dropbox Business spoke, includes actions in the Dropbox app console, in the ServiceNow AI Platform® user interface, and in the Workflow Studio. Setup is easier if you keep each of these pages open in separate tabs.

## About this task

You must set up three connection and credential records for Team Management, File Access, and Content alias, in that order. The connection and credential forms contain the OAuth 2.0 credentials needed to establish a connection with the Dropbox business application. Before setting up the form, you must configure the data it needs by setting up an OAuth 2.0 authentication at the Dropbox Business application end. You must also ensure that you've already set up the alias and application registries.

## Set up OAuth 2.0 authentication

Set up an OAuth 2.0 authentication between the Dropbox Business application and the ServiceNow instance by setting up a custom Dropbox Business application.

### Before you begin

OAuth 2.0 setup requirements:

-   A Dropbox Business account.
-   Role required: team admin.

### About this task

This procedure creates a custom application on the Dropbox Business account. The application provides the OAuth 2.0 credentials necessary to set up the connection and credential records for all three Dropbox Business aliases. For more information on setting up applications, see [https://www.dropbox.com/developers/documentation](https://www.dropbox.com/developers/documentation).

### Procedure

1.  Log in to the Dropbox Professional My apps console, [https://www.dropbox.com/developers/apps](https://www.dropbox.com/developers/apps).

2.  Select **Create app**.

3.  On the Create a new app on the DBX Platform page, do the following actions.![Dropbox Business application setup.](../image/dropbox-business-spoke-setup-app.png)

    1.  Under Choose an API, select Scoped access.

    2.  Under Choose the type of access that you need, select the appropriate access type.

    3.  Under Name your app, enter a custom name for the application.

    4.  Select **Create app**.

        The custom application is created.

4.  To set up the OAuth 2.0 application, do the following steps under the **Settings** tab of the custom application.![OAuth setup under Dropbox Business application.](../image/dropbox-business-spoke-app-setup2.png)

    1.  Copy and store the value under the App key.

        Use the App key value in the Client ID field of the application registry on the ServiceNow instance.

    2.  Select Show under the App secret and then copy and store the value.

        **Tip:** You need both the App key and App secret values when you set up the application registries on the ServiceNow instance.

    3.  In the Redirect URIs field, enter the ServiceNow instance URL in the format [https://instancename/oauth\_redirect.do](https://instancename/oauth_redirect.do).

        **Note:** You can add multiple URIs.

    4.  To add a redirect URI, select **Add** and then enter the ServiceNow instance URL.

    5.  Select **Submit**.

    All three connection and credential records for the Dropbox Business application use the same App secret, App key, and Redirect URI that you set up in this step.


### What to do next

[Create Connection and Credential records for the Dropbox Business Team Management alias](setup-dbox-busi.md#)

## Create Connection and Credential records for the Dropbox Business Team Management alias

Create connection records to a Dropbox Business account. A connection alias resolves your Dropbox connection and credential at runtime. Only one connection is active per Connection Alias at a time.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Select the Connections tab.

3.  In the Search all connections field, enter `Dropbox`.

4.  On the DropboxBusinessTeamManagement tile, select **View Details**.

5.  Select **Configure**.![Configure button for Team Management alias.](../image/dropbox-business-spoke-team-configure.png)

6.  In the Configure Connection form, fill the details.

<table id="table_h23_5hd_jxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

Name of the connection between the Dropbox Business application and the ServiceNow instance.**Note:** The default and read-only name is DropboxBusinessTeamManagement. To provide a custom name, create another connection and credential record.

</td></tr><tr><td>

Connection URL

</td><td>

The URL to connect to the Dropbox Business account. The URL is [https://api.dropboxapi.com](https://api.dropboxapi.com).

</td></tr><tr><td>

API Version

</td><td>

The version of the API.

</td></tr><tr><td>

Credential Name

</td><td>

The custom name of the credential to access the Dropbox Business account.

</td></tr><tr><td>

OAuth Entity Name

</td><td>

The custom name of the OAuth entity that you created in the Dropbox Business account.

</td></tr><tr><td>

OAuth Client ID

</td><td>

The client ID that you generated in the custom Dropbox Business application. To learn how to generate, see [Set up OAuth 2.0 authentication](setup-dbox-busi.md#).

</td></tr><tr><td>

OAuth Client Secret

</td><td>

The client secret that you generated in the custom Dropbox Business application. To learn how to generate, see [Set up OAuth 2.0 authentication](setup-dbox-busi.md#).

</td></tr><tr><td>

OAuth Redirect URL

</td><td>

The redirect URI that you had provided in the Dropbox business application.

</td></tr></tbody>
</table>7.  Select **Configure and Get OAuth Token**.

    A temporary OAuth token is generated.


### What to do next

[Create Connection and Credential records for the Dropbox Business File Access alias](setup-dbox-busi.md#)

## Create Connection and Credential records for the Dropbox Business File Access alias

Create connection records to a Dropbox Business account for the DropboxBusinessFileAccess alias. Connection aliases resolve your Dropbox connection and credential at runtime. Only one connection is active per Connection Alias at a time.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Select the Connections tab.

3.  In the Search all connections field, enter `Dropbox`.

4.  On the DropboxBusinessFileAccess tile, select **View Details**.

5.  Select **Configure**.![Configure button for Dropbox Business Content alias.](../image/dropbox-business-spoke-businesscontent-configure.png)

6.  In the Configure Connection form, fill the details.

<table id="table_h23_5hd_jxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

Name of the connection between the Dropbox Business application and the ServiceNow instance.**Note:** The default and read-only name is DropboxBusinessFileAccess. To provide a custom name, create another connection and credential record.

</td></tr><tr><td>

Connection URL

</td><td>

The URL to connect to the Dropbox Business account. The URL is [https://api.dropboxapi.com](https://api.dropboxapi.com).

</td></tr><tr><td>

API Version

</td><td>

The version of the API.

</td></tr><tr><td>

Credential Name

</td><td>

The custom name of the credential to access the Dropbox Business account.

</td></tr><tr><td>

OAuth Entity Name

</td><td>

The custom name of the OAuth entity that you created in the Dropbox Business account.

</td></tr><tr><td>

OAuth Client ID

</td><td>

The client ID that you generated in the custom Dropbox Business application. To learn how to generate, see [Set up OAuth 2.0 authentication](setup-dbox-busi.md#).

</td></tr><tr><td>

OAuth Client Secret

</td><td>

The client secret that you generated in the custom Dropbox Business application. To learn how to generate, see [Set up OAuth 2.0 authentication](setup-dbox-busi.md#).

</td></tr><tr><td>

OAuth Redirect URL

</td><td>

The redirect URI that you had provided in the Dropbox business application.

</td></tr></tbody>
</table>7.  Select **Configure and Get OAuth Token**.

    A temporary OAuth token is generated.


### What to do next

[Create Connection and Credential records for the Dropbox Content alias](setup-dbox-busi.md#)

## Create Connection and Credential records for the Dropbox Content alias

Create connection records to a Dropbox Business account for the DropboxBusinessContent alias. Connection aliases resolve your Dropbox connection and credential at runtime. Only one connection is active per Connection Alias at a time.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Select the Connections tab.

3.  In the Search all connections field, enter `Dropbox`.

4.  On the DropboxBusinessContent tile, select **View Details**.

5.  Select **Configure**.![Configure button for Dropbox Business Content alias.](../image/dropbox-business-spoke-business-content-configure.png)

6.  In the Configure Connection form, fill the details.

<table id="table_h23_5hd_jxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

Name of the connection between the Dropbox Business application and the ServiceNow instance.**Note:** The default and read-only name is DropboxBusinessContent. To provide a custom name, create another connection and credential record.

</td></tr><tr><td>

Connection URL

</td><td>

The URL to connect to the Dropbox Business account. The URL is [https://api.dropboxapi.com](https://api.dropboxapi.com).

</td></tr><tr><td>

API Version

</td><td>

The version of the API.

</td></tr><tr><td>

Credential Name

</td><td>

The custom name of the credential to access the Dropbox Business account.

</td></tr><tr><td>

OAuth Entity Name

</td><td>

The custom name of the OAuth entity that you created in the Dropbox Business account.

</td></tr><tr><td>

OAuth Client ID

</td><td>

The client ID that you generated in the custom Dropbox Business application. To learn how to generate, see [Set up OAuth 2.0 authentication](setup-dbox-busi.md#).

</td></tr><tr><td>

OAuth Client Secret

</td><td>

The client secret that you generated in the custom Dropbox Business application. To learn how to generate, see [Set up OAuth 2.0 authentication](setup-dbox-busi.md#).

</td></tr><tr><td>

OAuth Redirect URL

</td><td>

The redirect URI that you had provided in the Dropbox business application.

</td></tr></tbody>
</table>7.  Select **Configure and Get OAuth Token**.

    A temporary OAuth token is generated.


### Result

The Dropbox Business spoke is set up and integrated with the ServiceNow instance.

