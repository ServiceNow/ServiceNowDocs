---
title: Set up the Google Cloud DNS spoke
description: Integrate the ServiceNow instance and Google Cloud DNS account by creating a custom OAuth application in Google Cloud Platform to authenticate ServiceNow requests.Create a custom OAuth application in your Google Cloud Platform account to enable OAuth 2.0 authentication with the Google Cloud DNS spoke.Use the information generated during the Google Cloud DNS application configuration to register Google Cloud DNS as an OAuth provider and allow the ServiceNow instance to request OAuth 2.0 tokens.Create a default credential record for the Google Cloud DNS application. The Google Cloud DNS spoke connection and credential alias uses this credential to authorize actions.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Google Cloud DNS Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Set up the Google Cloud DNS spoke

Integrate the ServiceNow instance and Google Cloud DNS account by creating a custom OAuth application in Google Cloud Platform to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate Google Cloud DNS spoke.
-   Role required: admin

## Create a custom application

Create a custom OAuth application in your Google Cloud Platform account to enable OAuth 2.0 authentication with the Google Cloud DNS spoke.

### Before you begin

Role required: admin.

### About this task

Complete these steps from the [Google Cloud Platform](https://cloud.google.com/). See the [Google Cloud Platform](https://cloud.google.com/docs) product documentation for instructions on creating and configuring custom applications.

### Procedure

1.  Register a new custom application by navigating to [https://console.cloud.google.com/](https://console.cloud.google.com/).

2.  Create a project with your administrator credentials, and open the project.

3.  From the APIs &amp; Services menu, select **OAuth consent screen**, enter the application name, and specify the Authorized domain `service-now.com`.

4.  Click **Save**.

5.  From the APIs &amp; Services menu, select **Credentials**, and select **Create OAuth client ID** from the **Create credentials** list.

6.  Select the application type **OAuth client ID**.

7.  Enter the following **Authorized redirect URI**: `https://<instance>.service-now.com/oauth_redirect.do` and click **Create**.

    The OAuth client window shows your client ID and client secret.

8.  Copy these two values to a text file so that you can use them when you [Register Google Cloud DNS as an OAuth provider](setup-gcloud-dns.md#).

    The client ID and secret can always be accessed in the Google APIs &amp; Services interface. Click **Credentials** and select the OAuth 2.0 client ID name.


## Register Google Cloud DNS as an OAuth provider

Use the information generated during the Google Cloud DNS application configuration to register Google Cloud DNS as an OAuth provider and allow the ServiceNow instance to request OAuth 2.0 tokens.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **System OAuth** &gt; **Application Registry**.

2.  Open for the record, **Google Cloud DNS**.

3.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Client ID|Client ID of the Google Cloud DNS application.|
    |Client Secret|Client Secret of the Google Cloud DNS application.|
    |OAuth API Script|**OAuthGoogleCloudDNSUtils** is selected by default.|
    |Authorization URL|The OAuth authorization code endpoint: `https://accounts.google.com/o/oauth2/auth`.|
    |Token URL|The OAuth server token endpoint: `https://oauth2.googleapis.com/token`.|
    |Redirect URL|OAuth callback endpoint in this format: `https://<instance>.service-now.com/oauth_redirect.do`. If left blank, the instance auto-generates the URL.|

4.  Right-click the form header, and click **Save**.


## Create a credential record for the Google Cloud DNS spoke

Create a default credential record for the Google Cloud DNS application. The Google Cloud DNS spoke connection and credential alias uses this credential to authorize actions.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Integration Hub** &gt; **Connections &amp; Credentials**.

2.  Open the record, **GoogleCloudDNS**.

3.  In the **Credentials** tab, click **New**.

    The system displays this message: `What type of Credentials would you like to create?`

4.  Select **OAuth 2.0 Credentials**.

5.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Name|Name to identify the credential record. For example, `Google Cloud DNS Cred`.|
    |OAuth Entity Profile|Select the default OAuth entity profile, **Google Cloud DNS default\_profile**.|
    |Credential alias|Credential alias associated with this record. The default alias record, **sn\_gcp\_dns\_spoke.GoogleCloudDNS** is selected.|

    ![Credential record for the Google Cloud DNS spoke.](../image/gcloud-dns-cred.png)

6.  Right-click the form header and click **Save**.

7.  To generate the OAuth token, click the **Get OAuth Token** related link.


