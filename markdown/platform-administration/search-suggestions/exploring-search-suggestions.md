---
title: Exploring Search Suggestions
description: Learn how Search Suggestions displays suggestions to users in AI Search applications and the Zing text indexing and search engine. Review the rules that dictate which suggestions are offered in each search application and context.
locale: en-US
release: zurich
product: Search Suggestions
classification: search-suggestions
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Search Suggestions, Search administration, Configure core features, Administer]
---

# Exploring Search Suggestions

Learn how Search Suggestions displays suggestions to users in AI Search applications and the Zing text indexing and search engine. Review the rules that dictate which suggestions are offered in each search application and context.

## Search Suggestions overview

The Search Suggestions application makes it possible for search applications to display suggested search completions or results to users as they enter terms into a search field.

Search Suggestions saves query terms and results from user searches. A Build Search Suggestions script runs against this saved data periodically to generate auto-complete suggestions for AI Search and search suggestions for Zing text search. The Prune Search Suggestions script runs periodically to remove low-relevancy suggestions.

Administrators can limit the age of saved search data used to generate suggestions. They can also configure specific suggestions to prevent them from being displayed to search application users.

## Search Suggestions workflow

In this infographic, see a sample workflow of how different users in an organization configure and use auto-complete suggestions and search suggestions with the Search Suggestions application.

![Infographic showing how administrators, search users, and non-authenticated guest users configure and use Search Suggestions. For details, refer to the following description.](../image/search-suggestions-workflow.png "Configuring and using Search Suggestions")

In this Search Suggestions workflow:

1.  -   Administrators configure Search Suggestions settings, including scheduling of scripts and restrictions on which saved search results the system uses to create auto-complete suggestions and search suggestions.
-   The system saves users' search results and uses them to generate new auto-complete suggestions and search suggestions.
2.  -   Search users view and select generated auto-complete suggestions in AI Search applications.
-   Search users view and select generated search suggestions in Zing.
-   Non-authenticated guest users access and review the list of generated suggestions created from searches by external users.
3.  Administrators review and analyze saved search results to improve understanding of how users interact with generated suggestions, allowing for more effective tuning of Search Suggestions settings.

## Search Suggestions benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|View and select relevant auto-complete suggestions when searching in AI Search applications.|[Auto-complete suggestions in AI Search applications](../../ai-search/concept/auto-complete-ais.md#)|AI Search users|
|View and select relevant search suggestions when searching with the Zing text search engine.|[Zing displays search suggestions as users enter search terms](search-suggestions-zing.md)|Zing search users|
|See the list of auto-complete suggestions and search suggestions created from searches by external users.|[Use the GraphQL REST API to view suggestions created from external user searches](../task/view-ext-user-search-suggestions.md)|Non-authenticated guest user|
|Control suggestion generation time by configuring how often the system builds auto-complete suggestions and search suggestions from user search strings.|[Schedule the Build Search Suggestions script](../task/schedule-search-suggestion-builds.md)|Administrator|
|Improve suggestion relevancy by configuring how often the system prunes the least relevant auto-complete suggestions and search suggestions from the Search Suggestion \[sys\_search\_suggestion\] table.|[Schedule suggestion pruning](../task/limit-number-of-suggestions.md)|Administrator|
|Increase suggestion freshness by using only the most recent search event records to create auto-complete suggestions and search suggestions.|[Set maximum age for searches used in suggestion generation](../task/set-maximum-number-of-search-strings.md)|Administrator|
|Prevent creation of unwanted auto-complete suggestions and search suggestions.|[Prevent the creation of suggestions in special cases](../task/preventing-suggestions.md)|Administrator|
|Understand how users interact with search by analyzing data from the Search Suggestions tables.|[Analyze search relevancy](../task/improve-search-results.md)|Administrator|

