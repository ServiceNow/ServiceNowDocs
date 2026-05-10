---
title: Change the query mode of an indexed table
description: Set the query mode to specify whether searches on an indexed table must match all or only some of the search terms.
locale: en-US
release: australia
product: Search Administration
classification: search-administration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Zing indexes words, Zing text indexing and search engine, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Change the query mode of an indexed table

Set the query mode to specify whether searches on an indexed table must match all or only some of the search terms.

## Before you begin

To change the query mode of an indexed table, a text index must be present for the table. Make sure that text indexing is enabled for the table before changing the query mode. See [Configure a table for indexing and searching](configure-single-table-for-indexing.md#).

Role required: ts\_admin or admin

## About this task

Once a table is indexed, the data within the table can be searched through the global search bar. Change the query mode for the indexed table to allow global search to match all or only some of the searched terms. Enable a partial match rule to return results that partially match the searched terms.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Text Indexes**.

2.  Select the table you want to configure from the list of indexed tables.

3.  Use the combo box to select a **Default query mode**.

<table id="choicetable_rjr_4mz_yy"><tbody><tr><td id="d115067e103">

**Default**

</td><td>

The default query mode for a table is an AND query.

</td></tr><tr><td id="d115067e112">

**AND**

</td><td>

Matches all search terms.

</td></tr><tr><td id="d115067e121">

**OR**

</td><td>

Matches one or more search terms.

</td></tr><tr><td id="d115067e130">

**AND\_OR**

</td><td>

Matches all search terms. If no results are found, matches one or more search terms.

</td></tr></tbody>
</table>4.  To enable partial matching of search terms, configure the partial match rule in the **Partial Match Rule** field.

    Partial match rules return results that partially match the search terms. Use a partial match rule if queries often include many keywords \(if, for example, users cut and paste phrases into the global search bar\).

<table id="table_wdx_fpz_yy"><thead><tr><th>

Input type

</th><th>

Example

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Integer

</td><td>

3

</td><td>

Indicates the minimum number of search terms to be matched.

</td></tr><tr><td>

Negative integer

</td><td>

-2

</td><td>

Indicates that the number of search terms, minus this number, should be matched.

</td></tr><tr><td>

Percentage

</td><td>

75%

</td><td>

Indicates the minimum percentage of search terms to be matched. The minimum number of search terms is the number computed from the percentage rounded down.

</td></tr><tr><td>

Negative percentage

</td><td>

-25%

</td><td>

Indicates that the number of search terms, minus this percentage, should be matched. The minimum number of search terms is the number computed from the percentage rounded down and subtracted from the total number of search terms.

</td></tr><tr><td>

Combination

</td><td>

3&lt;70%

</td><td>

A positive integer, followed by a less than symbol, followed by any of the previously mentioned input types. Indicates that if the number of search terms is equal to or less than the integer, all search terms are required. If the number of search terms is greater than the integer, the specification applies. In this example: if there are 1–3 search terms, all are required. If there are 4 or more search terms, only 70% are required.

</td></tr><tr><td>

Multiple combinations

</td><td>

3&lt;-25%, 9&lt;-5

</td><td>

Multiple conditional specifications separated by commas. In this example: if there are 1–3 search terms, all are required. If there are 4–9 search terms, all but 25% are required. If there are more than 9 search terms, all but 5 are required.

</td></tr></tbody>
</table>
**Parent Topic:**[Zing indexes words](../concept/zing-indexes-words.md)

**Related topics**  


[Zing indexes punctuation as part of some words](../concept/c_PunctuationForSearchResults.md)

[Zing indexes some HTML elements](../concept/c_SearchingHTMLContent.md)

[Configure a table for indexing and searching](configure-single-table-for-indexing.md#)

[Configure a text index group to search across multiple tables](index-multiple-tables.md)

[Zing index and search dictionary attributes](../reference/index-attributes.md)

[Regenerate a text index for a table](t_RegenerateATextIndexForATable.md)

[Remove an index](t_RemoveAnIndex.md)

[Remove an index for a specific field](t_RemoveAnIndexForASpecificField.md)

[Remove the text index for a child table](remove-index-child-table.md)

[Enable indexing of text in multi-row variable sets](index-text-multi-row-variable-sets.md)

[Text indexing statistics and status](../reference/r_ViewTextIndexingStatsAndStatus.md)

[Configure tables to use the Japanese tokenizer](configure-tables-japanese-tokenizer.md)

