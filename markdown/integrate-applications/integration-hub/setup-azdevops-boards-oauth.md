---
title: Set up the Microsoft Azure DevOps Boards spoke using OAuth
description: Integrate the ServiceNow instance and Azure DevOps Boards using OAuth 2.0 authentication to authenticate ServiceNow requests.Provide authorization to the ServiceNow instance by registering an application in the Microsoft Azure portal.Create a connection record that enables the ServiceNow instance to send connection requests to the Microsoft Azure DevOps Boards.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/integration-hub/setup-azdevops-boards-oauth.html
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Microsoft Azure DevOps Boards Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Microsoft Azure DevOps Boards spoke using OAuth

Integrate the ServiceNow instance and Azure DevOps Boards using OAuth 2.0 authentication to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate Azure DevOps Boards spoke
-   Role required: admin.

**Important:**

-   If you are setting up the Azure DevOps Boards spoke using OAuth, you need not set up the spoke using personal access token.
-   If the Azure DevOps Boards spoke is already configured and set up, ensure that you set the value of **Active** to **false** for the existing connection before you proceed to set up the spoke using OAuth.

    \[Omitted image "azdevops-conn-false.png"\] Alt text: If connection is already configured, set the value of Active to false.


## Register an application using the Microsoft Azure portal

Provide authorization to the ServiceNow instance by registering an application in the Microsoft Azure portal.

### Before you begin

Role required: admin.

### About this task

Complete these steps from the Microsoft Azure portal.

### Procedure

1.  Log in to the [Microsoft Azure portal](https://portal.azure.com/) as an admin.

2.  Click **App Registrations**.

3.  Click **New registration**.

4.  On the form, fill in fields as per your requirement.

    For Redirect URI, specify the ServiceNow instance URL in this format: `https://<ServiceNow-Instance-Name>.service-now.com/oauth_redirect.do`.

    \[Omitted image "azdevops-boards-app.png"\] Alt text: Register an application in Microsoft Azure portal.

5.  Click **Register**.

    The application is created and the values of **Application \(client\) ID** and **Directory \(tenant\) ID** are displayed.

    \[Omitted image "azdevops-boards-app-ids.png"\] Alt text: Values of Application \(client\) ID and Directory \(tenant\) ID displayed after application creation.

6.  Copy and record the values of **Application \(client\) ID** and **Directory \(tenant\) ID**.

7.  Generate a client secret for the application.

    1.  Under **Manage**, click **Certificates &amp; secrets**.

    2.  Click **New client secret**.

    3.  On the form, enter provide a description and specify the duration after which the secret expires.

    4.  Click **Add**.

        \[Omitted image "azdevops-boards-app-secret.png"\] Alt text: Create a client secret.

        The client secret is created and its value is displayed.

    5.  Copy the value of client secret for later use.

        \[Omitted image "azdevops-boards-app-clsecret.png"\] Alt text: Copy the value of client secret for later use.

8.  Provide the required API permissions to the application.

    1.  Under **Manage**, click **API permissions**.

    2.  Click **Add a permission**.

    3.  Under **Microsoft APIs**, click **Azure DevOps**.

        \[Omitted image "azdevops-boards-app-api.png"\] Alt text: Add API permissions.

    4.  Expand **vso** and select these permissions **vso.project\_manage** and **vso.work\_full**.

        The **User.Read** permission under **Microsoft Graph** is selected by default. Configure other permissions as per your requirement.

    5.  Click **Grant admin consent for ServiceNow**.

        \[Omitted image "azdevops-boards-app-api-perm.png"\] Alt text: Grant admin consent for ServiceNow.

    6.  When prompted, confirm your choice to grant admin consent for ServiceNow.


### Result

An application has been registered in Microsoft Azure portal. You can use this application to connect to your Azure DevOps project from ServiceNow instance.

## Create a connection record for the Microsoft Azure DevOps Boards Spoke

Create a connection record that enables the ServiceNow instance to send connection requests to the Microsoft Azure DevOps Boards.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Select **Integrations**.

3.  In the Search all connections field, enter `Azure DevOps Boards`.

    Confirm that the **Outbound** tab is selected.

4.  In the Azure\_DevOps\_Boards tile, select **View Details**.

    \[Omitted image "ms-devops-board-spk-view-details.png"\] Alt text: View Details button on Azure DevOps Boards tile.

5.  Select **Configure**.

6.  Fill the form.

    |Field|Description|
    |-----|-----------|
    |Connection Name|Option to provide the name of the connection record. The default and read-only name of the first connection record that you create is Azure\_DevOps\_Boards.|
    |Connection URL|Option to provide the endpoint that the alias uses to interact with your Azure DevOps environment.|
    |Client ID|Option to provide the client ID that you generated while registering an application on Microsoft Azure portal.|
    |Client Secret|Option to provide the client secret that you generated while registering an application on Microsoft Azure portal.|
    |OAuth Redirect URL|Option to provide the redirect URL. You must provide the redirect URL in the format `https://<your-instance-name>.service.now.com/oauth_redirect.do`.|
    |Tenant ID|Option to provide the tenant ID that you generated while registering an application on Microsoft Azure portal.|

    \[Omitted image "ms-azure-devops-board-spk-conn-form.png"\] Alt text: Create Connection form.

7.  Select **Create and Get OAuth Token**.

    You log in to the Microsoft Azure portal and upon successful authentication, OAuth token is issued.

    \[Omitted image "ms-azuredevops-board-spk-oauth-token.png"\] Alt text: OAuth token is available.


