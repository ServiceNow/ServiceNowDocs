---
title: Set up the Google Chat spoke
description: Integrate the ServiceNow instance and Google Chat by creating a custom OAuth application in Google Cloud console to authenticate ServiceNow requests.Create credentials in Google Cloud console account to enable OAuth 2.0 authentication with the Google Chat spoke.Add and configure a Docker connection to authenticate ServiceNow requests in Docker spoke.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Google Chat spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Google Chat spoke

Integrate the ServiceNow instance and Google Chat by creating a custom OAuth application in Google Cloud console to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Google Chat spoke.
-   Role required: admin.

## Create OAuth credentials in Google Cloud console for Google Chat spoke

Create credentials in Google Cloud console account to enable OAuth 2.0 authentication with the Google Chat spoke.

### About this task

Complete these steps from the [Google Cloud console](https://console.cloud.google.com/).

### Before you begin

-   Create a Google Chat application. For more information, see [Develop Google Chat apps](https://developers.google.com/workspace/chat) and [Google Apps Script Chat app quickstart](https://developers.google.com/apps-script/quickstart/chat-app).
-   Role required: none

### Procedure

1.  In the Google Cloud console, navigate to **Main menu** &gt; **IAM &amp; Admin** &gt; **Create a Project**.

    You can also directly go to [https://console.cloud.google.com/projectcreate](https://console.cloud.google.com/projectcreate)

2.  Enter a descriptive name for your project in the **Project Name** field.

    **Note:** The project ID can't be changed after the project is created, so choose an ID that meets your needs for the lifetime of the project.

3.  After creating a Google Chat app, get the deployment ID of the app and record it.

    You need to provide the deployment ID for connection configuration. For more information, see [Find a deployment ID](https://developers.google.com/apps-script/concepts/deployments#find-deployment).

4.  Navigate to **Navigation Menu** &gt; **APIs &amp; Services** &gt; **Enabled APIs &amp; Services**.

5.  Select **Google Chat API** from the list.

    ![Select Google Chat API in Google Cloud console](../image/google-chat-spoke-select-chat-apis.png)

6.  Click on the **CREDENTIALS** tab.

7.  Click on **+ CREATE CREDENTIALS** and select **OAuth client ID.**

    ![Create credentials for Google Chat app in Google Cloud console](../image/google-chat-gc-console-create-creds.png)

8.  On the **Create OAuth client ID** form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Application|Select Web application from the list.|
    |Name|Enter a unique name to identify the OAuth 2.0 client.|
    |Authorized JavaScript origins URI|Enter the URI of your ServiceNow instance. For example, `https://<your-instance-name>.servicen-now.com`|
    |Authorized redirect URIs|Enter the redirect URI of your ServiceNow instance. For example, `https://<your-instance-name>.servicen-now.com/oauth_redirect.do`|

    ![Create OAuth client ID for Google Chat spoke in Google Cloud console](../image/google-chat-gc-create-oauth-cl-id.png)

9.  Click **CREATE**.

    An OAuth client is created with client ID and client secret. Record the client ID and client secret.

10. Click on the **CONFIGURATION** tab and fill in the fields.

    |Field|Description|
    |-----|-----------|
    |App name|Enter a name for your application.|
    |Avatar URL|Specify an HTTPS URL for your app's avatar image.|
    |Description|Enter a description for your application.|

11. In **Connection** settings, specify the deployment ID of the Google Chat app from Step 4 in the **Deployment ID** field.

    **Note:** If you have created any Slash commands while creating the app, specify them.

    ![Add deployment ID of the app in Connection settings](../image/google-chat-deployment-id.png)

12. Save the configuration of your app in Google Cloud console.


## Configure a connection for Google Chat spoke

Add and configure a Docker connection to authenticate ServiceNow requests in Docker spoke.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Click the **Connections** tab.

3.  Locate the alias for **Google\_Chat** and and click **View Details**.

    **Note:** Don't click**Add Connection**.

    ![Google Chat spoke connection template](../image/google-chat-spoke-conn-temp.png)

4.  Click **Configure** if you are configuring the connection for the first time.

    ![Google Chat spoke connection configuration](../image/google-chat-spoke-conn-config.png)

5.  On the **Configure Connection** form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Connection Name|Name to uniquely identify the connection record.|
    |Connection URL|URL to Google Chat APIs. Enter `https://chat.googleapis.com`|
    |API Version|Google Chat API version. Enter `v1`.|
    |OAuth Client ID|OAuth client ID of Google Chat app in Google Cloud console.|
    |OAuth Client Secret|OAuth client secret of Google Chat app in Google Cloud console.|
    |OAuth Redirect URL|OAuth redirect URL of your ServiceNow instance. Enter in this format`https://<your-instance-name>.service-now.com/oauth_redirect.do`|

6.  Click **Configure and Get OAuth Token**.

    You will be redirected to Google accounts login page.

7.  Enter your Google Chat API credentials.


### Result

An OAuth token is generated and configured for the Google Chat spoke.

