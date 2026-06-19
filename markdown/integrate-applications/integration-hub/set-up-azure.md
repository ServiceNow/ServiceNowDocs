---
title: Set up Microsoft Entra ID spoke
description: Integrate the ServiceNow instance and your Microsoft Entra account by creating a custom OAuth application in Microsoft Entra ID to authenticate ServiceNow requests.Create a custom app using your Azure portal to enable OAuth 2.0 authentication with the Microsoft Entra ID spoke.Configure a connection to your Microsoft Entra ID account. The Microsoft Entra ID spoke connection and credential aliases use these connections to perform actions in the Microsoft Entra ID.Regenerate the Entra ID OAuth token when it expires.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/integration-hub/set-up-azure.html
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Microsoft Entra ID Spoke \(formerly Microsoft Azure Active Directory spoke\), Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up Microsoft Entra ID spoke

Integrate the ServiceNow instance and your Microsoft Entra account by creating a custom OAuth application in Microsoft Entra ID to authenticate ServiceNow requests.

Demonstrates how to set up theMicrosoft Entra ID spoke \(formerly known as Microsoft Azure Active Directory spoke\). 

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Microsoft Entra ID spoke.
-   Role required: admin.

## Create an Microsoft Entra ID application

Create a custom app using your Azure portal to enable OAuth 2.0 authentication with the Microsoft Entra ID spoke.

### Before you begin

-   Request Integration Hub subscription.
-   Activate the Microsoft Entra ID spoke.
-   Microsoft Entra ID spoke requirements:
    -   Microsoft Entra ID account
    -   Microsoft Entra ID administrator credentials
-   Role required: admin

### About this task

Complete these steps from your Azure portal. See the [Microsoft identity platform documentation](https://learn.microsoft.com/en-us/entra/identity-platform/) documentation for instructions on creating and configuring custom applications.

### Procedure

1.  From your Azure portal, access Microsoft Entra ID.

2.  Create an Microsoft Entra ID application.

    Alternatively, you can use an existing application. Ensure that you configure the existing application as outlined here.

3.  Navigate to **App registrations** and click **New registration**.

4.  On the form, fill the values.

5.  In **Redirect URI**, enter your ServiceNow instance URL in this format: `https://<Instance-Name>.service-now.com/oauth_redirect.do`.

    See [Create a Microsoft Entra application and service principal that can access resources](https://learn.microsoft.com/en-us/entra/identity-platform/howto-create-service-principal-portal) for instructions on registering and configuring an application.

    \[Omitted image "ms-azure-ad-create-app.png"\] Alt text: Create an application.

6.  Click **Register**.

    The application is created and the required details are displayed.

7.  Copy and record the value of Directory ID.

    This value is required to register the app as a third-party OAuth provider on your ServiceNow instance.

    \[Omitted image "ms-azure-ad-copy-dir-id.png"\] Alt text: Copy Directory ID.

8.  Click **Certificates &amp; secrets**.

9.  Click **New client secret**.

    Secret is generated and displayed.

10. Copy and record the value.

    This value is required to register the app as a third-party OAuth provider on your ServiceNow instance.

    \[Omitted image "ms-azure-ad-copy-sec.png"\] Alt text: Copy value of client secret.

11. Click **API permissions**.

12. Click **Add a permission** to add the required permissions to access the APIs.

    For information about permissions needed to perform the required actions, see the Spoke actions section here: [Microsoft Entra ID Spoke \(formerly Microsoft Azure Active Directory spoke\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/integration-hub/microsoft-azure-ad-spoke.md).

    \[Omitted image "ms-azure-ad-api-perm.png"\] Alt text: Add API permissions.

13. Grant admin consent to your application.

    See [Quickstart: Configure a client application to access a web API](https://learn.microsoft.com/en-us/entra/identity-platform/quickstart-configure-app-access-web-apis#understanding-api-permissions-and-admin-consent-ui) for more information.


## Configure a connection for the Microsoft Entra ID spoke

Configure a connection to your Microsoft Entra ID account. The Microsoft Entra ID spoke connection and credential aliases use these connections to perform actions in the Microsoft Entra ID.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click the **Integrations** tab.

3.  Under **Connections**, toggle and enable the **Outbound** connections.

4.  Locate the alias for **AzureAD** and click **View Details**.

    -   To configure the default connection and credential alias record that is shipped along with the Entra ID spoke, click **View Details**.

        \[Omitted image "entra-id-connection.png"\] Alt text: Connection for the Entra ID spoke

    -   To manage more than one Entra ID spoke connection records, you should create a new child alias record by clicking **Add Connection**. For more information about using multiple connections, see [Supporting multiple connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/integration-hub/support-multiple-connections.md).
    If you are configuring the spoke for the first time, click **Configure**. Otherwise, click **Edit**.

    \[Omitted image "entra-id-connection-conf.png"\] Alt text: Initial connection configuration.

5.  On the form, fill in these fields:

    |Field|Value required|
    |-----|--------------|
    |Connection Information|
    |Name|Auto-generated name to identify the connection record.|
    |Credential Information|
    |Auth URL|Authorization URL in this format: `https://login.microsoftonline.com/<Directory ID>/oauth2/v2.0/authorize`. Replace `<Directory ID>` with the directory ID in your Entra ID configuration.|
    |Token URL|Token URL in this format: `https://login.microsoftonline.com/<Directory ID>/oauth2/v2.0/token`. Replace `<Directory ID>` with the directory ID in your Microsoft Entra ID configuration properties.|
    |Revoke token URL|Revoke token URL in this format: `https://login.microsoftonline.com/<Directory ID>/oauth2/v2.0/revoke`. Replace `<Directory ID>` with the directory ID in your Entra ID configuration properties.|
    |OAuth Client ID|Client ID you created during the Entra ID application registration.|
    |OAuth Client Secret|Key value you created during the Entra ID application registration.|
    |OAuth Redirect URL|Redirect URL of your ServiceNow instance in this format: `https://<instance-name>.service-now.com/oauth_redirect.do`.|

    \[Omitted image "entra-id-conf-temp.png"\] Alt text: Configure a connection for the Entra ID spoke.

6.  Click **Configure and Get OAuth Token**.


### Result

The Microsoft Entra ID spoke is set up and integrated with the ServiceNow instance.

**Note:** By default, the grant type of the application registry record is set to **Authorization Code**.

-   If you want to use credentials of an Azure user to obtain the OAuth token and run all flows with that user delegation, use **Authorization Code**. Currently, delegation of permission to each logged in ServiceNow user isn't supported.
-   If you want to grant permission to an app instead of an individual user, change the grant type to **Client Credentials**. This ensures that all flows, either interactive or background, will use the app permissions to execute the flows. For more information on how to use Client Credentials, see [KB0993701](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0993701).
-   In situations where you can't use one grant type but require both the **Authorization Code** and **Client Credentials** grant types to perform the actions, create a child alias.

## Regenerate Entra ID OAuth token

Regenerate the Entra ID OAuth token when it expires.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Select the Entra ID spoke OAuth Credential record.

    For example, select **Azure AD Credentials**.

3.  From Related Links, click **Get OAuth Token**.


