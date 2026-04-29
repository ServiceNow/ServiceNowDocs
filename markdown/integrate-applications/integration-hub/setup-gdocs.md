---
title: Set up the Google Docs
description: Integrate the ServiceNow instance and Google Docs by creating a custom OAuth application in G Suite credentials to authenticate ServiceNow requests.Create a custom OAuth application from your G Suite account to enable OAuth 2.0 authentication with the Google Docs spoke.Add and configure a Google Docs connection to authenticate ServiceNow requests in Google Docs spoke.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Google Docs Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Google Docs

Integrate the ServiceNow instance and Google Docs by creating a custom OAuth application in G Suite credentials to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Google Docs spoke.
-   Role required: admin.

## Configure Google Docs application

Create a custom OAuth application from your G Suite account to enable OAuth 2.0 authentication with the Google Docs spoke.

### Before you begin

-   A Google G Suite or login created with the domain
-   Role required: admin

### About this task

Complete these steps from your Google G Suite account. See the G Suite product documentation for instructions on creating and configuring custom applications.

### Procedure

1.  Register a new custom application.

    1.  Navigate to [https://console.developers.google.com](https://console.developers.google.com).

    2.  Create a project with your G Suite administrator credentials.

    3.  Open the project.

2.  Set the Authorized domain.

    1.  From the **APIs &amp; Services** menu, select **OAuth consent screen**.

    2.  Enter the application name.

    3.  Specify the Authorized domain `service-now.com`.

    4.  Click **Save**.

3.  Search for the Google Docs API and enable it.

4.  Create the OAuyth client ID.

    1.  From the APIs &amp; Services menu, select **Credentials**.

    2.  Select **Create OAuth client ID** from the **Create credentials** list.

5.  Select the application type **Web application**.

6.  Enter the following Authorized redirect URI: `https://<instance>.service-now.com/oauth_redirect.do` and click **Create**.

    This redirect URI must match the **Redirect URL** you provide when you configure a connection for the Google Docs spoke.

7.  The OAuth client window shows your client ID and client secret.

    Copy these two values to a text file so that you can use them when you configure a connection for the Google Docs spoke.

    **Tip:**

    You can always access the client ID and secret in the Google APIs &amp; Services interface by clicking **Credentials** and select the OAuth 2.0 client ID name.


## Configure a connection for the Google Docs spoke

Add and configure a Google Docs connection to authenticate ServiceNow requests in Google Docs spoke.

### Before you begin

-   [Configure Google Docs application](setup-gdocs.md#)
-   Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Select the **Integrations** tab.

3.  Select the **Connections** tab.

4.  In the Search all connections field, enter `Google Docs`.

5.  On the Google Docs card, select **View Details**.

    ![View Details button on Google Docs alias card.](../image/google-docs-alias-view-details.png)

6.  Select **Configure**.

    ![Button to open the Google Docs alias connection.](../image/google-docs-conn-config-button.png)

7.  On the **Connection** form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Connection Name|Name to uniquely identify the connection record. For example, `Google Docs Connection`.|
    |Connection URL|Connection URL for the spoke. Enter `https://www.googleapis.com/`|
    |OAuth Entity Name|Name to identify the OAuth entity record. For example, `Google Docs entity`.|
    |OAuth Client ID|Client ID generated while creating the application in G suite.|
    |OAuth Client Secret|Client secret generated while creating the application in G suite.|
    |OAuth Redirect URL|Redirect URL of your ServiceNow instance in this format: `https://<instance_name>.service-now.com/oauth_redirect.do` .|

8.  Click **Configure and Get OAuth Token**.

    ![Google Docs connection form.](../image/google-docs-conn-form.png)

9.  Log in to Google to get the OAuth token.


### Result

The spoke connection is configured and ready to be used.

