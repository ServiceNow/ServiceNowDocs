---
title: Search profiles in AI Search
description: Search profiles contain settings for a search experience, including synonyms, stop words, typo handling, Genius Results, and result improvement rules. Define a search profile for each unique search experience that you want to offer in a ServiceNow AI Platform application. Publish search profiles to make them available in your search applications.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2026-02-13"
reading_time_minutes: 4
breadcrumb: [Configure, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Search profiles in AI Search

Search profiles contain settings for a search experience, including synonyms, stop words, typo handling, Genius Results, and result improvement rules. Define a search profile for each unique search experience that you want to offer in a ServiceNow AI Platform® application. Publish search profiles to make them available in your search applications.

A search profile contains settings that determine how AI Search generates search results for a given search experience. Publishing a search profile makes it available so you can link it to one or more search application configurations.

A search application configuration specifies a search profile to use, and also determines how generated search results are displayed in the application. To learn about search application configuration display settings, see [Search application configurations](defining-search-app-cfgs-ais.md).

The following table describes the search experience settings that you can configure in a search profile.

<table id="table_u5k_p3q_gnb"><thead><tr><th>

Setting

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Search sources](search-sources-ais.md)

</td><td>

Link one or more search sources to a search profile. Search sources give administrators precise control over the searchable content available to users.

</td></tr><tr><td>

[Synonyms](synonyms-ais.md)

</td><td>

Define language-specific dictionaries of terms that AI Search treats as equivalent in search queries. Synonyms improve search recall and provide a more natural search experience for users.

</td></tr><tr><td>

[Stop words](stop-words-ais.md)

</td><td>

Define language-specific dictionaries of common terms for AI Search to remove from search queries. Stop words improve search precision and result relevancy by discarding irrelevant matches.

</td></tr><tr><td>

[Typo handling](typo-handling-ais.md)

</td><td>

Configure settings for derivation of auto-correction terms from search source indexed content. AI Search replaces misspelled search query terms with auto-correction terms.

</td></tr><tr><td>

[Genius Results](genius-results-ais.md)

</td><td>

Analyze search query intent and display the best answers as Genius Result answer cards. Genius Results enable users to act directly on their search results.

</td></tr><tr><td>

[Result improvement rules](result-improvement-rules-ais.md)

</td><td>

Define rules with configurable triggers to modify search results for specific search queries. Result improvement rules enable administrators to boost, block, or promote records in a search query's result set.

</td></tr></tbody>
</table>## Publishing search profile settings

To make a search profile's settings active in search queries, you must publish it. Publishing propagates the following settings to search application configurations that reference the search profile.

-   The set of synonym and stop word dictionaries linked to the search profile
-   Settings, blocked terms, and derived auto-correction terms for typo handling dictionaries linked to the search profile
-   Result improvement rules and actions defined in the search profile

A search profile can have one of these states:

-   **New**: The search profile has never been published.
-   **Draft**: The search profile is saved with unpublished changes.
-   **Published**: The search profile is saved with all changes published.

In the **All** &gt; **AI Search** &gt; **Search Experience** &gt; **Search Profiles** list, search profiles with the **New** state display an alert triangle icon ![](../image/icon-alert-triangle.png). An informational message notifies you to publish these search profiles.

-   **[Create a search profile](../task/create-search-profile-ais.md)**  
Create a new search profile to store search experience settings for a search application.
-   **[Clone a search profile](../task/clone-search-profile-ais.md)**  
Create a copy of an existing search profile. The cloned search profile retains search sources, stop word and synonym dictionaries, Genius Result configurations, and result improvement rules from the original search profile.
-   **[Publish an AI Search search profile](../task/publish-search-profile-ais.md)**  
Publish a search profile to make pending changes to its settings take effect in linked search applications.
-   **[Link a search source to a search profile](../task/link-search-source-profile-ais.md)**  
Link search sources to a search profile to specify the content users can search through that profile.
-   **[Synonyms](synonyms-ais.md)**  
Synonyms expand search queries to include additional terms with equivalent meaning or usage. Improve search recall by configuring synonym dictionaries and defining synonyms.
-   **[Stop words](stop-words-ais.md)**  
Stop words remove search query terms that don't produce meaningful results. Improve search precision and relevancy by configuring stop word dictionaries and defining stop words.
-   **[Typo handling](typo-handling-ais.md)**  
AI Search replaces misspelled search query terms with auto-correction terms derived from indexed content. Configure typo handling dictionary settings to control derivation of auto-correction terms.
-   **[Genius Results](genius-results-ais.md)**  
Optionally display the best answers for a search query as actionable Genius Result cards included with search results.
-   **[Result improvement rules](result-improvement-rules-ais.md)**  
Define rules with configurable trigger conditions to boost, block, or promote search results for specific searches. You can also boost search results for documents matching elements of the user context, such as a user's country, OS, or device type.

**Parent Topic:**[Configuring AI Search](configuring-ais.md)

