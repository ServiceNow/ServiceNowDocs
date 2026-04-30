---
title: Disable a stop word in Zing
description: Configure Zing to return results for text search terms that match a stop word's stemmed form.
locale: en-US
release: yokohama
product: Search Administration
classification: search-administration
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Zing removes stop words from queries, Zing text indexing and search engine, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Disable a stop word in Zing

Configure Zing to return results for text search terms that match a stop word's stemmed form.

## Before you begin

Role required: admin

## About this task

Zing's stemming feature can cause search to return no results for an acronym or short word if its stemmed form is defined as a stop word.

Indications that a search term may be stemmed to a stop word include:

-   Text search returns no results for the affected term.
-   The system displays an informational message: `Your text query contained only common words or ambiguous wildcards, please refine your search and try again.`

As an example, imagine that a user searches for the acronym `AMS`. Zing stems this search term to `am`. Because `am` is defined as a stop word, Zing ignores the search term. The user's `AMS` search returns no results, and the system displays the informational message.

To enable correct search results for an affected term, administrators can disable the relevant stop word in the global and table-specific stop word lists.

**Note:** Disabling a stop word can impact search performance and relevancy. Text search will return matching results for the disabled stop word as well as for its stemmed forms.

For more details on stemming in Zing, see [Zing matches derived words with stemming](../concept/stemming-matches-derived-words.md).

## Procedure

1.  To disable a stop word in the global stop word list, perform the following steps:

    1.  Navigate to **All** &gt; **System Definition** &gt; **Text Index Stop Words**.

    2.  Open the record for the stop word you want to disable.

    3.  On the Stop Word form, clear the **Active** option, then select **Update**.

2.  To disable a stop word in table-specific stop word lists, perform the following steps for each table that includes the stop word:

    1.  Navigate to **All** &gt; **System Definition** &gt; **Text Indexes**.

    2.  Open the table's text index record.

    3.  In the Index Stop Words related list, open the record for the stop word.

        **Note:** If the Index Stop Words related list isn't visible, open the form context menu and select **View** &gt; **Default view**.

    4.  On the Index Stop Word form, set the stop word's stop mode to **Not a Stop Word** and select **Update**.

    5.  On the Text Index form, select the **Regenerate Text Index** related link.


## Result

Zing no longer ignores the disabled stop word and its stemmed forms in text searches.

**Parent Topic:**[Zing removes stop words from queries](../concept/stop-words-removed-from-queries.md)

**Related topics**  


[Configure a global stop word](t_ConfigureAGlobalStopWord.md)

[Configure a table-specific stop word](t_ConfigureATableSpecificStopWord.md)

[Enable automatic stop words for a table](t_ConfigureAnAutomaticStopWord.md)

