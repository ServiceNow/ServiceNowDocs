---
title: Link a search source to a search profile
description: Link search sources to a search profile to specify the content users can search through that profile.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Search profiles, Configuring AI Search, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Link a search source to a search profile

Link search sources to a search profile to specify the content users can search through that profile.

## Before you begin

You must have already created at least one search source. For instructions on creating search sources, see [Create a search source for AI Search](create-search-source-ais.md).

Role required: ais\_admin

## About this task

Linking a search source to a search profile makes its filtered content available for searches using that search profile. AI Search only uses content from the search profile's linked search sources when finding and generating standard search results and Genius Result answers.

When linking a search source to a search profile, you can specify options that control how the search source's content is accessed for searches using that search profile. You can exclude the search source's content from being considered when finding standard search results, or prevent it from being considered during Genius Result answer generation. For a search source that includes internal content \(from a ServiceNow AI Platform® table\), you can also exclude indexed attachment content from being considered during Genius Result answer generation.

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **Search Experience** &gt; **Search Profiles**.

2.  Open the search profile that you want to link the search source to.

3.  In the Search Sources related list, select **Link Existing**.

4.  On the Search Profile - Search Source Mapping form, fill in the fields.

    For a description of the field values, see [Search Profile - Search Source Mapping form](../reference/search-prof-src-mapping-form-ais.md).

5.  Select **Submit**.


## Result

The new search source appears in the Search Sources related list. Search query results immediately reflect changes to the set of records searchable through the search profile.

## What to do next

Derived auto-correction term lists for the search profile's typo handling dictionary don't automatically update to reflect changes to the set of searchable records. To update these auto-correction term lists, publish the search profile you edited. For details on publishing a search profile, see [Publish an AI Search search profile](publish-search-profile-ais.md).

**Parent Topic:**[Search profiles in AI Search](../concept/defining-search-profiles-ais.md)

