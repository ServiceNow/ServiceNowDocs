---
title: Configure crawl settings for a Lucidchart external content connector
description: Specify the folders you want your Lucidchart external content connector to crawl. Define inclusion or exclusion filters to dictate the types of content the crawl retrieves and feeds to AI Search for indexing.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Lucidchart external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure crawl settings for a Lucidchart external content connector

Specify the folders you want your Lucidchart external content connector to crawl. Define inclusion or exclusion filters to dictate the types of content the crawl retrieves and feeds to AI Search for indexing.

## Before you begin

A connector admin must have already created the Lucidchart external content connector that you want to configure crawl settings for. To learn about this procedure, see [Create a Lucidchart external content connector](create-ext-cont-connector-lucidchart.md).

Role required: sn\_ext\_conn.xcc\_admin

## About this task

This task is optional. By default, the Lucidchart external content connector crawls all folders from its specified source system and sends documents with all supported file extensions to AI Search for indexing. You only need to perform this task if you want the connector to use any of the following non-default settings:

-   Inclusion or exclusion filters for the folders to crawl when running content crawls
-   Inclusion or exclusion filters for the file extensions to retrieve when running content crawls

Content is only retrieved from the source system if it passes all of your configured crawl setting filters. If any crawl setting filter excludes a content item, the external content connector doesn't retrieve it.

**Important:**

By default, each external content connector can index up to ten million \(10,000,000\) content items from its source system. When a connector exceeds this limit, it continues to crawl the source system, but only sends content item deletions and updates to AI Search for indexing, ignoring new content items. The connector logs an error message for every 10,000 content items it crawls beyond the indexing limit.

When a connector's indexed content item count exceeds 800,000, a warning message appears in the connector's UI to indicate that it's approaching the indexing limit. If the connector reaches the indexing limit, an error message appears in its UI.

External content connectors that support user permissions crawls can retrieve up to five hundred thousand \(500,000\) users.

If one of your connectors reaches the content indexing limit, you can update its crawl settings and file inclusion/exclusion filters to reduce the number of content items it retrieves. Alternately, if you need a connector to index more than 10,000,000 content items or to retrieve more than 500,000 users, you can create a Customer Service and Support case at [https://support.servicenow.com/now](https://support.servicenow.com/now) to request a limit increase for the connector.

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  In the Connectors list, select the record for the Lucidchart external content connector whose settings you want to modify.

3.  In the connector editor's Settings tab, select **Crawl settings**.

4.  Select one of the following **Date** options:

    -   To retrieve content from documents that were published in the last year, select **Published last year**.
    -   To retrieve content from documents that were published in the last quarter, select **Published last quarter**.
    -   To retrieve content from documents that were published in the last month, select **Published last month**.
    -   To retrieve content from documents that were published in the last week, select **Published last week**.
5.  Select one of the following **Folders** options:

    -   To crawl all folders encountered on the source system, select **Crawl all folders**.
    -   To crawl only a specified set of folders encountered on the source system, select **Include only these folders**, then use the **Add folder name or ID to include** field and **Add** button to enter names or IDs for folders you want the connector to include when crawling.

        As an example, you might enter `MarketingFolder` to only retrieve searchable content from documents in folders with the specified name or ID.

    -   To crawl all but a specified set of folders encountered on the source system, select **Exclude only these folders**, then use the **Add folder name or ID to exclude** field and **Add** button to enter names or IDs for folders you want the connector to exclude when crawling.

        As an example, you might enter `DraftFolder` to exclude searchable content from documents in folders with the specified name or ID.

6.  Select one of the following **Documents** options:

    -   To crawl all documents from the source system, select **Crawl all documents**.
    -   To crawl only a specified set of documents from the source system, select **Include only these documents**, then use the **Add document name or ID to include** field and **Add** button to enter names or IDs for documents you want the connector to include in retrieval.

        As an example, you might enter `release_document` to only retrieve searchable content from documents with the specified name or ID.

    -   To crawl all but a specified set of documents from the source system, select **Exclude only these documents**, then use the **Add document name or ID to exclude** field and **Add** button to enter names or IDs for documents you want the connector to exclude from retrieval.

        As an example, you might enter `DraftFolder2` to exclude searchable content from documents with the specified name or ID.

7.  Select **Save and validate**.


## Result

The Lucidchart external content connector is updated with your modified crawl settings.

## What to do next

To retrieve content from your Lucidchart source system using your modified crawl settings, create and run a one-time content crawl for your Lucidchart external content connector. To learn about creating and running one-time content crawls, see [Create a content crawl for an external content connector](create-content-crawl-external-content-connector.md).

**Parent Topic:**[Lucidchart external content connector](../concept/lucidchart-external-content-connector.md)

