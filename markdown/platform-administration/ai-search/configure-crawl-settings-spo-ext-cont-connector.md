---
title: Configure crawl settings for the Microsoft SharePoint Online external content connector
description: Specify the sites you want your Microsoft SharePoint Online external content connector to crawl. Define inclusion or exclusion filters for file extensions to dictate the types of documents the crawl retrieves and feeds to AI Search for indexing.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-10-06"
reading_time_minutes: 5
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Microsoft SharePoint Online external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Configure crawl settings for the Microsoft SharePoint Online external content connector

Specify the sites you want your Microsoft SharePoint Online external content connector to crawl. Define inclusion or exclusion filters for file extensions to dictate the types of documents the crawl retrieves and feeds to AI Search for indexing.

## Before you begin

A connector admin must have already created the Microsoft SharePoint Online external content connector that you want to configure crawl settings for. To learn about this procedure, see [Create a Microsoft SharePoint Online external content connector](create-ext-cont-connector-mspo.md).

Role required: sn\_ext\_conn.xcc\_admin

## About this task

This task is optional. By default, the Microsoft SharePoint Online external content connector crawls all sites from its specified source system and sends documents with all supported file extensions to AI Search for indexing. You only need to perform this task if you want the connector to use any of the following non-default settings:

-   Inclusion or exclusion filters for the sites to crawl when running content crawls
-   Inclusion or exclusion filters for the attachment file extensions to retrieve when running content crawls

**Important:**

By default, each external content connector can index up to ten million \(10,000,000\) content items from its source system. When a connector exceeds this limit, it continues to crawl the source system, but only sends content item deletions and updates to AI Search for indexing, ignoring new content items. The connector logs an error message for every 10,000 content items it crawls beyond the indexing limit.

When a connector's indexed content item count exceeds 800,000, a warning message appears in the connector's UI to indicate that it's approaching the indexing limit. If the connector reaches the indexing limit, an error message appears in its UI.

External content connectors that support user permissions crawls can retrieve up to five hundred thousand \(500,000\) users.

If one of your connectors reaches the content indexing limit, you can update its crawl settings and file inclusion/exclusion filters to reduce the number of content items it retrieves. Alternately, if you need a connector to index more than 10,000,000 content items or to retrieve more than 500,000 users, you can create a Customer Service and Support case at [https://support.servicenow.com/now](https://support.servicenow.com/now) to request a limit increase for the connector.

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  In the Connectors list, select the record for the Microsoft SharePoint Online external content connector whose settings you want to modify.

3.  In the connector editor's Settings tab, select **Crawl settings**.

4.  Select one of the following **Content filtering** options:

    -   To crawl all sites from the source system, select **All**, then optionally select **Exclude sites** and use the **Add URL** field and **Add** button to enter the SiteCollection, Site, or SubSite URLs for sites that you want to exclude from the crawl.

        **Note:** The **Exclude sites** option only accepts SiteCollection, Site, and SubSite URLs. Don't enter other types of URL when using this option.

    -   To crawl only a specified set of sites from the source system, select **Specify**, then use the **Add URL** field and **Add** button to enter the SiteCollection URLs for sites that you want to include in the crawl.

        **Note:** The **Specify** option only accepts SiteCollection URLs. Don't add other types of URL when using this option.

    **Important:** The connector validates access permissions for your specified sites on every crawl. If it encounters a site that it doesn't have FullControl SharePoint API permission for, it records an alert for that site. The type of event depends on whether the site in question was automatically discovered or whether it was specified in your site inclusion list.

    -   If the connector automatically discovers a site that it doesn't have FullControl permission for, it records an informational alert indicating that it can't index that site.
    -   If the connector doesn't have FullControl SharePoint API permission for a site in your inclusion list, it records a warning alert indicating that it can't traverse \(crawl\) that site.
    For details on configuring SharePoint API permissions for your Microsoft SharePoint Online sites, see [Configure Microsoft SharePoint Online for external content indexing](cfg-azure-spo-ext-cont-connector.md) and [Configure site and site collection access for the Microsoft SharePoint Online external content connector](configure-site-collection-access-spo-external-content-connector.md).

5.  To apply inclusion or exclusion filters to a crawl based on file extensions, perform the following steps:

    1.  Select **Filter by file extension**.

    2.  To specify the type of filter, select **Include** or **Exclude**.

        Select **Include** if you want the crawl to only retrieve documents that have one of the specified file extensions. Select **Exclude** if you want the crawl to retrieve all documents except those that have one of the specified file extensions.

    3.  In the **File extension** field, select the file extensions that you want to include or exclude.

        For details on the supported file extensions, see [Binary file extensions supported in External Content Connectors](../reference/file-extensions-ext-cont-connector.md).

6.  Select **Save**.


## Result

The Microsoft SharePoint Online external content connector is updated with your crawl scope and file extension filter settings.

## What to do next

To retrieve content from your Microsoft SharePoint Online source system using your modified crawl settings, create and run a one-time content crawl for your Microsoft SharePoint Online external content connector. To learn about creating and running one-time content crawls, see [Create a content crawl for an external content connector](create-content-crawl-external-content-connector.md).

**Parent Topic:**[Microsoft SharePoint Online external content connector](../concept/microsoft-sharepoint-online-external-content-connector.md)

