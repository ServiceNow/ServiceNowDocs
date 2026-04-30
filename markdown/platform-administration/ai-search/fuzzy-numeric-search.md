---
title: Fuzzy numeric search in AI Search
description: Fuzzy numeric search lets you find indexed records by their Number field values without needing to enter alphabetic prefixes or leading zeroes.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2026-01-29"
reading_time_minutes: 5
breadcrumb: [Search, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Fuzzy numeric search in AI Search

Fuzzy numeric search lets you find indexed records by their Number field values without needing to enter alphabetic prefixes or leading zeroes.

## Fuzzy numeric search overview

Fuzzy numeric search in AI Search allows your numerical search terms to match indexed ServiceNow AI Platform® records by their Number field values. The fuzzy matching compares the numeric search term with each indexed record's Number, ignoring its alphabetical prefix and any leading zeroes. As an example, if you index knowledge article and problem records, a search for `23583` might return knowledge article KB00023583 and problem PRB00023583 as search results.

When fuzzy numeric search is activated, AI Search checks all-numeric search terms for fuzzy numeric matches when you search and when computing auto-complete suggestions for your search terms.

**Important:**

Fuzzy numeric search only searches records from numbered tables. These are tables with Number fields that have prefixes defined in the Number \[sys\_number\] table. To learn about record numbering and the Number table, see [Record numbering](../../field-administration/concept/c_ManagingRecordNumbering.md).

Child tables that inherit the Number field from their parent table can't be searched using fuzzy numeric search. Only tables that have their own Number field defined work with this feature.

Fuzzy numeric search only finds numeric field values in predefined fields named **number**. It doesn't search custom fields or predefined fields with other names.

## Fuzzy numeric matching behavior

The following table provides additional details on how fuzzy numeric matching operates.

|Fuzzy numeric matching behavior|Description|
|-------------------------------|-----------|
|AI Search only checks all-numeric search terms for fuzzy matches|A search for `KB52578` doesn't match knowledge article KB00052578 because the search term includes non-numeric characters. If you search for `16867 test`, your all-numeric `16867` search term is checked for fuzzy numeric matches, but your non-numeric `test` search term isn't.|
|Fuzzy numeric matching ignores leading zeroes in all-numeric search terms|A search for `07295` returns the same fuzzy numeric matches as a search for `7295` \(without the leading zero\) does.|
|Fuzzy numeric search only matches Number field values from indexed records|A search for `28761` matches the knowledge article with Number field value KB00028761, but it doesn't match the term `KB00028761` if it occurs in the text of other knowledge articles.|
|Fuzzy numeric matching only ignores alphabetical prefixes and leading zeroes in record Number field values|A search for `729` matches knowledge article KB00000729, but doesn't match article KB00003729 because its Number field value has a non-zero digit before the matching substring.|
|To be a fuzzy match, a numeric substring must match the final digits of a record's Number field value|A search for `1164` matches knowledge article KB00001164, but doesn't match article KB00116497 because its Number field value includes digits after the matching substring.|

## Examples of fuzzy numeric search

The following table includes examples to illustrate how fuzzy numeric searches match search results. These examples assume that records are indexed from the Knowledge \[kb\_knowledge\] and Problem \[problem\] tables.

<table id="table_gcn_bt1_zdc"><thead><tr><th>

Search

</th><th>

Search results

</th></tr></thead><tbody><tr><td>

73492

</td><td>

Search matches these results:-   Knowledge article with Number KB00073492
-   Problem with Number PRB00073492
-   Any indexed record or document that includes `73492` as a whole term \(not a substring\)

</td></tr><tr><td>

05638

</td><td>

Search matches these results:-   Knowledge article with Number KB0005638
-   Problem with Number PRB0005638
-   Any indexed record or document that includes `05638` as a whole term \(not a substring\)

</td></tr><tr><td>

2541 828

</td><td>

Search matches these results when using the AND \(conjunctive\) operator:-   Knowledge article with Number KB0002541 and text including `828` as a whole term \(not a substring\)
-   Knowledge article with Number KB0000828 and text including `2541` as a whole term \(not a substring\)
-   Problem with Number PRB0002541 and text including `828` as a whole term \(not a substring\)
-   Problem with Number PRB0000828 and text including `2541` as a whole term \(not a substring\)
-   Any indexed record or document that includes `2541` and `828` as whole terms \(not substrings\)

 Search matches these results when using the OR \(disjunctive\) operator:

-   Knowledge article with Number KB0002541
-   Knowledge article with Number KB0000828
-   Problem with Number PRB0002541
-   Problem with Number PRB0000828
-   Any indexed record or document that includes `2541` as a whole term \(not a substring\)
-   Any indexed record or document that includes `828` as a whole term \(not a substring\)

**Note:** For more details on the AND and OR operators, see the description of the **glide.ais.query.search\_operator** system property in [AI Search system properties](../reference/system-properties-ais.md).

</td></tr><tr><td>

model 9433

</td><td>

Search matches these results when using the AND \(conjunctive\) operator:-   Knowledge article with Number KB0009433 and text including `model` as a whole term \(not a substring\)
-   Problem with Number PRB0009433 and text including `model` as a whole term \(not a substring\)
-   Any indexed record or document that includes `model` and `9433` as whole terms \(not substrings\)

 Search matches these results when using the OR \(disjunctive\) operator:

-   Knowledge article with Number KB0009433
-   Problem with Number PRB0009433
-   Any indexed record or document that includes `model` as a whole term \(not a substring\)
-   Any indexed record or document that includes `9433` as a whole term \(not a substring\)

**Note:** For more details on the AND and OR operators, see the description of the **glide.ais.query.search\_operator** system property in [AI Search system properties](../reference/system-properties-ais.md).

</td></tr></tbody>
</table>## Fuzzy numeric search availability

Starting with the Xanadu Patch 9 release, fuzzy numeric search is included with AI Search but is deactivated by default. It's only available at search time if your ServiceNow AI Platform® admin has activated it. To view activation steps for this feature, see [Activate fuzzy numeric search in AI Search](../task/activate-fuzzy-numeric-search-ais.md).

**Parent Topic:**[Searching in AI Search](use-ais.md)

