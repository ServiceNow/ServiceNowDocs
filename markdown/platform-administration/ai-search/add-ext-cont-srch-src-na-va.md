---
title: Add an external content search source to Now Assist in Virtual Agent
description: Include searchable content retrieved by an external content connector in your Now Assist in Virtual Agent conversations.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Add an external content search source to Now Assist in Virtual Agent

Include searchable content retrieved by an external content connector in your Now Assist in Virtual Agent conversations.

## Before you begin

You must have already created at least one search source for the indexed source associated with the external content connector. For instructions on creating search sources, see [Create a search source for AI Search](create-search-source-ais.md).

Role required: ais\_admin

## About this task

Linking a search source to the **Now Assist in VA** search profile makes its filtered content available in Now Assist in Virtual Agent conversations. AI Search only uses content from the search profile's linked search sources when generating responses for Now Assist in Virtual Agent conversations.

When linking a search source to the **Now Assist in VA** search profile, you can specify options that control how the search source's content is accessed for Now Assist in Virtual Agent conversations. You can exclude the search source's content from being considered when finding standard search results, or prevent it from being considered during Genius Result answer generation.

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **Search Experience** &gt; **Search Profiles**.

2.  Open the **Now Assist in VA** search profile record.

3.  In the Search Sources related list, select **Link Existing**.

4.  On the Search Profile - Search Source Mapping form, fill in the fields.

    For a description of the field values, see [Search Profile - Search Source Mapping form](../reference/search-prof-src-mapping-form-ais.md).

5.  Select **Submit**.


## Result

The new search source appears in the Search Sources related list. Now Assist in Virtual Agent conversations immediately reflect changes to the set of records searchable through the search profile.

## What to do next

Derived auto-correction term lists for the **Now Assist in VA** search profile's typo handling dictionary don't automatically update to reflect changes to the set of searchable records. To update these auto-correction term lists, publish the **Now Assist in VA** search profile. For details on publishing a search profile, see [Publish an AI Search search profile](publish-search-profile-ais.md).

**Parent Topic:**[Configuring External Content Connectors](../concept/configuring-ext-cont-connectors.md)

