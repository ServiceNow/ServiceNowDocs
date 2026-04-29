---
title: Configure crawl settings for a ServiceNow product documentation external content connector
description: Choose the products that you want your ServiceNow product documentation external content connector to crawl documentation for.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [ServiceNow product documentation external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure crawl settings for a ServiceNow product documentation external content connector

Choose the products that you want your ServiceNow product documentation external content connector to crawl documentation for.

## Before you begin

A connector admin must have already created the ServiceNow® product documentation external content connector that you want to configure crawl settings for. To learn about this procedure, see [Create a ServiceNow product documentation external content connector](create-ext-cont-connector-snowdoc.md).

Role required: sn\_ext\_conn.xcc\_admin

## About this task

This task is optional. By default, the ServiceNow product documentation external content connector crawls documentation for all ServiceNow products. You only need to perform this task if you want to exclude the documentation for some products from the connector's crawls.

Content is only retrieved from the source system if it passes all of your configured crawl setting filters. If any crawl setting filter excludes a content item, the external content connector doesn't retrieve it.

**Important:**

By default, each external content connector can index up to ten million \(10,000,000\) content items from its source system. When a connector exceeds this limit, it continues to crawl the source system, but only sends content item deletions and updates to AI Search for indexing, ignoring new content items. The connector logs an error message for every 10,000 content items it crawls beyond the indexing limit.

When a connector's indexed content item count exceeds 800,000, a warning message appears in the connector's UI to indicate that it's approaching the indexing limit. If the connector reaches the indexing limit, an error message appears in its UI.

External content connectors that support user permissions crawls can retrieve up to five hundred thousand \(500,000\) users.

If one of your connectors reaches the content indexing limit, you can update its crawl settings and file inclusion/exclusion filters to reduce the number of content items it retrieves. Alternately, if you need a connector to index more than 10,000,000 content items or to retrieve more than 500,000 users, you can create a Customer Service and Support case at [https://support.servicenow.com/now](https://support.servicenow.com/now) to request a limit increase for the connector.

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  In the Connectors list, select the record for the ServiceNow product documentation external content connector whose settings you want to modify.

3.  In the connector editor's Settings tab, select **Crawl settings**.

4.  To restrict the connector's content crawl scope, select the products that you want to crawl the documentation for.

    By default, all products are selected. You can use the option in the list header to select or deselect all products.

5.  Select **Save**.


## Result

The ServiceNow product documentation external content connector is updated with your chosen crawl scope.

**Parent Topic:**[ServiceNow product documentation external content connector](../concept/servicenow-product-documentation-external-content-connector.md)

