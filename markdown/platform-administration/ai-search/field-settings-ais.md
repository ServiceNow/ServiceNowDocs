---
title: Field settings for AI Search
description: A field setting controls indexing behavior for a specified field \(column\) on all records from an indexed source.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/ai-search/field-settings-ais.html
release: zurich
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2025-07-28"
reading_time_minutes: 1
breadcrumb: [Indexed sources, Configure, AI Search, Search administration, Configure core features, Administer]
---

# Field settings for AI Search

A field setting controls indexing behavior for a specified field \(column\) on all records from an indexed source.

Examples of how you might use field settings include the following.

-   Disable text indexing or searchability for a field found on source table records
-   Modify default mappings between source table fields and fields in the AI Search index
-   Add a referenced table field to the index by dot-walking from a reference field on source table records

An indexed source's field settings appear in its Field Settings &amp; Mapping related list.

-   **[Create a field setting for an AI Search indexed source](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/create-field-setting-ais.md)**  
Define an indexed source field setting to configure AI Search content indexing behavior for a specific field on source table records.
-   **[Enable indexing of referenced table fields for an AI Search indexed source](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/enable-ref-table-field-index-ais.md)**  
Configure an indexed source to index field values from tables referenced by fields in the source table. You can index these field values for use in filters and EVAM search result configurations, index them for search, or both.
-   **[List of AI Search indexed source field settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/field-settings-list-ais.md)**  
You can adjust indexing behavior for source record fields in an AI Search indexed source by configuring field setting attributes and values.
-   **[Security for searchable referenced table field values in AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/security-srch-dot-walk-values.md)**  
When a user searches referenced table field values that you have indexed for search with the **searchable\_dot\_walk\_fields** field setting, only field values that the user can view appear in the search results. The system uses a field value's role-based access control list rules \(ACLs\) to determine whether the search user can view that field value.

**Parent Topic:**[Indexed sources in AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/indexed-sources-ais.md)

