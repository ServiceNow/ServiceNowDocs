---
title: Configure crawl settings for the Slack external content connector
description: Specify the public channels you want your Slack external content connector to crawl. Define inclusion or exclusion filters for file extensions to dictate the types of documents the crawl retrieves and feeds to AI Search for indexing.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-07-02"
reading_time_minutes: 4
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configuring crawl settings for external content connectors, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure crawl settings for the Slack external content connector

Specify the public channels you want your Slack external content connector to crawl. Define inclusion or exclusion filters for file extensions to dictate the types of documents the crawl retrieves and feeds to AI Search for indexing.

## Before you begin

An admin must have already created the Slack external content connector that you want to configure crawl settings for. To learn about this procedure, see [Create a Slack external content connector](create-ext-cont-connector-slack.md).

Role required: ais\_admin

## About this task

This task is optional. By default, the Slack external content connector crawls all public channels from its specified source system and sends documents with all supported file extensions to AI Search for indexing. You only need to perform this task if you want the connector to use any of the following non-default settings:

-   Crawl only a specified set of public channels from the source system
-   Include only documents with specific file extensions when crawling the source system
-   Exclude documents with specific file extensions when crawling the source system

**Important:**

By default, an external content connector can index up to one million \(1,000,000\) documents from its source system. When a connector exceeds this limit, it continues to crawl the source system, but only sends document deletions and updates to AI Search for indexing, ignoring new documents. The connector logs an error message for every 10,000 documents it crawls beyond the indexing limit.

When a connector's indexed document count exceeds 800,000, a warning message appears in the connector's UI to indicate that it's approaching the indexing limit. If the connector reaches the indexing limit, an error message appears in its UI.

If one of your connectors reaches the indexing limit, you can update its crawl settings and file inclusion/exclusion filters to reduce the number of documents it retrieves. Alternately, if you need to index more than 1,000,000 documents, you can create a Customer Service and Support case at [https://support.servicenow.com/now](https://support.servicenow.com/now) to request a limit increase for the connector.

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  In the Connectors list, select the record for the Slack external content connector whose settings you want to modify.

3.  In the connector editor's Settings tab, select **Crawl settings**.

4.  Specify the connector's crawl scope by selecting one of the following **Channels to crawl** options:

    -   To crawl all public channels from the source system, select **All**, then optionally select **Exclude channels** and use the **Add URL** field and **Add** button to enter URLs for any public channels that you want to exclude from the crawl.
    -   To crawl only a specified set of public channels from the source system, select **Specify**, then use the **Add URL** field and **Add** button to enter URLs for the public channels that you want to include in the crawl.
    **Important:**

    When specifying URLs for Slack channels, always use the format that includes your Slack workspace's hostname followed by `/archives/` and a channel ID, as in this example: `https://example.slack.com/archives/C69S1L3SS`. You can obtain the URL for a channel by selecting and holding \(or right-clicking\) the channel in Slack and then selecting **Copy** &gt; **Copy link** from the context menu.

    Don't use channel URLs that include `app.slack.com` as the hostname, such as `https://app.slack.com/client/TP6U2MGFM/C69S1L3SS`, as these aren't supported by the Slack external content connector.

5.  To apply inclusion or exclusion filters to a crawl based on file extensions, perform the following steps:

    1.  Select **Filter by file extension**.

    2.  To specify the type of filter, select **Include** or **Exclude**.

        Select **Include** if you want the crawl to only retrieve documents that have one of the specified file extensions. Select **Exclude** if you want the crawl to retrieve all documents except those that have one of the specified file extensions.

    3.  In the **File extension** field, select the file extensions that you want to include or exclude.

        For details on the supported file extensions, see [File extensions supported in External Content Connectors](../reference/file-extensions-ext-cont-connector.md).

6.  Select **Save**.


## Result

The Slack external content connector is updated with your crawl scope and file extension filter settings.

## What to do next

Now that you've configured the crawl for your Slack external content connector, you can schedule crawls to run on a recurring basis, or you can run one-time crawls on demand. For details on scheduling crawls, see [Define a crawl schedule for an external content connector](define-schedule-ext-cont-connector.md). To learn how to run one-time crawls on demand, see [Run a one-time full or partial document crawl for an external content connector](run-doc-crawl-ext-cont-connector.md).

**Parent Topic:**[Configuring crawl settings for external content connectors](../concept/cfg-crawl-settings-ext-cont-connector.md)

