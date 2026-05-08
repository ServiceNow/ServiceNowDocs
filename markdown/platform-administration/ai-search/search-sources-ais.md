---
title: Search sources in AI Search
description: Define search sources to make your searchable content available in search experiences. Choose an indexed source and configure optional filter conditions to limit the content that users can search.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configuring AI Search, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Search sources in AI Search

Define search sources to make your searchable content available in search experiences. Choose an indexed source and configure optional filter conditions to limit the content that users can search.

## Search source structure

A search source includes two elements:

-   A reference to an indexed source. By default, search queries using the search source can return all records from the referenced indexed source. For more information on indexed sources, see [Indexed sources in AI Search](indexed-sources-ais.md).
-   An optional set of filter conditions applied to the indexed source's records. Indexed source records must pass all of these filter conditions to be returned as search results for queries using the search source.

You can define multiple search sources that reference the same indexed source, specifying distinct filter conditions for each.

## Filter conditions

To limit the set of indexed source table records that AI Search returns as search results, you can apply filter conditions to your search source.

**Note:** Search source filter conditions can only operate on source record fields that are indexed. Fields on referenced records aren't indexed by default. To use a referenced record field in a search source filter condition, you must first configure indexing for the field in the indexed source. For details on this procedure, see [Enable indexing of referenced table fields for an AI Search indexed source](../task/enable-ref-table-field-index-ais.md).

You can use static and dynamic filter conditions to filter search source records. As an example, you could apply a dynamic **\[Assigned to\] \[is \(dynamic\)\] \[Me\]** user filter to make your search source only return results corresponding to indexed source table records assigned to the search user.

Search sources don't support any of the following filter options:

-   Filters that reference fields from child tables of the indexed source table. As an example, if you create an indexed source for the Task \[task\] table, search sources for that indexed source can't use filters to reference fields from the Incident \[incident\] table because the Incident table is a child of the Task table.
-   Dynamic filters with scripts that use the **current** keyword or global variable
-   Dynamic filters with scripts that reference any global business rules
-   Dynamic filters with scripts that use script includes

For more information on filter conditions, see Filters. To learn about relationships between parent and child tables, see [Table extension and classes](../../table-administration/concept/table-extension-and-classes.md). For details on dynamic filter options and their associated scripts, see Create a dynamic filter option.

## Linking search sources to search profiles

To make your search source's content available to users, link it to one or more search profiles. You can link multiple search sources to a single search profile.

For more information, see [Link a search source to a search profile](../task/link-search-source-profile-ais.md).

## Viewing search sources

You can view or edit search sources from any of the following application modules:

-   To view all defined search sources, navigate to **All** &gt; **AI Search** &gt; **Search Experience** &gt; **Search Sources**.
-   To view search sources that reference a particular indexed source, navigate to **All** &gt; **AI Search** &gt; **AI Search Index** &gt; **Indexed Sources**. Open the indexed source and select its Search Source Mappings related list.
-   To view search sources linked to a particular search profile, navigate to **All** &gt; **AI Search** &gt; **Search Experience** &gt; **Search Profiles**. Open the search profile and select its Search Sources related list.

-   **[Create a search source for AI Search](../task/create-search-source-ais.md)**  
Make searchable content from an indexed source available in user search experiences by defining a search source.
-   **[Preview matching records for an AI Search search source](../task/preview-search-source-records-ais.md)**  
View the ServiceNow AI Platform® table records that match a search source's indexed source table and filter conditions.

**Parent Topic:**[Configuring AI Search](configuring-ais.md)

