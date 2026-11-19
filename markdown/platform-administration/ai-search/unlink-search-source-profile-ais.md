---
title: Unlink a search source from a search profile
description: Unlink search sources from a search profile to prevent their content from being searchable through that profile. Deleted search sources aren't automatically unlinked from search profiles.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/ai-search/unlink-search-source-profile-ais.html
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-08-11"
reading_time_minutes: 1
breadcrumb: [Search profiles, Configure, AI Search, Search administration, Configure core features, Administer]
---

# Unlink a search source from a search profile

Unlink search sources from a search profile to prevent their content from being searchable through that profile. Deleted search sources aren't automatically unlinked from search profiles.

## Before you begin

Role required: ais\_admin

## About this task

Unlinking a search source from a search profile prevents its filtered content from being searchable through that search profile.

When you delete a search source, the system doesn't automatically unlink it from search profiles. In this case, you must manually unlink the search source from each search profile that's it's linked to.

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **Search Experience** &gt; **Search Profiles**.

2.  Open the search profile that you want to unlink the search source from.

3.  In the Search Sources related list, select the search source that you want to unlink from the search profile.

4.  Select **Unlink Selected**.


## Result

The search source no longer appears in the Search Sources related list.

## What to do next

To make the search source change take effect, publish the search profile you edited. For details on publishing a search profile, see [Publish an AI Search search profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/publish-search-profile-ais.md).

**Parent Topic:**[Search profiles in AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/defining-search-profiles-ais.md)

