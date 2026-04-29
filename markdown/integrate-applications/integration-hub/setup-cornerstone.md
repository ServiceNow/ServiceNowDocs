---
title: Set up the Cornerstone spoke
description: Integrate your Cornerstone application with your ServiceNow instance. Register an OAuth application in Cornerstone and authenticate requests from ServiceNow.Register an application in the Cornerstone instance and record the generated Client ID and Client Secret for later use.Add and configure a Cornerstone connection to authenticate ServiceNow requests in Cornerstone spoke.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Cornerstone Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Cornerstone spoke

Integrate your Cornerstone application with your ServiceNow instance. Register an OAuth application in Cornerstone and authenticate requests from ServiceNow.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Cornerstone spoke.
-   Role required: admin.

## Register an application in the Cornerstone instance

Register an application in the Cornerstone instance and record the generated Client ID and Client Secret for later use.

### Before you begin

Role required: admin

### Procedure

1.  Log in to the Cornerstone instance as an admin.

2.  Navigate to **Admin** &gt; **Tools**.

    ![Navigate to Admin > Tools .](../image/cornerstone-app.png)

3.  Click **EDGE**.

4.  Click **API Management** under **Develop**.

    ![Access API Management.](../image/cornerstone-app-1.png)

    The API Management window is displayed in a new browser tab.

5.  Click the **Manage OAuth 2.0 Applications**.

6.  Click **+ Register New Application**.

7.  On the form, fill the values.

    |Field|Description|
    |-----|-----------|
    |Application Name|Name to identify the application.|
    |User ID|User ID for an active user account in your Cornerstone portal.|

8.  Select the scopes as per your requirement.

    ![Select the required scopes.](../image/cornerstone-app-2.png)

9.  Click **Register Application**.

    The values of Client ID and Client Secret are generated. Copy and record these values for later use.


## Configure connection for the Cornerstone spoke

Add and configure a Cornerstone connection to authenticate ServiceNow requests in Cornerstone spoke.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **Process Automation** &gt; **Flow Designer**.

2.  Click the **Connections** tab.

3.  Locate the **Cornerstone** connection alias in the outbound connections.

4.  Click **View Details**.

    **Note:** Don't click **Add Connection**.

5.  Click **Edit** or if you are configuring the spoke for the first time, click **Configure**.

6.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Connection Name|Name to identify the connection record.|
    |Connection URL|URL of the Cornerstone instance.|
    |Base URL|URL of the Cornerstone instance.|
    |OAuth Entity Name|Name to identify the application registry record.|
    |OAuth Client ID|Client ID created during the application configuration in Cornerstone.|
    |OAuth Client Secret|Client Secret created during the application configuration in Cornerstone.|
    |Token URL|OAuth server token endpoint. For example, `https://<Cornerstone-Instance>.com/services/api/oauth2/token`.|

7.  Click **Configure and Get OAuth Token**.


### Result

The spoke connection is configured and ready to be used.

