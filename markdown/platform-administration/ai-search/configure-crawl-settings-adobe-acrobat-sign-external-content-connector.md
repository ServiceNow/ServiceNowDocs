---
title: Configure crawl settings for an Adobe Acrobat Sign external content connector
description: Specify the agreement documents you want your Adobe Acrobat Sign external content connector to crawl. Define inclusion or exclusion filters to dictate the types of content the crawl retrieves and feeds to AI Search for indexing.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Adobe Acrobat Sign external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure crawl settings for an Adobe Acrobat Sign external content connector

Specify the agreement documents you want your Adobe Acrobat Sign external content connector to crawl. Define inclusion or exclusion filters to dictate the types of content the crawl retrieves and feeds to AI Search for indexing.

## Before you begin

A connector admin must have already created the Adobe Acrobat Sign external content connector that you want to configure crawl settings for. To learn about this procedure, see [Create an Adobe Acrobat Sign external content connector](create-ext-cont-connector-adobe-acrobat-sign.md).

Role required: sn\_ext\_conn.xcc\_admin

## About this task

This task is optional. By default, the Adobe Acrobat Sign external content connector crawls all agreements from its specified source system and sends all documents to AI Search for indexing. You only need to perform this task if you want the connector to use inclusion or exclusion filters for the agreements to crawl when running content crawls.

Content is only retrieved from the source system if it passes all of your configured crawl setting filters. If any crawl setting filter excludes a content item, the external content connector doesn't retrieve it.

**Important:**

By default, each external content connector can index up to ten million \(10,000,000\) content items from its source system. When a connector exceeds this limit, it continues to crawl the source system, but only sends content item deletions and updates to AI Search for indexing, ignoring new content items. The connector logs an error message for every 10,000 content items it crawls beyond the indexing limit.

When a connector's indexed content item count exceeds 800,000, a warning message appears in the connector's UI to indicate that it's approaching the indexing limit. If the connector reaches the indexing limit, an error message appears in its UI.

External content connectors that support user permissions crawls can handle permissions for up to five hundred thousand \(500,000\) users and their groups. If a connector retrieves users in excess of this limit, user and group permissions may not be correctly applied to the connector's retrieved content. As a result, the content may not be searchable.

If one of your connectors reaches the content indexing limit, you can update its crawl settings and file inclusion/exclusion filters to reduce the number of content items it retrieves. Alternatively, if you need a connector to index more than 10,000,000 content items, you can create a Customer Service and Support case at [https://support.servicenow.com/now](https://support.servicenow.com/now) to request a limit increase for the connector.

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  In the Connectors list, select the record for the Adobe Acrobat Sign external content connector whose settings you want to modify.

3.  In the connector editor's Settings tab, select **Crawl settings**.

4.  In the Agreements section, select one of the following agreement creation date filter options:

    -   To crawl only agreements created in the last year, select **Created last year**.
    -   To crawl only agreements created in the last quarter, select **Created last quarter**.
    -   To crawl only agreements created in the last month, select **Created last month**.
    -   To crawl only agreements created in the last week, select **Created last week**.
5.  In the Agreements section, select one of the following status filter options:

    -   To crawl agreements with all statuses from the source system, select **Crawl all statuses**.
    -   To crawl only agreements with a specified set of statuses from the source system, select **Include only these statuses**, then use the **Statuses to include** field to enter statuses you want the connector to include when crawling.

        As an example, you might enter `Approved` to only retrieve searchable content from agreements with this status.

    -   To crawl agreements with all but a specified set of statuses from the source system, select **Exclude only these statuses**, then use the **Statuses to exclude** field enter statuses you want the connector to exclude when crawling.

        As an example, you might enter `Cancelled` to exclude searchable content from agreements with this status.

6.  Select **Save and validate**.


## Result

The Adobe Acrobat Sign external content connector is updated with your modified crawl settings.

## What to do next

To retrieve content from your Adobe Acrobat Sign source system using your modified crawl settings, create and run a one-time content crawl for your Adobe Acrobat Sign external content connector. To learn about creating and running one-time content crawls, see [Create a content crawl for an external content connector](create-content-crawl-external-content-connector.md).

**Parent Topic:**[Adobe Acrobat Sign external content connector](../concept/adobe-acrobat-sign-external-content-connector.md)

