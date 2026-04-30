---
title: Set up the Microsoft Entra Entitlement Management spoke
description: Integrate your ServiceNow instance and the Microsoft Entra account by creating a custom OAuth application in Microsoft Entra Entitlement Management to authenticate ServiceNow requests.Create a custom app using your Azure portal to enable OAuth 2.0 authentication with the Microsoft Entra Entitlement Management spoke.Configure a connection to your Microsoft Entra Entitlement Management account. The Microsoft Entra Entitlement Management spoke connection and credential aliases use these connections to perform actions in the Microsoft Entra Entitlement Management.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Microsoft Entra Entitlement Management Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Set up the Microsoft Entra Entitlement Management spoke

Integrate your ServiceNow instance and the Microsoft Entra account by creating a custom OAuth application in Microsoft Entra Entitlement Management to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Microsoft Entra Entitlement Management spoke.
-   Role required: admin.

## Create a custom application in Azure portal

Create a custom app using your Azure portal to enable OAuth 2.0 authentication with the Microsoft Entra Entitlement Management spoke.

### Before you begin

-   Request Integration Hub subscription.
-   Activate the Microsoft Entra Entitlement Management spoke.
-   Microsoft Entra Entitlement Management spoke requirements:
    -   Microsoft Entra Entitlement Management account
    -   Microsoft Entra Entitlement Management administrator credentials
-   Role required: admin

### About this task

Complete these steps from your Azure portal. See the [Microsoft identity platform documentation](https://learn.microsoft.com/en-us/entra/identity-platform/) documentation for instructions on creating and configuring custom applications.

### Procedure

1.  From your Azure portal, navigate to **App registrations** and click **New registration**.

2.  On the form, fill the values.

3.  In **Redirect URI**, enter your ServiceNow instance URL in this format: `https://<Instance-Name>.service-now.com/oauth_redirect.do`.

    See [Create a Microsoft Entra application and service principal that can access resources](https://learn.microsoft.com/en-us/entra/identity-platform/howto-create-service-principal-portal) for instructions on registering and configuring an application.

    ![Create an application.](../../integrationhub/images/ms-azure-ad-create-app.png)

4.  Click **Register**.

    The application is created and the required details are displayed.

5.  Copy and record the value of Directory ID.

    This value is required to register the app as a third-party OAuth provider on your ServiceNow instance.

    ![Copy Directory ID.](../../integrationhub/images/ms-azure-ad-copy-dir-id.png)

6.  Click **Certificates &amp; secrets**.

7.  Click **New client secret**.

    Secret is generated and displayed.

8.  Copy and record the value.

    This value is required to register the app as a third-party OAuth provider on your ServiceNow instance.

    ![Copy value of client secret.](../../integrationhub/images/ms-azure-ad-copy-sec.png)

9.  Click **API permissions**.

10. Click **Add a permission** to add the required permissions to access the APIs.

    For information about permissions needed to perform the required actions, see the Spoke actions section here: [Spoke actions](../concept/ms-entra-ent-mgmt-spk.md#section_d3k_1vt_33c).

    ![Add API permissions.](../../integrationhub/images/ms-azure-ad-api-perm.png)

11. Grant admin consent to your application.

    See [Quickstart: Configure a client application to access a web API](https://learn.microsoft.com/en-us/entra/identity-platform/quickstart-configure-app-access-web-apis#understanding-api-permissions-and-admin-consent-ui) for more information.


## Configure a connection for the Microsoft Entra Entitlement Management spoke

Configure a connection to your Microsoft Entra Entitlement Management account. The Microsoft Entra Entitlement Management spoke connection and credential aliases use these connections to perform actions in the Microsoft Entra Entitlement Management.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click the **Integrations** tab.

3.  Under **Connections**, toggle and enable the **Outbound** connections.

4.  Locate the alias for **EntraEntitlementManagement** and click **View Details**.

    -   To configure the default connection and credential alias record that is shipped along with the Entra Entitlement Management spoke, click **View Details**.
    -   To manage more than one Entra Entitlement Management spoke connection records, you should create a new child alias record by clicking **Add Connection**. For more information about using multiple connections, see [Supporting multiple connections](../../integrationhub/concept/support-multiple-connections.md).
    If you are configuring the spoke for the first time, click **Configure**. Otherwise, click **Edit**.

5.  On the form, fill in these fields:

    |Field|Value required|
    |-----|--------------|
    |Connection Information|
    |Name|Auto-generated name to identify the connection record.|
    |Credential Information|
    |Auth URL|Authorization URL in this format: `https://login.microsoftonline.com/<Directory ID>/oauth2/v2.0/authorize`. Replace `<Directory ID>` with the directory ID in your Entra Entitlement Management configuration.|
    |Token URL|Token URL in this format: `https://login.microsoftonline.com/<Directory ID>/oauth2/v2.0/token`. Replace `<Directory ID>` with the directory ID in your Microsoft Entra Entitlement Management configuration properties.|
    |Revoke token URL|Revoke token URL in this format: `https://login.microsoftonline.com/<Directory ID>/oauth2/v2.0/revoke`. Replace `<Directory ID>` with the directory ID in your Entra Entitlement Management configuration properties.|
    |OAuth Client ID|Client ID you created during the Entra Entitlement Management application registration.|
    |OAuth Client Secret|Key value you created during the Entra Entitlement Management application registration.|
    |OAuth Redirect URL|Redirect URL of your ServiceNow instance in this format: `https://<instance-name>.service-now.com/oauth_redirect.do`.|

6.  Click **Configure and Get OAuth Token**.


### Result

The Microsoft Entra Entitlement Management spoke is set up and integrated with the ServiceNow instance.

