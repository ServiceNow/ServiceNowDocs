---
title: Configure crawl settings for the predefined web sources external content connector
description: Specify the pages and subdomains you want your predefined web sources external content connector to crawl.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-04-16"
reading_time_minutes: 2
breadcrumb: [Configuring crawl settings for external content connectors, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure crawl settings for the predefined web sources external content connector

Specify the pages and subdomains you want your predefined web sources external content connector to crawl.

## Before you begin

Role required: ais\_admin

## About this task

This task is optional. By default, the predefined web sources external content connector crawls all pages and subdomains from its specified source system. You only need to perform this task if you want to exclude pages or subdomains from the connector's crawl.

**Important:**

By default, an external content connector can index up to one million \(1,000,000\) documents from its source system. When a connector exceeds this limit, it continues to crawl the source system, but only sends document deletions and updates to AI Search for indexing, ignoring new documents. The connector logs an error message for every 10,000 documents it crawls beyond the indexing limit.

When a connector's indexed document count exceeds 800,000, a warning message appears in the connector's UI to indicate that it's approaching the indexing limit. If the connector reaches the indexing limit, an error message appears in its UI.

If one of your connectors reaches the indexing limit, you can update its crawl settings and file inclusion/exclusion filters to reduce the number of documents it retrieves. Alternately, if you need to index more than 1,000,000 documents, you can create a Customer Service and Support case at [https://support.servicenow.com/now](https://support.servicenow.com/now) to request a limit increase for the connector.

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  In the Connectors list, select the record for the predefined web sources external content connector whose settings you want to modify.

3.  In the connector editor's Settings tab, select **Crawl settings**.

4.  Specify the connector's crawl scope by selecting one of the following **Site to crawl** options:

    -   To crawl all pages and subdomains from the source system, select **All**, then optionally select **Exclude sites** and use the **Add URL** field and **Add** button to enter URLs for any pages and subdomains that you want to exclude from the crawl.
    -   To crawl only a specified set of pages and subdomains from the source system, select **Specify**, then use the **Add URL** field and **Add** button to enter URLs for the pages and subdomains that you want to include in the crawl.
5.  Select **Save**.


## Result

The predefined web sources external content connector is updated with your chosen crawl scope.

**Parent Topic:**[Configuring crawl settings for external content connectors](../concept/cfg-crawl-settings-ext-cont-connector.md)

