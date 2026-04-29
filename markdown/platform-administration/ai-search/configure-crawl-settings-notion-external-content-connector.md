---
title: Configure crawl settings for a Notion external content connector
description: Specify the pages you want your Notion external content connector to crawl and feed to AI Search for indexing.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Notion external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure crawl settings for a Notion external content connector

Specify the pages you want your Notion external content connector to crawl and feed to AI Search for indexing.

## Before you begin

A connector admin must have already created the Notion external content connector that you want to configure crawl settings for. To learn about this procedure, see [Create a Notion external content connector](create-ext-cont-connector-notion.md).

Role required: sn\_ext\_conn.xcc\_admin

## About this task

The Notion external content connector crawls pages in your Notion workspace. To make a page eligible for crawling, you must add a connection from that page to the internal integration registered for the Notion external content connector.

Content is only retrieved from the source system if it passes all of your configured crawl setting filters. If any crawl setting filter excludes a content item, the external content connector doesn't retrieve it.

**Important:**

By default, each external content connector can index up to ten million \(10,000,000\) content items from its source system. When a connector exceeds this limit, it continues to crawl the source system, but only sends content item deletions and updates to AI Search for indexing, ignoring new content items. The connector logs an error message for every 10,000 content items it crawls beyond the indexing limit.

When a connector's indexed content item count exceeds 800,000, a warning message appears in the connector's UI to indicate that it's approaching the indexing limit. If the connector reaches the indexing limit, an error message appears in its UI.

External content connectors that support user permissions crawls can retrieve up to five hundred thousand \(500,000\) users.

If one of your connectors reaches the content indexing limit, you can update its crawl settings and file inclusion/exclusion filters to reduce the number of content items it retrieves. Alternately, if you need a connector to index more than 10,000,000 content items or to retrieve more than 500,000 users, you can create a Customer Service and Support case at [https://support.servicenow.com/now](https://support.servicenow.com/now) to request a limit increase for the connector.

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  In the Connectors list, select the record for the Notion external content connector whose settings you want to modify.

3.  In the connector editor's Settings tab, select **Crawl settings**.

4.  Select **Go to Notion to share content**, then perform the following steps in your Notion workspace for each page you want the connector to be able to retrieve searchable content, metadata, and files from:

    1.  Navigate to the selected Notion page.

    2.  In the menu at the upper right of the page, navigate to **. . .** &gt; **Connections** &gt; **Add connection**.

    3.  Select the internal integration registered for the Notion external content connector from the list of available connections.

    4.  Select **Confirm**.

    A **Configured** status indicator appears once you've added the internal integration as a connection for one or more pages in your Notion workspace.

5.  Select **Save and validate**.


## Result

The Notion external content connector is updated with your modified crawl settings.

**Important:** The Notion external content connector doesn't retrieve per-user permissions when running content crawls. All content indexed by the connector is searchable by all mapped users who have access to your configured AI Search experience.

## What to do next

To retrieve content from your Notion source system using your modified crawl settings, create and run a one-time content crawl for your Notion external content connector. To learn about creating and running one-time content crawls, see [Create a content crawl for an external content connector](create-content-crawl-external-content-connector.md).

**Parent Topic:**[Notion external content connector](../concept/notion-external-content-connector.md)

