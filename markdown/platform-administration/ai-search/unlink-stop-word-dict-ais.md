---
title: Unlink a stop word dictionary from a search profile
description: Remove a stop word dictionary that isn't linked from any search profile.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Stop words, Search profiles, Configure, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Unlink a stop word dictionary from a search profile

Remove a stop word dictionary that isn't linked from any search profile.

## Before you begin

Role required: ais\_admin

## About this task

Unlinking a stop word dictionary from a search profile doesn't delete the dictionary. To delete a stop word dictionary, you must first unlink it from all search profiles. For steps to delete a stop word dictionary, see [Delete a stop word dictionary](delete-stop-word-dict-ais.md).

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **Search Experience** &gt; **Search Profiles**.

2.  Open the search profile that you want to unlink the stop word dictionary from.

3.  In the Stop Words related list, select the option for the stop word dictionary that you want to unlink from the search profile.

4.  Select **Unlink Selected**.


## Result

The selected stop word dictionary disappears from the search profile's Stop Words related list.

## What to do next

To make the change in stop word dictionary linking take effect, publish the search profile. For more information on publishing a search profile, see [Publish an AI Search search profile](publish-search-profile-ais.md).

**Parent Topic:**[Stop words](../concept/stop-words-ais.md)

