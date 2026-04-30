---
title: Configure crawl settings for an Aha! Roadmaps external content connector
description: Specify the products you want your Aha! Roadmaps external content connector to crawl. Define inclusion or exclusion filters to dictate the types of content the crawl retrieves and feeds to AI Search for indexing.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-01-23"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Aha! Roadmaps external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Configure crawl settings for an Aha! Roadmaps external content connector

Specify the products you want your Aha! Roadmaps external content connector to crawl. Define inclusion or exclusion filters to dictate the types of content the crawl retrieves and feeds to AI Search for indexing.

## Before you begin

A connector admin must have already created the Aha! Roadmaps external content connector that you want to configure crawl settings for. To learn about this procedure, see [Create an Aha! Roadmaps external content connector](create-ext-cont-connector-aha-roadmaps.md).

Role required: sn\_ext\_conn.xcc\_admin

## About this task

This task is optional. By default, the Aha! Roadmaps external content connector crawls all products from its specified source system and sends all Features, Goals, Ideas, Notes, and Releases to AI Search for indexing. You only need to perform this task if you want the connector to use any of the following non-default settings:

-   Inclusion or exclusion filters for the products to crawl when running content crawls
-   Inclusion or exclusion filters for the content types to retrieve when running content crawls

Content is only retrieved from the source system if it passes all of your configured crawl setting filters. If any crawl setting filter excludes a content item, the external content connector doesn't retrieve it.

**Important:**

By default, each external content connector can index up to ten million \(10,000,000\) content items from its source system. When a connector exceeds this limit, it continues to crawl the source system, but only sends content item deletions and updates to AI Search for indexing, ignoring new content items. The connector logs an error message for every 10,000 content items it crawls beyond the indexing limit.

When a connector's indexed content item count exceeds 800,000, a warning message appears in the connector's UI to indicate that it's approaching the indexing limit. If the connector reaches the indexing limit, an error message appears in its UI.

External content connectors that support user permissions crawls can retrieve up to five hundred thousand \(500,000\) users.

If one of your connectors reaches the content indexing limit, you can update its crawl settings and file inclusion/exclusion filters to reduce the number of content items it retrieves. Alternately, if you need a connector to index more than 10,000,000 content items or to retrieve more than 500,000 users, you can create a Customer Service and Support case at [https://support.servicenow.com/now](https://support.servicenow.com/now) to request a limit increase for the connector.

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  In the Connectors list, select the record for the Aha! Roadmaps external content connector whose settings you want to modify.

3.  In the connector editor's Settings tab, select **Crawl settings**.

4.  In the Products section, select one of the following options:

    -   To crawl content found in all products from the source system, select **Crawl all products**.
    -   To crawl only content found in a specified set of products from the source system, select **Include only these products**, then use the **Add products to include** field and **Add** button to enter URLs for products whose content you want the connector to include when crawling.

        As an example, you might enter `https://example.aha.io/future-innovations` and `https://example.aha.io/launchpad-initiatives` to only retrieve searchable content from the specified products.

    -   To crawl content found in all but a specified set of products from the source system, select **Exclude only these products**, then use the **Add products to exclude** field and **Add** button to enter URLs for products whose content you want the connector to exclude when crawling.

        As an example, you might enter `https://example.aha.io/internal` and `https://example.aha.io/test` to exclude searchable content from the specified products.

5.  In the Crawl content types section, select the options for the Aha! Roadmaps content types \(Features, Goals, Ideas, Notes, and Releases\) that you want the connector to retrieve from products when running content crawls.

6.  Select **Save and validate**.


## Result

The Aha! Roadmaps external content connector is updated with your modified crawl settings.

## What to do next

To retrieve content from your Aha! Roadmaps source system using your modified crawl settings, create and run a one-time content crawl for your Aha! Roadmaps external content connector. To learn about creating and running one-time content crawls, see [Create a content crawl for an external content connector](create-content-crawl-external-content-connector.md).

**Parent Topic:**[Aha! Roadmaps external content connector](../concept/aha-roadmaps-external-content-connector.md)

