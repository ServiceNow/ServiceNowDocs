---
title: Configure OAuth application in Microsoft Azure
description: Create an OAuth application in Microsoft Azure to verify and authorize connection requests from your ServiceNow instance.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Microsoft SharePoint Online Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Configure OAuth application in Microsoft Azure

Create an OAuth application in Microsoft Azure to verify and authorize connection requests from your ServiceNow instance.

## Before you begin

Role required: admin

Access to Microsoft Azure portal to create an OAuth application.

## Procedure

1.  Register an application on Microsoft Azure.

    1.  Log in to [https://portal.azure.com/](https://portal.azure.com/).

    2.  Select **App registrations**.

        ![App registration button.](../image/MS-sharepoint-spoke-app-reg-button.png)

    3.  On the App registrations page, select **+ New registration**.

    4.  Fill the form.

        |Field|Description|
        |-----|-----------|
        |Name|Custom name of the OAuth application that you are creating.|
        |Supported account types|Accounts the tenant in Microsoft Azure AD directory supports.|
        |Redirect URI|The redirect URL to your ServiceNow instance that requests connection to Microsoft SharePoint online. From the Select a platform list, select Web and enter your ServiceNow instance URL in the format `https://<instance-name>.service-now.com/oauth_redirect.do`.|

        ![Add Redirect URL.](../image/ms-exchng-ol-redirect-url.png)

    5.  Select **Register**.

        The OAuth app is registered.

2.  To get the application ID, from the OAuth application page, copy the Application \(client\) ID.

    ![Application Client ID.](../image/MS-sharepoint-copy-client-ID.png)

    You need the Application \(client\) ID when you set up the connection record for Microsoft SharePoint Graph.

3.  Get the client secret.

    1.  On the OAuth application page, select Certificates &amp; secrets.

        ![Certificates & secrets tab.](../image/MS-sharepoint-certificates-and-secrets.png)

    2.  Select **+ New client secret**.

        ![New client secret button.](../image/MS-sharepoint-add-a-secret-button.png)

    3.  Set up the client secret.

        ![Client secret details.](../image/MS-sharepoint-client-secret-details.png)

        -   Description: A contextual description of the client secret.
        -   Expires: Time limit after which the client secret is invalid.
        **Note:** You need the client secret when you set up the connection record for Microsoft SharePoint Graph.

    4.  Select **Add**.

        The Client secret is generated.

    5.  Copy the secret and store at a secure place.

        ![Client secret copy button.](../image/MS-sharepoint-client-secret-copy.png)


