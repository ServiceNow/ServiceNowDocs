---
title: Set up the Google Identity and Access Spoke
description: Integrate the ServiceNow instance and Google Identity and Access spoke by using Google Cloud Platform credentials to authenticate ServiceNow requests.Create a custom OAuth application from your Google Cloud Platform account to enable OAuth 2.0 authentication with the Google Identity and Access spoke.Use the information generated during Google Identity and Access account configuration to register the Google Identity and Access application as an OAuth provider and allow the instance to request OAuth 2.0 tokens.Create Credential records to connect the Google Identity and Access custom OAuth application you created during account configuration. The Google Identity and Access spoke connection and credential aliases use these credentials to authorize actions.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Google Identity and Access Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Set up the Google Identity and Access Spoke

Integrate the ServiceNow instance and Google Identity and Access spoke by using Google Cloud Platform credentials to authenticate ServiceNow requests.

## Before you begin

-   Request Integration Hub subscription
-   Activate the Google Identity and Access spoke
-   Role required: admin

## Configure the Google Identity and Access application

Create a custom OAuth application from your Google Cloud Platform account to enable OAuth 2.0 authentication with the Google Identity and Access spoke.

### Before you begin

Google Identity and Access integration requirements:

-   Google Cloud Platform account.
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

6.  Copy your client ID and client secret to a text file so that you can use them when you Register Google Identity and Access as an OAuth provider.

    **Tip:** You can always access the client ID and secret in the Google APIs &amp; Services interface by clicking **Credentials** and selecting the OAuth 2.0 client ID name.


## Register Google Identity and Access as an OAuth provider

Use the information generated during Google Identity and Access account configuration to register the Google Identity and Access application as an OAuth provider and allow the instance to request OAuth 2.0 tokens.

### Before you begin

Role required: admin

### Procedure

1.  In ServiceNow instance, navigate to **System OAuth** &gt; **Application Registry**.

2.  Open the record, **Google cloud platform**.

3.  On the form, fill these fields:

    |Field|Description|
    |-----|-----------|
    |Name|Name to uniquely identify the record, for example `Google Identity and Access`.|
    |Client ID|Client ID of the Google Identity and Access application.|
    |Client Secret|Client Secret you generated when you create the application.|
    |OAuth API Script|Script to customize the request and response. Select `OAuthGoogleIAMUtil`.|
    |Default Grant type|Grant type used to establish the token. Select **Authorization Code**.|
    |Authorization URL|OAuth authorization code endpoint. Enter `https://accounts.google.com/o/oauth2/v2/auth`.|
    |Token URL|OAuth server token endpoint. Enter `https://oauth2.googleapis.com/token`.|
    |Redirect URL|URL of the ServiceNow instance in this format: `https://<instance>.service-now.com/oauth_redirect.do`.|

4.  Right-click the form header, and click **Save**.

    The system validates the OAuth credentials.


## Create Credential record for the Google Identity and Access spoke

Create Credential records to connect the Google Identity and Access custom OAuth application you created during account configuration. The Google Identity and Access spoke connection and credential aliases use these credentials to authorize actions.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **IntegrationHub** &gt; **Connections &amp; Credentials** &gt; **Credentials** and click **New**.

2.  Select OAuth 2.0 Credentials.

3.  Enter a unique name for the credential, for example, `GCPIAM Cred`.

4.  Click the **OAuth Entity Profile** search icon \(![Search icon](../image/SearchIcon.png)\) and select the profile with the name of the OAuth application registry you created when you registered the Google Identity and Access service as an OAuth provider.

5.  Click **Get Oauth Token**.


