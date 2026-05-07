---
title: Configure crawl settings for a Smartsheet external content connector
description: Specify the items you want your Smartsheet external content connector to crawl. Define inclusion or exclusion filters to dictate the types of content the crawl retrieves and feeds to AI Search for indexing.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Smartsheet external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure crawl settings for a Smartsheet external content connector

Specify the items you want your Smartsheet external content connector to crawl. Define inclusion or exclusion filters to dictate the types of content the crawl retrieves and feeds to AI Search for indexing.

## Before you begin

A connector admin must have already created the Smartsheet external content connector that you want to configure crawl settings for. To learn about this procedure, see [Create a Smartsheet external content connector](create-ext-cont-connector-smartsheet.md).

Role required: sn\_ext\_conn.xcc\_admin

## About this task

This task is optional. By default, the Smartsheet external content connector crawls all workspaces from its specified source system and sends all sheets and attachments with all supported file extensions to AI Search for indexing. You only need to perform this task if you want the connector to use any of the following non-default settings:

-   Inclusion or exclusion filters for workspaces to crawl when running content crawls
-   Inclusion or exclusion filters for sheets to retrieve when running content crawls
-   Inclusion or exclusion filters for the attachment file extensions to retrieve when running content crawls
-   Inclusion or exclusion filters for the content types to retrieve when running content crawls

Content is only retrieved from the source system if it passes all of your configured crawl setting filters. If any crawl setting filter excludes a content item, the external content connector doesn't retrieve it.

**Important:**

By default, each external content connector can index up to ten million \(10,000,000\) content items from its source system. When a connector exceeds this limit, it continues to crawl the source system, but only sends content item deletions and updates to AI Search for indexing, ignoring new content items. The connector logs an error message for every 10,000 content items it crawls beyond the indexing limit.

When a connector's indexed content item count exceeds 800,000, a warning message appears in the connector's UI to indicate that it's approaching the indexing limit. If the connector reaches the indexing limit, an error message appears in its UI.

External content connectors that support user permissions crawls can handle permissions for up to five hundred thousand \(500,000\) users and their groups. If a connector retrieves users in excess of this limit, user and group permissions may not be correctly applied to the connector's retrieved content. As a result, the content may not be searchable.

If one of your connectors reaches the content indexing limit, you can update its crawl settings and file inclusion/exclusion filters to reduce the number of content items it retrieves. Alternatively, if you need a connector to index more than 10,000,000 content items, you can create a Customer Service and Support case at [https://support.servicenow.com/now](https://support.servicenow.com/now) to request a limit increase for the connector.

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  In the Connectors list, select the record for the Smartsheet external content connector whose settings you want to modify.

3.  In the connector editor's Settings tab, select **Crawl settings**.

4.  In the Workspaces, Sheets, Attachments, and Crawl content types sections, select the options for the items you want the connector to visit and retrieve when you run content crawls.

5.  Select one of the following **Workspaces** options:

    -   To crawl all workspaces found in the source system, select **Crawl all workspaces**.
    -   To crawl only a specified set of workspaces found in the source system, select **Include only these workspaces**, then use the **Add workspace name to include** field and **Add** button to enter names for workspaces you want the connector to include when crawling.

        As an example, you might enter `Project Horizon` to only retrieve content from this workspace.

    -   To crawl all but a specified set of workspaces found in the source system, select **Exclude only these workspaces**, then use the **Add workspace name to exclude** field and **Add** button to enter names for workspaces you want the connector to exclude when crawling.

        As an example, you might enter `Catalyst Programs` to exclude content from this workspace.

6.  Select one of the following **Sheets** options:

    -   To crawl all sheets found in the source system, select **Crawl all sheets**.
    -   To crawl only a specified set of sheets found in the source system, select **Include only these sheets**, then use the **Add sheet name to include** field and **Add** button to enter names for sheets you want the connector to include when crawling.

        As an example, you might enter `Efficiency Enhancements` to only retrieve content from sheets with this name.

    -   To crawl all but a specified set of sheets found in the source system, select **Exclude only these sheets**, then use the **Add sheet name to exclude** field and **Add** button to enter names for sheets you want the connector to exclude when crawling.

        As an example, you might enter `Future Plans` to exclude sheets with this name.

7.  Select one of the following **Attachments** options:

    -   To retrieve all attachments with supported file extensions from the source system, select **Crawl all attachments**.
    -   To retrieve only attachments with specified file extensions from the source system, select **Include only these file extensions**, then use the **File extensions to include** field to enter attachment file extensions you want the connector to include when crawling.

        As an example, you might enter `.docx` to retrieve only attachments with the Microsoft Word file format.

    -   To retrieve all attachments except those with specified file extensions from the source system, select **Exclude only these file extensions**, then use the **File extensions to exclude** field to enter attachment file extensions you want the connector to exclude when crawling.

        As an example, you might enter `.csv` to exclude attachments with the Comma-Separated Values \(CSV\) file format.

    For details on the supported attachment file extensions, see [Binary file extensions supported in External Content Connectors](../reference/file-extensions-ext-cont-connector.md).

8.  Select **Save and validate**.


## Result

The Smartsheet external content connector is updated with your modified crawl settings.

## What to do next

To retrieve content from your Smartsheet source system using your modified crawl settings, create and run a one-time content crawl for your Smartsheet external content connector. To learn about creating and running one-time content crawls, see [Create a content crawl for an external content connector](create-content-crawl-external-content-connector.md).

**Parent Topic:**[Smartsheet external content connector](../concept/smartsheet-external-content-connector.md)

