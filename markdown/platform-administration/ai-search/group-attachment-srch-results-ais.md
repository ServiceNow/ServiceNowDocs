---
title: Group attachment search results with their parent results
description: Configure your AI Search applications to display attachment search results grouped with the results for their parent records.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Search application configurations, Configure, AI Search, Search administration, Configure core features, Administer]
---

# Group attachment search results with their parent results

Configure your AI Search applications to display attachment search results grouped with the results for their parent records.

## Before you begin

The **index\_attachments** attribute can't be set to **false** for any indexed source used in the AI Search application. For details on creating and editing attributes for indexed sources, see [Indexed source attributes for AI Search](../concept/indexed-source-attributes-ais.md#).

**Note:** If you remove a **index\_attachments** attribute value of **false** from an indexed source, perform a full reindex for the indexed source before continuing with this procedure. To learn how to reindex content for an indexed source, see [Perform a full table index or reindex for a single AI Search indexed source](index-single-source-ais.md).

Role required: search\_application\_admin

## About this task

Attachment grouping is enabled by default for new search application configuration records. You only need to perform this procedure to enable attachment grouping for existing search application configuration records after upgrading from a previous release.

For details on how attachment grouping appears in the search results list and how you can interact with grouped attachment search results, see .

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **Search Experience** &gt; **Search Applications**.

2.  Select the record for the AI Search application that you want to enable attachment grouping for.

3.  Select the **Show parent for results that are attachments** option.

4.  Select **Update**.

    If any indexed source used in the search application doesn’t have the **index\_attachments** attribute set to **true**, the system displays a warning message. For each affected indexed source, set the **index\_attachments** attribute to **true**, then perform a full reindex.


## Result

AI Search groups matching attachment search results with their parent record results on the search application results page.

**Parent Topic:**[Search application configurations](../concept/defining-search-app-cfgs-ais.md)

