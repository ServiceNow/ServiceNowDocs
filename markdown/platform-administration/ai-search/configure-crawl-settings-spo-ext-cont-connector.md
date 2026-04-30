---
title: Configure crawl settings for a Microsoft SharePoint Online external content connector
description: Specify the sites you want your Microsoft SharePoint Online external content connector to crawl. Define inclusion or exclusion filters to dictate the types of content the crawl retrieves and feeds to AI Search for indexing.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-10-06"
reading_time_minutes: 5
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Microsoft SharePoint Online external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure crawl settings for a Microsoft SharePoint Online external content connector

Specify the sites you want your Microsoft SharePoint Online external content connector to crawl. Define inclusion or exclusion filters to dictate the types of content the crawl retrieves and feeds to AI Search for indexing.

## Before you begin

A connector admin must have already created the Microsoft SharePoint Online external content connector that you want to configure crawl settings for. To learn about this procedure, see [Create a Microsoft SharePoint Online external content connector](create-ext-cont-connector-mspo.md).

Role required: sn\_ext\_conn.xcc\_admin

## About this task

This task is optional. By default, the Microsoft SharePoint Online external content connector crawls all sites from its specified source system and sends documents with all supported file extensions to AI Search for indexing. You only need to perform this task if you want the connector to use any of the following non-default settings:

-   Inclusion or exclusion filters for the sites to crawl when running content crawls
-   Inclusion or exclusion filters for the attachment file extensions to retrieve when running content crawls

Content is only retrieved from the source system if it passes all of your configured crawl setting filters. If any crawl setting filter excludes a content item, the external content connector doesn't retrieve it.

**Important:**

By default, an external content connector can index up to one million \(1,000,000\) documents from its source system. When a connector exceeds this limit, it continues to crawl the source system, but only sends document deletions and updates to AI Search for indexing, ignoring new documents. The connector logs an error message for every 10,000 documents it crawls beyond the indexing limit.

When a connector's indexed document count exceeds 800,000, a warning message appears in the connector's UI to indicate that it's approaching the indexing limit. If the connector reaches the indexing limit, an error message appears in its UI.

If one of your connectors reaches the indexing limit, you can update its crawl settings and file inclusion/exclusion filters to reduce the number of documents it retrieves. Alternately, if you need to index more than 1,000,000 documents, you can create a Customer Service and Support case at [https://support.servicenow.com/now](https://support.servicenow.com/now) to request a limit increase for the connector.

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  In the Connectors list, select the record for the Microsoft SharePoint Online external content connector whose settings you want to modify.

3.  In the connector editor's Settings tab, select **Crawl settings**.

4.  Select one of the following **Content filtering** options:

    -   To crawl all sites from the source system, select **Crawl all content**.
    -   To crawl only a specified set of sites from the source system, select **Include only these sites**, then use the **Add URL** field and **Add** button to enter URLs for sites that you want to include in the crawl.

        For example, you might enter `https://example.sharepoint.com/sites/ProductionSite` to include only searchable content from the specified site.

    -   To crawl all except a specified set of sites from the source system, select **Exclude only these sites**, then use the **Add URL** field and **Add** button to enter URLs for sites that you want to exclude from the crawl.

        For example, you might enter `https://example.sharepoint.com/sites/TestSite` to exclude searchable content from the specified site.

    **Important:** The connector validates access permissions for your specified sites on every crawl. If it encounters a site that it doesn't have FullControl SharePoint API permission for, it records an alert for that site. The type of event depends on whether the site in question was automatically discovered or whether it was specified in your site inclusion list.

    -   If the connector automatically discovers a site that it doesn't have FullControl permission for, it records an informational alert indicating that it can't index that site.
    -   If the connector doesn't have FullControl SharePoint API permission for a site in your inclusion list, it records a warning alert indicating that it can't traverse \(crawl\) that site.
    For details on configuring SharePoint API permissions for your Microsoft SharePoint Online sites, see [Configure Microsoft SharePoint Online for external content indexing](cfg-azure-spo-ext-cont-connector.md) and [Configure site and site collection access for the Microsoft SharePoint Online external content connector](configure-site-collection-access-spo-external-content-connector.md).

5.  Select one of the following **Attachment filtering** options:

    -   To retrieve all attachments with supported file extensions from the source system, select **Crawl all attachments**.
    -   To retrieve only attachments with specified file extensions from the source system, select **Include only these file extensions**, then use the **File extensions to include** field to enter attachment file extensions you want the connector to include when crawling.

        As an example, you might enter `.docx` to retrieve only attachments with the Microsoft Word file format.

    -   To retrieve all attachments except those with specified file extensions from the source system, select **Exclude only these file extensions**, then use the **File extensions to exclude** field to enter attachment file extensions you want the connector to exclude when crawling.

        As an example, you might enter `.csv` to exclude attachments with the Comma-Separated Values \(CSV\) file format.

    For details on the supported attachment file extensions, see [Binary file extensions supported in External Content Connectors](../reference/file-extensions-ext-cont-connector.md).

6.  Select **Save**.


## Result

The Microsoft SharePoint Online external content connector is updated with your crawl scope and file extension filter settings.

## What to do next

To retrieve content from your Microsoft SharePoint Online source system using your modified crawl settings, create and run a one-time content crawl for your Microsoft SharePoint Online external content connector. To learn about creating and running one-time content crawls, see [Create a content crawl for an external content connector](create-content-crawl-external-content-connector.md).

**Parent Topic:**[Microsoft SharePoint Online external content connector](../concept/microsoft-sharepoint-online-external-content-connector.md)

