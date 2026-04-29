---
title: Set up the OneLogin spoke
description: Integrate the ServiceNow instance and OneLogin account using the OAuth credentials to authenticate ServiceNow requests.Create an API credential in the OneLogin portal to enable OAuth 2.0 authentication and obtain the values of client ID and client secret.Configure the default connection and credential alias to integrate the ServiceNow instance and OneLogin account to authenticate ServiceNow requests.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [OneLogin Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the OneLogin spoke

Integrate the ServiceNow instance and OneLogin account using the OAuth credentials to authenticate ServiceNow requests.

## Create an API credential in the OneLogin portal

Create an API credential in the OneLogin portal to enable OAuth 2.0 authentication and obtain the values of client ID and client secret.

### Before you begin

Role required: admin or account owner.

### Procedure

1.  Log in to your OneLogin account as an account owner or administrator.

2.  Navigate to **Developers** &gt; **API Credentials**.

3.  In the API Access page, click **New Credential**.

4.  On the form, enter the credential name and select scope for the credential.

    For more information, see [Working with API Credentials](https://developers.onelogin.com/api-docs/1/getting-started/working-with-api-credentials).

    **Note:** Ensure that you select either **Manage users** or **Manage all** permission.

    ![OneLogin credential.](../image/onelogin-credential.png)

5.  Click **Save**.

    The values of client ID and client secret are displayed.

    ![Values of client ID and client secret.](../image/onelogin-creds.png)

6.  Copy and record the values of client ID and client secret for later use.


## Configure the OneLogin connection and credential alias record

Configure the default connection and credential alias to integrate the ServiceNow instance and OneLogin account to authenticate ServiceNow requests.

### Before you begin

-   Request an Integration Hub subscription.
-   Activate the OneLogin spoke.
-   Role required: admin.

### Procedure

1.  Navigate to **Connection &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Open the record, **OneLogin**.

3.  Click the **Create New Connection &amp; Credential** related link.

4.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Connection Name|Name to identify the connection record.|
    |Connection URL|Connection URL in this format: `https://api.<region>.onelogin.com`. Replace `<region>` with the region of your OneLogin account.|
    |Credential Name|Name to identify the credential record.|
    |OAuth Entity Name|Name to identify the OAuth record.|
    |OAuth Client ID|Client ID of the credential created in the OneLogin portal.|
    |OAuth Client Secret|Client secret of the credential created in the OneLogin portal.|
    |OAuth Token URL|Token URL in this format: `https://api.<region>.onelogin.com/auth/oauth2/v2/token`. Replace `<region>` with the region of your OneLogin account.|

5.  Click **Create and Get OAuth Token**.

    ServiceNow instance is integrated with the OneLogin account.


