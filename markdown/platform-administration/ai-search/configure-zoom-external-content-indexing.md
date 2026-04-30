---
title: Configure Zoom for external content indexing
description: Create and activate a Server-to-Server OAuth app in the Zoom App Marketplace to allow the Zoom external content connector to access your Zoom source system.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-10-17"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Zoom external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Configure Zoom for external content indexing

Create and activate a Server-to-Server OAuth app in the Zoom App Marketplace to allow the Zoom external content connector to access your Zoom source system.

## Before you begin

You need admin privileges for the Zoom App Marketplace.

Role required: none

## About this task

The Zoom external content connector retrieves webinars and meetings from your Zoom source system using the Zoom APIs.

To allow the connector to access your Zoom source system via the Zoom APIs, you must configure and activate a Server-to-Server OAuth app in the Zoom App Marketplace. Your connector admin can use settings copied from this app to configure the Zoom external connector for proper connection to your source system.

## Procedure

1.  In the Zoom App Marketplace, create a new Server-to-Server OAuth app for the Zoom external content connector.

    1.  Navigate to [https://marketplace.zoom.us/](https://marketplace.zoom.us/) and log in with your admin credentials.

    2.  Navigate to **Develop** &gt; **Build app**.

    3.  If prompted, agree to the Zoom API license and terms of use by selecting **Agree**.

    4.  Select **Server to Server OAuth App** as the kind of app to create, then select **Create**.

    5.  Enter a name for your new Server-to-Server OAuth app.

        As an example, you might enter `Zoom external content connector`.

    6.  Select **Create**.

    You're taken to the App Credentials page for your new Server-to-Server OAuth app.

2.  On the App Credentials page, record the account ID, client ID, and client secret for your new Server-to-Server OAuth app.

    1.  Copy the account ID for your new Server-to-Server OAuth app and store it in a secure location.

        **Important:** Your external content connector admin needs this account ID when configuring the Zoom external content connector.

    2.  Copy the client ID for your new Server-to-Server OAuth app and store it in a secure location.

        **Important:** Your external content connector admin needs this client ID when configuring the Zoom external content connector.

    3.  Copy the client secret for your new Server-to-Server OAuth app and store it in a secure location.

        **Important:** Your external content connector admin needs this client secret when configuring the Zoom external content connector.

    4.  Select **Continue**.

    You're taken to the Information page for your new Server-to-Server OAuth app.

3.  On the Information page, add details about your new Server-to-Server OAuth app.

    These details are required in order to activate your new app.

    1.  In the Company Name field, enter the name of your organization.

    2.  In the Short Description field, enter a brief description of your new Server-to-Server OAuth app.

    3.  In the Name field, enter your name.

    4.  In the Email field, enter your email address.

    5.  Select **Continue**.

    You're taken to the Feature page for your new Server-to-Server OAuth app.

4.  On the Feature page, select **Continue**.

    You're taken to the Scopes page for your new Server-to-Server OAuth app.

5.  On the Scopes page, add the required API scopes to your new Server-to-Server OAuth app.

    1.  Select **Add Scopes**.

    2.  In the Add Scopes window, search for and then select each of the following scopes.

        -   cloud\_recording:read:list\_user\_recordings:admin
        -   meeting:read:list\_meetings:admin
        -   meeting:read:list\_past\_instances:admin
        -   meeting:read:list\_past\_participants:admin
        -   meeting:read:meeting:admin
        -   meeting:read:participant:admin
        -   meeting:read:past\_meeting:admin
        -   meeting:read:past\_qa:admin
        -   meeting:read:summary:admin
        -   user:read:list\_users:admin
        -   user:read:user:admin
        -   webinar:read:list\_panelists:admin
        -   webinar:read:list\_past\_instances:admin
        -   webinar:read:list\_past\_participants:admin
        -   webinar:read:list\_webinars:admin
        -   webinar:read:past\_qa:admin
        -   webinar:read:webinar:admin
        These scopes grant read access to your new Server-to-Server OAuth app for the specified content elements in your Zoom source system. The app can't modify your source system content with these scopes.

    3.  Select **Continue**.

    You're taken to the Activation page for your new Server-to-Server OAuth app.

6.  On the Activation page, activate your new Server-to-Server OAuth app by selecting **Activate your app**.

    Your new Server-to-Server OAuth app is activated.


## What to do next

Provide the following items to your connector admin:

-   The account ID that you copied in step [2.a](configure-zoom-external-content-indexing.md#copy-account-id-step).
-   The client ID that you copied in step [2.b](configure-zoom-external-content-indexing.md#copy-client-id-step).
-   The client secret that you copied in step [2.c](configure-zoom-external-content-indexing.md#copy-client-secret-step).

Your connector admin needs these items to configure a Zoom external content connector to retrieve meetings, webinars, and security principals from your Zoom source system.

For details on creating and configuring a Zoom external content connector, see [Create a Zoom external content connector](create-ext-cont-connector-zoom.md).

**Parent Topic:**[Zoom external content connector](../concept/zoom-external-content-connector.md)

