---
title: Boolean operators allow conditional search results
description: Construct complex searches using Boolean AND, OR, and NOT operators in global text searches.
locale: en-US
release: australia
product: Search Administration
classification: search-administration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Available search options, Zing text indexing and search engine, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Boolean operators allow conditional search results

Construct complex searches using Boolean AND, OR, and NOT operators in global text searches.

You can use Boolean operators in all global text search interfaces:

-   Global text search field
-   Knowledge Base search
-   List search for text

**Note:** Boolean operators are case-sensitive. As an example, the system recognizes `OR` as a Boolean operator, but treats `Or` and `or` as regular search terms.

<table id="table_zg4_fvp_w4"><thead><tr><th>

Operator

</th><th>

Description

</th></tr></thead><tbody><tr><td>

OR or vertical bar symbol \(\|\)

</td><td>

Finds a match if any of the search terms exist in a document \(a union of sets\). For example, to find documents that contain either `email password` or just `email`, you can search for `"email password" OR email` or `"email password"|email`. Using the `.or.` operator, which the system uses when you create OR condition groups for fields other than Keywords with the condition builder, can produce different results. For example, this filter searches for records with short descriptions containing `SSO` and then searches separately for records with short descriptions containing `SAML`:

![Searching with the filter choice lists.](../image/search_with_lists.png "Searching with the filter choice lists")

**Note:** By design, you can only have one Keywords filter condition per condition set. If you select the Keywords field in a filter choice list, the OR button for that filter condition becomes unavailable. Similarly, if you construct an OR filter condition, the Keywords field becomes unavailable in the filter choice lists.

</td></tr><tr><td>

AND

</td><td>

Finds a match if all search terms exist in a document \(an intersection of sets\). For example, to find documents that contain both "CPU load" and "10 minutes", search for `"CPU load" AND "10 minutes"` By default, Zing applies an AND operator between all search terms not separated by OR or NOT operators. For example, if you enter `email server down` as your search terms, the system searches for `email AND server AND down`.

**Note:** For Knowledge Base searches, if the default AND search returns poor results, the search is automatically re-run with the OR operator. Administrators can configure the knowledge base search to always use OR by modifying the **glide.knowman.search.operator** system property.

</td></tr><tr><td>

NOT, minus \(-\), or exclamation point \(!\)

</td><td>

Excludes documents that contain the search term after the NOT operator \(a difference of sets\). For example, to find documents that contain "CPU load" but not "10 minutes", you can search for `"CPU load" NOT "10 minutes"` or `"CPU load" -"10 minutes"` or `"CPU load" !"10 minutes"`. NOT must be a stand-alone term in your search. For example, `atom NOT ion` excludes the term `ion`, but `NOTION` searches for the term `notion`.

 The minus and exclamation point symbols must immediately precede the search term that you want to exclude. For example, a search for `email !Joe` excludes `Joe` but a search for `email ! Joe` includes `Joe`.

 You can't use the NOT operator to exclude all terms in your search. For example, the following search returns no results: `NOT "10 minutes"`.

</td></tr></tbody>
</table>**Parent Topic:**[Available search options](c_IntroductionToSearching.md)

**Related topics**  


[List search finds records from the current table](c_TextSearchesInRecordLists.md)

[Quotation marks allow exact phrase searches](c_PhraseSearches.md)

[Wildcard characters allow searching for patterns and variations](c_Wildcards.md)

[Enable or disable the Zing junk filter](../task/t_DisableTheJunkFilter.md)

[Debug Zing](../task/t_DebugZing.md)

[Knowledge properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management/r_KnowledgeProperties.md)

