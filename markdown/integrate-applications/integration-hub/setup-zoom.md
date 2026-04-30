---
title: Set up the Zoom spoke
description: Integrate your Zoom account with your ServiceNow instance so that you can use the Zoom spoke to perform various actions on your Zoom account. You can also create a custom OAuth application in the Zoom account so that it can authenticate requests from your instance.Create a connected app in your Zoom account to establish an OAuth 2.0 level of authentication between the Zoom APIs and the Zoom spoke on the ServiceNow AI Platform. After creating the connected app, you can add scopes that enable you to perform different actions from the Zoom spoke.Use the information generated during Zoom account configuration to register Zoom spoke as an OAuth provider and allow the instance to request OAuth 2.0 tokens. Add the Zoom connection in Workflow Studio to perform actions in Zoom.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Zoom Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Set up the Zoom spoke

Integrate your Zoom account with your ServiceNow instance so that you can use the Zoom spoke to perform various actions on your Zoom account. You can also create a custom OAuth application in the Zoom account so that it can authenticate requests from your instance.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Zoom spoke.
-   Role required: admin.

## Create a connected app in Zoom

Create a connected app in your Zoom account to establish an OAuth 2.0 level of authentication between the Zoom APIs and the Zoom spoke on the ServiceNow AI Platform. After creating the connected app, you can add scopes that enable you to perform different actions from the Zoom spoke.

### Before you begin

1.  Create a Zoom account
2.  Role required: Zoom admin

### About this task

Creating the connected app is a one-time activity.

### Procedure

1.  Log in to [Zoom marketplace](https://marketplace.zoom.us/).

2.  Navigate to **Develop** &gt; **Build App**.

3.  Select **General App**.

    ![General App option to create an app.](../image/zoom-spk-build-app-general.png)

4.  Select **Create**.

5.  Double-click the default name of the app and update the name.

    ![Update general app name.](../image/zoom-spk-app-name.png)

6.  Select **Admin-managed**.

7.  Select **Save**.

8.  Under the App Credentials section, copy the Client ID and Client secret and store them at a secure place.

    ![Client ID and client secret.](../image/zoom-spk-client-id-secret.png)

9.  Under the OAuth Information section, do the steps.

    1.  In the **OAuth Redirect URL** field, enter the redirect URL in this format: `https://<ServiceNow-Instance-Name>.service-now.com/oauth_redirect.do`.

    2.  Under the **OAuth Allow List**, add a ServiceNow instance redirect URL in this format: `https://<ServiceNow-Instance-Name>.service-now.com/oauth_redirect.do`.

        A token is generated. This token is used by the OAuth app to give the Zoom spokes access to the Zoom APIs.

    3.  To add another URL to the allow list, click **Add New List**.

        The following example shows the screen that you use to generate the credentials for the OAuth app.

        ![OAuth credentials configuration for Zoom spokes.](../image/zoom-app-conf.png "OAuth credentials configuration for Zoom spokes")

        **Note:** To know the difference between the Redirect URL for OAuth and the URL that is mentioned in the OAuth allow list, see [Zoom Developer Forum](https://devforum.zoom.us/t/difference-between-redirect-url-and-allow-list-in-app-settings/58709).

10. On the left panel, select Access.

11. Under the Access section, copy the Secret Token and Verification Token.

12. On the left panel, select **Scopes**.

13. Select **+ Add Scopes**.

14. In the Search scope field, enter the granular scope.

    An example of a granular scope is `meeting:delete:meeting:admin`.

    The granular scope appears.

    ![Scope search and find.](../image/zoom-spk-find-scope.png)

15. Select the scope and then select **Done**.

    The granular scope is added.

    ![Granular scope is added.](../image/zoom-spk-scope-added.png)

16. Repeat the steps to add more granular scopes.


## Add Zoom connection in ServiceNow instance

Use the information generated during Zoom account configuration to register Zoom spoke as an OAuth provider and allow the instance to request OAuth 2.0 tokens. Add the Zoom connection in Workflow Studio to perform actions in Zoom.

### Before you begin

Role required: admin

### Procedure

1.  From your ServiceNow instance, navigate to **Process Automation** &gt; **Workflow Studio**.

2.  Select the **Integrations** tab.

3.  In the Search all connections field, enter `Zoom`.

    **Note:** The **Outbound** tab is selected by default. Confirm that the **Outbound** tab is already selected.

4.  In the Zoom card, select **View Details**.

    -   To configure the default connection and credential alias record that is shipped along with the Zoom spoke, click **View Details**.
    -   To manage more than one Zoom spoke connection records, you should create a new child alias record by clicking **Add Connection**. For more information about using multiple connections, see [Supporting multiple connections](../../integrationhub/concept/support-multiple-connections.md).
    If you are configuring the spoke for the first time, select **Configure**. Otherwise, click **Edit**.

5.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Connection Name|Name to identify the connection record.|
    |Connection URL|Base URL to connect to your Zoom instance. Enter `https://api.zoom.us`.|
    |OAuth Entity Name|Name to identify the application registry record.|
    |OAuth Client ID|Client ID created during application registration.|
    |OAuth Client Secret|Client secret created during application registration.|
    |OAuth Redirect URL|OAuth callback endpoint. Enter `https://<instance-name>.service-now.com/oauth_redirect.do`.|

    ![Generate OAuth token.](../image/zoom-conn-template.png)

6.  Click **Configure and Get OAuth Token**.

    A confirmation message is displayed that the token is available.![Confirmation that refresh token is available.](../image/zoom-conn-confirmation.png)


