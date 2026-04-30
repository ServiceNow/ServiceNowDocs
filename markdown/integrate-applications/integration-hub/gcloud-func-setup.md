---
title: Set up the Google Cloud Functions spoke
description: Integrate the ServiceNow instance and Google Cloud Functions account by creating a custom OAuth application in Google Cloud Platform to authenticate ServiceNow requests.Create a custom OAuth application in your Google Cloud Platform account to enable OAuth 2.0 authentication with the Google Cloud Functions spoke.Use the information generated during the Google Cloud Functions application configuration to register Google Cloud Functions as an OAuth provider and allow the ServiceNow instance to request OAuth 2.0 tokens.Create a credential record for the Google Cloud Functions application. The Google Cloud Functions spoke connection and credential alias uses these credentials to authorize actions.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Google Cloud Functions Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Google Cloud Functions spoke

Integrate the ServiceNow instance and Google Cloud Functions account by creating a custom OAuth application in Google Cloud Platform to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Google Cloud Functions spoke.
-   Role required: admin.

## Configure the Google Cloud Functions application

Create a custom OAuth application in your Google Cloud Platform account to enable OAuth 2.0 authentication with the Google Cloud Functions spoke.

### About this task

Complete these steps from the [Google Cloud Platform](https://cloud.google.com/). See the [Google Cloud Platform](https://cloud.google.com/docs) product documentation for instructions on creating and configuring custom applications.

### Procedure

1.  Register a new custom application by navigating to [https://console.cloud.google.com/](https://console.cloud.google.com/) and creating a project with your administrator credentials.

2.  Open your new project and, in the APIs &amp; Services menu, select **OAuth consent screen**.

3.  Enter the application name, specify the Authorized domain `service-now.com`, and select **Save**.

4.  From the APIs &amp; Services menu, select **Credentials**, and select **Create OAuth client ID** from the **Create credentials** list.

5.  Select the application type **OAuth client ID**.

6.  Enter the following **Authorized redirect URI**: `https://<instance>.service-now.com/oauth_redirect.do` and select **Create**.

7.  Copy your client ID and client secret from the OAuth client window to a text file so that you can use them when you [Register Google Cloud Functions as an OAuth provider](gcloud-func-setup.md#).

    The client ID and secret can be accessed in the Google APIs &amp; Services interface. Select **Credentials** and select the OAuth 2.0 client ID name.


## Register Google Cloud Functions as an OAuth provider

Use the information generated during the Google Cloud Functions application configuration to register Google Cloud Functions as an OAuth provider and allow the ServiceNow instance to request OAuth 2.0 tokens.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

2.  Open for the record, **Google Cloud Functions**.

3.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Client ID|Client ID of the Google Cloud Functions application.|
    |Client Secret|Client Secret of the Google Cloud Functions application.|
    |OAuth API Script|**OauthGoogleCloudFunctionsUtils** is selected by default.|
    |Authorization URL|The OAuth authorization code endpoint: `https://accounts.google.com/o/oauth2/auth`.|
    |Token URL|The OAuth server token endpoint: `https://oauth2.googleapis.com/token`.|
    |Redirect URL|OAuth callback endpoint in this format: `https://<instance>.service-now.com/oauth_redirect.do`. If left blank, the instance auto-generates the URL.|

4.  Right-click the form header, and click **Save**.


## Create a credential record for the Google Cloud Functions spoke

Create a credential record for the Google Cloud Functions application. The Google Cloud Functions spoke connection and credential alias uses these credentials to authorize actions.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Integration Hub** &gt; **Connections &amp; Credentials**.

2.  Open the record, **GoogleCloudFunctions**.

3.  In the **Credentials** tab, click **New**.

    The system displays this message: `What type of Credentials would you like to create?`

4.  Select **OAuth 2.0 Credentials**.

5.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Name|Name to identify the credential record. For example, `Google Cloud Functions Cred`.|
    |OAuth Entity Profile|Select the default OAuth entity profile, **Google Cloud Functions default\_profile**.|
    |Credential alias|Credential alias associated with this record. The default alias record, **sn\_gcp\_cf\_spoke.GoogleCloudFunctions** is selected.|

    ![Credential record for Google Cloud Functional spoke.](../image/gcloud-func-cred.png)

6.  Right-click the form header and click **Save**.

7.  To generate the OAuth token, click the **Get OAuth Token** related link.


