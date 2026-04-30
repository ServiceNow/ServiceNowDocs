---
title: Configure crawl settings for a monday.com external content connector
description: Specify the workspaces you want your monday.com external content connector to crawl. Define inclusion or exclusion filters to dictate the types of content the crawl retrieves and feeds to AI Search for indexing.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-10-22"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [monday.com external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure crawl settings for a monday.com external content connector

Specify the workspaces you want your monday.com external content connector to crawl. Define inclusion or exclusion filters to dictate the types of content the crawl retrieves and feeds to AI Search for indexing.

## Before you begin

A connector admin must have already created the monday.com external content connector that you want to configure crawl settings for. To learn about this procedure, see [Create a monday.com external content connector](create-ext-cont-connector-monday-com.md).

Role required: sn\_ext\_conn.xcc\_admin

## About this task

This task is optional. By default, the monday.com external content connector crawls all workspaces, boards, items, and workdocs found in its specified source system and sends them all to AI Search for indexing. You only need to perform this task if you want the connector to apply inclusion or exclusion filters for the workspaces to crawl when running content crawls.

Content is only retrieved from the source system if it passes all of your configured crawl setting filters. If any crawl setting filter excludes a content item, the external content connector doesn't retrieve it.

**Important:**

By default, an external content connector can index up to one million \(1,000,000\) documents from its source system. When a connector exceeds this limit, it continues to crawl the source system, but only sends document deletions and updates to AI Search for indexing, ignoring new documents. The connector logs an error message for every 10,000 documents it crawls beyond the indexing limit.

When a connector's indexed document count exceeds 800,000, a warning message appears in the connector's UI to indicate that it's approaching the indexing limit. If the connector reaches the indexing limit, an error message appears in its UI.

If one of your connectors reaches the indexing limit, you can update its crawl settings and file inclusion/exclusion filters to reduce the number of documents it retrieves. Alternately, if you need to index more than 1,000,000 documents, you can create a Customer Service and Support case at [https://support.servicenow.com/now](https://support.servicenow.com/now) to request a limit increase for the connector.

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  In the Connectors list, select the record for the monday.com external content connector whose settings you want to modify.

3.  In the connector editor's Settings tab, select **Crawl settings**.

4.  Select one of the following **Workspaces** options:

    -   To crawl all workspaces from the source system, select **Crawl all workspaces**.
    -   To crawl only a specified set of workspaces from the source system, select **Include only these workspaces**, then use the **Add workspaces to include** field and **Add** button to enter URLs for workspaces you want the connector to include when crawling.

        As an example, you might enter `https://example.monday.com/workspaces/2871949` to only retrieve searchable content from the specified workspace.

    -   To crawl all but a specified set of workspaces from the source system, select **Exclude only these workspaces**, then use the **Add workspaces to exclude** field and **Add** button to enter URLs for workspaces you want the connector to exclude when crawling.

        As an example, you might enter `https://example.monday.com/workspaces/6743223` to exclude searchable content from the specified workspace.

5.  Select **Save and validate**.


## Result

The monday.com external content connector is updated with your modified crawl settings.

## What to do next

To retrieve content from your monday.com source system using your modified crawl settings, create and run a one-time content crawl for your monday.com external content connector. To learn about creating and running one-time content crawls, see [Create a content crawl for an external content connector](create-content-crawl-external-content-connector.md).

**Parent Topic:**[monday.com external content connector](../concept/monday-com-external-content-connector.md)

