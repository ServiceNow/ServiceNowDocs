---
title: Analyze search relevancy
description: Analyze data from the Search Suggestions tables to understand how your users interact with search.
locale: en-US
release: zurich
product: Search Suggestions
classification: search-suggestions
topic_type: task
last_updated: "2025-11-19"
reading_time_minutes: 2
breadcrumb: [Using Search Suggestions, Search Suggestions, Search administration, Configure core features, Administer]
---

# Analyze search relevancy

Analyze data from the Search Suggestions tables to understand how your users interact with search.

## Before you begin

Role required: ais\_admin

## About this task

Search Suggestions uses the following tables:

-   [Search Event \[sys\_search\_event\]](../reference/understanding-search-suggestion-tables.md#section_eqs_xwj_xhb): Stores all search strings and search results.
-   [Search Source Event \[sys\_search\_source\_event\]](../reference/understanding-search-suggestion-tables.md#section_fj1_zzj_xhb): Stores search strings and search results and ties them to a data source, for example, the suggestion came from the knowledge base table rather than the catalog table.
-   [Search Suggestion \[sys\_search\_suggestion\]](../reference/understanding-search-suggestion-tables.md#section_ic4_j2k_xhb): Stores suggestions for searches.

For details on the Search Suggestions tables, see [Search Suggestions tables](../reference/understanding-search-suggestion-tables.md).

## Procedure

1.  Display the Search Event \[sys\_search\_event\] table by navigating in your browser to `https://<instance name>.service-now.com/sys_search_event_list.do`.

2.  Find search queries with **Has results** column values of **false**.

    A value of false means that someone searched but didn’t get any search results. You can choose to create information, such as a Knowledge article, to provide search results in the future, create synonyms for the search words that would surface a search result, or not provide information if the question is irrelevant.

3.  Average the numbers in the **Click rank** column.

    Click rank shows which search result you selected. If you click the first result in the list of search results, the click rank value is 1. If you click the 6th result listed, the click rank value is 6. If you click multiple search results, the click rank is the highest listing value. For example, if you click the first result, return to the search page and click the 6th result, return to the search page and click the 4th result and find an answer, the click rank is 6 \(not 4\). A click rank of 0 means that you didn't select any search result, or that you selected a Genius Result answer card in AI Search. Lower positive click rank values indicate that the top search results are the most relevant, so the goal is to reduce the average value for this field.

4.  Determine the click-through rate by dividing the number of records where the click rank isn't zero by the total number of records.

    Higher click-through rate numbers are better. Click-through rate is a good indicator of how often users find relevant results, but it doesn’t reveal how much effort it took to find those results. That’s where click rank comes in. Click rank describes how much effort it took the user to find what they perceived to be a relevant result.

5.  Average the numbers in the **Refinements** column.

    Refinement is the number of actions a user took to reduce the number of search results. Actions include sorting and filtering. More refinements means more effort to find relevant search results, so lower numbers are better.

6.  Display the Search Source Event \[sys\_search\_source\_event\] table by navigating in your browser to `https://<instance name>.service-now.com/sys_search_source_event_list.do`.

7.  Find search queries with **Has results** column values of **false**.

    False means that someone searched but didn't get any search results from a particular source table, for example, the Knowledge Base table. You can choose to create information, such as a Knowledge article, on the source to provide search results in the future, create synonyms for the search words that would surface a search result in that source table, or not provide information if the question is irrelevant.


