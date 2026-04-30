---
title: Create synonyms
description: Define terms to treat as equivalent in search queries.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Synonyms, Search profiles, Configure, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Create synonyms

Define terms to treat as equivalent in search queries.

## Before you begin

Role required: ais\_admin

## About this task

You must have already created a synonym dictionary. For information on creating synonym dictionaries, see [Create a synonym dictionary linked to a search profile](create-synonym-dict-ais.md).

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **AI Search Engine** &gt; **Dictionaries**.

2.  Open the synonym dictionary that you want to add the new synonym to.

3.  In the AI Search Dictionary Terms related list, select **New**.

4.  On the Dictionary Term form, fill in the fields.

    For a description of the field values, see [Dictionary Term form](../reference/dictionary-term-form-ais.md).

5.  Select **Submit**.

    The new synonym appears in the AI Search Dictionary Terms related list.

6.  Repeat the preceding steps for each additional synonym that you want to create.

7.  Choose one of the following actions.

    -   To save the modified dictionary and refresh its active synonyms in all linked search profiles, select **Publish**.
    -   To save the modified dictionary without refreshing its active synonyms in all linked search profiles, select **Update**.

## Define a synonym with equivalent words and phrases

This example shows a synonym defining `vacation`, `holiday`, `PTO`, and the phrase `time off` as equivalent.

![The AI Search Dictionary Term new record form in Synonym view shows Term set to vacation and Payload set to ["holiday","pto","time off"].](../image/synonym-example-vacation.png)

**Parent Topic:**[Synonyms](../concept/synonyms-ais.md)

