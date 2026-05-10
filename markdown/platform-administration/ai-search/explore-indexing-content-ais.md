---
title: Index searchable content from ServiceNow AI Platform tables and external sources
description: Make alphanumeric content from text and string fields on your records searchable by configuring an indexed source. Each indexed source retrieves data from a table and adds it to the AI Search index.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Explore, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Index searchable content from ServiceNow AI Platform tables and external sources

Make alphanumeric content from text and string fields on your records searchable by configuring an indexed source. Each indexed source retrieves data from a table and adds it to the AI Search index.

Define an indexed source for each ServiceNow AI Platform table with records that you want to make searchable. Search administrators can configure settings for each indexed source:

-   Enable indexing for child tables of the source table.
-   Configure indexing of alphanumeric content from source record tags, attachments, translated fields, and referenced fields.
-   Map source table fields to AI Search index fields for ease of search.

The base system includes preconfigured indexed sources for Knowledge Base articles, Catalog Items, and user records. You can create your own indexed sources to index records from other ServiceNow AI Platform tables.

To learn more about configuring and using indexed sources for ServiceNow AI Platform table records, see [Indexed sources in AI Search](indexed-sources-ais.md).

**Note:** AI Search doesn't index Unicode characters from the High Surrogate Area \(code units in the range U+D800 to U+DBFF\). Characters from this range are replaced with spaces during indexing.

By activating the External Content for AI Search plugin \(com.glide.ais.external\_content\), you can enable indexing and search for record content from external sources. Supported sources include SharePoint collections, Confluence sites, and [remote tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/remote-tables/remote-tables.md). For more details, see [Indexing and searching external content in AI Search](external-content-ais.md).

**Parent Topic:**[Exploring AI Search](explore-ais.md)

