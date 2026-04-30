---
title: Configure Workvivo for external content indexing
description: Create and authorize a new application in your Workvivo instance to allow the Workvivo external content connector to access your source system and content.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-02-05"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Workvivo external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Configure Workvivo for external content indexing

Create and authorize a new application in your Workvivo instance to allow the Workvivo external content connector to access your source system and content.

## Before you begin

You need the Developer role for your Workvivo instance.

Role required: none

## About this task

The Workvivo external content connector retrieves articles, comments, documents, events, kudos, pages, and updates that are present globally, in teams, or in spaces in your Workvivo source system using the Workvivo API.

To allow the connector to access your Workvivo source system via the API, you must configure and configure an app in your Workvivo instance. Your connector admin can use this app's API key and settings from your instance to configure the Workvivo external connector for proper connection to your source system.

## Procedure

1.  In your Workvivo instance, create a new app to grant the Workvivo external content connector access to your content.

    1.  Navigate to your Workvivo instance URL and log in with credentials for your account with the Developer role.

    2.  In the navigation bar, navigate to **Admin** &gt; **Tools**.

    3.  Navigate to **Platform** &gt; **API Keys &amp; JWT Settings**.

    4.  Copy your organization's Workvivo ID from the banner and store it in a secure location.

        **Important:** Your external content connector admin needs this Workvivo ID when configuring the Workvivo external content connector.

    5.  Copy your organization's API URL from the banner and store it in a secure location.

        **Important:** Your external content connector admin needs this API URL when configuring the Workvivo external content connector.

    6.  Select **Add New App**.

    7.  On the Create New App form, enter a name for your new app.

    8.  Select all of the following permissions for your new app.

        -   users.\*.read
        -   users.peerendorsement.read
        -   teams.\*.read
        -   teams.types.read
        -   spaces.\*.read
        -   spaces.public.read
        -   spaces.private.read
        -   spaces.hidden.read
        -   articles.\*.read
        -   events.\*.read
        -   updates.\*.read
        -   pages.\*.read
        -   likes.\*.read
        -   comments.\*.read
        -   kudos.\*.read
        -   documents.\*.read
    9.  Select **Save**.

    Workvivo creates your new app.

2.  Create an API key for your new app.

    1.  In the list item for your new app, select **Manage Keys**.

    2.  Select **Add new Key**.

    3.  On the New API Key form, enter a name for your new key, then select **Save**.

    4.  Copy your the token for your new API key and store it in a secure location.

        **Important:** Your external content connector admin needs this API key token when configuring the Workvivo external content connector.


## What to do next

Provide the following items to your connector admin:

-   The host URL for your Workvivo instance. This is typically `https://<organization-name>.workvivo.us`, where `<organization-name>` is the name of your organization.
-   Your organization's Workvivo ID that you copied in step [1.d](configure-workvivo-external-content-indexing.md#copy-workvivo-id-step).
-   The API URL that you copied in step [1.e](configure-workvivo-external-content-indexing.md#copy-api-url-step).
-   The API key token that you copied in step [2.d](configure-workvivo-external-content-indexing.md#copy-api-key-step).

Your connector admin needs these items to configure a Workvivo external content connector to retrieve articles, comments, documents, events, kudos, pages, and updates and security principals from your Workvivo source system.

For details on creating and configuring a Workvivo external content connector, see [Create a Workvivo external content connector](create-ext-cont-connector-workvivo.md).

**Parent Topic:**[Workvivo external content connector](../concept/workvivo-external-content-connector.md)

