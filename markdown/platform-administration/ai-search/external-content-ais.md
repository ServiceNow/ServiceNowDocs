---
title: Indexing and searching external content in AI Search
description: With a subscription for the External Content for AI Search plugin, you can enable AI Search users to search content and metadata from documents in external repositories and remote tables.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Configuring AI Search, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Indexing and searching external content in AI Search

With a subscription for the External Content for AI Search plugin, you can enable AI Search users to search content and metadata from documents in external repositories and remote tables.

The External Content for AI Search plugin enables you to index documents located outside of your ServiceNow AI Platform® instance, such as those stored in SharePoint collections, Confluence sites, and [remote tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/remote-tables/remote-tables.md). Indexing these documents makes their content and metadata searchable in AI Search.

AI Search displays search results for indexed external documents just as it does for indexed ServiceNow AI Platform records. Users don't need to perform any special searches to match content and metadata from external documents.

Indexing doesn't duplicate external documents as records in your ServiceNow AI Platform instance. When a user selects an external document search result, they are directed to the source document in its original location.

## External content indexing tools

The following diagram illustrates how AI Search provides indexing and search for external document content and metadata:

![Diagram showing AI Search indexing and search options for external documents.](../image/ai-search-external-content-diagram.png "AI Search external content architecture diagram")

As shown in the architecture diagram, you can index content and metadata from external documents using any or all of the following tools:

<table id="table_cyt_kyw_ksb"><thead><tr><th>

External content indexing tool

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Search connector applications

</td><td>

Search connector applications available in the ServiceNow Store provide simple tools for indexing content and metadata from documents in supported external sources. They handle some of the configuration work, such as creation of external content schema tables, for you. Each search connector application supports a specific external document source \(or set of sources\). For example, the [SharePoint Online Search Connector](https://store.servicenow.com/sn_appstore_store.do#!/store/application/32e3b8addb2a5450e7048d7e13961908/) only supports documents in SharePoint collections, while the [Raytion Connector Hub for AI Search](https://store.servicenow.com/sn_appstore_store.do#!/store/application/f7a8af54db9ee01035d0c6cd13961901/) supports multiple document sources. If no search connector application is available for your external document source, you must use the Integration Hub AI Search spoke or the External Content REST API to index content and metadata for documents from that source.

 Search connector applications provide the most straightforward way to index document content and metadata from supported external sources.

</td></tr><tr><td>

Integration Hub AI Search spoke

</td><td>

The Integration Hub AI Search spoke provides Workflow Studio actions that you can use to ingest external documents for indexing:-   **Ingest Document**: Define property name-value pairs for an external document and submit the document to AI Search for indexing.
-   **Ingest Document Using Download URL**: Specify an external document's URL and have AI Search download it for indexing.

 You can specify security principal access permissions for documents ingested using these actions. To learn more about access permissions and security for external document content, see [External content security for AI Search](external-content-security-ais.md).

 For the full list of Workflow Studio actions provided by the AI Search spoke, see [AI Search spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/ai-search-spoke.md).

 The Integration Hub AI Search spoke combines flexible configuration and handling with the simple drag-and-drop Workflow Studio interface.

</td></tr><tr><td>

External Content REST API

</td><td>

The External Content REST API provides endpoints that you can use to index content and metadata from external documents:-   Send external document text content and metadata to AI Search for indexing using the ingestDocuments API endpoint.
-   Upload external document binary content to AI Search using the storeContent API endpoint. You can associate the stored binary content with a document fed using the ingestDocuments endpoint.

 **Note:** To access the External Content REST API endpoints, you need either the ais\_external\_content role or the admin role.

 You can specify security principal access permissions for documents ingested using the ingestDocuments endpoint. To learn more about access permissions and security for external document content, see [External content security for AI Search](external-content-security-ais.md).

 For full descriptions of the External Content REST API endpoints, see [External Content Ingestion REST API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/rest-apis/external-content-ingestion-api.md).

 The External Content REST API is the most complex tool for indexing content and metadata from your external documents, but it offers the most flexibility.

</td></tr></tbody>
</table>## External content search prerequisites

Before you can index external document content and metadata for search in AI Search, you must satisfy the following requirements. Except as noted in the table, these requirements apply regardless of which external content indexing tools you use.

<table id="table_eyp_xsw_ksb"><thead><tr><th>

Requirement

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Have an active subscription for the External Content for AI Search plugin \(com.glide.ais.external\_content\)

</td><td>

The External Content for AI Search plugin provides functionality for indexing content from external data sources. For instructions on purchasing a subscription for the plugin and activating it, see [Request the External Content for AI Search plugin](../task/activate-ext-content-ais-plugin.md).

</td></tr><tr><td>

Define an external content schema table for the external document source

</td><td>

An external content schema table doesn't store external document content in the database. Instead, its columns serve as a map of AI Search index fields to populate when you index content from external data sources. For instructions on creating a new external content schema table, see [Create an external content schema table](../task/create-ext-content-schema-ais.md).

 When documents from multiple external data sources share the same set of fields and have unique document identifiers, you can use a single external content schema table for all of them. To avoid data loss, the external data sources must satisfy these conditions:

-   All documents in the external data sources must include the same fields, matching the columns defined in the content schema table.
-   Every document in the external data sources must have a unique identifier so that documents don't overwrite one another in the AI Search index.

 If the external data sources can't satisfy these conditions, create a separate external content schema table for each data source.

 **Note:** Search connector applications from the ServiceNow Store automatically create external content schema tables as needed. You only need to create your own external content schema tables when indexing external documents using the Integration Hub AI Search spoke or the External Content REST API.

</td></tr><tr><td>

Create an indexed source with your external content schema table specified as the table to index

</td><td>

The indexed source sends external documents' content and metadata to the AI Search index. For instructions on creating an indexed source, see [Create an indexed source](../task/create-indexed-source-ais.md).

</td></tr><tr><td>

Create one or more search sources for the indexed source

</td><td>

Each search source specifies a subset of external documents from the indexed source whose content you want to make searchable in AI Search. For instructions on creating search sources, see [Create a search source for AI Search](../task/create-search-source-ais.md).

</td></tr></tbody>
</table>-   **[Request the External Content for AI Search plugin](../task/activate-ext-content-ais-plugin.md)**  
Request activation of the External Content for AI Search plugin \(com.glide.ais.external\_content\) to enable indexing of searchable content and metadata from records in external data sources.
-   **[Create an external content schema table](../task/create-ext-content-schema-ais.md)**  
Define a schema table with columns corresponding to fields on records from an external data source. AI Search uses the schema when indexing content from the external data source.
-   **[External content security for AI Search](external-content-security-ais.md)**  
AI Search preserves user and group security access permissions specified for documents indexed from external sources. You can control access to external content search results by mapping these externally defined users and groups to ServiceNow AI Platform® users.
-   **[Components installed with External Content for AI Search](../reference/installed-with-ext-content-ais.md)**  
When you activate the External Content for AI Search plugin \(com.glide.ais.external\_content\), the system creates a new virtual table.

**Parent Topic:**[Configuring AI Search](configuring-ais.md)

