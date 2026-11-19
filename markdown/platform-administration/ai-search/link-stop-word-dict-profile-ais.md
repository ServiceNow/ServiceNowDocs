---
title: Link a stop word dictionary to a search profile
description: Link an existing stop word dictionary to one or more search profiles.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/ai-search/link-stop-word-dict-profile-ais.html
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Stop words, Search profiles, Configure, AI Search, Search administration, Configure core features, Administer]
---

# Link a stop word dictionary to a search profile

Link an existing stop word dictionary to one or more search profiles.

## Before you begin

Role required: ais\_admin

## About this task

You can link a single stop word dictionary to multiple search profiles. You can only link one stop word dictionary per language to a given search profile.

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **Search Experience** &gt; **Search Profiles**.

2.  Open the search profile that you want to link the stop word dictionary to.

3.  In the Stop Words related list, select **Link Existing**.

4.  On the Search Profile - Dictionary Mapping form, select the stop word dictionary and search profile to link.

    1.  Select the reference lookup icon \[Omitted image "IconReferencelookup.png"\] Alt text: for the **Dictionary** field.

    2.  Select the stop word dictionary that you want to link to the search profile.

    3.  Select **Submit**.

    For a description of the field values, see [Search Profile - Dictionary Mapping form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/search-prof-dict-mapping-form-ais.md).


## Result

The selected stop word dictionary appears in the search profile's Stop Words related list.

## What to do next

To make the new stop word dictionary linking take effect, publish the search profile. For more information on publishing a search profile, see [Publish an AI Search search profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/publish-search-profile-ais.md).

**Parent Topic:**[Stop words](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/stop-words-ais.md)

