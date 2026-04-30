---
title: Set up the YouTube spoke
description: Integrate the ServiceNow instance and YouTube account by creating a custom OAuth application in Google Cloud Platform to authenticate ServiceNow requests.Create a custom OAuth application in your Google Cloud Platform account to enable OAuth 2.0 authentication with the YouTube spoke.Use the information generated during the YouTube application configuration to register YouTube as an OAuth provider and allow the ServiceNow instance to request OAuth 2.0 tokens.Create a credential record for the YouTube application. The YouTube spoke connection and credential alias uses these credentials to authorize actions.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [YouTube Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Set up the YouTube spoke

Integrate the ServiceNow instance and YouTube account by creating a custom OAuth application in Google Cloud Platform to authenticate ServiceNow requests.

## Before you begin

-   Request Integration Hub subscription.
-   Activate YouTube spoke.
-   Role required: admin

## Configure the YouTube application

Create a custom OAuth application in your Google Cloud Platform account to enable OAuth 2.0 authentication with the YouTube spoke.

### Before you begin

Role required: admin.

### About this task

Complete the [Create a Google Cloud project](https://developers.google.com/workspace/guides/create-project) steps from the [Google Cloud Platform](https://cloud.google.com/). See the [Creating and managing projects](https://cloud.google.com/resource-manager/docs/creating-managing-projects) product documentation for instructions on creating and configuring custom applications.

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

4.  Select the application type **OAuth client ID**.

5.  Enter the following **Authorized redirect URI**: `https://<instance>.service-now.com/oauth_redirect.do` and click **Create**.

6.  Copy your client ID and client secret to a text file so that you can use them when you [Register YouTube as an OAuth provider](youtube-setup.md#).

    **Tip:** You can always access the client ID and secret in the Google APIs &amp; Services interface by clicking **Credentials** and selecting the OAuth 2.0 client ID name.


## Register YouTube as an OAuth provider

Use the information generated during the YouTube application configuration to register YouTube as an OAuth provider and allow the ServiceNow instance to request OAuth 2.0 tokens.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

2.  Open for the record, **Youtube**.

3.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Client ID|Client ID of the YouTube application.|
    |Client Secret|Client Secret of the YouTube application.|
    |Redirect URL|OAuth callback endpoint in this format: `https://<instance>.service-now.com/oauth_redirect.do`.|

4.  Ensure that these scopes are available in the **OAuth Entity Scopes** tab.

    |Name|OAuth scope|
    |----|-----------|
    |YouTube Partner|`https://www.googleapis.com/auth/youtubepartner`|
    |YouTube Reporting S1|`https://www.googleapis.com/auth/yt-analytics.readonly`|
    |YouTube Reporting S2|`https://www.googleapis.com/auth/yt-analytics-monetary.readonly`|
    |YouTube Scope|`https://www.googleapis.com/auth/youtube`|
    |YouTube Scope Force SSL|`https://www.googleapis.com/auth/youtube.force-ssl`|

5.  Right-click the form header, and click **Save**.


## Create a credential record for the YouTube spoke

Create a credential record for the YouTube application. The YouTube spoke connection and credential alias uses these credentials to authorize actions.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connections &amp; Credential Aliases**.

2.  Open record for the YouTube spoke, for example, `YouTube`.

3.  In the **Credentials** tab, click **New**.

4.  Select **OAuth 2.0 Credentials**.

5.  Enter a unique name for the credential, for example, `Youtube_Cred`.

6.  Click the **OAuth Entity Profile** search icon \(![Search icon](../image/SearchIcon.png)\) and select the profile with the name of the OAuth application registry you configured when you registered the YouTube service as an OAuth provider.

    See [Register YouTube as an OAuth provider](youtube-setup.md#) for more information.

7.  Right-click the form header and click **Save**.

8.  Click **Get OAuth Token**.


