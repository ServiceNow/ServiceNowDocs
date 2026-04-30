---
title: AI Search for Next Experience properties
description: A system property allows you to control whether facets are shown when no source is selected in global search and workspace search results pages.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [AI Search for Next Experience reference, AI Search for Next Experience, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# AI Search for Next Experience properties

A system property allows you to control whether facets are shown when no source is selected in global search and workspace search results pages.

This property is available for AI Search for Next Experience.

**Note:** To open the System Properties \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter.

<table id="table_ctw_npp_vfc"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glide.ui.ais.show\_all\_facets

</td><td>

-   Type: true \| false
-   Default value: **false**
-   Supported values:
    -   **true**: Show facets from all sources in the Filters list on global and workspace search results pages, even when no source is selected.
    -   **false**: Only show facets from selected sources in the Filters list on global and workspace search results pages.
-   Location: System Property \[sys\_properties\] table \(record not present by default\)

</td></tr></tbody>
</table>**Parent Topic:**[AI Search for Next Experience reference](reference-ais-next-experience-app.md)

