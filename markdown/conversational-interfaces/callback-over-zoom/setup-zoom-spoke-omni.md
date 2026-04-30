---
title: Setting up the Zoom spoke for Zoom extension for Omnichannel Callback
description: Enable the Zoom spoke to perform various actions such as creating meetings, rescheduling meetings, deleting a meeting, or fetching the participant details from your Zoom account by integrating your Zoom account with your ServiceNow instance.Create a connected app in your Zoom account to enable OAuth 2.0 authentication with the Zoom spoke.Use the information generated during Zoom account configuration to register the Zoom spoke as an OAuth provider and allow the instance to request OAuth 2.0 tokens.
locale: en-US
release: zurich
product: Callback over Zoom
classification: callback-over-zoom
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Setting up Zoom extension for Omnichannel Callback, Zoom extension for Omnichannel Callback, Manage people and work, Conversational Interfaces]
---

# Setting up the Zoom spoke for Zoom extension for Omnichannel Callback

Enable the Zoom spoke to perform various actions such as creating meetings, rescheduling meetings, deleting a meeting, or fetching the participant details from your Zoom account by integrating your Zoom account with your ServiceNow instance.

## Create a connected app in Zoom

Create a connected app in your Zoom account to enable OAuth 2.0 authentication with the Zoom spoke.

### Before you begin

-   Ensure that you have an Integration Hub subscription.
-   Ensure that Omnichannel Callback is installed on your instance.
-   Ensure that the Zoom spoke is activated. For more information, see [Zoom spoke](https://www.servicenow.com/docs/access?context=zoom-spoke&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)

Role required: Zoom admin

### Procedure

1.  Log in to [Zoom marketplace](https://marketplace.zoom.us/).

2.  In the **Develop** drop-down list, select **Build App**.

3.  Choose the **OAuth** card from the available cards.

4.  Disable the **Would you like to publish this app on Zoom App Marketplace?** option.

5.  Select **Create.**

6.  Provide a name for the app in the **Name** field.

7.  Set the app type to **Account-level app**.

    **Note:** Account-level apps must be installed by a Zoom admin, who manage the app for all account users in the account.

8.  Configure the redirect URLs for authentication.

    1.  In the App credentials section, enter the ServiceNow instance redirect URL in the **Redirect URL for OAuth** field in the following format:

        `https://<instance name>.com/oauth_redirect.do`

    2.  In the OAuth allow list section, add the ServiceNow instance redirect URL in the following format:

        `https://<instance name>.com/oauth_redirect.do`

    3.  Record the values of the **Client ID** and **Client Secret** fields to use them for the application registry.

9.  In the left panel, select **Scopes**.

10. In the Add Scopes section, select **Add Scopes**.

11. On the **Add Scopes** dialog box, select the scope type.

12. Select the **Meeting** scope type.

13. Select the following scopes:

    -   View all user meetings
    -   View and manage all user meetings
14. Select the **Recording** scope type.

15. Select the following scopes:

    -   View all user recordings
    -   View and manage all user recordings
16. Select the **User** scope type.

17. Select the **View all user information** scope.

18. Select **Done**.


### Result

The actions under the selected scopes become available to the Zoom spoke.

## Configure a Zoom connection in ServiceNow instance

Use the information generated during Zoom account configuration to register the Zoom spoke as an OAuth provider and allow the instance to request OAuth 2.0 tokens.

### Before you begin

Role required: admin

### Procedure

1.  From your ServiceNow instance, navigate to **Process Automation** &gt; **Flow Designer**.

2.  In the Flow Designer, select the **Connections** tab.

3.  Search for the Zoom connection and select **View Details**.

4.  On the Zoom connection card, select **Edit**.

5.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Connection Name|Name to identify the connection record.|
    |Connection URL|Base URL to connect to your Zoom instance: `https://api.zoom.us`.|
    |OAuth Entity Name|Name to identify the application registry record.|
    |OAuth Client ID|Client ID created during application registration.|
    |OAuth Client Secret|Client secret created during application registration.|
    |OAuth Redirect URL|OAuth callback endpoint: `https://instance name.service-now.com/oauth_redirect.do`.|

6.  Select **Edit and Get OAuth Token**.

    A confirmation message is displayed that the token is available.


