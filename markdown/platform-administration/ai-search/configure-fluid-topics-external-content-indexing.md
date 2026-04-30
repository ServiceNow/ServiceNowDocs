---
title: Configure Fluid Topics for external content indexing
description: Generate an API key in your Fluid Topics tenant to allow the Fluid Topics external content connector to access your Fluid Topics source system.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-02-12"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Fluid Topics external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Configure Fluid Topics for external content indexing

Generate an API key in your Fluid Topics tenant to allow the Fluid Topics external content connector to access your Fluid Topics source system.

## Before you begin

You need administrator access and API access for your Fluid Topics tenant.

Role required: none

## About this task

The Fluid Topics external content connector retrieves Topics, Articles, Publications, and associated content pages delivered through portals from your Fluid Topics source system using the Fluid Topics API.

To allow the connector to access your source system via the API, you must generate an API key in Fluid Topics. Your connector admin can use this API key and the URL for your Fluid Topics tenant to configure the Fluid Topics external connector for proper connection to your source system.

## Procedure

1.  Navigate to your Fluid Topics tenant and log in with administrator credentials.

2.  Generate an API key.

    1.  Navigate to **Administration** &gt; **Integrations** &gt; **API keys**.

    2.  Select **Create &amp; Add**.

    3.  In the Name field, enter a unique name for your new API key.

        The API key name can only contain alphanumeric characters, hyphens, and underscores.

    4.  Select **Create &amp; Add**.

        Fluid Topics displays your new API key.

3.  Copy the generated API key and store its value in a secure location.

    **Important:** Your external content connector admin needs this API key when configuring the Fluid Topics external content connector.

4.  Create a new Fluid Topics source and assign your new API key to it.

    **Note:** You only need to perform this step if there are no sources in your Fluid Topics tenant for this external indexing configuration.

    1.  Navigate to **Administration** &gt; **Knowledge Hub** &gt; **Sources**.

    2.  Select **New source**.

    3.  Select the **Exact Source Type Name** source type.

    4.  Enter a unique ID and unique name for your new source.

    5.  Enter a category and description for your new source.

    6.  Select **Next**.

    7.  Select **Admins and KHUB Admins**.

    8.  In the Allowed API keys section, select your new API key as an allowed API key for your new source.

    9.  Select **Save**.


## What to do next

Provide the following items to your connector admin:

-   The URL for your Fluid Topics tenant.
-   The API key that you copied in step [3](configure-fluid-topics-external-content-indexing.md#copy-api-key-step).

Your connector admin needs these items to configure a Fluid Topics external content connector to retrieve content and security principals from your Fluid Topics source system.

For details on creating and configuring a Fluid Topics external content connector, see [Create a Fluid Topics external content connector](create-ext-cont-connector-fluid-topics.md).

**Parent Topic:**[Fluid Topics external content connector](../concept/fluid-topics-external-content-connector.md)

