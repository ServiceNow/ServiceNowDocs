---
title: Set up Google Drive spoke
description: Integrate a ServiceNow instance and Google Drive spoke by using Google Drive credentials to authenticate ServiceNow requests.Create a custom OAuth application from your Google Drive account to enable OAuth 2.0 authentication with the Google Drive spoke.Use the information generated during Google Drive account configuration to register the Google Drive application as an OAuth provider and allow the instance to request OAuth 2.0 tokens.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2023-08-03"
reading_time_minutes: 2
breadcrumb: [Google Drive Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Set up Google Drive spoke

Integrate a ServiceNow instance and Google Drive spoke by using Google Drive credentials to authenticate ServiceNow requests.

## Before you begin

-   Request Integration Hub subscription.
-   Activate the Google Drive spoke.
-   Role required: admin

## Configure Google Drive application

Create a custom OAuth application from your Google Drive account to enable OAuth 2.0 authentication with the Google Drive spoke.

### Before you begin

Google Drive integration requirements:

-   A domain and an email address associated with the domain. For example, www.mydomain.com and jane-admin@mydomain.com. Note that you can only register one email address per domain in GSuite or Google Drive.
-   A Google G Suite or Google Drive login created with the domain.
-   A Google Drive account.

Role required: admin.

### About this task

Complete these steps from your Google G Suite or Google Drive account. See the G Suite product documentation for instructions on creating and configuring custom applications.

### Procedure

1.  Log in to the G Suite portal, [https://gsuite.google.com/](https://gsuite.google.com/), with your domain email credentials.

2.  Enter your business name, the number of employees, and your country, and click **Next**.

3.  Enter the administrator contact name, email address and business phone number, and click **Next**.

4.  Enter the domain associated with this spoke.

5.  Provide the user name and password for your domain.

6.  Add users to the G Suite account.

7.  Verify your domain and email address.

    Users must create their own logins by navigating to the Google documentation.

8.  Register a new custom application.

    1.  Navigate to [https://console.developers.google.com](https://console.developers.google.com).

    2.  Create a project with your G Suite administrator credentials.

9.  Search for the Google Drive API and enable it.

10. Create a Credentials application and save the Client ID and Client secret.

    The Client Secret is only displayed in plain text for a short time. Copy the Client ID and the Client Secret to a text file so that you can use them when you [Configure the Google Drive connection](setup-gdrive.md#).


## Configure the Google Drive connection

Use the information generated during Google Drive account configuration to register the Google Drive application as an OAuth provider and allow the instance to request OAuth 2.0 tokens.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click the **Connections** tab.

3.  Toggle and enable the **Outbound** connections.

4.  Locate the **Google Drive** connection alias and click **View Details**.

    -   To configure the default connection and credential alias record that is shipped along with the Google Drive spoke, click **View Details**.
    -   To manage more than one Google Drive spoke connection records, you should create a new child alias record by clicking **Add Connection**. For more information about using multiple connections, see [Supporting multiple connections](../../integrationhub/concept/support-multiple-connections.md).
    If you are configuring the spoke for the first time, click **Configure**. Otherwise, click **Edit**.

5.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Connection Information|
    |Connection Name|Name to identify the connection record.|
    |Connection URL|Enter the URL `https://www.googleapis.com/`.|
    |Credential Information|
    |Credential Name|Name to identify the credential record.|
    |OAuth Name|Name to identify the application registry record.|
    |OAuth Client ID|Client ID of the Google Drive application you created in G Suite.|
    |OAuth Client Secret|Client Secret you generated when you created the application in G Suite.|
    |OAuth Redirect URL|ServiceNow instance URL in this format: `https://<Instance-Name>.service-now.com/oauth_redirect.do`|

    ![Google Drive Connection.](../image/gdrive-connection.png)

6.  Click **Configure and Get OAuth Token**.


