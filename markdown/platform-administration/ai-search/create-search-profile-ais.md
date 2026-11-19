---
title: Create a search profile
description: Create a new search profile to store search experience settings for a search application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/ai-search/create-search-profile-ais.html
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Search profiles, Configure, AI Search, Search administration, Configure core features, Administer]
---

# Create a search profile

Create a new search profile to store search experience settings for a search application.

## Before you begin

Role required: ais\_admin

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **Search Experience** &gt; **Search Profiles**.

2.  Select **New**.

3.  On the Search Profile form, fill in the fields.

    For a description of the field values, see [Search Profile form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/search-profile-form-ais.md).

4.  Select **Submit**.


## Result

The new search profile appears in the AI Search Search Profiles list with **State** set to **New**. An informational message and an alert triangle icon \[Omitted image "icon-alert-triangle.png"\] Alt text: indicate that the new search profile has never been published.

## What to do next

To make content searchable using your new search profile, link one or more search sources to it. For instructions on linking search sources, see [Link a search source to a search profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/link-search-source-profile-ais.md).

Your new search profile includes sample synonym and stop word dictionaries and a default typo handling dictionary. For more details on configuring and populating these dictionaries, see [Synonyms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/synonyms-ais.md), [Stop words](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/stop-words-ais.md), and [Typo handling](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/typo-handling-ais.md).

**Parent Topic:**[Search profiles in AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/defining-search-profiles-ais.md)

