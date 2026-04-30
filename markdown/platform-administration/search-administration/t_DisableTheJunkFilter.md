---
title: Enable or disable the Zing junk filter
description: When its junk filter is enabled, Zing doesn't index or search for 2-digit numbers or single-character words \(unless they are Chinese or Japanese characters\). You can enable or disable the junk filter for individual tables.
locale: en-US
release: xanadu
product: Search Administration
classification: search-administration
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Available search options, Zing text indexing and search engine, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Enable or disable the Zing junk filter

When its junk filter is enabled, Zing doesn't index or search for 2-digit numbers or single-character words \(unless they are Chinese or Japanese characters\). You can enable or disable the junk filter for individual tables.

## Before you begin

Role required: admin

## About this task

For example, to disable matches for search terms like `a` or `40` in the Knowledge Base, turn on junk filtering for the kb\_knowledge table.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Dictionary**.

2.  Open the dictionary entry for the table.

3.  In the Attributes related list, set the value of the **Text index filter junk** attribute:

    1.  If you want Zing to include 2-digit numbers and single-character words when indexing and searching the table, set the attribute value to `false`.

    2.  If you want Zing to ignore 2-digit numbers and single-character words when indexing and searching the table, set the attribute value to `true`.

4.  Select the additional actions icon ![](../../ai-search/image/polaris-ui-form-context-menu-icon.png) in the Dictionary Entry form header, then select **Save**.

5.  Select the **Generate Text Index** related link and select **OK**.

    **Note:**

    -   To have the desired effect, you may also need to reconfigure the [automatic stop words](t_ConfigureAnAutomaticStopWord.md). For example, if a specific 2-digit number appears in all of your problem numbers \(92-0001, 92-0002, and so on\), the automatic stop word threshold is quickly exceeded and the word is no longer found in searches. To find that 2-digit number in the problem table, you must disable both junk filtering and automatic stop words.
    -   Disabling the junk filter results in a larger table index. For optimal performance, don't apply this attribute unless it's required.

**Parent Topic:**[Available search options](../concept/c_IntroductionToSearching.md)

**Related topics**  


[List search finds records from the current table](../concept/c_TextSearchesInRecordLists.md)

[Boolean operators allow conditional search results](../concept/c_BooleanOperators.md)

[Quotation marks allow exact phrase searches](../concept/c_PhraseSearches.md)

[Wildcard characters allow searching for patterns and variations](../concept/c_Wildcards.md)

[Debug Zing](t_DebugZing.md)

