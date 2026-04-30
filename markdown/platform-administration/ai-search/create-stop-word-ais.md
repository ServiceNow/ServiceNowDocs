---
title: Create stop words
description: Define terms to remove from search queries.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Stop words, Search profiles, Configure, AI Search, Search administration, Configure core features, Administer]
---

# Create stop words

Define terms to remove from search queries.

## Before you begin

Role required: ais\_admin

## About this task

You must have already created a stop word dictionary. For information on creating stop word dictionaries, see [Create a stop word dictionary linked to a search profile](create-stop-word-dict-ais.md).

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **AI Search Engine** &gt; **Dictionaries**.

2.  Open the stop word dictionary that you want to add the new stop word to.

3.  In the AI Search Dictionary Terms related list, select **New**.

4.  On the Dictionary Term form, fill in the fields.

    For a description of the field values, see [Dictionary Term form](../reference/dictionary-term-form-ais.md).

5.  Select **Submit**.

    The new stop word appears in the AI Search Dictionary Terms related list.

6.  Repeat the preceding steps for each additional stop word that you want to create.

7.  Choose one of the following actions.

    -   To save the modified dictionary and refresh its active stop words in all linked search profiles, select **Publish**.
    -   To save the modified dictionary without refreshing its active stop words in all linked search profiles, select **Update**.

**Parent Topic:**[Stop words](../concept/stop-words-ais.md)

