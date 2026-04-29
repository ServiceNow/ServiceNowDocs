---
title: Exclude a term from a typo handling dictionary
description: Prevent AI Search from auto-correcting a term in user search queries by excluding the term from a typo handling dictionary.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Typo handling, Search profiles, Configuring AI Search, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Exclude a term from a typo handling dictionary

Prevent AI Search from auto-correcting a term in user search queries by excluding the term from a typo handling dictionary.

## Before you begin

You must have already defined a search profile with one or more linked search sources.

Role required: ais\_admin

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **Search Experience** &gt; **Search Profiles**.

2.  Open the search profile that you want to exclude a typo handling term for.

3.  In the Typo Handling related list, open the typo handling dictionary.

4.  In the AI Search Dictionary Terms related list, select **New**.

5.  On the Dictionary Term form, fill in the fields.

    For a description of the field values, see [Dictionary Term form](../reference/dictionary-term-form-ais.md).

6.  Select **Submit**.

    The new term appears in the AI Search Dictionary Terms related list with the **State** set to **New**.

7.  Repeat the preceding steps for each additional term that you want to exclude.

8.  Select **Publish**.

    The typo handling dictionary appears in the Typo Handling related list with the **State** set to **Published**.


## What to do next

To make updated typo handling settings take effect, publish the search profile that you edited. For details on publishing a search profile, see [Publish an AI Search search profile](publish-search-profile-ais.md).

**Parent Topic:**[Typo handling](../concept/typo-handling-ais.md)

