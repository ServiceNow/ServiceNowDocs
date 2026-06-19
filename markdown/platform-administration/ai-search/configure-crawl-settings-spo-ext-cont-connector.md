---
title: Configure crawl settings for the Microsoft SharePoint Online external content connector
description: Specify the sites you want your Microsoft SharePoint Online external content connector to crawl. Define inclusion or exclusion filters for file extensions to dictate the types of documents the crawl retrieves and feeds to AI Search for indexing.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/ai-search/configure-crawl-settings-spo-ext-cont-connector.html
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-06-02"
reading_time_minutes: 6
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Microsoft SharePoint Online external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Configure crawl settings for the Microsoft SharePoint Online external content connector

Specify the sites you want your Microsoft SharePoint Online external content connector to crawl. Define inclusion or exclusion filters for file extensions to dictate the types of documents the crawl retrieves and feeds to AI Search for indexing.

## Before you begin

A connector administrator must have already created the Microsoft SharePoint Online external content connector that you want to configure crawl settings for. To learn about this procedure, see [Create a Microsoft SharePoint Online external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/create-ext-cont-connector-mspo.md).

Role required: sn\_ext\_conn.xcc\_admin

## About this task

This task is optional. By default, the Microsoft SharePoint Online external content connector crawls all sites from its specified source system. It sends all supported content types, including files and attachments with all supported file extensions, to AI Search for indexing. Only perform this task if you want the connector to use any of the following non-default settings:

-   Inclusion or exclusion filters for the sites to crawl when running content crawls
-   Inclusion or exclusion filters for individual content types \(sites, lists, list items, attachments, and files\)
-   Inclusion or exclusion filters for the attachment file extensions to retrieve when running content crawls

Content is only retrieved from the source system if it passes all of your configured crawl setting filters. If any crawl setting filter excludes a content item, the external content connector doesn't retrieve it.

**Important:**

By default, the Microsoft SharePoint Online external content connector can index up to ten million \(10,000,000\) content items from its source system. When the connector exceeds this limit, it continues to crawl the source system, but only sends content item deletions and updates to AI Search for indexing, ignoring new content items. The connector logs an error message for every 10,000 content items it crawls beyond the indexing limit.

When the connector's indexed content item count exceeds eight million \(8,000,000\) content items, a warning message appears in the connector's UI to indicate that it's approaching the indexing limit. If the connector reaches the indexing limit, an error message appears in its UI.

The Microsoft SharePoint Online external content connector can handle permissions for up to five hundred thousand \(500,000\) users and their groups. If the connector retrieves users in excess of this limit, user and group permissions may not be correctly applied to the connector's retrieved content. As a result, the content may not be searchable.

If your Microsoft SharePoint Online connector reaches the content indexing limit, you can update its crawl settings and file inclusion/exclusion filters to reduce the number of content items it retrieves. Alternatively, if you need the connector to index more than 1,000,000 content items, you can create a Customer Service and Support case at [https://support.servicenow.com/now](https://support.servicenow.com/now) to request a limit increase for the connector.

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
    For details on configuring SharePoint API permissions for your Microsoft SharePoint Online sites, see [Configure Microsoft SharePoint Online for external content indexing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/cfg-azure-spo-ext-cont-connector.md) and [Configure site and site collection access for the Microsoft SharePoint Online external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/configure-site-collection-access-spo-external-content-connector.md).

5.  In the Content types section, deselect the options for any content types you want the connector to exclude when crawling.

    Supported content types include sites, lists, list items, attachments, and files.

    As an example, to exclude lists and list items from the connector's content crawls, deselect the **Lists** and **List items** options. You must include at least one content type.

6.  To apply inclusion or exclusion filters to a crawl based on file extensions, perform the following steps:

    1.  Select **Filter by file extension**.

    2.  To specify the type of filter, select **Include** or **Exclude**.

        Select **Include** if you want the crawl to only retrieve documents that have one of the specified file extensions. Select **Exclude** if you want the crawl to retrieve all documents except those that have one of the specified file extensions.

    3.  In the **File extension** field, select the file extensions that you want to include or exclude.

        For details on the supported file extensions, see [Binary file extensions supported in External Content Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/file-extensions-ext-cont-connector.md).

7.  Select **Save**.


## Result

The Microsoft SharePoint Online external content connector is updated with your crawl scope and file extension filter settings.

## What to do next

To retrieve content from your Microsoft SharePoint Online source system using your modified crawl settings, create and run a one-time content crawl for your Microsoft SharePoint Online external content connector. To learn about creating and running one-time content crawls, see [Create a content crawl for an external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/create-content-crawl-external-content-connector.md).

**Parent Topic:**[Microsoft SharePoint Online external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/microsoft-sharepoint-online-external-content-connector.md)

