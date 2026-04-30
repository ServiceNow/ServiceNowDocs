---
title: Configure monday.com for external content indexing
description: Obtain an API token for a monday.com user account with admin privileges to allow the monday.com external content connector to access searchable content and metadata from your monday.com source system.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-10-15"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [monday.com external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Configure monday.com for external content indexing

Obtain an API token for a monday.com user account with admin privileges to allow the monday.com external content connector to access searchable content and metadata from your monday.com source system.

## Before you begin

Your monday.com account must have administrator privileges or API access for your monday.com organization.

Your monday.com account must also have permissions to access all the workspaces, boards, board items, and workdocs that you want the monday.com external content connector to retrieve searchable content and metadata from.

Role required: none

## About this task

The monday.com external content connector retrieves searchable content from workspaces, boards, board items, and workdocs found in your monday.com source system using the monday.com API.

To allow the connector to access your monday.com source system via the monday.com API, you need an API token for a monday.com user account with administrator privileges or API access. Your connector admin can use this API token and the monday.com API endpoint URL to configure the monday.com external connector for proper connection to your source system.

## Procedure

1.  Log in to monday.com with your credentials.

2.  If your account has administrator privileges, perform these steps.

    1.  Open the context menu by selecting your profile picture.

    2.  Navigate to **Administration** &gt; **Connections** &gt; **Personal API token**.

    3.  Copy the value of your personal API token and store it in a secure location.

        **Important:** Your external content connector admin needs this API token when configuring the monday.com external content connector.

3.  If your account doesn't have administrator privileges but has API access, perform these steps.

    1.  Open the context menu by selecting your profile picture.

    2.  Select **Developers**.

        The monday.com Developer Center opens.

    3.  In the Developer Center, navigate to **API token**.

    4.  On the API token page, display your personal API token by selecting **Show**.

    5.  Copy the value of your personal API token and store it in a secure location.

        **Important:** Your external content connector admin needs this API token when configuring the monday.com external content connector.


## What to do next

Provide the following items to your connector admin:

-   The URL for the monday.com API endpoint. This is typically `https://api.monday.com/v2`. To find the current API endpoint URL, see [https://developer.monday.com/api-reference/docs/introduction-to-graphql](https://developer.monday.com/api-reference/docs/introduction-to-graphql).
-   The API token that you copied in step [2.c](configure-monday-com-external-content-indexing.md#copy-admin-api-token-step) or step [3.e](configure-monday-com-external-content-indexing.md#copy-api-access-api-token-step).

Your connector admin needs these items to configure a monday.com external content connector to retrieve searchable content and metadata from workspaces, boards, board items, workdocs, and security principals found in your monday.com source system.

For details on creating and configuring a monday.com external content connector, see [Create a monday.com external content connector](create-ext-cont-connector-monday-com.md).

**Parent Topic:**[monday.com external content connector](../concept/monday-com-external-content-connector.md)

