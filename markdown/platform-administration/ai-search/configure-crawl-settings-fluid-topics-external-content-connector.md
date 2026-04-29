---
title: Configure crawl settings for a Fluid Topics external content connector
description: Specify restrictions on source content status, visibility, category/collection, tags, languages, and modification dates for the Fluid Topics external content connector's content crawls. Define inclusion or exclusion filters to limit the content the crawl retrieves and feeds to AI Search for indexing.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Fluid Topics external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure crawl settings for a Fluid Topics external content connector

Specify restrictions on source content status, visibility, category/collection, tags, languages, and modification dates for the Fluid Topics external content connector's content crawls. Define inclusion or exclusion filters to limit the content the crawl retrieves and feeds to AI Search for indexing.

## Before you begin

A connector admin must have already created the Fluid Topics external content connector that you want to configure crawl settings for. To learn about this procedure, see [Create a Fluid Topics external content connector](create-ext-cont-connector-fluid-topics.md).

Role required: sn\_ext\_conn.xcc\_admin

## About this task

This task is optional. By default, the Fluid Topics external content connector crawls all content found in its specified source system and sends all retrieved items and binary files with all supported file extensions to AI Search for indexing. You only need to perform this task if you want the connector to use any of the following non-default settings:

-   Filter retrieved content by status when running content crawls
-   Filter retrieved content by visibility when running content crawls
-   Filter retrieved content based on its category/collection, tags, languages, or modification dates when running content crawls
-   Filter attachment binary files by extension when running content crawls

Content is only retrieved from the source system if it passes all of your configured crawl setting filters. If any crawl setting filter excludes a content item, the external content connector doesn't retrieve it.

**Important:**

By default, each external content connector can index up to ten million \(10,000,000\) content items from its source system. When a connector exceeds this limit, it continues to crawl the source system, but only sends content item deletions and updates to AI Search for indexing, ignoring new content items. The connector logs an error message for every 10,000 content items it crawls beyond the indexing limit.

When a connector's indexed content item count exceeds 800,000, a warning message appears in the connector's UI to indicate that it's approaching the indexing limit. If the connector reaches the indexing limit, an error message appears in its UI.

External content connectors that support user permissions crawls can retrieve up to five hundred thousand \(500,000\) users.

If one of your connectors reaches the content indexing limit, you can update its crawl settings and file inclusion/exclusion filters to reduce the number of content items it retrieves. Alternately, if you need a connector to index more than 10,000,000 content items or to retrieve more than 500,000 users, you can create a Customer Service and Support case at [https://support.servicenow.com/now](https://support.servicenow.com/now) to request a limit increase for the connector.

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  In the Connectors list, select the record for the Fluid Topics external content connector whose settings you want to modify.

3.  In the connector editor's Settings tab, select **Crawl settings**.

4.  Select one of the following **Status** options:

    -   To retrieve content with any status, select **All**.
    -   To retrieve only content with Published status, select **Published**.
    -   To retrieve only content with Draft status, select **Draft**.
5.  To crawl only content with public visibility, select the **Public visibility only** option.

    Selecting this option excludes all content that has user or group permission restrictions. With this option selected, the external content connector only retrieves content that's visible to all users in the source system.

6.  In the **Content** section, select one of the following category/collection options:

    -   To retrieve source system content from all categories and collections, select **Crawl all categories/collections**.
    -   To retrieve only source system content from a specified set of categories and collections, select **Include only these categories/collections**, then use the **Add categories/collections to include** field and **Add** button to enter names for categories or collections you want the connector to include when crawling.

        As an example, you might enter `Wiki` to only retrieve searchable content from this category or collection.

    -   To retrieve source system content from all but a specified set of categories and collections, select **Exclude only these categories/collections**, then use the **Add categories/collections to exclude** field and **Add** button to enter names for categories or collections you want the connector to exclude when crawling.

        As an example, you might enter `Confidential` to exclude searchable content from this category or collection.

7.  In the **Content** section, select one of the following tags options:

    -   To retrieve source system content with all tags, select **Crawl all tags**.
    -   To retrieve only source system content with a specified set of tags from the source system, select **Include only these tags**, then use the **Add tags to include** field and **Add** button to enter tags you want the connector to include when crawling.

        As an example, you might enter `Glossary` and `New` to only retrieve searchable content with the specified tags.

    -   To retrieve source system content with all but a specified set of tags, select **Exclude only these tags**, then use the **Add tags to exclude** field and **Add** button to enter tags you want the connector to exclude when crawling.

        As an example, you might enter `Draft` to exclude searchable content with the specified tag.

8.  In the **Content** section, select one of the following language options:

    -   To retrieve source system content in all languages, select **Crawl all languages**.
    -   To retrieve source system content in only a specified set of languages, select **Include only these languages**, then use the **Languages to include** field to enter two-letter identifier codes for languages you want the connector to include when crawling.

        As an example, you might enter `en` and `ja` to retrieve only searchable content in English or Japanese.

    -   To retrieve source system content in all but a specified set of languages from the source system, select **Exclude only these languages**, then use the **Languages to exclude** field to enter two-letter identifier codes for languages you want the connector to exclude when crawling.

        As an example, you might enter `en` and `fr` to exclude searchable content in English and French.

9.  In the **Content** section, select one of the following modification date options:

    -   To retrieve content modified within the last year, select **Modified last year**.
    -   To retrieve content modified within the last quarter, select **Modified last quarter**.
    -   To retrieve content modified within the last month, select **Modified last month**.
    -   To retrieve content modified within the last week, select **Modified last week**.
10. Select one of the following **Files** options:

    -   To retrieve all attachments with supported file extensions from the source system, select **Crawl all attachments**.
    -   To retrieve only attachments with specified file extensions from the source system, select **Include only these file extensions**, then use the **File extensions to include** field to enter attachment file extensions you want the connector to include when crawling.

        As an example, you might enter `.docx` to retrieve only attachments with the Microsoft Word file format.

    -   To retrieve all attachments except those with specified file extensions from the source system, select **Exclude only these file extensions**, then use the **File extensions to exclude** field to enter attachment file extensions you want the connector to exclude when crawling.

        As an example, you might enter `.csv` to exclude attachments with the Comma-Separated Values \(CSV\) file format.

    For details on the supported attachment file extensions, see [Binary file extensions supported in External Content Connectors](../reference/file-extensions-ext-cont-connector.md).

11. In the **Files** options, change the **Max file size \(MB\)** value to your desired value.

    AI Search only indexes content and metadata from retrieved attachment files that satisfy this file size limit. It ignores attachment files that exceed this file size limit.

12. Select **Save and validate**.


## Result

The Fluid Topics external content connector is updated with your modified crawl settings.

## What to do next

To retrieve content from your Fluid Topics source system using your modified crawl settings, create and run a one-time content crawl for your Fluid Topics external content connector. To learn about creating and running one-time content crawls, see [Create a content crawl for an external content connector](create-content-crawl-external-content-connector.md).

**Parent Topic:**[Fluid Topics external content connector](../concept/fluid-topics-external-content-connector.md)

