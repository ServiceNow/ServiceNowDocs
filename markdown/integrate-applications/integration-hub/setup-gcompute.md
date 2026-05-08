---
title: Set up the Google Compute Engine spoke
description: Integrate the ServiceNow instance and Google Compute Engine spoke by using OAuth 2.0 credentials to authenticate ServiceNow requests.Create a custom OAuth application from your Google Cloud Platform account to enable OAuth 2.0 authentication with the Google Compute Engine spoke.Use the information generated during Google Compute Engine account configuration to register the Google Compute Engine application as an OAuth provider and allow the instance to request OAuth 2.0 tokens.Create a credential record to connect the Google Compute Engine custom OAuth application you created during account configuration. The Google Compute Engine spoke connection and credential aliases use these credentials to authorize actions.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Google Compute Engine Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Google Compute Engine spoke

Integrate the ServiceNow instance and Google Compute Engine spoke by using OAuth 2.0 credentials to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Google Compute Engine spoke.
-   Access to Google Cloud Platform.
-   Role required: admin.

**Note:** This procedure outlines steps to configure the custom app using OAuth. You can also configure the custom app using Service Account associated with JWT tokens. For more information about setting up the spoke using JWT tokens, see [Choosing an Authentication Method - Service accounts](https://cloud.google.com/endpoints/docs/openapi/authentication-method#service_accounts) and Set up OAuth provider with JWT Bearer grant type.

## Configure the Google Compute Engine application

Create a custom OAuth application from your Google Cloud Platform account to enable OAuth 2.0 authentication with the Google Compute Engine spoke.

### Before you begin

Role required: admin.

### About this task

Complete these steps from the [Google Cloud Platform](https://cloud.google.com/). See the [Google Cloud Platform](https://cloud.google.com/docs) product documentation for instructions on creating and configuring custom applications.

### Procedure

1.  Register a new custom application and open it.

    1.  Navigate to [https://console.developers.google.com](https://console.developers.google.com).

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

6.  Copy your client ID and client secret to a text file so that you can use them when you [Register Google Compute Engine as an OAuth provider](setup-gcompute.md#).

    **Tip:** You can always access the client ID and secret in the Google APIs &amp; Services interface by clicking **Credentials** and selecting the OAuth 2.0 client ID name.


## Register Google Compute Engine as an OAuth provider

Use the information generated during Google Compute Engine account configuration to register the Google Compute Engine application as an OAuth provider and allow the instance to request OAuth 2.0 tokens.

### Before you begin

Role required: admin

### Procedure

1.  In ServiceNow, navigate to **System OAuth** &gt; **Application Registry**.

2.  Open the record for **Google Compute Engine**.

3.  Fill these values in the Application Registries form:

    |Field|Value required|
    |-----|--------------|
    |Name|Name to uniquely identify the record, for example `Google Compute Engine`.|
    |Client ID|Client ID of the Google Compute Engine application you created in G Suite.|
    |Client Secret|Client Secret you generated when you created the application in G Suite.|
    |OAuth API Script|Script to customize the request and response. Select `OAuthGoogleComputeUtil`|
    |Default Grant type|Grant type used to establish the token. Select **Authorization Code**.|
    |Authorization URL|OAuth authorization code endpoint. Enter `https://accounts.google.com/o/oauth2/v2/auth`.|
    |Token URL|OAuth server token endpoint. Enter `https://oauth2.googleapis.com/token`.|
    |Redirect URL|URL of the ServiceNow instance in this format: `https://<instance>.service-now.com/oauth_redirect.do`.|

4.  Right-click the form header, and click **Save**.

    The system validates the OAuth credentials.


## Create a credential record for the Google Compute Engine spoke

Create a credential record to connect the Google Compute Engine custom OAuth application you created during account configuration. The Google Compute Engine spoke connection and credential aliases use these credentials to authorize actions.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Integration Hub** &gt; **Connections &amp; Credentials**.

2.  Open the record, **GoogleCloudCompute**.

3.  In the **Credentials** tab, click **New**.

    The system displays this message: `What type of Credentials would you like to create?`

4.  Select **OAuth 2.0 Credentials**.

5.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Name|Name to identify the credential record. For example, `Google Cloud Compute Cred`.|
    |OAuth Entity Profile|Select the default OAuth entity profile, **Google Compute default\_profile**.|
    |Credential alias|Credential alias associated with this record. The default alias record, **sn\_gcompute\_spoke.GoogleCloudCompute** is selected.|

    ![Credential record for the Google Cloud Compute Engine spoke.](../image/gcloud-comp-eng.png)

6.  Right-click the form header and click **Save**.

7.  To generate the OAuth token, click the **Get OAuth Token** related link.


