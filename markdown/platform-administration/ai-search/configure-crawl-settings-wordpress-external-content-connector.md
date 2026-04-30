---
title: Configure crawl settings for a WordPress external content connector
description: Specify the pages and blog posts you want your WordPress external content connector to crawl. Define inclusion or exclusion filters to dictate the types of content the crawl retrieves and feeds to AI Search for indexing.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-10-06"
reading_time_minutes: 7
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [WordPress external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Configure crawl settings for a WordPress external content connector

Specify the pages and blog posts you want your WordPress external content connector to crawl. Define inclusion or exclusion filters to dictate the types of content the crawl retrieves and feeds to AI Search for indexing.

## Before you begin

A connector admin must have already created the WordPress external content connector that you want to configure crawl settings for. To learn about this procedure, see [Create a WordPress external content connector](create-ext-cont-connector-wordpress.md).

Role required: sn\_ext\_conn.xcc\_admin

## About this task

This task is optional. By default, the WordPress external content connector crawls all pages and blog posts from its specified source system and sends attachments with all supported file extensions to AI Search for indexing. You only need to perform this task if you want the connector to use any of the following non-default settings:

-   Inclusion or exclusion filters for the pages and blog posts to crawl when running content crawls
-   Inclusion or exclusion filters for the file extensions to retrieve when running content crawls

Content is only retrieved from the source system if it passes all of your configured crawl setting filters. If any crawl setting filter excludes a content item, the external content connector doesn't retrieve it.

**Important:**

By default, each external content connector can index up to ten million \(10,000,000\) content items from its source system. When a connector exceeds this limit, it continues to crawl the source system, but only sends content item deletions and updates to AI Search for indexing, ignoring new content items. The connector logs an error message for every 10,000 content items it crawls beyond the indexing limit.

When a connector's indexed content item count exceeds 800,000, a warning message appears in the connector's UI to indicate that it's approaching the indexing limit. If the connector reaches the indexing limit, an error message appears in its UI.

External content connectors that support user permissions crawls can retrieve up to five hundred thousand \(500,000\) users.

If one of your connectors reaches the content indexing limit, you can update its crawl settings and file inclusion/exclusion filters to reduce the number of content items it retrieves. Alternately, if you need a connector to index more than 10,000,000 content items or to retrieve more than 500,000 users, you can create a Customer Service and Support case at [https://support.servicenow.com/now](https://support.servicenow.com/now) to request a limit increase for the connector.

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  In the Connectors list, select the record for the WordPress external content connector whose settings you want to modify.

3.  In the connector editor's Settings tab, select **Crawl settings**.

4.  Select one of the following **Pages** options:

    -   To crawl all pages from the source system, select **Crawl all pages**.
    -   To crawl only a specified set of pages from the source system, select **Include only these pages**, then use the **Add page URL to include** field and **Add** button to enter URLs for pages you want the connector to include when crawling.

        As an example, you might enter `https://example.com/mainSite/mainPage` to only retrieve searchable content from this page.

    -   To crawl all but a specified set of pages from the source system, select **Exclude only these pages**, then use the **Add page URL to exclude** field and **Add** button to enter URLs for pages you want the connector to exclude when crawling.

        As an example, you might enter `https://example.com/testSite/testPage` to exclude searchable content from this page.

5.  Select one of the following **Blog posts** options:

    -   To crawl all blog posts from the source system, select **Crawl all blog posts**.
    -   To crawl only a specified set of blog posts from the source system, select **Include only these blog posts**, then use the **Add URL to include** field and **Add** button to enter URLs for blog posts you want the connector to include when crawling.

        As an example, you might enter `https://example.com/blog/latestContent` to only retrieve searchable content from this blog post.

    -   To crawl all but a specified set of blog posts from the source system, select **Exclude only these blog posts**, then use the **Add URL to exclude** field and **Add** button to enter URLs for blog posts you want the connector to exclude when crawling.

        As an example, you might enter `https://example.com/blog/testPost` to exclude searchable content from this blog post.

6.  Select one of the following **Categories** options:

    -   To retrieve blog posts that belong to all categories from the source system, select **Crawl all categories**.
    -   To retrieve only blog posts belonging to a specified set of categories from the source system, select **Include only these categories**, then use the **Categories to include** field and **Add** button to enter URLs for categories you want the connector to include when crawling blog posts.

        As an example, you might enter `Company news`, `Tech blog`, and `Press events` to only retrieve searchable content from blog posts that belong to the specified categories.

    -   To retrieve blog posts belonging to all but a specified set of categories from the source system, select **Exclude only these blog posts**, then use the **Categories to exclude** field and **Add** button to enter URLs for categories you want the connector to exclude when crawling blog posts.

        As an example, you might enter `Testing` to exclude searchable content from blog posts that belong to the specified category.

7.  Select one of the following **Date** options:

    -   To retrieve pages and blog posts from the source system that were modified in the last year, select **Modified last year**.
    -   To retrieve pages and blog posts from the source system that were modified in the last quarter, select **Modified last quarter**.
    -   To retrieve pages and blog posts from the source system that were modified in the last month, select **Modified last month**.
    -   To retrieve pages and blog posts from the source system that were modified in the last week, select **Modified last week**.
8.  Select one of the following **State** options:

    -   To retrieve pages and blog posts with all states from the source system, select **Crawl all states**.
    -   To retrieve only pages and blog posts with a specified set of states from the source system, select **Include only these states**, then use the **States to include** field and **Add** button to enter states you want the connector to include when crawling.

        As an example, you might enter `publish` to only retrieve pages and blog that have this state.

    -   To retrieve pages and blog posts with all but a specified set of states from the source system, select **Exclude only these states**, then use the **States to exclude** field and **Add** button to enter states you want the connector to exclude when crawling.

        As an example, you might enter `private`, `future`, `pending`, and `draft` to exclude pages and blog that have any of the specified states.

9.  Select one of the following **Attachments** options:

    -   To retrieve all attachments with supported file extensions from the source system, select **Crawl all attachments**.
    -   To retrieve only attachments with specified file extensions from the source system, select **Include only these file extensions**, then use the **File extensions to include** field to enter attachment file extensions you want the connector to include when crawling.

        As an example, you might enter `.docx` to retrieve only attachments with the Microsoft Word file format.

    -   To retrieve all attachments except those with specified file extensions from the source system, select **Exclude only these file extensions**, then use the **File extensions to exclude** field to enter attachment file extensions you want the connector to exclude when crawling.

        As an example, you might enter `.csv` to exclude attachments with the Comma-Separated Values \(CSV\) file format.

    For details on the supported attachment file extensions, see [Binary file extensions supported in External Content Connectors](../reference/file-extensions-ext-cont-connector.md).

10. Select **Save and validate**.


## Result

The WordPress external content connector is updated with your modified crawl settings.

## What to do next

To retrieve content from your WordPress source system using your modified crawl settings, create and run a one-time content crawl for your WordPress external content connector. To learn about creating and running one-time content crawls, see [Create a content crawl for an external content connector](create-content-crawl-external-content-connector.md).

**Parent Topic:**[WordPress external content connector](../concept/wordpress-external-content-connector.md)

