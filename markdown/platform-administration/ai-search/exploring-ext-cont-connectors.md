---
title: Exploring External Content Connectors
description: Using External Content Connectors, AI Search applications can search content and metadata from external content repositories such as Atlassian Confluence Cloud and Microsoft SharePoint Online. Expanding search recall to include external content makes it easier and faster for search users to locate the information they need.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Exploring External Content Connectors

Using External Content Connectors, AI Search applications can search content and metadata from external content repositories such as Atlassian Confluence Cloud and Microsoft SharePoint Online. Expanding search recall to include external content makes it easier and faster for search users to locate the information they need.

## External Content Connectors overview

The External Content Connectors application adds support for indexing content and metadata from external source systems to make those systems searchable in AI Search applications. Indexing preserves the content's original user access permissions from the source system using AI Search's content security model.

The current release includes these external content connectors:

-   Adobe Acrobat Sign external content connector
-   Adobe Experience Manager as a Cloud Service external content connector
-   Aha! Roadmaps external content connector
-   Amazon S3 external content connector
-   Asana external content connector
-   Atlassian Confluence Cloud external content connector
-   Atlassian Jira Cloud external content connector
-   Box external content connector
-   Cornerstone external content connector
-   Docusign external content connector
-   Fluid Topics external content connector
-   Dropbox external content connector
-   GitHub Enterprise Cloud external content connector
-   GitLab external content connector
-   Google Drive external content connector
-   HubSpot external content connector
-   Lucidchart external content connector
-   ManageEngine external content connector
-   Microsoft OneDrive external content connector
-   Microsoft SharePoint Online external content connector
-   Microsoft Teams external content connector
-   Microsoft Viva Engage external content connector
-   Miro external content connector
-   monday.com external content connector
-   Notion external content connector
-   SAP DMS external content connector
-   ServiceNow documentation external content connector
-   ServiceNow instance external content connector
-   Slack external content connector
-   Smartsheet external content connector
-   Trello external content connector
-   Webcrawler external content connector
-   WordPress external content connector
-   Workday external content connector
-   Workvivo external content connector
-   Zendesk Guide external content connector
-   Zoom external content connector

Connector administrators can schedule content and user permission crawls to suit your indexing requirements. If the need arises, connector administrators can also run either type of crawl on demand.

**Important:** The External Content Connectors application consumes Integration Hub transactions when feeding crawled content to AI Search. You can monitor available and used transactions for your Integration Hub subscription packages in the Integration Hub Usage Dashboard. For details on transaction monitoring, see [Transaction reports in Integration Hub Usage Dashboard](https://www.servicenow.com/docs/access?context=use-the-integration-hub-usage-dashboard&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

Each external content connector has its own indexed source for crawled content. You can configure search sources for an external content connector's indexed source and include those search sources in your search profiles, just as you would for any other indexed source. To learn more about indexed sources, see [Indexed sources in AI Search](indexed-sources-ais.md).

All external content connectors support semantic vector indexing of content retrieved from crawled source systems. Only features which use semantic vector search with the Now LLM Service can take advantage of this support. For details on semantic vector indexing and search, see [Semantic vector search in AI Search](semantic-search-ais.md).

## External Content Connectors workflow

In this infographic, see a sample workflow of how different users in an organization interact with External Content Connectors to enable indexing and search of content and metadata from supported external sources.

![Infographic showing how connector admins, AI Search users, and AI Search high security administrators work with the External Content Connectors to enable search for content from source systems. For details, refer to the following description.](../image/exploring-external-content-connectors.svg "Configuring and using External Content Connectors")

In this External Content Connectors workflow:

1.  Connector administrators configure connection settings for external content connectors, configure crawl start points and inclusion/exclusion filters to define the scope of connector crawls, and define schedules that specify when crawls run.
2.  The system runs connectors at their scheduled times or when connector administrators start one-time crawls. When crawling, connectors retrieve searchable content and security principals from their source systems and feed them to AI Search for indexing.
3.  Search users are presented with content and metadata from external content source systems when interacting with AI Search applications. AI Search's content security model retains user and group access permissions set in the source system, so users can only view content that they have permission to access.
4.  Connector administrators review and analyze crawl metrics, crawl histories, and user permission data to understand how external data is crawled and indexed, allowing for more effective tuning of crawl settings for their external content connectors.

**Important:**

By default, each external content connector can index up to ten million \(10,000,000\) content items from its source system. When a connector exceeds this limit, it continues to crawl the source system, but only sends content item deletions and updates to AI Search for indexing, ignoring new content items. The connector logs an error message for every 10,000 content items it crawls beyond the indexing limit.

When a connector's indexed content item count exceeds 800,000, a warning message appears in the connector's UI to indicate that it's approaching the indexing limit. If the connector reaches the indexing limit, an error message appears in its UI.

External content connectors that support user permissions crawls can handle permissions for up to five hundred thousand \(500,000\) users and their groups. If a connector retrieves users in excess of this limit, user and group permissions may not be correctly applied to the connector's retrieved content. As a result, the content may not be searchable.

If one of your connectors reaches the content indexing limit, you can update its crawl settings and file inclusion/exclusion filters to reduce the number of content items it retrieves. Alternatively, if you need a connector to index more than 10,000,000 content items, you can create a Customer Service and Support case at [https://support.servicenow.com/now](https://support.servicenow.com/now) to request a limit increase for the connector.

## External Content Connectors benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Configure source systems for external content indexing|[Configuring source systems for external content indexing](cfg-src-sys-ext-content-indexing.md)|Source system administrators|
|Create connectors to retrieve searchable content and metadata and user permissions from supported external data source systems|[Creating external content connectors](../task/creating-ext-cont-connectors.md)|Connector administrators|
|Control the scope of external content connector crawls by specifying source system locations to crawl and content types to feed to AI Search for indexing|[Configuring crawl settings for external content connectors](cfg-crawl-settings-ext-cont-connector.md)|Connector administrators|
|Update searchable content and metadata from source systems on demand or on a scheduled recurring basis|[Create a content crawl for an external content connector](../task/create-content-crawl-external-content-connector.md)|Connector administrators|
|Update user and group access permissions from source systems on demand or on a scheduled recurring basis|[Create a user permission crawl for an external content connector](../task/create-user-mapping-crawl-external-content-connector.md)|Connector administrators|
|Review metrics for source system items retrieved by content crawls|[Review crawl history for an external content connector](../task/review-crawl-ext-cont-connector.md)|Connector administrators|
|Review user and group access permissions retrieved by user permission crawls|[Review user permissions for an external content connector](../task/review-usr-maps-ext-cont-connector.md)|Search high security administrators|
|Search content and metadata indexed from external data source systems|[Searching in AI Search](use-ais.md)|AI Search users|

## Interaction with Now Assist Genius Results

If you have the Now Assist in AI Search and Now Assist in Virtual Agent ServiceNow Store applications installed, external content search results are eligible for inclusion in Now Assist Multi-Content Response Genius Result answers. This includes answers generated for in Now Assist in Virtual Agent chat.

External content search results are ignored when generating Now Assist Q&amp;A or Now Assist Actions Genius Result answers.

-   **[Estimating document volume for source systems](estimating-doc-volume-src-sys.md)**  
Source system tools allow you to estimate the number of documents available for retrieval by external content connectors. By estimating the available document count for a source system, you can determine whether you need to apply crawl scope restrictions when configuring an external content connector for that source system.
-   **[Configuring source systems for external content indexing](cfg-src-sys-ext-content-indexing.md)**  
Source system administrators configure settings to allow external content connectors to index your documents and security settings for search. These settings must be configured for a source system before you create an external content connector to crawl that source system.
-   **[Creating external content connectors](../task/creating-ext-cont-connectors.md)**  
Connector administrators can create external content connectors to retrieve searchable content and metadate and security permissions from supported source systems.
-   **[Configuring crawl settings for external content connectors](cfg-crawl-settings-ext-cont-connector.md)**  
Connector administrators can configure crawl settings for each external content connector, such as which source system locations it crawls and which types of content it sends to AI Search for indexing.
-   **[Domain separation and External Content Connectors](ext-cont-connectors-domain-separation.md)**  
Domain separation is unsupported for External Content Connectors. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

**Parent Topic:**[External Content Connectors](../reference/ext-cont-connectors-landing-page.md)

