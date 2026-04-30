---
title: Zing displays search suggestions as users enter search terms
description: Display possible search query completions as users enter search terms.
locale: en-US
release: yokohama
product: Search Administration
classification: search-administration
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Zing text indexing and search engine, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Zing displays search suggestions as users enter search terms

Display possible search query completions as users enter search terms.

To use the Search Suggestions application, activate the com.glide.search.suggestions plugin if it's not already installed. For information, see [Request a plugin](../../plugins/task/t_RequestAPlugin.md) and [Activate a plugin](../../plugins/task/t_ActivateAPlugin.md).

Once you enable Search Suggestions, suggestions appear automatically when users enter text into Zing search fields in the Service Portal or Now Mobile.

![Search suggestions.](../image/search-suggestions.png "Automatic search suggestions")

If there are any matching suggestions from the user’s own previous searches, those suggestions appear first, with a clock icon. The remaining suggestions are those suggestions coming from the searches of other users.

In the Service Portal, you can use Search Suggestions or type-ahead functionality, but not both at the same time. In Now Mobile, only Search Suggestions is available. By default, new ServiceNow instances use Search Suggestions in the Service Portal. Upgraded instances use whatever was previously enabled. You can easily enable Search Suggestions on upgraded instances. To learn more, see [Enable and disable Search Suggestions in Zing](../task/enable-search-suggestions.md).

For full details on configuration and use of the Search Suggestions application, see [Search Suggestions](../reference/search-suggestions-overview.md).

-   **[Enable and disable Search Suggestions in Zing](../task/enable-search-suggestions.md)**  
Enable the Search Suggestions application to improve the Zing search user experience.
-   **[Set the maximum number of search suggestions Zing displays](../task/set-max-num-of-suggestions.md)**  
Set the maximum number of search suggestions Zing displays when users enter search strings in search applications.

**Parent Topic:**[Zing text indexing and search engine](c_ZingTextSearch.md)

**Related topics**  


[Features of Zing text indexing and search engine](../reference/features-zing.md)

[Available search options](c_IntroductionToSearching.md)

[Global search finds records from multiple tables](c_GlobalTextSearch.md)

[Zing generates search results in four phases](c_SearchProcess.md)

[Zing filters search results with access controls](zing-filters-search-results.md)

[Zing computes document scores using three components](c_DocumentScoring.md)

[Zing indexes words](zing-indexes-words.md)

[Zing can include attachments in search results](c_SearchingForAttachments.md)

[Zing removes stop words from queries](stop-words-removed-from-queries.md)

[Zing matches derived words with stemming](stemming-matches-derived-words.md)

[Zing can expand search results with synonyms](search-synonyms-expand-results.md)

[Installed with Zing](../reference/installed-with-zing.md)

