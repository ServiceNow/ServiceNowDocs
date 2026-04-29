---
title: Configure crawl settings for an Asana external content connector
description: Specify the projects you want your Asana external content connector to crawl. Define inclusion or exclusion filters to dictate the types of content the crawl retrieves and feeds to AI Search for indexing.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Asana external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure crawl settings for an Asana external content connector

Specify the projects you want your Asana external content connector to crawl. Define inclusion or exclusion filters to dictate the types of content the crawl retrieves and feeds to AI Search for indexing.

## Before you begin

A connector admin must have already created the Asana external content connector that you want to configure crawl settings for. To learn about this procedure, see [Create an Asana external content connector](create-ext-cont-connector-asana.md).

Role required: sn\_ext\_conn.xcc\_admin

## About this task

This task is optional. By default, the Asana external content connector crawls all projects from its specified source system and sends documents with all supported file extensions to AI Search for indexing. You only need to perform this task if you want the connector to use any of the following non-default settings:

-   Inclusion or exclusion filters for the projects to crawl when running content crawls
-   Inclusion or exclusion filters for the file extensions to retrieve when running content crawls

Content is only retrieved from the source system if it passes all of your configured crawl setting filters. If any crawl setting filter excludes a content item, the external content connector doesn't retrieve it.

**Important:**

By default, each external content connector can index up to ten million \(10,000,000\) content items from its source system. When a connector exceeds this limit, it continues to crawl the source system, but only sends content item deletions and updates to AI Search for indexing, ignoring new content items. The connector logs an error message for every 10,000 content items it crawls beyond the indexing limit.

When a connector's indexed content item count exceeds 800,000, a warning message appears in the connector's UI to indicate that it's approaching the indexing limit. If the connector reaches the indexing limit, an error message appears in its UI.

External content connectors that support user permissions crawls can retrieve up to five hundred thousand \(500,000\) users.

If one of your connectors reaches the content indexing limit, you can update its crawl settings and file inclusion/exclusion filters to reduce the number of content items it retrieves. Alternately, if you need a connector to index more than 10,000,000 content items or to retrieve more than 500,000 users, you can create a Customer Service and Support case at [https://support.servicenow.com/now](https://support.servicenow.com/now) to request a limit increase for the connector.

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  In the Connectors list, select the record for the Asana external content connector whose settings you want to modify.

3.  In the connector editor's Settings tab, select **Crawl settings**.

4.  Select one of the following **Content** options:

    -   To crawl all projects from the source system, select **Crawl all content**.
    -   To crawl only a specified set of projects from the source system, select **Include only these projects**, then use the **Add Projects** field and **Add** button to enter names for projects you want the connector to include when crawling.

        As an example, you might enter `Production` to only retrieve searchable content from the project with the specified name.

    -   To crawl all but a specified set of projects from the source system, select **Exclude only these projects**, then use the **Add Projects** field and **Add** button to enter names for projects you want the connector to exclude when crawling.

        As an example, you might enter `Test` to exclude searchable content from the project with the specified name.

5.  Select **Save and validate**.


## Result

The Asana external content connector is updated with your modified crawl settings.

## What to do next

To retrieve content from your Asana source system using your modified crawl settings, create and run a one-time content crawl for your Asana external content connector. To learn about creating and running one-time content crawls, see [Create a content crawl for an external content connector](create-content-crawl-external-content-connector.md).

**Parent Topic:**[Asana external content connector](../concept/asana-external-content-connector.md)

