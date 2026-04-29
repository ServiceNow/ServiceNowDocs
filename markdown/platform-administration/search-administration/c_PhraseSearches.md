---
title: Quotation marks allow exact phrase searches
description: Wrap search terms in quotation marks to search for an exact phrase consisting of one or more words.
locale: en-US
release: australia
product: Search Administration
classification: search-administration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Available search options, Zing text indexing and search engine, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Quotation marks allow exact phrase searches

Wrap search terms in quotation marks to search for an exact phrase consisting of one or more words.

Search terms in quotation marks are treated as exact phrase searches. When you search for an exact phrase, Zing only matches documents that contain the quoted words in the exact order you specify.

As an example, searching for `email password` returns search results that include `email` and `password` in any order, including records with these text strings:

-   `enter your email password`
-   `your email account password`

If you search for the quoted phrase `"email password"`, Zing returns search results with text `enter your email password` because they contain `email password` as an exact phrase. It doesn't return results with text `your email account password` because the search terms don't occur in the exact order specified in your search phrase.

Exact phrase searches ignore:

-   stop words
-   punctuation marks
-   wildcard characters

**Note:** Wildcard characters are ignored as punctuation.

For example, searching for the phrase `"email password"` returns the same search results as these phrases:

-   `"email the password"` because the stop word `the` is ignored.
-   `"email password?"` because the punctuation mark `?` is ignored.
-   `"email password*"` because the wildcard character `*` is ignored as punctuation.

**Parent Topic:**[Available search options](c_IntroductionToSearching.md)

**Related topics**  


[List search finds records from the current table](c_TextSearchesInRecordLists.md)

[Boolean operators allow conditional search results](c_BooleanOperators.md)

[Wildcard characters allow searching for patterns and variations](c_Wildcards.md)

[Enable or disable the Zing junk filter](../task/t_DisableTheJunkFilter.md)

[Debug Zing](../task/t_DebugZing.md)

