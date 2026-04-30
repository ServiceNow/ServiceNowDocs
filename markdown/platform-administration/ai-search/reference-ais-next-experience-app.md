---
title: AI Search for Next Experience reference
description: Reference information for the AI Search for Next Experience application.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: reference
last_updated: "2025-07-01"
reading_time_minutes: 7
breadcrumb: [AI Search for Next Experience, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# AI Search for Next Experience reference

Reference information for the AI Search for Next Experience application.

## Plugins installed with AI Search for Next Experience

<table id="table_fvc_nlj_ntb"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AI Search for Next Experience \(sn\_aisearch\_global\)

</td><td>

Includes system and search configuration settings required to enable AI Search as the search engine for the Unified Navigation search field in Next Experience.-   Search profile: Now Experience Search Configuration
-   Search application configuration: \[AIS\] Now Experience Search Configuration

 To learn more about search profiles and search application configurations, see [Search profiles in AI Search](../concept/defining-search-profiles-ais.md) and [Search application configurations](../concept/defining-search-app-cfgs-ais.md).

</td></tr><tr><td>

AI Search Index Sources \(com.glide.ais.index\_sources\)

</td><td>

Includes indexed source definitions for ServiceNow AI Platform® tables beyond those provided with AI Search:-   Catalog Task \[sc\_task\]
-   Change \[change\_request\]
-   Change Task \[change\_task\]
-   Company \[core\_company\]
-   Group \[sys\_user\_group\]
-   Incident \[incident\]
-   Location \[cmn\_location\]
-   Problem \[problem\]
-   Request \[sc\_request\]
-   Requested Item \[sc\_req\_item\]

 For more details on indexed sources, see [Indexed sources in AI Search](../concept/indexed-sources-ais.md).

</td></tr></tbody>
</table>## System properties installed with AI Search for Next Experience

<table id="table_slk_nlj_ntb"><thead><tr><th>

System property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**glide.ui.polaris.ais\_ready**

</td><td>

Option to enable AI Search as the search engine for the Unified Navigation search field in Next Experience.-   Type: true \| false
-   Default value: **false**
-   Supported values:
    -   **true**: The system uses AI Search as the search engine for the Unified Navigation search field in Next Experience.
    -   **false**: The system uses Zing indexing and text search as the search engine for the Unified Navigation search field in Next Experience.
-   Location: System Property \[sys\_properties\] table

</td></tr></tbody>
</table>## Search profiles installed with AI Search for Next Experience

<table id="table_fwd_2yf_cxb"><thead><tr><th>

Search profile

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Next Experience Search Configuration

</td><td>

Contains search experience settings for AI Search for Next Experience:-   Search sources
-   Stop word dictionaries
-   Synonym dictionaries
-   Typo handling dictionaries
-   Result improvement rules
-   Genius Results

 For details on configuring these settings, see [Search profiles in AI Search](../concept/defining-search-profiles-ais.md).

 -   Application scope: AI Search For Next Experience
-   Location: **All** &gt; **AI Search** &gt; **Search Experience** &gt; **Search Profiles**

</td></tr></tbody>
</table>## Search application configurations installed with AI Search for Next Experience

<table id="table_bzk_2yf_cxb"><thead><tr><th>

Search application configuration

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\[AIS\] Next Experience Search Configuration

</td><td>

Contains search result display and refinement settings for AI Search for Next Experience:-   Navigation tabs
-   Facets
-   Auto-complete suggestions
-   Search scripted post-processors
-   Search result sort options

 For details on configuring these settings, see [Search application configurations](../concept/defining-search-app-cfgs-ais.md).

 -   Application scope: AI Search For Next Experience
-   Location: **All** &gt; **AI Search** &gt; **Search Experience** &gt; **Search Applications**

**Note:** If you install AI Search for Next Experience 3.x on a San Diego instance and then upgrade to Tokyo or a later release, an informational message appears when you view the search application configuration record, pointing out that search-based auto-complete suggestion types aren't enabled for global search. To enable these auto-complete suggestion types for global search, see [Enable search-based auto-complete suggestions in AI Search for Next Experience](../task/enable-srch-autosugg-ais-next-exp.md).

</td></tr></tbody>
</table>## Entity View Action Mapper \(EVAM\) configurations installed with AI Search for Next Experience

<table id="table_rnf_j3f_zwb"><thead><tr><th>

Configuration

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AI Search Global \| Catalog Genius Results

</td><td>

Contains view configuration settings for the Catalog Item Genius Result configuration in AI Search for Next Experience. To learn more about this Genius Result configuration, see [Catalog Item Genius Results](../concept/genius-result-catalog-item-ais.md).-   Application scope: AI Search For Next Experience
-   Location: **All** &gt; **Entity View Action Mapper \(EVAM\)** &gt; **View Definitions** &gt; **View Configurations**

</td></tr><tr><td>

AI Search Global \| Q&amp;A Genius Result

</td><td>

Contains view configuration settings for the Q&amp;A Genius Result configuration in AI Search for Next Experience. To learn more about this Genius Result configuration, see [Q&amp;A Genius Results](../concept/genius-result-q-a-ais.md).-   Application scope: AI Search For Next Experience
-   Location: **All** &gt; **Entity View Action Mapper \(EVAM\)** &gt; **View Definitions** &gt; **View Configurations**

</td></tr><tr><td>

AI Search Global \| User Genius Results

</td><td>

Contains view configuration settings for the People Genius Result configuration in AI Search for Next Experience. To learn more about this Genius Result configuration, see [People Genius Results](../concept/genius-result-people-ais.md).-   Application scope: AI Search For Next Experience
-   Location: **All** &gt; **Entity View Action Mapper \(EVAM\)** &gt; **View Definitions** &gt; **View Configurations**

</td></tr></tbody>
</table>## Entity View Action Mapper \(EVAM\) templates installed with AI Search for Next Experience

<table id="table_by1_shf_zwb"><thead><tr><th>

Template

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AI Search Global \| Catalog Genius Results Template

</td><td>

Contains component, static value, field mapping, and action mapping settings for the Catalog Item Genius Result configuration in AI Search for Next Experience. To learn more about this Genius Result configuration, see [Catalog Item Genius Results](../concept/genius-result-catalog-item-ais.md).-   Application scope: AI Search For Next Experience
-   Location: **All** &gt; **Entity View Action Mapper \(EVAM\)** &gt; **View Definitions** &gt; **View Templates**

</td></tr><tr><td>

AI Search Global \| Q&amp;A Genius Result Template

</td><td>

Contains component, static value, field mapping, and action mapping settings for the Q&amp;A Genius Result configuration in AI Search for Next Experience. To learn more about this Genius Result configuration, see [Q&amp;A Genius Results](../concept/genius-result-q-a-ais.md).-   Application scope: AI Search For Next Experience
-   Location: **All** &gt; **Entity View Action Mapper \(EVAM\)** &gt; **View Definitions** &gt; **View Templates**

</td></tr><tr><td>

AI Search Global \| User Genius Results Template

</td><td>

Contains component, static value, field mapping, and action mapping settings for the People Genius Result configuration in AI Search for Next Experience. To learn more about this Genius Result configuration, see [People Genius Results](../concept/genius-result-people-ais.md).-   Application scope: AI Search For Next Experience
-   Location: **All** &gt; **Entity View Action Mapper \(EVAM\)** &gt; **View Definitions** &gt; **View Templates**

</td></tr></tbody>
</table>## List of all components installed with AI Search for Next Experience

To view the complete list of components installed with AI Search for Next Experience, follow the steps described in [Find components installed with an application](../../plugins/task/find-components.md). The application's package name is **AI Search For Next Experience**.

-   **[AI Search for Next Experience default navigation tabs for global search](ais-ne-global-search-nav-tabs.md)**  
List of navigation tabs that appear by default in AI Search for Next Experience global search results.

**Parent Topic:**[AI Search for Next Experience](../concept/ais-next-experience-app.md)

