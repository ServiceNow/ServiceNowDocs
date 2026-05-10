---
title: External content security for AI Search
description: AI Search preserves user and group security access permissions specified for documents indexed from external sources. You can control access to external content search results by mapping these externally defined users and groups to ServiceNow AI Platform users.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Indexing and searching external content, Configuring AI Search, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# External content security for AI Search

AI Search preserves user and group security access permissions specified for documents indexed from external sources. You can control access to external content search results by mapping these externally defined users and groups to ServiceNow AI Platform® users.

For an overview of AI Search content security, see [Content security in AI Search](content-security-ais.md).

## Requirements

To use external content security, include the following two steps in your ingestion and indexing process for external documents:

<table id="table_zhf_1qn_wpb"><thead><tr><th>

Step

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Specify access permissions on each external document fed for ingestion

</td><td>

Access permissions for an external document can allow or deny access to the document globally \(for all users\), or can include lists of specific externally defined users and groups who are allowed or denied access to the document. AI Search preserves the external document's security access permissions during indexing. Additional information:

-   For an overview of specifying access permissions on external documents, see [Defining access permissions for external documents](defining-access-perms-ext-docs-ais.md#).
-   To learn about the set of access permissions supported for external content security, see [External content access permissions](defining-access-perms-ext-docs-ais.md#).
-   For details on special access permissions granted by certain user roles, see [Special external content access permissions by role](defining-access-perms-ext-docs-ais.md#).
-   To learn how to reverse the default precedence of **users.read** and **groups.deny** access permissions for an external content indexed source, see [Change the precedence of user read and group deny permissions for an external content indexed source](defining-access-perms-ext-docs-ais.md#).

</td></tr><tr><td>

Define user mappings in tables linked to external content indexed sources

</td><td>

A user mapping specifies externally defined user and group aliases for a ServiceNow AI Platform user. Link these user mappings to indexed sources for external content. AI Search uses an indexed source's user mappings in conjunction with indexed records' access permissions to determine ServiceNow AI Platform user access for search results from the indexed source. Additional information:

-   For an overview of user mappings, see [Mapping external users and groups to ServiceNow AI Platform users](user-mappings-ais.md#).
-   To learn about the set of externally defined security principal types supported in user mappings, see [External user mapping security principal types](user-mappings-ais.md#).
-   For instructions on creating a table to store your user mappings, see [Create a user mapping table](user-mappings-ais.md#).
-   For instructions on linking your user mapping tables to external content indexed sources, see [Link a user mapping table to an external content indexed source](user-mappings-ais.md#).
-   To learn about importing user mappings via the [AI Search External User Mapping API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/rest-apis/ext-user-mapping-api.md), see [Importing user mappings](user-mappings-ais.md#).
-   For instructions on viewing user mapping import history records to confirm that user mappings imported correctly, see [View history records for user mapping import operations](user-mappings-ais.md#).

</td></tr></tbody>
</table>## Security implementation for search queries

When a user's search query matches an indexed record created from an external document, AI Search performs these steps:

1.  Examines the user mappings linked to the record's indexed source and retrieves the set of all externally defined users and groups aliased to the current ServiceNow AI Platform user's account.
2.  Compares the mapped set of externally defined user and group aliases with the access permissions on the indexed search result record to see whether the ServiceNow AI Platform user should be allowed to view the search result.

-   **[Defining access permissions for external documents](defining-access-perms-ext-docs-ais.md#)**  
You can specify access permissions for externally defined users and groups when ingesting external documents. AI Search preserves these permissions during indexing so that user content security filters can operate on them at search time.
-   **[Mapping external users and groups to ServiceNow AI Platform users](user-mappings-ais.md#)**  
AI Search external user mappings enable you to configure externally defined user and group aliases for ServiceNow AI Platform users. AI Search uses these aliased security principals to apply content security filters that control user access to search results indexed from external documents.

**Parent Topic:**[Indexing and searching external content in AI Search](external-content-ais.md)

