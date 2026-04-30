---
title: Configure crawl settings for a Docusign external content connector
description: Define inclusion or exclusion filters to control which agreements you want your Docusign external content connector to make searchable.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-10-14"
reading_time_minutes: 4
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Docusign external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Configure crawl settings for a Docusign external content connector

Define inclusion or exclusion filters to control which agreements you want your Docusign external content connector to make searchable.

## Before you begin

A connector admin must have already created the Docusign external content connector that you want to configure crawl settings for. To learn about this procedure, see [Create a Docusign external content connector](create-ext-cont-connector-docusign.md).

Role required: sn\_ext\_conn.xcc\_admin

## About this task

This task is optional. By default, the Docusign external content connector retrieves agreements from all envelopes in its specified source system and sends them to AI Search for indexing. You only need to perform this task if you want to apply any of the following filters to limit which envelopes the connector retrieves agreements from when running content crawls:

-   Inclusion or exclusion filter based on the sent date of the envelope
-   Inclusion or exclusion filter based on the name of the envelope
-   Inclusion or exclusion filter based on the status of the envelope

Content is only retrieved from the source system if it passes all of your configured crawl setting filters. If any crawl setting filter excludes a content item, the external content connector doesn't retrieve it.

**Important:**

By default, each external content connector can index up to ten million \(10,000,000\) content items from its source system. When a connector exceeds this limit, it continues to crawl the source system, but only sends content item deletions and updates to AI Search for indexing, ignoring new content items. The connector logs an error message for every 10,000 content items it crawls beyond the indexing limit.

When a connector's indexed content item count exceeds 800,000, a warning message appears in the connector's UI to indicate that it's approaching the indexing limit. If the connector reaches the indexing limit, an error message appears in its UI.

External content connectors that support user permissions crawls can retrieve up to five hundred thousand \(500,000\) users.

If one of your connectors reaches the content indexing limit, you can update its crawl settings and file inclusion/exclusion filters to reduce the number of content items it retrieves. Alternately, if you need a connector to index more than 10,000,000 content items or to retrieve more than 500,000 users, you can create a Customer Service and Support case at [https://support.servicenow.com/now](https://support.servicenow.com/now) to request a limit increase for the connector.

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  In the Connectors list, select the record for the Docusign external content connector whose settings you want to modify.

3.  In the connector editor's Settings tab, select **Crawl settings**.

4.  Select one of the following **Date** options:

    -   To only retrieve content from agreements in envelopes that were sent in the last year, select **Sent last year**.
    -   To only retrieve content from agreements in envelopes that were sent in the last quarter, select **Sent last quarter**.
    -   To only retrieve content from agreements in envelopes that were sent in the last month, select **Sent last month**.
    -   To only retrieve content from agreements in envelopes that were sent in the last week, select **Sent last week**.
5.  Select one of the following **Envelopes** options:

    -   To crawl all envelopes from the source system, select **Crawl all envelopes**.
    -   To crawl only a specified set of envelopes from the source system, select **Include only these envelopes**, then use the **Add ID to include** field and **Add** button to enter IDs for envelopes you want the connector to include when crawling.

        As an example, you might enter `CS313157`, `CS214083`, and `CS990276` to only retrieve searchable content from the three specified envelopes.

    -   To crawl all but a specified set of envelopes from the source system, select **Exclude only these envelopes**, then use the **Add ID to exclude** field and **Add** button to enter IDs for envelopes you want the connector to exclude when crawling.

        As an example, you might enter `CS398287` to exclude searchable content from the specified envelope.

6.  Select one of the following **Status** options:

    -   To crawl envelopes with any status from the source system, select **Crawl all statuses**.
    -   To crawl only envelopes with a specified set of statuses from the source system, select **Include only these statuses**, then use the **Status to include** field and **Add** button to enter statuses you want the connector to include when crawling.

        As an example, you might enter `published` to only retrieve searchable content from envelopes with the specified status.

    -   To crawl envelopes with all but a specified set of statuses from the source system, select **Exclude only these statuses**, then use the **Status to exclude** field and **Add** button to enter statuses you want the connector to exclude when crawling.

        As an example, you might enter `draft` to exclude searchable content from envelopes with the specified status.

7.  Select **Save and validate**.


## Result

The Docusign external content connector is updated with your modified crawl settings.

## What to do next

To retrieve content from your Docusign source system using your modified crawl settings, create and run a one-time content crawl for your Docusign external content connector. To learn about creating and running one-time content crawls, see [Create a content crawl for an external content connector](create-content-crawl-external-content-connector.md).

**Parent Topic:**[Docusign external content connector](../concept/docusign-external-content-connector.md)

