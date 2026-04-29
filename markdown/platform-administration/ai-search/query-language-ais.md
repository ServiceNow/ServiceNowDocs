---
title: AI Search query language
description: Learn how to construct search queries using terms, phrases, and AI Search query operators.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Search, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# AI Search query language

Learn how to construct search queries using terms, phrases, and AI Search query operators.

## Search query terms and phrases

Specify terms and quoted phrases in the search query to find records that contain the same terms or phrases.

<table id="table_npg_gjn_mnb"><thead><tr><th>

Search query terms

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`conference`

</td><td>

Single-term search. Finds records that contain the term `conference`.**Note:** Search terms don't match substrings of indexed terms. As an example, searching for `exam` finds records that contain the term `exam`, but not records that contain the term `example`. To search for substring matches, you can use the `%` or `*` wildcard matching operators.

</td></tr><tr><td>

`conference room`

</td><td>

Conjunctive multi-term search. Finds records that contain both of the terms `conference` and `room` \(an intersection of sets\). The search terms can appear in any order or proximity in the record and may appear in different fields.**Note:** If you set the **Boolean search operator to use when a search query includes multiple terms** \(**glide.ais.query.search\_operator**\) system property to **OR query**, this search finds records that contain either of the terms `conference` or `room` \(a union of sets\).

</td></tr><tr><td>

`"conference room"`

</td><td>

Quoted phrase search. Finds records that contain the term `conference` followed immediately by the term `room`. The search terms must appear in this order and in the same field. **Note:** Quoting a phrase doesn't disable linguistic features \(such as normalization, synonym expansion, and stop word removal\) or wildcard operators. For example, a search for the quoted phrase `"email acc*"` expands the wildcard operator normally to find records that contain `email account` and `email access`.

</td></tr></tbody>
</table>AI Search ignores letter case for search query terms and phrases. For example, searching for `PIN` finds records containing `PIN` and `pin`.

**Note:** When processing search query terms, AI Search automatically strips out HTML and XML content by removing strings that start with `<` and end with `>`. As an example, if you enter `user <beth.anglin@example.com>` as your search terms, AI Search only searches for `user`. If you search for `<abel.tuter@example.com>`, AI Search treats the search as empty and returns no results. This behavior isn't configurable.

## Boolean search operators

Separate query terms and phrases with Boolean operators to override the default matching logic for the search query.

<table id="table_wwl_ll5_knb"><thead><tr><th>

Operator

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`OR`

</td><td>

Boolean disjunction operator. Finds records that contain any of the terms or phrases separated by `OR`. For example, searching for `"conference room" OR suite` finds records that contain the phrase `conference room` and records that contain the term `suite`.

 **Note:** If you set the **Boolean search operator to use when a search query includes multiple terms** \(**glide.ais.query.search\_operator**\) system property to **OR query**, this operator has no effect because search already treats all query terms and phrases as though separated by the `OR` operator.

</td></tr><tr><td>

hyphen \(`-`\)

</td><td>

Boolean negation operator. Excludes records containing the term or phrase that immediately follows the hyphen. For example, searching for `email -"email signature"` finds records that contain the term `email` but don't contain the phrase `email signature`.

</td></tr></tbody>
</table>## Wildcard matching operators

Use wildcard operators to find records that contain indexed terms matching a wildcard pattern.

<table id="table_nqj_wm5_knb"><thead><tr><th>

Operator

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`%`

</td><td>

Single-character wildcard operator. Include `%` in a search query term to match any one character in an indexed term. As an example, searching for `the%e` finds results containing wildcard matches such as `theme`, `there`, or `these`.

 AI Search also evaluates the search with the wildcard operator ignored, to look for literal matches. The non-wildcard operator parts of the search term are treated as a phrase, meaning that they must appear in the same order in the result as they do in the search. As an example, a search for `5000%000` returns results that contain `5000` followed by `000` as well as results that contain wildcard matches like `50007000`.

**Note:** The `%` operator must follow a string of three or more non-wildcard characters. For search query terms that don't satisfy this condition, AI Search only returns literal matches. As an example, if you search for `99%`, with only two non-wildcard characters preceding the `%` operator, AI Search only returns results with literal matches for `99`.

</td></tr><tr><td>

`*`

</td><td>

String wildcard operator. Include `*` in a search query term to match any string of zero or more characters in an indexed term. As an example, searching for `acc*` finds results containing wildcard matches such as `access`, `account`, `accrue`, `accumulate`, and `accuracy`.

 AI Search also evaluates the search with the wildcard operator ignored, to look for literal matches. The non-wildcard operator parts of the search term are treated as a phrase, meaning that they must appear in the same order in the result as they do in the search. As an example, a search for `753*268` returns results that contain `753` followed by `268` as well as results that contain wildcard matches like `7539268`.

**Note:** The `*` operator must follow a string of three or more non-wildcard characters. For search query terms that don't satisfy this condition, AI Search only returns literal matches. As an example, if you search for `ad*`, with only two non-wildcard characters preceding the `*` wildcard operator, AI Search only returns results with literal matches for `ad`.

</td></tr><tr><td>

`***`

</td><td>

Universal wildcard operator. Specify `***` as a search query to find all indexed terms and thus all records.**Note:** AI Search doesn't apply relevancy ranking to `***` queries. Results from `***` queries appear in an unspecified order.

</td></tr></tbody>
</table>**Note:** When expanding search terms that contain `%` or `*` wildcard operators, AI Search ignores terms defined as stop words. For example, suppose you define `the` and `their` as stop words. A search for `the*` won't expand to match `the` or `their`, but will still match non-stop word terms such as `there` and `these`.

**Parent Topic:**[Searching in AI Search](use-ais.md)

