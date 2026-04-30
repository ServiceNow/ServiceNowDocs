---
title: Publish an AI Search search profile
description: Publish a search profile to make pending changes to its settings take effect in linked search applications.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Search profiles, Configure, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Publish an AI Search search profile

Publish a search profile to make pending changes to its settings take effect in linked search applications.

## Before you begin

Role required: ais\_admin

## About this task

To make a search profile's settings active in search queries, you must publish it. Publishing propagates the following settings to search application configurations that reference the search profile.

-   The set of synonym and stop word dictionaries linked to the search profile
-   Settings, blocked terms, and derived auto-correction terms for typo handling dictionaries linked to the search profile
-   Result improvement rules and actions defined in the search profile

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **Search Experience** &gt; **Search Profiles**.

    **Note:** Search profiles with the **New** state display an alert triangle icon ![](../image/icon-alert-triangle.png). An informational message notifies you to publish these search profiles.

2.  Open the search profile that you want to publish.

3.  Select **Publish**.


## Result

The search profile appears in the AI Search Search Profiles list with **State** set to **Published**.

**Parent Topic:**[Search profiles in AI Search](../concept/defining-search-profiles-ais.md)

