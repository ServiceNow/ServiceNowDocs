---
title: Components installed with ServiceNow Otto for AI Search
description: The ServiceNow Otto for AI Search application installs new system components including scheduled jobs and Entity View Action Mapping \(EVAM\) configurations and templates.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/ai-search/components-now-assist-ais.html
release: australia
product: AI Search
classification: ai-search
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [ServiceNow Otto for AI Search reference, ServiceNow Otto for AI Search, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Components installed with ServiceNow Otto for AI Search

The ServiceNow Otto for AI Search application installs new system components including scheduled jobs and Entity View Action Mapping \(EVAM\) configurations and templates.

## Scheduled jobs installed with ServiceNow Otto for AI Search

<table id="table_ifp_p3g_jzb"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Update Semantic Cache

</td><td>

-   Populate the second-level Knowledge base articles Genius Results cache with results for the most frequently submitted queries found in the Search Event \[sys\_search\_event\] search signal table. For more information on this table, see [Search signal tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/search-signal-tables.md).
-   Purge all unpinned entries in the Knowledge base articles Genius Results second-level cache that have not been used in the past seven days. Search administrators can pin results in the second-level cache table to prevent them from being purged. For more details on this procedure, see [Pin cached answers for Knowledge base articles Genius Results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/caching-now-assist-q-a-gr.md).

</td></tr></tbody>
</table>## Entity View Action Mapper \(EVAM\) configurations installed with ServiceNow Otto for AI Search

<table id="table_rnf_j3f_zwb"><thead><tr><th>

Configuration

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AI Search Global - Knowledge base articles Genius Result

</td><td>

Contains the view configuration settings for the Knowledge base articles Genius Result configuration in AI Search for Next Experience global search.-   Application scope: ServiceNow Otto for AI Search
-   Location: **All** &gt; **Entity View Action Mapper \(EVAM\)** &gt; **View Definitions** &gt; **View Configurations**

</td></tr><tr><td>

Knowledge base articles Genius Result

</td><td>

Contains the view configuration settings for the Knowledge base articles Genius Result configuration in a search application.-   Application scope: ServiceNow Otto for AI Search
-   Location: **All** &gt; **Entity View Action Mapper \(EVAM\)** &gt; **View Definitions** &gt; **View Configurations**

</td></tr><tr><td>

Taxonomy - Knowledge base articles Genius Result

</td><td>

Contains the view configuration settings for the Knowledge base articles Genius Result configuration in Content Taxonomy.-   Application scope: ServiceNow Otto for AI Search
-   Location: **All** &gt; **Entity View Action Mapper \(EVAM\)** &gt; **View Definitions** &gt; **View Configurations**

</td></tr><tr><td>

Virtual Agent - Knowledge base articles Genius Result

</td><td>

Contains the view configuration settings for the Knowledge base articles Genius Result configuration in Virtual Agent.-   Application scope: ServiceNow Otto for AI Search
-   Location: **All** &gt; **Entity View Action Mapper \(EVAM\)** &gt; **View Definitions** &gt; **View Configurations**

</td></tr></tbody>
</table>## Entity View Action Mapper \(EVAM\) templates installed with ServiceNow Otto for AI Search

<table id="table_by1_shf_zwb"><thead><tr><th>

Template

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AI Search Global - Knowledge base articles Genius Result Template

</td><td>

Contains the component, static value, field-mapping, and action-mapping settings for the Knowledge base articles Genius Result configuration in AI Search for Next Experience global search.-   Application scope: ServiceNow Otto for AI Search
-   Location: **All** &gt; **Entity View Action Mapper \(EVAM\)** &gt; **View Definitions** &gt; **View Templates**

</td></tr><tr><td>

Knowledge base articles Genius Result Template

</td><td>

Contains the component, static value, field-mapping, and action-mapping settings for the Knowledge base articles Genius Result configuration in Service Portal.-   Application scope: ServiceNow Otto for AI Search
-   Location: **All** &gt; **Entity View Action Mapper \(EVAM\)** &gt; **View Definitions** &gt; **View Templates**

</td></tr><tr><td>

Virtual Agent - Knowledge base articles Genius Result Template

</td><td>

Contains the component, static value, field-mapping, and action-mapping settings for the Knowledge base articles Genius Result configuration in Virtual Agent.-   Application scope: ServiceNow Otto for AI Search
-   Location: **All** &gt; **Entity View Action Mapper \(EVAM\)** &gt; **View Definitions** &gt; **View Templates**

</td></tr></tbody>
</table>## List of all components installed with ServiceNow Otto for AI Search

To view the complete list of components installed with ServiceNow Otto for AI Search, follow the steps in [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/find-components.md). The application's package name is **ServiceNow Otto for AI Search**.

**Parent Topic:**[ServiceNow Otto for AI Search reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/reference-now-assist-ais.md)

