---
title: Components installed with External Content for AI Search
description: When you activate the External Content for AI Search plugin \(com.glide.ais.external\_content\), the system creates a new virtual table.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: reference
last_updated: "2025-05-14"
reading_time_minutes: 1
breadcrumb: [Indexing and searching external content, Configure, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Components installed with External Content for AI Search

When you activate the External Content for AI Search plugin \(com.glide.ais.external\_content\), the system creates a new virtual table.

## Tables installed

<table id="table_dkf_czw_rnb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AI Search External Search Content \[v\_ais\_external\_search\_content\]

</td><td>

Stores the base set of field mapping columns for inclusion in external content schema tables.**Note:** All user-created external content schema tables extend this table.

</td></tr><tr><td>

AI Search External Search User Mapping Table Data Source Relationship \[ais\_external\_search\_user\_mapping\_data\_source\_m2m\]

</td><td>

Stores links between user mapping tables and indexed sources.

</td></tr></tbody>
</table>**Parent Topic:**[Indexing and searching external content in AI Search](../concept/external-content-ais.md)

