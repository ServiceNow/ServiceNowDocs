---
title: Set up the Google Directory spoke
description: Integrate the ServiceNow instance and Google Directory spoke by using G Suite credentials to authenticate ServiceNow requests.Create a custom OAuth application from your Google G Suit account to enable OAuth 2.0 authentication with the Google Directory spoke.Add the Google Directory connection in Workflow Studio to configure the Google Directory spoke.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Google Directory Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Google Directory spoke

Integrate the ServiceNow instance and Google Directory spoke by using G Suite credentials to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Google Directory spoke.
-   Role required: admin.

## Configure the Google Directory application

Create a custom OAuth application from your Google G Suit account to enable OAuth 2.0 authentication with the Google Directory spoke.

### Before you begin

Google Directory integration requirements:

-   A domain and an email address associated with the domain. For example, www.mydomain.com and jane-admin@mydomain.com. Note that you can only register one email address per domain in G Suite.
-   A Google G Suite or login created with the domain.

Role required: admin.

### About this task

Complete these steps from the [Google Developers Console](https://console.developers.google.com/). See the G Suite product documentation for instructions on creating and configuring custom applications.

### Procedure

1.  Register a new custom application and open it.

    1.  Navigate to [https://console.developers.google.com](https://console.developers.google.com).

    2.  Create a project with your G Suite administrator credentials.

    3.  Open the project.

2.  Provide the OAuth authorized domain name.

    1.  From the APIs &amp; Services menu, select **OAuth consent screen**.

    2.  Enter the application name.

    3.  Specify the Authorized domain `service-now.com`.

    4.  Click **Save**.

3.  Create the credentials.

    1.  From the APIs &amp; Services menu, select **Credentials**.

    2.  Select **Create OAuth client ID** from the **Create credentials** list.

4.  Select the application type **Web application**.

5.  Enter the following Authorized redirect URI: `https://<instance>.service-now.com/oauth_redirect.do` and click **Create**.

    The OAuth client window shows your client ID and client secret.

6.  Copy these two values to a text file so that you can use them when you add the Google Directory connection in ServiceNow instance.

    **Tip:** You can always access the client ID and secret in the Google APIs &amp; Services interface by clicking **Credentials** and selecting the OAuth 2.0 client ID name.


## Add Google Directory connection in ServiceNow instance

Add the Google Directory connection in Workflow Studio to configure the Google Directory spoke.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click the **Connections** tab.

3.  Toggle and enable the **Outbound** connections.

4.  Locate the **Google Directory** connection alias and click **View Details**.

    -   To configure the default connection and credential alias record that is shipped along with the Google Directory spoke, click **View Details**.
    -   To manage more than one Google Directory spoke connection records, you should create a new child alias record by clicking **Add Connection**. For more information about using multiple connections, see [Supporting multiple connections](../../integrationhub/concept/support-multiple-connections.md).
    If you are configuring the spoke for the first time, click **Configure**. Otherwise, click **Edit**.

5.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Connection URL|URL to connect to Google Directory. Enter `https://googleapis.com`.|
    |Credential Name|Name to identify the credential record. For example, `Google Directory Cred`.|
    |OAuth Name|Name to identify the OAuth record. For example, `Google_Directory OAuth`.|
    |OAuth Client ID|Client ID of your Google app.|
    |OAuth Client Secret|Client Secret of your Google app.|
    |OAuth Redirect URL|Redirect URL provided in your Google app. This value is auto-populated.|
    |OAuth Authorization URL|OAuth authorization code endpoint. Enter `https://accounts.google.com/o/oauth2/v2/auth`.|
    |OAuth Token URL|Token URL. Enter `https://oauth2.googleapis.com/token`.|

    ![Configure Google Directory connection.](../image/gdirectory-conf-temp.png)

6.  Click **Configure and Get OAuth Token**.

7.  In the pop-up window, click **Allow**.

    The OAuth Access token is generated for the Google Directory spoke.


