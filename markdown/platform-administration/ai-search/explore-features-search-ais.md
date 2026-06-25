---
title: Provide users with powerful and flexible search
description: AI Search includes search features that help users find the answers they need.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/ai-search/explore-features-search-ais.html
release: australia
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Explore, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Provide users with powerful and flexible search

AI Search includes search features that help users find the answers they need.

-   **Powerful query language**

    Query for indexed terms and phrases. Control query logic with Boolean operators. Match a range of indexed terms using wildcard operators.

    For a complete guide to supported query language syntax and operators, see [AI Search query language](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/query-language-ais.md).

-   **Auto-complete search queries**

    Display suggestions in the input field as users compose their searches. Suggestions include recent and popular search queries and results as well as entries from the user's personal search history.

    Auto-complete suggestions are linguistic features that search administrators configure in search application configurations. For more information on auto-complete suggestion type settings, see [Configure an auto-complete suggestion type in an AI Search application configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/auto-complete-ais.md).

-   **Language-sensitive lemma and Unicode normalization of search query terms**

    Support natural language search by expanding search query terms to match alternate inflections and forms. AI Search supports language-specific lemma normalization for Arabic, Brazilian Portuguese, Czech, Danish, Dutch, English, Finnish, French, French - Canada, German, Hebrew, Hungarian, Italian, Japanese, Korean, Norwegian \(Bokmål\), Polish, Portuguese, Russian, Simplified Chinese, Spanish, Swedish, Traditional Chinese, and Turkish. It supports Unicode normalization for content in all ServiceNow AI Platform® languages.

    Lemma and Unicode normalization are linguistic features that don't require configuration. For more details on normalization behavior, see [Lemma and Unicode normalization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/lemma-unicode-normalization-ais.md).

-   **Expand search query terms using configurable synonyms**

    Improve search recall by configuring language-specific dictionaries of terms with equivalent meanings or usage. When a search query includes any of these terms, AI Search expands it to include all equivalent terms, providing users with a more natural search experience.

    Synonyms are linguistic features that search administrators configure in search profiles. For details on configuring synonyms and synonym dictionaries, see [Synonyms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/synonyms-ais.md). AI Search supports synonym dictionaries for Arabic, Brazilian Portuguese, Czech, Danish, Dutch, English, Finnish, French, French - Canada, German, Hebrew, Hungarian, Italian, Japanese, Korean, Norwegian \(Bokmål\), Polish, Portuguese, Russian, Simplified Chinese, Spanish, Swedish, Traditional Chinese, and Turkish.

-   **Remove excessively frequent search terms using configurable stop words**

    Increase search precision by configuring language-specific dictionaries of frequently appearing terms that dilute search relevancy. AI Search removes these stop words from user search queries to exclude irrelevant results.

    Stop words are linguistic features that search administrators configure in search profiles. For details on configuring stop words and stop word dictionaries, see [Stop words](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/stop-words-ais.md). AI Search supports stop word dictionaries for Arabic, Brazilian Portuguese, Czech, Danish, Dutch, English, Finnish, French - Canada, French, German, Hebrew, Hungarian, Italian, Norwegian \(Bokmål\), Polish, Portuguese, Russian, Spanish, Swedish, and Turkish.

-   **Auto-correct typos in search query terms**

    Automatically replace misspelled search query terms with spellings found in indexed content. Typo corrections are displayed above search results. Users can always choose to repeat the search with their original query terms.

    Typo handling auto-correction is a linguistic feature that search administrators configure in search profiles. For details on controlling the set of available auto-correction terms, see [Typo handling](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/typo-handling-ais.md). AI Search supports derivation of auto-correction terms for Arabic, Brazilian Portuguese, Czech, Danish, Dutch, English, Finnish, French - Canada, French, German, Hebrew, Hungarian, Italian, Norwegian \(Bokmål\), Polish, Portuguese, Russian, Spanish, Swedish, and Turkish.


**Parent Topic:**[Exploring AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/explore-ais.md)

