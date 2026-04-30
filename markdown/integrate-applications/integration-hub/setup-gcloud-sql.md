---
title: Set up the Google Cloud SQL spoke
description: Integrate the ServiceNow instance and Google Cloud SQL spoke using Google Cloud Platform credentials to authenticate ServiceNow requests.Create a custom OAuth application from your Google Cloud Platform account to enable OAuth 2.0 authentication with the Google Cloud SQL spoke.Use the information generated during Google Cloud SQL account configuration to register the Google Cloud SQL application as an OAuth provider and allow the instance to request OAuth 2.0 tokens.Create a credential record to connect the Google Cloud custom application you created during account configuration. The Google Cloud SQL spoke connection and credential aliases use these credentials to authorize actions.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Google Cloud SQL Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Set up the Google Cloud SQL spoke

Integrate the ServiceNow instance and Google Cloud SQL spoke using Google Cloud Platform credentials to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Google Cloud SQL spoke.
-   Role required: admin.

## Configure the Google Cloud SQL application

Create a custom OAuth application from your Google Cloud Platform account to enable OAuth 2.0 authentication with the Google Cloud SQL spoke.

### Before you begin

Google Identity and Access integration requirements:

-   Google Cloud SQL account.
-   Role required: admin.

### About this task

Complete these steps from the Google Cloud Platform.

### Procedure

1.  Register a new custom application and open it.

    1.  Navigate to [https://console.developers.google.com](https://console.developers.google.com).

    2.  Create a project with your Google Cloud Platform administrator credentials.

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

6.  Copy your client ID and client secret to a text file so that you can use them when you register Google Cloud SQL as an OAuth provider.

    **Tip:** You can always access the client ID and secret in the Google APIs &amp; Services interface by clicking **Credentials** and selecting the OAuth 2.0 client ID name.


## Register Google Cloud SQL as an OAuth provider

Use the information generated during Google Cloud SQL account configuration to register the Google Cloud SQL application as an OAuth provider and allow the instance to request OAuth 2.0 tokens.

### Before you begin

Role required: admin

### Procedure

1.  In ServiceNow instance, navigate to **System OAuth** &gt; **Application Registry**.

2.  Open the record, **Google Cloud SQL**.

3.  On the form, fill these fields:

    |Field|Description|
    |-----|-----------|
    |Client ID|Client ID of the Google Cloud SQL application.|
    |Client Secret|Client Secret you generated when you create the application.|
    |OAuth API Script|Script to customize the request and response. Select `OAuthGCPSQLUtil`.|
    |Default Grant type|Grant type used to establish the token. Select **Authorization Code**.|
    |Authorization URL|OAuth authorization code endpoint. Enter `https://accounts.google.com/o/oauth2/v2/auth`.|
    |Token URL|OAuth server token endpoint. Enter `https://oauth2.googleapis.com/token`.|
    |Redirect URL|URL of the ServiceNow instance in this format: `https://<instance>.service-now.com/oauth_redirect.do`.|

4.  Right-click the form header, and click **Save**.

    The system validates the OAuth credentials.


## Create a credential record for the Google Cloud SQL spoke

Create a credential record to connect the Google Cloud custom application you created during account configuration. The Google Cloud SQL spoke connection and credential aliases use these credentials to authorize actions.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Integration Hub** &gt; **Connections &amp; Credentials**.

2.  Open the record, **Google\_Cloud\_SQL**.

3.  In the **Credentials** tab, click **New**.

    The system displays this message: `What type of Credentials would you like to create?`

4.  Select **OAuth 2.0 Credentials**.

5.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Name|Name to identify the credential record. For example, `Google Cloud SQL Cred`.|
    |OAuth Entity Profile|Select the default OAuth entity profile, **Google Cloud SQL**.|
    |Credential alias|Credential alias associated with this record. The default alias record, **sn\_gcpcloudsql\_spk.Google\_Cloud\_SQL** is selected.|

    ![Credential record for Google Cloud SQL spoke.](../image/gcloud-sql-cred.png)

6.  Right-click the form header and click **Save**.

7.  To generate the OAuth token, click the **Get OAuth Token** related link.


