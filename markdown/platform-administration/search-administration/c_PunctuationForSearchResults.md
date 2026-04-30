---
title: Zing indexes punctuation as part of some words
description: Zing indexes some punctuation marks as part of some words to improve search results for common search terms.
locale: en-US
release: zurich
product: Search Administration
classification: search-administration
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Zing indexes words, Zing text indexing and search engine, Search administration, Configure core features, Administer]
---

# Zing indexes punctuation as part of some words

Zing indexes some punctuation marks as part of some words to improve search results for common search terms.

<table id="table_vyb_g1w_1q"><thead><tr><th>

Punctuation

</th><th>

Indexed to find

</th><th>

Search behavior

</th></tr></thead><tbody><tr><td>

Ampersands \[&amp;\]

</td><td>

Company names

</td><td>

Zing locates terms containing punctuation characters that are common in company names: ampersands \(&amp;\), plus signs \(+\), or hyphens \(-\). For example, a search for `H&R Block` locates exact matches to the search term.

</td></tr><tr><td>

Apostrophes \['\]

</td><td>

Proper names

</td><td>

Zing ignores trailing possessives and retains most others to find company names. For example, a search for `O'Reilly's` locates matches to O'Reilly and O'Reilly's.

</td></tr><tr><td rowspan="2">

Hyphens \[-\]

</td><td>

Company names

</td><td>

Zing locates terms containing punctuation characters that are common in company names: ampersands \(&amp;\), plus signs \(+\), or hyphens \(-\). For example, a search for `Coca-Cola` locates exact matches to the search term.

</td></tr><tr><td>

Product numbers

</td><td>

Zing locates product numbers that follow a typical pattern. To meet this pattern, search terms must contain frequent numbers and only include underscores \(\_\), hyphens \(-\), or periods for punctuation. For example, a search for `PROD-10-987` locates exact matches to the search term.

</td></tr><tr><td rowspan="2">

Numbers \[123\]

</td><td>

Product numbers

</td><td>

Zing locates product numbers that follow a typical pattern. To meet this pattern, search terms must contain frequent numbers and only include underscores \(\_\), hyphens \(-\), or periods for punctuation. For example, a search for `PROD10987` locates exact matches to the search term.

</td></tr><tr><td>

Record numbers

</td><td>

Zing locates record numbers that follow a typical pattern. To meet this pattern, search terms must start with a recognized record number prefix. For example, a search for `INT1234567` locates exact matches to the Incident record.

</td></tr><tr><td rowspan="4">

Periods \[.\]

</td><td>

Acronyms

</td><td>

Zing locates acronyms whether they are separated by periods or not. For example, a search for `u.s.a.` locates matches to usa or u.s.a.. Note that wildcard searches may affect acronym handling.

 In another example, a search for `u.s.*` may yield better results than a search for `u.s*`.

</td></tr><tr><td>

Host names

</td><td>

Zing locates sequences of letters and numbers separated only by periods. For example, a search for `en.myhost123.com` locates exact matches to the search term.

</td></tr><tr><td>

IP addresses

</td><td>

Zing locates numbers that follow a typical IPv4 address pattern. For example, a search for `10.0.0.1` locates exact matches to the search term.

</td></tr><tr><td>

Product numbers

</td><td>

Zing locates product numbers that follow a typical pattern. To meet this pattern, search terms must contain frequent numbers and only include underscores \(\_\), hyphens \(-\), or periods for punctuation. For example, a search for `PROD.10.987` locates exact matches to the search term.

</td></tr><tr><td>

Plus signs \[+\]

</td><td>

Company names

</td><td>

Zing locates terms containing punctuation characters that are common in company names: ampersands \(&amp;\), plus signs \(+\), or hyphens \(-\). For example, a search for `Google+` locates exact matches to the search term.

</td></tr><tr><td>

Underscores \[\_\]

</td><td>

Product numbers

</td><td>

Zing locates product numbers that follow a typical pattern. To meet this pattern, search terms must contain frequent numbers and only include underscores \(\_\), hyphens \(-\), or periods for punctuation. For example, a search for `PROD_10_987` locates exact matches to the search term.

</td></tr></tbody>
</table>**Note:** The punctuation handling described here doesn't affect wildcard and boolean operators. These operators provide separate Zing functions.

**Parent Topic:**[Zing indexes words](zing-indexes-words.md)

**Related topics**  


[Zing indexes some HTML elements](c_SearchingHTMLContent.md)

[Configure a table for indexing and searching](../task/configure-single-table-for-indexing.md#)

[Configure a text index group to search across multiple tables](../task/index-multiple-tables.md)

[Zing index and search dictionary attributes](../reference/index-attributes.md)

[Regenerate a text index for a table](../task/t_RegenerateATextIndexForATable.md)

[Remove an index](../task/t_RemoveAnIndex.md)

[Remove an index for a specific field](../task/t_RemoveAnIndexForASpecificField.md)

[Remove the text index for a child table](../task/remove-index-child-table.md)

[Change the query mode of an indexed table](../task/configure-table-query-mode.md)

[Enable indexing of text in multi-row variable sets](../task/index-text-multi-row-variable-sets.md)

[Text indexing statistics and status](../reference/r_ViewTextIndexingStatsAndStatus.md)

[Configure tables to use the Japanese tokenizer](../task/configure-tables-japanese-tokenizer.md)

