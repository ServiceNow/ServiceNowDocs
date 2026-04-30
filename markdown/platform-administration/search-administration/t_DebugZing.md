---
title: Debug Zing
description: Debugging messages create a log of search processes as they occur. These messages may help administrators configure optimal performance settings.
locale: en-US
release: yokohama
product: Search Administration
classification: search-administration
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Available search options, Zing text indexing and search engine, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Debug Zing

Debugging messages create a log of search processes as they occur. These messages may help administrators configure optimal performance settings.

## Before you begin

Role required: admin

## About this task

-   To view debugging messages, navigate to **All** &gt; **System Diagnostics** &gt; **Session Debug** &gt; **Debug Text Search**. The search log messages appear at the bottom of the results page for the remainder of your session.

    ![Search results page showing Debug Output pane with search log messages.](../image/DebuggingMessages.png "Debugging Messages")

-   To debug text indexing problems, you may want to view text\_index events in the system log.
-   In rare cases, you may need to reset the text search caches after regenerating a text index. If text search fails for known words, diagnose and fix this problem:

## Procedure

1.  Enable text search debugging messages.

2.  In any table with search problems, search for the problem text.

3.  In the debug output, note the numbers used for the Stemmed terms.

4.  Navigate to the Ts Word \[ts\_word\] table's list view.

    1.  Select **All**.

    2.  In the **Filter** field, enter `ts_word.list`.

    3.  Press Enter.

5.  Locate the stemmed terms and compare the numbers in the list to the debug output from step [3](t_DebugZing.md#note-stemmed-term-numbers).

    If the numbers are different, the UI node's cache is stale.

6.  Navigate to **All** &gt; **System Definition** &gt; **Text Indexes**.

7.  Select the **Reset Text Search Caches** related link and select **OK**.


**Parent Topic:**[Available search options](../concept/c_IntroductionToSearching.md)

**Related topics**  


[List search finds records from the current table](../concept/c_TextSearchesInRecordLists.md)

[Boolean operators allow conditional search results](../concept/c_BooleanOperators.md)

[Quotation marks allow exact phrase searches](../concept/c_PhraseSearches.md)

[Wildcard characters allow searching for patterns and variations](../concept/c_Wildcards.md)

[Enable or disable the Zing junk filter](t_DisableTheJunkFilter.md)

