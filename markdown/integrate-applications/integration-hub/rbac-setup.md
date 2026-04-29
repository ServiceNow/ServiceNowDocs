---
title: Set up the Microsoft Azure RBAC spoke
description: Integrate the ServiceNow instance and Microsoft Azure RBAC using OAuth 2.0 authentication to authenticate ServiceNow requests.Provide authorization to the ServiceNow instance by registering an application in the Microsoft Azure portal.Add and configure a Microsoft Azure RBAC spoke connection to authenticate ServiceNow requests.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Microsoft Azure RBAC Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Microsoft Azure RBAC spoke

Integrate the ServiceNow instance and Microsoft Azure RBAC using OAuth 2.0 authentication to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate Microsoft Azure RBAC spoke.
-   Role required: admin.

## Register an application using the Microsoft Azure portal

Provide authorization to the ServiceNow instance by registering an application in the Microsoft Azure portal.

### Before you begin

Role required: Privileged Role Administrator

1.  Log in to the [Microsoft Azure portal](https://portal.azure.com/) as an admin.
2.  Under **Azure services**, click **Microsoft Entra Privileged Identity**.
3.  Under **Tasks**, click **My roles**.
4.  Ensure that **Privileged Role Administrator** role is available and is activated.

    ![Privileged Role Administrator is available and is activated.](../image/rbac-role.jpg)


### About this task

Complete these steps from the Microsoft Azure portal.

### Procedure

1.  Log in to the [Microsoft Azure portal](https://portal.azure.com/) as an admin.

2.  Click **App Registrations**.

3.  Click **New registration**.

4.  On the form, fill in fields as per your requirement.

    For Redirect URI, specify the ServiceNow instance URL in this format: `https://<ServiceNow-Instance-Name>.service-now.com/oauth_redirect.do`.

    ![Register an application in Microsoft Azure portal.](../image/azdevops-boards-app.png)

5.  Click **Register**.

    The application is created and the values of **Application \(client\) ID** and **Directory \(tenant\) ID** are displayed.

    ![Values of Application (client) ID and Directory (tenant) ID displayed after application creation.](../image/azdevops-boards-app-ids.png)

6.  Copy and record the values of **Application \(client\) ID** and **Directory \(tenant\) ID**.

7.  Generate a client secret for the application.

    1.  Under **Manage**, click **Certificates &amp; secrets**.

    2.  Click **New client secret**.

    3.  On the form, enter provide a description and specify the duration after which the secret expires.

    4.  Click **Add**.

        ![Create a client secret.](../image/azdevops-boards-app-secret.png)

        The client secret is created and its value is displayed.

    5.  Copy the value of client secret for later use.

        ![Copy the value of client secret for later use.](../image/rbac-secret.jpg)

8.  Provide the required API permissions.

    1.  Under **Manage**, click **API permissions**.

    2.  Click **Add a permission** to add the required permissions to access the APIs.

        For information about permissions needed to perform the required actions, see the Spoke actions section here: [Microsoft Azure RBAC Spoke](../concept/azure-rbac-spoke.md).

        ![Add the required API permissions.](../image/rbac-api-perm.jpg)

    3.  Click **Grant admin consent for ServiceNow**.

        See [Quickstart: Configure a client application to access a web API](https://learn.microsoft.com/en-us/entra/identity-platform/quickstart-configure-app-access-web-apis#understanding-api-permissions-and-admin-consent-ui) for more information.


## Configure a connection record for the Microsoft Azure RBAC spoke

Add and configure a Microsoft Azure RBAC spoke connection to authenticate ServiceNow requests.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click the **Integrations** tab.

3.  Under **Connections**, toggle and enable the **Outbound** connections.

4.  Locate the alias for **Azure RBAC** and click **View Details**.

    -   To configure the default connection and credential alias record that is shipped along with the Microsoft Azure RBAC spoke, click **View Details**.

        ![Click View Details to configure the default alias.](../image/rbac-conn-temp.jpg)

    -   To manage more than one Microsoft Azure RBAC spoke connection records, you should create a new child alias record by clicking **Add Connection**. For more information about using multiple connections, see [Supporting multiple connections](../../integrationhub/concept/support-multiple-connections.md).
    If you are configuring the spoke for the first time, click **Configure**. Otherwise, click **Edit**.

    ![Click Configure if you are configuring the spoke for the first time.](../image/rbac-conn-temp-2.jpg)

5.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Connection Information|
    |Name|Name to identify the connection record. By default, the name is **Azure RBAC**.|
    |Credential Information|
    |Auth URL|OAuth authorization code endpoint. Enter `https://login.microsoftonline.com/<Directory-ID>/oauth2/v2.0/authorize`.|
    |Token URL|OAuth server token endpoint. Enter `https://login.microsoftonline.com/<Directory-ID>/oauth2/v2.0/token`.|
    |Revoke token URL|OAuth server token revocation endpoint. Enter `https://login.microsoftonline.com/<Directory-ID>/oauth2/v2.0/revoke`.|
    |OAuth Client ID|Application ID created during application registration.|
    |OAuth Client Secret|Client secret created during application registration.|
    |OAuth Redirect URL|OAuth callback endpoint. Enter `https://<instance-name>.service-now.com/oauth_redirect.do`.|

    ![Configure the default connection.](../image/rbac-conn-temp-3.jpg)

6.  Click **Configure Connection**.


### Result

The spoke connection is configured and is ready to be used.

