---
title: Set up the Wrike spoke
description: Integrate your ServiceNow instance with Wrike by creating a custom OAuth application in the Wrike API Developer Site and configuring a connection in the Wrike spoke.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Wrike Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Wrike spoke

Integrate your ServiceNow instance with Wrike by creating a custom OAuth application in the Wrike API Developer Site and configuring a connection in the Wrike spoke.

## Before you begin

-   Copy and record the **Client ID** and **Client Secret** by logging in to [Wrike account](https://login.wrike.com/login/?redirectUrl=/frontend/apps/index.html#/api) as an admin and add an app. For more information about creating an app, see [OAuth 2.0 Authorization](https://developers.wrike.com/oauth-20-authorization/).
-   Request an Integration Hub subscription.
-   Activate the Wrike spoke.
-   Role required: admin.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Select **Integrations**.

3.  Select the **Connections** tab.

4.  Locate the alias for **Wrike** and select **View Details**.

    -   To configure the default connection and credential alias record that is shipped along with the Wrike, click **View Details**.

        ![Connection for the Wrike spoke](../image/wrike-spoke-tile.png)

    -   To manage more than one Wrike spoke connection records, you should create child alias record by clicking **Add Connection**. For more information about using multiple connections, see [Supporting multiple connections](../../integrationhub/concept/support-multiple-connections.md).
    If you're configuring the spoke for the first time, click **Configure**. Otherwise, select **Edit**.

    ![Initial connection configuration.](../image/wrike-spoke-configure.png)

5.  On the form, fill in these fields:

    |Field|Description|
    |-----|-----------|
    |Connection Name|Name of the connection.|
    |Connection URL|Web address that specifies the location and access details of the Wrike portal.|
    |OAuth Client ID|OAuth client ID that you generated when you set up the OAuth app.|
    |OAuth Client Secret|OAuth client secret that you generated when you set up the OAuth app.|
    |OAuth Redirect URL|Redirect URL that you had provided when you set up the OAuth app. The redirect URL must be in the format `https://instance-name.service-now.com/oauth_redirect.do`.|

    ![Configure a connection for the Wrike spoke.](../image/wrike-spoke-connection-config.png)

6.  Select **Create and Get OAuth Token**.

    You will be asked to log in to the Wrike API developer's portal before getting the OAuth token.


## Result

The Wrike spoke is set up and integrated with the ServiceNow instance.

