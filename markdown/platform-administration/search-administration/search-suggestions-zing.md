---
title: Zing displays search suggestions as users enter search terms
description: Display possible search query completions as users enter search terms.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/search-administration/search-suggestions-zing.html
release: australia
product: Search Administration
classification: search-administration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Zing text indexing and search engine, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Zing displays search suggestions as users enter search terms

Display possible search query completions as users enter search terms.

To use the Search Suggestions application, activate the com.glide.search.suggestions plugin if it's not already installed. For information, see [Request a plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_RequestAPlugin.md) and [Activate a plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_ActivateAPlugin.md).

Once you enable Search Suggestions, suggestions appear automatically when users enter text into Zing search fields in the Service Portal or Now Mobile.

\[Omitted image "search-suggestions.png"\] Alt text: Search suggestions.

If there are any matching suggestions from the user’s own previous searches, those suggestions appear first, with a clock icon. The remaining suggestions are those suggestions coming from the searches of other users.

In the Service Portal, you can use Search Suggestions or type-ahead functionality, but not both at the same time. In Now Mobile, only Search Suggestions is available. By default, new ServiceNow instances use Search Suggestions in the Service Portal. Upgraded instances use whatever was previously enabled. You can easily enable Search Suggestions on upgraded instances. To learn more, see [Enable and disable Search Suggestions in Zing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/enable-search-suggestions.md).

For full details on configuration and use of the Search Suggestions application, see [Search Suggestions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-suggestions/search-suggestions-overview.md).

-   **[Enable and disable Search Suggestions in Zing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/enable-search-suggestions.md)**  
Enable the Search Suggestions application to improve the Zing search user experience.
-   **[Set the maximum number of search suggestions Zing displays](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/set-max-num-of-suggestions.md)**  
Set the maximum number of search suggestions Zing displays when users enter search strings in search applications.

**Parent Topic:**[Zing text indexing and search engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/c_ZingTextSearch.md)

**Related topics**  


[Features of Zing text indexing and search engine]()

[Available search options]()

[Global search finds records from multiple tables]()

[Zing generates search results in four phases]()

[Zing filters search results with access controls]()

[Zing computes document scores using three components]()

[Zing indexes words]()

[Zing can include attachments in search results]()

[Zing removes stop words from queries]()

[Zing matches derived words with stemming]()

[Zing can expand search results with synonyms]()

[Installed with Zing]()

