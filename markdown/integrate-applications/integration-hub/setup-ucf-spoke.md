---
title: Set up the UCF spoke
description: Integrate the ServiceNow instance and UCF by creating a custom OAuth application in UCF to authenticate ServiceNow requests.Create an application in Common Controls Hub \(CCH\) to enable OAuth 2.0 authentication with the UCF spoke.Add and configure a UCF connection to authenticate ServiceNow requests in the UCF spoke.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [UCF Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the UCF spoke

Integrate the ServiceNow instance and UCF by creating a custom OAuth application in UCF to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the UCF spoke.
-   Role required: admin.

## Create an application in UCF

Create an application in Common Controls Hub \(CCH\) to enable OAuth 2.0 authentication with the UCF spoke.

### Before you begin

Role required: CCH administrator

### Procedure

1.  Create an application in UCF.

    For a step-by-step procedure to create an application using your CCH account, see the [CCH Support](https://support.commoncontrolshub.com/hc/en-us/articles/115001792983-How-do-I-create-an-Application-) documentation.

2.  While creating the application, ensure that you provide this information:

    -   **Redirect URL**: ServiceNow instance URL in the format, `https://<Instance-Name>.service-now.com/oauth_redirect.do`
    -   **Authorization URL**: Location on your website to which CCH redirects the interested users.
3.  Copy and record the **Client ID** and **Client Secret** for later use.


### Result

The application is created in CCH to enable OAuth 2.0 authentication with the UCF spoke.

## Configure a connection for the UCF spoke

Add and configure a UCF connection to authenticate ServiceNow requests in the UCF spoke.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **Process Automation** &gt; **Flow Designer**.

2.  Click the **Connections** tab.

3.  Locate the **UCF** connection alias and click **View Details**.

4.  Click **Edit** or if you are configuring the spoke for the first time, click **Configure**.

5.  On the form, fill in the values.

    |Field|Description|
    |-----|-----------|
    |Connection Name|Name to identify the connection record.|
    |Connection URL|Enter `https://api.unifiedcompliance.com/`.|
    |OAuth Entity Name|Name to identify the OAuth entity record.|
    |OAuth Client ID|Client ID created during the application configuration in CCH.|
    |OAuth Client Secret|Client Secret created during the application configuration in CCH.|
    |OAuth Redirect URL|OAuth callback endpoint. System generates the URL upon saving the application registry. This is the URL of the ServiceNow instance in this format: `https://<Instance-Name>/service-now.com/oauth_redirect.do`.|

6.  Click **Create and Get OAuth Token**.


