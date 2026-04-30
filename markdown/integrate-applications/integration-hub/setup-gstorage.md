---
title: Set up the Google Cloud Storage spoke
description: Integrate the ServiceNow instance and Google Cloud Storage spoke by using G Suite credentials to authenticate ServiceNow requests.Create a custom OAuth application from your Google Cloud Platform account to enable OAuth 2.0 authentication with the Google Cloud Storage spoke.Use the information generated during Google Cloud Storage account configuration to register the Google Cloud Storage application as an OAuth provider and allow the instance to request OAuth 2.0 tokens.Create a credential record to connect the Google Cloud Storage custom OAuth application you created during account configuration. The Google Cloud Storage spoke connection and credential aliases use these credentials to authorize actions.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Google Cloud Storage Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Set up the Google Cloud Storage spoke

Integrate the ServiceNow instance and Google Cloud Storage spoke by using G Suite credentials to authenticate ServiceNow requests.

## Before you begin

-   Request Integration Hub subscription.
-   Activate the Google Cloud Storage spoke.
-   Access to Google Cloud Platform.
-   Role required: admin.

## Configure the Google Cloud Storage application

Create a custom OAuth application from your Google Cloud Platform account to enable OAuth 2.0 authentication with the Google Cloud Storage spoke.

### Before you begin

Role required: admin.

### About this task

Complete these steps from the [Google Cloud Platform](https://cloud.google.com/). See the [Google Cloud Platform](https://cloud.google.com/docs) product documentation for instructions on creating and configuring custom applications.

### Procedure

1.  Register a new custom application and open it.

    1.  Navigate to [https://console.cloud.google.com](https://console.developers.google.com).

    2.  Create a project with your administrator credentials.

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

6.  Copy your client ID and client secret to a text file so that you can use them when you [Register Google Cloud Storage as an OAuth provider](setup-gstorage.md#).

    **Tip:** You can always access the client ID and secret in the Google APIs &amp; Services interface by clicking **Credentials** and selecting the OAuth 2.0 client ID name.


## Register Google Cloud Storage as an OAuth provider

Use the information generated during Google Cloud Storage account configuration to register the Google Cloud Storage application as an OAuth provider and allow the instance to request OAuth 2.0 tokens.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **System OAuth** &gt; **Application Registry**.

2.  Open for the record, **Google Cloud Storage**.

3.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Client ID|Client ID of the Google Cloud Storage application.|
    |Client Secret|Client Secret of the Google Cloud Storage application.|
    |OAuth API Script|**OAuthGoogleCloudStorageUtils** is selected by default.|
    |Authorization URL|The OAuth authorization code endpoint: `https://accounts.google.com/o/oauth2/auth`.|
    |Token URL|The OAuth server token endpoint: `https://oauth2.googleapis.com/token`.|
    |Redirect URL|OAuth callback endpoint in this format: `https://<instance>.service-now.com/oauth_redirect.do`. If left blank, the instance auto-generates the URL.|

4.  Right-click the form header, and click **Save**.


## Create a credential for the Google Cloud Storage spoke

Create a credential record to connect the Google Cloud Storage custom OAuth application you created during account configuration. The Google Cloud Storage spoke connection and credential aliases use these credentials to authorize actions.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Integration Hub** &gt; **Connections &amp; Credentials**.

2.  Open the record, **Google\_Cloud\_Storage**.

3.  In the **Credentials** tab, click **New**.

    The system displays this message: `What type of Credentials would you like to create?`

4.  Select **OAuth 2.0 Credentials**.

5.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Name|Name to identify the credential record. For example, `Google Cloud Storage Cred`.|
    |OAuth Entity Profile|Select the default OAuth entity profile, **GCP Cloud Storage default\_profile**.|
    |Credential alias|Credential alias associated with this record. The default alias record, **sn\_gcp\_cs\_spoke.Google\_Cloud\_Storage** is selected.|

    ![Credential record for the Google Cloud Storage spoke.](../image/gcloud-storage-cred.png)

6.  Right-click the form header and click **Save**.

7.  To generate the OAuth token, click the **Get OAuth Token** related link.


