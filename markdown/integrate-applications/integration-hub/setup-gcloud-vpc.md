---
title: Set up the Google Cloud VPC Access spoke
description: Integrate the ServiceNow instance and Google Cloud VPC Access account by creating a custom OAuth application in Google Cloud Platform to authenticate ServiceNow requests.Create a custom OAuth application in your Google Cloud Platform account to enable OAuth 2.0 authentication with the Google Cloud VPC Access spoke.Use the information generated during the Google Cloud VPC Access application configuration to register Google Cloud VPC Access as an OAuth provider and allow the ServiceNow instance to request OAuth 2.0 tokens.Create a credential record for the Google Cloud VPC Access application. The Google Cloud VPC Access spoke connection and credential alias uses these credentials to authorize actions.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Google Cloud VPC Access Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Google Cloud VPC Access spoke

Integrate the ServiceNow instance and Google Cloud VPC Access account by creating a custom OAuth application in Google Cloud Platform to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Google Cloud VPC Access spoke.
-   Role required: admin.

## Configure the Google Cloud VPC Access application

Create a custom OAuth application in your Google Cloud Platform account to enable OAuth 2.0 authentication with the Google Cloud VPC Access spoke.

### Before you begin

-   Complete these steps from the [Google Cloud Platform](https://cloud.google.com/). See the [Google Cloud Platform](https://cloud.google.com/docs) product documentation for instructions on creating and configuring custom applications.
-   Role required: admin.

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

4.  Select the application type **OAuth client ID**.

5.  Enter the following **Authorized redirect URI**: `https://<instance>.service-now.com/oauth_redirect.do` and click **Create**.

6.  Copy your client ID and client secret to a text file so that you can use them when you register Google Cloud VPC Access as an OAuth provider.

    **Tip:** You can always access the client ID and secret in the Google APIs &amp; Services interfaceby clicking **Credentials** and selecting the OAuth 2.0 client ID name.


## Register Google Cloud VPC Access as an OAuth provider

Use the information generated during the Google Cloud VPC Access application configuration to register Google Cloud VPC Access as an OAuth provider and allow the ServiceNow instance to request OAuth 2.0 tokens.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

2.  Open for the record, **Google Cloud VPC Access**.

3.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Client ID|Client ID of the Google Cloud VPC Access application.|
    |Client Secret|Client Secret of the Google Cloud VPC Access application.|
    |OAuth API Script|**OAuthGoogleVPCAccessUtils** is selected by default.|
    |Authorization URL|The OAuth authorization code endpoint: `https://accounts.google.com/o/oauth2/auth`.|
    |Token URL|The OAuth server token endpoint: `https://oauth2.googleapis.com/token`.|
    |Redirect URL|OAuth callback endpoint in this format: `https://<instance>.service-now.com/oauth_redirect.do`. If left blank, the instance auto-generates the URL.|

4.  Right-click the form header, and click **Save**.


## Create a credential record for the Google Cloud VPC Access spoke

Create a credential record for the Google Cloud VPC Access application. The Google Cloud VPC Access spoke connection and credential alias uses these credentials to authorize actions.

### Before you begin

-   [Register Google Cloud VPC Access as an OAuth provider](setup-gcloud-vpc.md#)
-   Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Integration Hub** &gt; **Connections &amp; Credentials**.

2.  Open the record, **GoogleCloudVPCAccess**.

3.  In the **Credentials** tab, click **New**.

    The system displays this message: `What type of Credentials would you like to create?`

4.  Select **OAuth 2.0 Credentials**.

5.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Name|Name to identify the credential record. For example, `Google Cloud VPC Access Cred`.|
    |OAuth Entity Profile|Select the default OAuth entity profile, **Google Cloud VPC Access default\_profile**.|
    |Credential alias|Credential alias associated with this record. The default alias record, **sn\_gcp\_vpca\_spoke.GoogleCloudVPCAccess** is selected.|

    ![Credential record for the Google Cloud VPC Access spoke.](../image/gcloud-vpc-access.png)

6.  Right-click the form header and click **Save**.

7.  To generate the OAuth token, click the **Get OAuth Token** related link.


