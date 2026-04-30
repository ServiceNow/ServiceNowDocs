---
title: Set up the Wrike spoke
description: Integrate the ServiceNow instance and Wrike account by creating a custom OAuth application in Wrike API Developer Site to authenticate ServiceNow requests.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Wrike Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Wrike spoke

Integrate the ServiceNow instance and Wrike account by creating a custom OAuth application in Wrike API Developer Site to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Wrike spoke.
-   Role required: admin.

## Procedure

1.  Log in to [Wrike account](https://login.wrike.com/login/?redirectUrl=/frontend/apps/index.html#/api) as an admin and add an app.

    For more information about creating an app, see [OAuth 2.0 Authorization](https://developers.wrike.com/oauth-20-authorization/).

2.  Copy and record the values of **Client ID** and **Client Secret** for later use.

    **Note:** You must have the Wrike Enterprise account to create an app and obtain values of Client ID and Client Secret from the Wrike account.

3.  Log in to your ServiceNow instance.

4.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

5.  Select **Integrations**.

6.  Select the **Connections** tab.

7.  In the Search all connections field, enter `Wrike`.

    **Note:** The **Outbound** tab is selected by default. Or else, toggle to select it.

8.  On the Wrike connection alias tile, select **View Details**.

    ![View Details button on the Wrike connection alias tile.](../image/wrike-conn-alias-view-details.png)

9.  Select **Configure**.

10. Fill the form.

    |Field|Description|
    |-----|-----------|
    |Connection Name|Name of the connection.|
    |Connection URL|Option to provide the web address that specifies the location and access details of Wrike portal.|
    |OAuth Client ID|Option to provide the OAuth client ID that you generated when you set up the OAuth app.|
    |OAuth Client Secret|Option to provide the OAuth client secret that you generated when you set up the OAuth app.|
    |OAuth Redirect URL|Option to provide the redirect URL that you had provided when you set up the OAuth app. The redirect URL must be in the format `https://instance-name.service-now.com/oauth_redirect.do`.|

    ![Create Connection form.](../image/wrike-create-conn-form.png)

11. Select **Create and Get OAuth Token**.

    You must log in to the Wrike API developer's portal before getting the OAuth token.


