---
title: Microsoft SharePoint Online external content connector
description: The Microsoft SharePoint Online external content connector retrieves pages from sites in your Microsoft SharePoint Online source system and makes their content and metadata searchable in AI Search applications.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2025-08-04"
reading_time_minutes: 4
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Microsoft SharePoint Online external content connector

The Microsoft SharePoint Online external content connector retrieves pages from sites in your Microsoft SharePoint Online source system and makes their content and metadata searchable in AI Search applications.

Connector administrators can run or schedule content crawls to retrieve updated content and access permissions from your source system, or user permission crawls to retrieve updated security principals from your source system. Both types of crawl feed their data to AI Search for indexing.

The indexed content and metadata are stored as records in a connector-specific indexed source. Search administrators can create search sources from this indexed source and link them to search profiles to make the indexed records searchable in AI Search applications.

## Microsoft SharePoint Online static and dynamic page content

Microsoft SharePoint Online pages built primarily with static text content authored in the Microsoft SharePoint Online editor produce searchable content that more closely matches what users see in a web browser. By contrast, pages that rely on dynamic web parts may not contain all of the content that users see in a web browser.

Microsoft SharePoint Online pages are stored as `.aspx` files in a site's Site Pages library. These files can include static content in their CanvasContent1 and WikiFields metadata fields, but they can also include scripts that call a server-side engine to dynamically render viewable content at request time. The exact content rendered depends on user context, permissions, and web parts loaded as part of the page request.

Rendering a page's full viewable content requires an authenticated user session. The Microsoft SharePoint Online connector can't impersonate a user to trigger this rendering process. As a result, the connector cannot capture the final HTML output that a web browser would display.

For each page retrieved, the Microsoft SharePoint Online connector queries the SharePoint REST API's `_api/web/lists('<list-id>')/items(<item-id>)` endpoint to access the page's underlying list item. Via this API endpoint, the connector retrieves content primarily from the page's CanvasContent1 and WikiFields metadata fields, and also captures the page's other metadata fields such as title, author, and modification date where available. Page content stored exclusively in dynamic web parts may be retrieved only partially or not at all, since that content doesn't exist in the list item metadata.

To learn how to view the portion of a page's content that can be retrieved using the Microsoft SharePoint Online connector, see [View retrievable page content using the Microsoft SharePoint Online REST API](../task/view-retrievable-page-content-mspo-rest-api.md).

-   **[Estimate document volume for Microsoft SharePoint Online](../task/estimate-doc-volume-mspo.md)**  
Estimate the total number of documents included in your Microsoft SharePoint Online source system and the document counts for individual sites. Use this information to determine crawl scope settings needed for your Microsoft SharePoint Online external content connector.
-   **[Create a public/private key pair for the Microsoft SharePoint Online external content connector](../task/gen-cert-spo-ext-cont-connector.md)**  
Generate a public/private key pair for the Microsoft SharePoint Online external content connector. Extract the public key as a DER-encoded binary X.509 format certificate for use in configuring API access for the connector in the Microsoft Entra admin center.
-   **[Configure Microsoft SharePoint Online for external content indexing](../task/cfg-azure-spo-ext-cont-connector.md)**  
Register an OAuth 2.0 application in the Microsoft Entra admin center to allow the Microsoft SharePoint Online external content connector to access your Microsoft SharePoint Online source system.
-   **[Configure site and site collection access for the Microsoft SharePoint Online external content connector](../task/configure-site-collection-access-spo-external-content-connector.md)**  
Allow the Microsoft SharePoint Online connector to crawl your sites and site collections by granting site-specific SharePoint API FullControl permissions to the OAuth 2.0 app registered in Microsoft Entra for the connector.
-   **[Create a Microsoft SharePoint Online external content connector](../task/create-ext-cont-connector-mspo.md)**  
Create an external content connector to retrieve searchable content and security principals from your Microsoft SharePoint Online source system.
-   **[Configure crawl settings for the Microsoft SharePoint Online external content connector](../task/configure-crawl-settings-spo-ext-cont-connector.md)**  
Specify the sites you want your Microsoft SharePoint Online external content connector to crawl. Define inclusion or exclusion filters for file extensions to dictate the types of documents the crawl retrieves and feeds to AI Search for indexing.
-   **[View retrievable page content using the Microsoft SharePoint Online REST API](../task/view-retrievable-page-content-mspo-rest-api.md)**  
Review the elements of of a Microsoft SharePoint Online page's content that can be retrieved by the Microsoft SharePoint Online external content connector.

**Parent Topic:**[Configuring External Content Connectors](configuring-ext-cont-connectors.md)

**Related topics**  


[Create a content crawl for an external content connector](../task/create-content-crawl-external-content-connector.md)

[Create a user permission crawl for an external content connector](../task/create-user-mapping-crawl-external-content-connector.md)

