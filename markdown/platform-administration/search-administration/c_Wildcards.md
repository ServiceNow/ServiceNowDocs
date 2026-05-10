---
title: Wildcard characters allow searching for patterns and variations
description: Expand search results to match any non-space character. Zing supports both single-character and multiple-character wildcards.
locale: en-US
release: australia
product: Search Administration
classification: search-administration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Available search options, Zing text indexing and search engine, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Wildcard characters allow searching for patterns and variations

Expand search results to match any non-space character. Zing supports both single-character and multiple-character wildcards.

The following searches support Zing wildcard characters.

-   Global text search
-   Knowledge Base

    **Note:** Users with the admin role can enable wildcard search in the Knowledge context by navigating to **All** &gt; **Contextual Search** &gt; **Search Contexts**, editing the **Knowledge Base Search** record, and selecting the **Enable wildcard searches** check box.

-   [Search a list](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/t_SearchAList.md)

    **Note:** To perform a wildcard text search of a list, you must select **for text** as the search field. If you select a list field instead of **for text**, wildcard characters in search terms will be interpreted as [list search wildcards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/t_SearchAList.md) \(for non-reference fields\) or as [auto-complete wildcards](../../field-administration/concept/c_AutoCompleteForReferenceFields.md#) \(for reference fields\).


To perform a single-character wildcard search, use the percent sign \(`%`\) character. This wildcard finds words that contain any one character in place of the percent-sign-character. For example, to find words such as **text** or **test**, search for `te%t`.

To perform a multiple-character wildcard search, use the asterisk \(`*`\) character. This wildcard finds words that contain zero or more characters in place of the asterisk-character. For example, to find words such as **planned** or **placed**, search for `pl*d`.

You can use wildcard characters anywhere in a search string, and can include multiple wildcards in the same word. For example, to find words including **affordable**, **effort**, and **offering**, search for `%ff%r*`.

If a wildcard search returns too many hits, the system displays a message asking you to refine the search. Administrators can [set a global text search property](../task/set-global-text-search-properties.md) to change the limit for wildcard search results.

**Note:** Wildcard text searches are only effective with multiple character words. A wildcard within a sequence of pictogram characters returns too many options for an efficient search. Wildcards are best used with letter-based words.

## Wildcard characters and synonym matching

Zing doesn't expand the `%` and `*` wildcard characters when looking for synonyms that match your search term. These characters are treated as literal characters when finding matching synonyms. As an example, if you search for `issu*`, Zing doesn't find synonyms for `issue`, but it does find synonyms for `issu*`.

**Parent Topic:**[Available search options](c_IntroductionToSearching.md)

**Related topics**  


[List search finds records from the current table](c_TextSearchesInRecordLists.md)

[Boolean operators allow conditional search results](c_BooleanOperators.md)

[Quotation marks allow exact phrase searches](c_PhraseSearches.md)

[Enable or disable the Zing junk filter](../task/t_DisableTheJunkFilter.md)

[Debug Zing](../task/t_DebugZing.md)

