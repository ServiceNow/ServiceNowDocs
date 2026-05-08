---
title: Configure AI Search as the source for Ask Now Assist suggestions
description: Enable term highlighting in enhanced chat's Ask Now Assist suggestions by configuring AI Search as the source for those suggestions.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configuring Now Assist in AI Search, Now Assist in AI Search, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure AI Search as the source for Ask Now Assist suggestions

Enable term highlighting in enhanced chat's Ask Now Assist suggestions by configuring AI Search as the source for those suggestions.

## Before you begin

You must have at least Now Assist in AI Search 15 installed.

Role required: admin

## About this task

By default, Ask Now Assist suggestions are generated using a prefix-based GlideAggregate query against the Utterance Suggestion \[sys\_suggested\_utterance\] table.

Admins can configure the system to use AI Search as the source for Ask Now Assist suggestions in enhanced chat. Making this change activates suggestion term highlighting in Ask Now Assist and provides improvements such as wildcard searching and lemmatization for suggestions.

For more information on Ask Now Assist suggestions in enhanced chat, see Enhanced chat.

## Procedure

1.  Index all content for the Ask Now Assist Suggestions indexed source.

    1.  Navigate to **All** &gt; **AI Search** &gt; **AI Search Index** &gt; **Indexed Sources**.

    2.  Open the record for the Ask Now Assist Suggestions indexed source.

    3.  Select **Index All Tables**.

2.  Publish the Ask Now Assist Suggestions search profile.

    1.  Navigate to **All** &gt; **AI Search** &gt; **Search Experience** &gt; **Search Profiles**.

    2.  Open the record for the Ask Now Assist Suggestions search profile.

    3.  Select **Publish**.

3.  Navigate to the list view for the System Property \[sys\_properties\] table.

    1.  Navigate to **All**.

    2.  In the **Filter** field, enter `sys_properties.list`, then press Enter.

4.  Search for the **glide.search.suggestions.utterance.use\_ais** system property record and perform the appropriate steps depending on whether it exists or not.

    -   If the **glide.search.suggestions.utterance.use\_ais** record already exists in the System Property table, open it.
    -   If no record with the name **glide.search.suggestions.utterance.use\_ais** exists in the System Property table, select **New**, then enter `glide.search.suggestions.utterance.use_ais` as the name for your new system property and select **true \| false** as its type.
5.  On the System Property form, set the system property's value to **true**, then select **Update**.


**Parent Topic:**[Configuring Now Assist in AI Search](../concept/configuring-now-assist-ais.md)

