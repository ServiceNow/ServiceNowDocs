---
title: Configure crawl settings for a Microsoft SharePoint Online external content connector
description: Specify the sites you want your Microsoft SharePoint Online external content connector to crawl. Define inclusion or exclusion filters to dictate the types of content the crawl retrieves and feeds to AI Search for indexing.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/search-administration/configure-crawl-settings-spo-ext-cont-connector.html
release: australia
product: Search Administration
classification: search-administration
topic_type: task
last_updated: "2026-06-02"
reading_time_minutes: 7
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Microsoft SharePoint Online external content connector, Configure, External Content Connectors, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure crawl settings for a Microsoft SharePoint Online external content connector

Specify the sites you want your Microsoft SharePoint Online external content connector to crawl. Define inclusion or exclusion filters to dictate the types of content the crawl retrieves and feeds to AI Search for indexing.

## Before you begin

A connector administrator must have already created the Microsoft SharePoint Online external content connector that you want to configure crawl settings for. To learn about this procedure, see [Create a Microsoft SharePoint Online external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/create-ext-cont-connector-mspo.md).

Role required: sn\_ext\_conn.xcc\_admin

## About this task

This task is optional. By default, the Microsoft SharePoint Online external content connector crawls all sites from its specified source system. It sends all supported content types, including files and attachments with all supported file extensions, to AI Search for indexing. Only perform this task if you want the connector to use any of the following non-default settings:

-   Inclusion or exclusion filters for the sites to crawl when running content crawls
-   Inclusion or exclusion filters for individual content types \(sites, lists, list items, attachments, and files\)
-   Inclusion or exclusion filters for the attachment file extensions to retrieve when running content crawls
-   Exclusion of guest users from Entra ID when retrieving users for user mappings.

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

    -   To crawl all sites from the source system, select **Crawl all content**.
    -   To crawl only a specified set of sites from the source system, select **Include only these sites**, then use the **Add URL** field and **Add** button to enter URLs for sites that you want to include in the crawl.

        For example, you might enter `https://example.sharepoint.com/sites/ProductionSite` to include only searchable content from the specified site.

    -   To crawl all except a specified set of sites from the source system, select **Exclude only these sites**, then use the **Add URL** field and **Add** button to enter URLs for sites that you want to exclude from the crawl.

        For example, you might enter `https://example.sharepoint.com/sites/TestSite` to exclude searchable content from the specified site.

    **Important:** The connector validates access permissions for your specified sites on every crawl. If it encounters a site that it doesn't have FullControl SharePoint API permission for, it records an alert for that site. The type of event depends on whether the site in question was automatically discovered or whether it was specified in your site inclusion list.

    -   If the connector automatically discovers a site that it doesn't have FullControl permission for, it records an informational alert indicating that it can't index that site.
    -   If the connector doesn't have FullControl SharePoint API permission for a site in your inclusion list, it records a warning alert indicating that it can't traverse \(crawl\) that site.
    For details on configuring SharePoint API permissions for your Microsoft SharePoint Online sites, see [Configure Microsoft SharePoint Online for external content indexing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/cfg-azure-spo-ext-cont-connector.md) and [Configure site and site collection access for the Microsoft SharePoint Online external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/configure-site-collection-access-spo-external-content-connector.md).

5.  In the Content types section, deselect the options for any content types you want the connector to exclude when crawling.

    Supported content types include sites, lists, list items, attachments, and files.

    As an example, to exclude lists and list items from the connector's content crawls, deselect the **Lists** and **List items** options. You must include at least one content type.

6.  Select one of the following **Attachment filtering** options:

    -   To retrieve all attachments with supported file extensions from the source system, select **Crawl all attachments**.
    -   To retrieve only attachments with specified file extensions from the source system, select **Include only these file extensions**, then use the **File extensions to include** field to enter attachment file extensions you want the connector to include when crawling.

        As an example, you might enter `.docx` to retrieve only attachments with the Microsoft Word file format.

    -   To retrieve all attachments except those with specified file extensions from the source system, select **Exclude only these file extensions**, then use the **File extensions to exclude** field to enter attachment file extensions you want the connector to exclude when crawling.

        As an example, you might enter `.csv` to exclude attachments with the Comma-Separated Values \(CSV\) file format.

    For details on the supported attachment file extensions, see [Binary file extensions supported in External Content Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/file-extensions-ext-cont-connector.md).

7.  If you want AI Search to automatically generate captions for content in attachments and files retrieved by the connector, select the **Multimodal captions** option.

    When you select this option, the Platform Multimodal Service automatically generates descriptive captions for images, tables, charts, and other visual elements found in retrieved attachments and files. You can discover these retrieved attachments and files by searching for terms from their generated captions.

    This option is only available when the Platform Multimodal Service plugin is activated on your instance.

    -   For details on activating the plugin, see [Activate the Platform Multimodal Service plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/activate-platform-multimodal-service-plugin.md).
    -   To learn how to select the VLM \(visual learning model\) provider and model used for the Platform Multimodal Service, see [Configure multimodal captioning for AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/configure-multimodal-captioning-for-ai-search.md).
8.  In the Users section, to exclude guest users when retrieving users from Entra ID, deselect the **Fetch guest users from Entra ID** option.

    **Note:** When the **Fetch guest users from Entra ID** option is selected, the connector retrieves guest users and tenant members from Entra ID. This can significantly increase the user corpus size for user mappings and can affect performance. With the option deselected, the connector only retrieves tenant members from Entra ID. Deselect this option unless mapping guest users from Entra ID to ServiceNow AI Platform users is a requirement for the external content connector.

9.  Select **Save**.


## Result

The Microsoft SharePoint Online external content connector is updated with your crawl scope and file extension filter settings.

## What to do next

To retrieve content from your Microsoft SharePoint Online source system using your modified crawl settings, create and run a one-time content crawl for your Microsoft SharePoint Online external content connector. To learn about creating and running one-time content crawls, see [Create a content crawl for an external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/create-content-crawl-external-content-connector.md).

**Parent Topic:**[Microsoft SharePoint Online external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/microsoft-sharepoint-online-external-content-connector.md)

