---
title: Group attachment search results with their parent results
description: Configure your AI Search applications to display attachment search results grouped with the results for their parent records.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-07-16"
reading_time_minutes: 3
breadcrumb: [Search application configurations, Configure, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Group attachment search results with their parent results

Configure your AI Search applications to display attachment search results grouped with the results for their parent records.

## Before you begin

The index\_attachments attribute can't be set to false for any indexed source used in the AI Search application. For details on creating and editing attributes for indexed sources, see [Indexed source attributes for AI Search](../concept/indexed-source-attributes-ais.md#).

**Note:** If you remove a false **index\_attachments** attribute value from an indexed source, perform a full reindex for the indexed source before continuing with this procedure. To learn how to reindex content for an indexed source, see [Perform a full table index or reindex for a single AI Search indexed source](index-single-source-ais.md).

Role required: search\_application\_admin

## About this task

Search administrators can enable grouping of attachment search results with the results for their parent records. With this option enabled, search results for attachments that match a user's search display inline with the search results for their parent record.

If the parent record itself or any of its attachments matches the user's search, the parent record appears in the search result list. Grouped attachments that match the search appear in descending relevancy order within the search result for their parent record.

When attachment grouping is in use, AI Search computes relevancy scores for the parent record and each of its grouped attachments. The final relevancy score of the grouped search result is the highest of these individual relevancy scores.

![Service Portal results page showing two attachment search results displayed as part of the search result for their parent Knowledge article.](../image/service-portal-group-attachments.png "Sample results page showing attachment results grouped with parent result")

By default, AI Search displays separate search results for the parent record and each of its attachments that matches the user's search. With attachment grouping enabled, you can view all matching attachments for a record in a single search result, instead of needing to collate information from multiple search results.

**Note:** When you select a grouped attachment search result, AI Search logs click rank signal data for the parent record search result. All other search signal data is specific to the selected attachment record. For more details on search signal logging, see [Search signal tables](../../search-administration/reference/search-signal-tables.md).

Attachment grouping is enabled by default for new search application configuration records. You only need to perform this procedure to enable attachment grouping for existing search application configuration records after upgrading from a previous release.

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **Search Experience** &gt; **Search Applications**.

2.  Select the record for the AI Search application that you want to enable attachment grouping for.

3.  Select the **Show parent for results that are attachments** option.

4.  Select **Update**.

    If any indexed source used in the search application doesn’t have the index\_attachments attribute set to true, the system displays a warning message. For each affected indexed source, set the index\_attachments attribute to true, then perform a full reindex.


## Result

AI Search groups matching attachment search results with their parent record results on the search application results page.

**Parent Topic:**[Search application configurations](../concept/defining-search-app-cfgs-ais.md)

