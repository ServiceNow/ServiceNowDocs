---
title: Components installed with Now Assist in AI Search
description: The Now Assist in AI Search application installs new system components including scheduled jobs and Entity View Action Mapping \(EVAM\) configurations and templates.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: reference
last_updated: "2025-10-03"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Now Assist in AI Search reference, Now Assist in AI Search, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Components installed with Now Assist in AI Search

The Now Assist in AI Search application installs new system components including scheduled jobs and Entity View Action Mapping \(EVAM\) configurations and templates.

## Scheduled jobs installed with Now Assist in AI Search

<table id="table_ifp_p3g_jzb"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Update Semantic Cache

</td><td>

-   Populate the second-level Now Assist Q&amp;A Genius Results cache with results for the most frequently submitted queries found in the Search Event \[sys\_search\_event\] search signal table. For more information on this table, see [Search signal tables](../../search-administration/reference/search-signal-tables.md).
-   Purge all unpinned entries in the Now Assist Q&amp;A Genius Results second-level cache that have not been used in the past seven days. Search administrators can pin results in the second-level cache table to prevent them from being purged. For more details on this procedure, see [Pin cached answers for Now Assist Q&amp;A Genius Results](../concept/caching-now-assist-q-a-gr.md#).

</td></tr></tbody>
</table>## Entity View Action Mapper \(EVAM\) configurations installed with Now Assist in AI Search

<table id="table_rnf_j3f_zwb"><thead><tr><th>

Configuration

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AI Search Global - Now Assist Q&amp;A Genius Result

</td><td>

Contains the view configuration settings for the Now Assist Q&amp;A Genius Result configuration in AI Search for Next Experience global search.-   Application scope: Now Assist in AI Search
-   Location: **All** &gt; **Entity View Action Mapper \(EVAM\)** &gt; **View Definitions** &gt; **View Configurations**

</td></tr><tr><td>

Now Assist Q&amp;A Genius Result

</td><td>

Contains the view configuration settings for the Now Assist Q&amp;A Genius Result configuration in a search application.-   Application scope: Now Assist in AI Search
-   Location: **All** &gt; **Entity View Action Mapper \(EVAM\)** &gt; **View Definitions** &gt; **View Configurations**

</td></tr><tr><td>

Taxonomy - Now Assist Q&amp;A Genius Result

</td><td>

Contains the view configuration settings for the Now Assist Q&amp;A Genius Result configuration in Content Taxonomy.-   Application scope: Now Assist in AI Search
-   Location: **All** &gt; **Entity View Action Mapper \(EVAM\)** &gt; **View Definitions** &gt; **View Configurations**

</td></tr><tr><td>

Virtual Agent - Now Assist Q&amp;A Genius Result

</td><td>

Contains the view configuration settings for the Now Assist Q&amp;A Genius Result configuration in Virtual Agent.-   Application scope: Now Assist in AI Search
-   Location: **All** &gt; **Entity View Action Mapper \(EVAM\)** &gt; **View Definitions** &gt; **View Configurations**

</td></tr></tbody>
</table>## Entity View Action Mapper \(EVAM\) templates installed with Now Assist in AI Search

<table id="table_by1_shf_zwb"><thead><tr><th>

Template

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AI Search Global - Now Assist Q&amp;A Genius Result Template

</td><td>

Contains the component, static value, field-mapping, and action-mapping settings for the Now Assist Q&amp;A Genius Result configuration in AI Search for Next Experience global search.-   Application scope: Now Assist in AI Search
-   Location: **All** &gt; **Entity View Action Mapper \(EVAM\)** &gt; **View Definitions** &gt; **View Templates**

</td></tr><tr><td>

Now Assist Q&amp;A Genius Result Template

</td><td>

Contains the component, static value, field-mapping, and action-mapping settings for the Now Assist Q&amp;A Genius Result configuration in Service Portal.-   Application scope: Now Assist in AI Search
-   Location: **All** &gt; **Entity View Action Mapper \(EVAM\)** &gt; **View Definitions** &gt; **View Templates**

</td></tr><tr><td>

Virtual Agent - Now Assist Q&amp;A Genius Result Template

</td><td>

Contains the component, static value, field-mapping, and action-mapping settings for the Now Assist Q&amp;A Genius Result configuration in Virtual Agent.-   Application scope: Now Assist in AI Search
-   Location: **All** &gt; **Entity View Action Mapper \(EVAM\)** &gt; **View Definitions** &gt; **View Templates**

</td></tr></tbody>
</table>## List of all components installed with Now Assist in AI Search

To view the complete list of components installed with Now Assist in AI Search, follow the steps in [Find components installed with an application](../../plugins/task/find-components.md). The application's package name is **Now Assist in AI Search**.

**Parent Topic:**[Now Assist in AI Search reference](../concept/reference-now-assist-ais.md)

