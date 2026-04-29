---
title: Create a stop word dictionary linked to a search profile
description: Define a new stop word dictionary and link it to a search profile.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Stop words, Search profiles, Configuring AI Search, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a stop word dictionary linked to a search profile

Define a new stop word dictionary and link it to a search profile.

## Before you begin

Role required: ais\_admin

## About this task

To make a stop word dictionary affect search behavior, you must link it to a search profile, either at creation time or afterward. You can only link one stop word dictionary per language to a given search profile. To learn about linking a saved stop word dictionary to a search profile, see [Link a stop word dictionary to a search profile](link-stop-word-dict-profile-ais.md).

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **Search Experience** &gt; **Search Profiles**.

2.  Open the search profile that you want to link the new stop word dictionary to.

3.  In the Stop Words related list, select **Create and Link**.

4.  On the Dictionary form, fill in the fields.

    For a description of the field values, see [Dictionary and AI Search Dictionary forms](../reference/dictionary-form-ais.md).

5.  To save the new stop word dictionary and link it to the specified search profile, select **Submit.**


## Result

The new stop word dictionary appears in the Stop Words related list.

## What to do next

To make new or updated stop word dictionary settings take effect, publish the search profile that you edited. For details on publishing a search profile, see [Publish an AI Search search profile](publish-search-profile-ais.md).

**Parent Topic:**[Stop words](../concept/stop-words-ais.md)

