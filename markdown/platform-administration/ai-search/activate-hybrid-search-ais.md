---
title: Activate hybrid search for a search application configuration in AI Search
description: Activate the hybrid search mode for a search application configuration that uses AI Search as its search engine. Hybrid search offers improved precision and recall for knowledge article, Catalog Item, external content, and topic retrieval searches.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/ai-search/activate-hybrid-search-ais.html
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Hybrid search, Configuring Now Assist in AI Search, Now Assist in AI Search, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Activate hybrid search for a search application configuration in AI Search

Activate the hybrid search mode for a search application configuration that uses AI Search as its search engine. Hybrid search offers improved precision and recall for knowledge article, Catalog Item, external content, and topic retrieval searches.

## Before you begin

Your ServiceNow AI Platform® instance must have at least Now Assist in AI Search 15 installed.

Role required: ais\_admin

## About this task

Beginning with Now Assist in AI Search 17, when Now Assist in AI Search is installed for the first time, hybrid search is automatically activated for all search application configurations \(SACs\) in the instance. If you upgraded to Now Assist in AI Search 17 from an earlier release, hybrid search isn't automatically activated in your SACs for search applications that use as their search engine. You can perform this task to manually activate hybrid search in the SAC for a search application that uses as its search engine. Repeat these steps for each application you want to switch to hybrid search for.

To learn more about the nature and benefits of hybrid search, see [Hybrid search in AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/hybrid-search-ais.md).

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **Search Experience** &gt; **Search Applications**.

2.  Edit the search application configuration record for the search application that you want to activate hybrid search for.

    **Note:** You can only activate hybrid search for search application configurations that use AI Search as their search engine. Search application configurations that use the legacy Zing text indexing and search engine don't support hybrid search.

3.  If you don't see the \[\[\[ **Hybrid search** \]\]\] option shown on the Search Application Configuration form, select a situation and follow the corresponding steps.

<table id="choicetable_ex3_b2j_njc"><thead><tr><th align="left" id="d63973e163">

Situation

</th><th align="left" id="d63973e166">

Steps

</th></tr></thead><tbody><tr><td id="d63973e172">

**Beginning with Australia patch 3**

</td><td>

1.  Select **New**.

The Search Application Attribute Configuration New record page appears.

2.  For the **Attribute**, select **enable\_hybrid\_search**.
3.  For the **Value**, enter `true`.
4.  Select **Submit**.


</td></tr><tr><td id="d63973e216">

**Versions before Australia patch 3**

</td><td>

1.  Configure the form layout.

For instructions on configuring the form layout, see [Configuring the form layout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/configure-form-layout.md).

2.  Select the \[\[\[ **Hybrid search** \]\]\] option.
3.  Select **Update**.


</td></tr></tbody>
</table>
## Result

Hybrid search is activated for the selected search application configuration.

**Parent Topic:**[Hybrid search in AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/hybrid-search-ais.md)

