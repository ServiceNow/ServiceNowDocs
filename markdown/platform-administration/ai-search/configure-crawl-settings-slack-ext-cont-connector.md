---
title: Configure crawl settings for a Slack external content connector
description: Specify the public channels you want your Slack external content connector to crawl. Define inclusion or exclusion filters to dictate the types of content the crawl retrieves and feeds to AI Search for indexing.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-11-05"
reading_time_minutes: 4
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Slack external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure crawl settings for a Slack external content connector

Specify the public channels you want your Slack external content connector to crawl. Define inclusion or exclusion filters to dictate the types of content the crawl retrieves and feeds to AI Search for indexing.

## Before you begin

A connector admin must have already created the Slack external content connector that you want to configure crawl settings for. To learn about this procedure, see [Create a Slack external content connector](create-ext-cont-connector-slack.md).

Role required: sn\_ext\_conn.xcc\_admin

## About this task

This task is optional. By default, the Slack external content connector crawls all public channels from its specified source system and sends documents with all supported file extensions to AI Search for indexing. You only need to perform this task if you want the connector to use any of the following non-default settings:

-   Inclusion or exclusion filters for the public channels to crawl when running content crawls
-   Inclusion or exclusion filters for the attachment file extensions to retrieve when running content crawls

Content is only retrieved from the source system if it passes all of your configured crawl setting filters. If any crawl setting filter excludes a content item, the external content connector doesn't retrieve it.

**Important:**

By default, an external content connector can index up to one million \(1,000,000\) documents from its source system. When a connector exceeds this limit, it continues to crawl the source system, but only sends document deletions and updates to AI Search for indexing, ignoring new documents. The connector logs an error message for every 10,000 documents it crawls beyond the indexing limit.

When a connector's indexed document count exceeds 800,000, a warning message appears in the connector's UI to indicate that it's approaching the indexing limit. If the connector reaches the indexing limit, an error message appears in its UI.

If one of your connectors reaches the indexing limit, you can update its crawl settings and file inclusion/exclusion filters to reduce the number of documents it retrieves. Alternately, if you need to index more than 1,000,000 documents, you can create a Customer Service and Support case at [https://support.servicenow.com/now](https://support.servicenow.com/now) to request a limit increase for the connector.

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  In the Connectors list, select the record for the Slack external content connector whose settings you want to modify.

3.  In the connector editor's Settings tab, select **Crawl settings**.

4.  Select one of the following **Content filtering** options:

    -   To crawl all channels from the source system, select **Crawl all content**.
    -   To crawl only a specified set of channels from the source system, select **Include only these channels**, then use the **Add URL** field and **Add** button to enter URLs for channels that you want to include in the crawl.

        For example, you might enter `https://example.slack.com/archives/D27X71EJRLU` to include only searchable content from the specified channel.

    -   To crawl all except a specified set of channels from the source system, select **Exclude only these channels**, then use the **Add URL** field and **Add** button to enter URLs for channels that you want to exclude from the crawl.

        For example, you might enter `https://example.slack.com/archives/K84Z67CKEIB` to exclude searchable content from the specified channel.

    **Important:**

    When specifying URLs for Slack channels, always use the format that includes your Slack workspace's hostname followed by `/archives/` and a channel ID, as in this example: `https://example.slack.com/archives/C69S1L3SS`. You can obtain the URL for a channel by long-pressing \(or right-clicking\) the channel in Slack and then selecting **Copy** &gt; **Copy link** from the context menu.

    Don't use channel URLs that include `app.slack.com` as the hostname, such as `https://app.slack.com/client/TP6U2MGFM/C69S1L3SS`, as these aren't supported by the Slack external content connector.

5.  Select one of the following **Attachment filtering** options:

    -   To retrieve all attachments with supported file extensions from the source system, select **Crawl all attachments**.
    -   To retrieve only attachments with specified file extensions from the source system, select **Include only these file extensions**, then use the **File extensions to include** field to enter attachment file extensions you want the connector to include when crawling.

        As an example, you might enter `.docx` to retrieve only attachments with the Microsoft Word file format.

    -   To retrieve all attachments except those with specified file extensions from the source system, select **Exclude only these file extensions**, then use the **File extensions to exclude** field to enter attachment file extensions you want the connector to exclude when crawling.

        As an example, you might enter `.csv` to exclude attachments with the Comma-Separated Values \(CSV\) file format.

    For details on the supported attachment file extensions, see [Binary file extensions supported in External Content Connectors](../reference/file-extensions-ext-cont-connector.md).

6.  Select **Save**.


## Result

The Slack external content connector is updated with your crawl scope and file extension filter settings.

## What to do next

To retrieve content from your Slack source system using your modified crawl settings, create and run a one-time content crawl for your Slack external content connector. To learn about creating and running one-time content crawls, see [Create a content crawl for an external content connector](create-content-crawl-external-content-connector.md).

**Parent Topic:**[Slack external content connector](../concept/slack-external-content-connector.md)

