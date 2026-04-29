---
title: Configure crawl settings for a Miro external content connector
description: Specify the Spaces and boards you want your Miro external content connector to crawl. Define inclusion or exclusion filters to restrict the content the crawl retrieves and feeds to AI Search for indexing.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Miro external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure crawl settings for a Miro external content connector

Specify the Spaces and boards you want your Miro external content connector to crawl. Define inclusion or exclusion filters to restrict the content the crawl retrieves and feeds to AI Search for indexing.

## Before you begin

A connector admin must have already created the Miro external content connector that you want to configure crawl settings for. To learn about this procedure, see [Create a Miro external content connector](create-ext-cont-connector-miro.md).

Role required: sn\_ext\_conn.xcc\_admin

## About this task

This task is optional. By default, the Miro external content connector crawls all accessible Spaces from its specified source system and sends searchable text content and metadata from all boards it finds to AI Search for indexing. You only need to perform this task if you want the connector to use any of the following non-default settings:

-   Inclusion or exclusion filters for the Spaces to crawl when running content crawls
-   Inclusion or exclusion filters for the boards to retrieve searchable text content and metadata from when running content crawls

Content is only retrieved from the source system if it passes all of your configured crawl setting filters. If any crawl setting filter excludes a content item, the external content connector doesn't retrieve it.

**Important:**

By default, each external content connector can index up to ten million \(10,000,000\) content items from its source system. When a connector exceeds this limit, it continues to crawl the source system, but only sends content item deletions and updates to AI Search for indexing, ignoring new content items. The connector logs an error message for every 10,000 content items it crawls beyond the indexing limit.

When a connector's indexed content item count exceeds 800,000, a warning message appears in the connector's UI to indicate that it's approaching the indexing limit. If the connector reaches the indexing limit, an error message appears in its UI.

External content connectors that support user permissions crawls can retrieve up to five hundred thousand \(500,000\) users.

If one of your connectors reaches the content indexing limit, you can update its crawl settings and file inclusion/exclusion filters to reduce the number of content items it retrieves. Alternately, if you need a connector to index more than 10,000,000 content items or to retrieve more than 500,000 users, you can create a Customer Service and Support case at [https://support.servicenow.com/now](https://support.servicenow.com/now) to request a limit increase for the connector.

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  In the Connectors list, select the record for the Miro external content connector whose settings you want to modify.

3.  In the connector editor's Settings tab, select **Crawl settings**.

4.  Select one of the following **Dates** options:

    -   To only retrieve searchable text content and metadata from boards that were published in the last year, select **Published last year**.
    -   To only retrieve searchable text content and metadata from boards that were published in the last quarter, select **Published last quarter**.
    -   To only retrieve searchable text content and metadata from boards that were published in the last month, select **Published last month**.
    -   To only retrieve searchable text content and metadata from boards that were published in the last week, select **Published last week**.
5.  Select one of the following **Spaces** options:

    -   To crawl boards from all Spaces found on the source system, select **Crawl all spaces**.
    -   To crawl only boards from a specified set of Spaces, select **Include only these spaces**, then use the **Add space ID to include** field and **Add** button to enter IDs for Spaces with boards that you want the connector to include when crawling.

        As an example, you might enter `3458764623126768011` to only retrieve searchable text content and metadata from boards in the Space with the specified ID.

    -   To crawl boards from all but a specified set of Spaces, select **Exclude only these spaces**, then use the **Add space ID to exclude** field and **Add** button to enter IDs for Spaces with boards you want the connector to exclude when crawling.

        As an example, you might enter `3074457347343237232` to exclude searchable text content and metadata from boards in the Space with the specified ID.

6.  Select one of the following **Boards** options:

    -   To retrieve searchable text content and metadata from all boards found in the source system, select **Crawl all boards**.
    -   To retrieve searchable text content and metadata from only a specified set of boards found in the source system, select **Include only these boards**, then use the **Add board ID to include** field and **Add** button to enter IDs for boards you want the connector to include when crawling.

        As an example, you might enter `uXjVJYMj0OM=` and `o9J_leLUTqM=` to only retrieve searchable text content and metadata from boards with the specified IDs.

    -   To retrieve searchable text content and metadata from all but a specified set of boards found in the source system, select **Exclude only these boards**, then use the **Add board ID to exclude** field and **Add** button to enter IDs for boards you want the connector to exclude when crawling.

        As an example, you might enter `uXjVK7XkyFY=` to exclude searchable text content and metadata from the board with the specified ID.

7.  Select **Save and validate**.


## Result

The Miro external content connector is updated with your modified crawl settings.

## What to do next

To retrieve searchable text content and metadata from your Miro source system using your modified crawl settings, create and run a one-time content crawl for your Miro external content connector. To learn about creating and running one-time content crawls, see [Create a content crawl for an external content connector](create-content-crawl-external-content-connector.md).

**Parent Topic:**[Miro external content connector](../concept/miro-external-content-connector.md)

