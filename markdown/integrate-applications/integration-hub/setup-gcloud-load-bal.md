---
title: Set up the Google Cloud Load Balancer Spoke
description: Integrate the ServiceNow instance and Google Cloud Load Balancer by creating a custom OAuth application in Google Cloud Storage to authenticate ServiceNow requests.Create a custom OAuth application in your Google Cloud Platform account to enable OAuth 2.0 authentication with the Google Cloud Load Balancer spoke.Use the information generated during the Google Cloud Storage application configuration to register Google Cloud Load Balancer as an OAuth provider and allow the ServiceNow instance to request OAuth 2.0 tokens.Create a credential record for the Google Cloud Load Balancer custom application. The Google Cloud Load Balancer Spoke connection and credential alias uses these credentials to authorize actions.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Google Cloud Load Balancer Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Google Cloud Load Balancer Spoke

Integrate the ServiceNow instance and Google Cloud Load Balancer by creating a custom OAuth application in Google Cloud Storage to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Google Cloud Load Balancer spoke.
-   Role required: admin.

## Create a custom application

Create a custom OAuth application in your Google Cloud Platform account to enable OAuth 2.0 authentication with the Google Cloud Load Balancer spoke.

### Before you begin

Role required: admin

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

8.  Copy these two values to a text file so that you can use them when you [Register Google Cloud Load Balancer as an OAuth provider](setup-gcloud-load-bal.md#).

    The client ID and secret can always be accessed in the Google APIs &amp; Services interface. Click **Credentials** and select the OAuth 2.0 client ID name.


## Register Google Cloud Load Balancer as an OAuth provider

Use the information generated during the Google Cloud Storage application configuration to register Google Cloud Load Balancer as an OAuth provider and allow the ServiceNow instance to request OAuth 2.0 tokens.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

2.  Open for the record, **Google Cloud Load Balancer**.

3.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Client ID|Client ID of the Google Cloud Load Balancer application.|
    |Client Secret|Client Secret of the Google Cloud Load Balancer application.|
    |OAuth API Script|**OAuthGoogleCloudLoadBalancerUtil** is selected by default.|
    |Authorization URL|The OAuth authorization code endpoint: `https://accounts.google.com/o/oauth2/auth`.|
    |Token URL|The OAuth server token endpoint: `https://oauth2.googleapis.com/token`.|
    |Redirect URL|OAuth callback endpoint in this format: `https://<instance>.service-now.com/oauth_redirect.do`. If left blank, the instance auto-generates the URL.|

4.  Right-click the form header, and click **Save**.


## Create a credential record for the Google Cloud Load Balancer Spoke

Create a credential record for the Google Cloud Load Balancer custom application. The Google Cloud Load Balancer Spoke connection and credential alias uses these credentials to authorize actions.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Integration Hub** &gt; **Connections &amp; Credentials**.

2.  Open the record, **GoogleCloudLoadBalancer**.

3.  In the **Credentials** tab, click **New**.

    The system displays this message: `What type of Credentials would you like to create?`

4.  Select **OAuth 2.0 Credentials**.

5.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Name|Name to identify the credential record. For example, `Google Cloud Load Balancer Cred`.|
    |OAuth Entity Profile|Select the default OAuth entity profile, **Google Cloud Load Balancer default\_profile**.|
    |Credential alias|Credential alias associated with this record. The default alias record, **sn\_gcp\_lb\_spoke.GoogleCloudLoadBalancer** is selected.|

    ![Credential record for Google Load Balancer spoke.](../image/gcloud-load-bal-cred.png)

6.  Right-click the form header and click **Save**.

7.  To generate the OAuth token, click the **Get OAuth Token** related link.


