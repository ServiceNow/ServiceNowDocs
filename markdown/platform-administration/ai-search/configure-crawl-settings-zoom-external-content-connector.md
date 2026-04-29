---
title: Configure crawl settings for a Zoom external content connector
description: Specify the content types you want your Zoom external content connector to retrieve.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Zoom external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure crawl settings for a Zoom external content connector

Specify the content types you want your Zoom external content connector to retrieve.

## Before you begin

A connector admin must have already created the Zoom external content connector that you want to configure crawl settings for. To learn about this procedure, see [Create a Zoom external content connector](create-ext-cont-connector-zoom.md).

Role required: sn\_ext\_conn.xcc\_admin

## About this task

This task is optional. By default, the Zoom external content connector crawls all webinars and meetings found in its specified source system and sends their searchable content and metadata to AI Search for indexing. You only need to perform this task if you want the connector to exclude content from webinars or from meetings.

Content is only retrieved from the source system if it passes all of your configured crawl setting filters. If any crawl setting filter excludes a content item, the external content connector doesn't retrieve it.

**Important:**

By default, each external content connector can index up to ten million \(10,000,000\) content items from its source system. When a connector exceeds this limit, it continues to crawl the source system, but only sends content item deletions and updates to AI Search for indexing, ignoring new content items. The connector logs an error message for every 10,000 content items it crawls beyond the indexing limit.

When a connector's indexed content item count exceeds 800,000, a warning message appears in the connector's UI to indicate that it's approaching the indexing limit. If the connector reaches the indexing limit, an error message appears in its UI.

External content connectors that support user permissions crawls can retrieve up to five hundred thousand \(500,000\) users.

If one of your connectors reaches the content indexing limit, you can update its crawl settings and file inclusion/exclusion filters to reduce the number of content items it retrieves. Alternately, if you need a connector to index more than 10,000,000 content items or to retrieve more than 500,000 users, you can create a Customer Service and Support case at [https://support.servicenow.com/now](https://support.servicenow.com/now) to request a limit increase for the connector.

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  In the Connectors list, select the record for the Zoom external content connector whose settings you want to modify.

3.  In the connector editor's Settings tab, select **Crawl settings**.

4.  Select the options for the webinar content types that you want the connector to retrieve searchable content and metadata from.

    -   **Past webinars**

        Select this option to index searchable content and metadata from completed webinars.

    -   **Index only transcriptions**

        Select this option to only index searchable content from webinar transcripts. This will ignore content and metadata from webinar agendas, summaries, and question and answer sessions. Webinars without transcripts will have no content or metadata indexed.

5.  Select the options for the meeting content types that you want the connector to retrieve searchable content and metadata from.

    -   **Past meetings**

        Select this option to index searchable content and metadata from completed meetings.

    -   **Index only transcriptions**

        Select this option to only index searchable content from meeting transcripts. This will ignore content and metadata from meeting agendas, summaries, and question and answer sessions. Meetings without transcripts will have no content or metadata indexed.

    **Note:** If you deselect both **Past webinars** and **Past meetings**, the connector won't retrieve any searchable content or metadata from your Zoom source system.

6.  Select **Save and validate**.


## Result

The Zoom external content connector is updated with your modified crawl settings.

## What to do next

To retrieve content from your Zoom source system using your modified crawl settings, create and run a one-time content crawl for your Zoom external content connector. To learn about creating and running one-time content crawls, see [Create a content crawl for an external content connector](create-content-crawl-external-content-connector.md).

**Parent Topic:**[Zoom external content connector](../concept/zoom-external-content-connector.md)

