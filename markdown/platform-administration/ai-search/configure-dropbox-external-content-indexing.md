---
title: Configure Dropbox for external content indexing
description: Create and authorize an OAuth 2.0 application in the Dropbox App Console to allow the Dropbox external content connector to access your Dropbox source system.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Dropbox external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure Dropbox for external content indexing

Create and authorize an OAuth 2.0 application in the Dropbox App Console to allow the Dropbox external content connector to access your Dropbox source system.

## Before you begin

You need developer privileges for the Dropbox App Console.

Role required: none

## About this task

The Dropbox external content connector retrieves files from user folders and team folders in your Dropbox source system using the Dropbox APIs.

To allow the connector to access your Dropbox source system via the Dropbox APIs, you must configure and authorize an OAuth 2.0 application in the Dropbox App Console. Your connector admin can use settings copied from the OAuth 2.0 application to configure the Dropbox external connector for proper connection to your source system.

## Procedure

1.  In the Dropbox App Console, create a new OAuth 2.0 application for the Dropbox external content connector.

    1.  Navigate to [https://www.dropbox.com/developers/apps](https://www.dropbox.com/developers/apps) and log in with developer credentials.

    2.  Select **Create app**.

    3.  In the Choose an API step, select **Scoped access**.

    4.  In the Choose the type of access you need step, select **Full Dropbox**.

    5.  Enter a name for your new app.

        As an example, you might enter `ServiceNow external content connector`.

    6.  Select **Create app**.

    You're taken to the Settings page for your new OAuth 2.0 application.

2.  Copy the app key and app secret for your new OAuth 2.0 application.

    1.  On the Settings screen, copy the app key value and record it in a secure location.

        **Important:** Your external content connector admin needs this app key when configuring the Dropbox external content connector.

    2.  To view the app secret, select **Show**.

    3.  Copy the app secret value and record it in a secure location.

        **Important:** Your external content connector admin needs this app secret when configuring the Dropbox external content connector.

3.  Configure the OAuth 2 redirect URI for your new OAuth 2.0 application.

    1.  In the OAuth 2 entry, enter `https://<instance-name>.service-now.com/oauth_redirect.do`, replacing `<instance-name>` with the name of your ServiceNow AI Platform® instance.

        As an example, you might enter `https://example.service-now.com/oauth_redirect.do`.

    2.  Select **Add**.

    The new redirect URI appears on the page for your application.

4.  Configure permissions for your new OAuth 2.0 application.

    1.  Navigate to the Permissions page for your new OAuth 2.0 application.

    2.  Select the options for each of the following scopes.

        -   account\_info.read
        -   files.metadata.read
        -   files.content.read
        -   sharing.write
        -   sharing.read
        -   team\_info.read
        -   team\_data.member
        -   team\_data.content.read
        -   files.team\_metadata.read
        -   members.read
        -   groups.read
        **Note:** Some of these scope options may be automatically selected by default or when you select other scope options.

    3.  Select **Submit**.

    A message indicates that your permissions change was successful.


## What to do next

Provide the following items to your connector admin:

-   The app key that you copied in step [2.a](configure-dropbox-external-content-indexing.md#copy-app-key-step).
-   The app secret that you copied in step [2.c](configure-dropbox-external-content-indexing.md#copy-app-secret-step).

Your connector admin needs these items to configure a Dropbox external content connector to retrieve files in user folders, files in team folders, and security principals from your Dropbox source system.

For details on creating and configuring a Dropbox external content connector, see [Create a Dropbox external content connector](create-ext-cont-connector-dropbox.md).

**Parent Topic:**[Dropbox external content connector](../concept/dropbox-external-content-connector.md)

