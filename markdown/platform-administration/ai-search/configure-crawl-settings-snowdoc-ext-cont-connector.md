---
title: Configure crawl settings for the ServiceNow product documentation external content connector
description: Choose the products that you want your ServiceNow product documentation external content connector to crawl documentation for.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-06-26"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configuring crawl settings for external content connectors, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure crawl settings for the ServiceNow product documentation external content connector

Choose the products that you want your ServiceNow product documentation external content connector to crawl documentation for.

## Before you begin

Role required: ais\_admin

## About this task

This task is optional. By default, the ServiceNow product documentation external content connector crawls documentation for all ServiceNow products. You only need to perform this task if you want to exclude documentation for some products from the connector's crawls.

**Important:**

By default, an external content connector can index up to one million \(1,000,000\) documents from its source system. When a connector exceeds this limit, it continues to crawl the source system, but only sends document deletions and updates to AI Search for indexing, ignoring new documents. The connector logs an error message for every 10,000 documents it crawls beyond the indexing limit.

When a connector's indexed document count exceeds 800,000, a warning message appears in the connector's UI to indicate that it's approaching the indexing limit. If the connector reaches the indexing limit, an error message appears in its UI.

If one of your connectors reaches the indexing limit, you can update its crawl settings and file inclusion/exclusion filters to reduce the number of documents it retrieves. Alternately, if you need to index more than 1,000,000 documents, you can create a Customer Service and Support case at [https://support.servicenow.com/now](https://support.servicenow.com/now) to request a limit increase for the connector.

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  In the Connectors list, select the record for the ServiceNow product documentation external content connector whose settings you want to modify.

3.  In the connector editor's Settings tab, select **Crawl settings**.

4.  Specify the connector's crawl scope by selecting the products that you want to crawl the documentation for.

    By default, all products are selected. You can use the option in the list header to select or deselect all products.

5.  Select **Save**.


## Result

The ServiceNow product documentation external content connector is updated with your chosen crawl scope.

**Parent Topic:**[Configuring crawl settings for external content connectors](../concept/cfg-crawl-settings-ext-cont-connector.md)

