---
title: Internationalization support
description: AI Search supports indexing and search for all languages offered by the ServiceNow AI Platform. Search administrators can configure AI Search search features for languages activated in your instance.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2025-09-10"
reading_time_minutes: 9
breadcrumb: [Explore, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Internationalization support

AI Search supports indexing and search for all languages offered by the ServiceNow AI Platform®. Search administrators can configure AI Search search features for languages activated in your instance.

For full details on language support in AI Search search features, see [Internationalization support for AI Search](international-language-support-ais.md).

## Search features

The following table displays the set of AI Search search features available for specific ServiceNow AI Platform languages.

<table id="table_pbc_qnw_rqb"><thead><tr><th>

Language

</th><th>

Search features supported

</th></tr></thead><tbody><tr><td>

English

</td><td>

-   [Genius Results](genius-results-ais.md)
-   [Language identification](international-language-support-ais.md)
-   [Lemma and Unicode normalization](lemma-unicode-normalization-ais.md)
-   [Result improvement rules](result-improvement-rules-ais.md)
-   [Stop words](stop-words-ais.md)
-   [Synonyms](synonyms-ais.md)
-   [Typo handling](typo-handling-ais.md)

</td></tr><tr><td>

Brazilian Portuguese, Dutch, French, French - Canada, Italian, Polish, and Spanish

</td><td>

-   [Language identification](international-language-support-ais.md)
-   [Lemma and Unicode normalization](lemma-unicode-normalization-ais.md)
-   [Result improvement rules](result-improvement-rules-ais.md)
-   [Stop words](stop-words-ais.md)
-   [Synonyms](synonyms-ais.md)
-   [Typo handling](typo-handling-ais.md)

</td></tr><tr><td>

Finnish

</td><td>

-   [Language identification](international-language-support-ais.md)
-   [Lemma and Unicode normalization](lemma-unicode-normalization-ais.md) \(using algorithmic stemming to identify lemmas\)
-   [Result improvement rules](result-improvement-rules-ais.md)
-   [Stop words](stop-words-ais.md)
-   [Synonyms](synonyms-ais.md)
-   [Typo handling](typo-handling-ais.md)

</td></tr><tr><td>

German, Norwegian \(Bokmål\), and Swedish

</td><td>

-   [Language identification](international-language-support-ais.md)
-   [Lemma and Unicode normalization](lemma-unicode-normalization-ais.md) \(including decompounding\)
-   [Result improvement rules](result-improvement-rules-ais.md)
-   [Stop words](stop-words-ais.md)
-   [Synonyms](synonyms-ais.md)
-   [Typo handling](typo-handling-ais.md)

</td></tr><tr><td>

Japanese, Simplified Chinese, and Traditional Chinese

</td><td>

-   [Language identification](international-language-support-ais.md) \(including text-region and search-term identification\)
-   [Lemma and Unicode normalization](lemma-unicode-normalization-ais.md)
-   [Result improvement rules](result-improvement-rules-ais.md)
-   [Stop words](stop-words-ais.md)
-   [Synonyms](synonyms-ais.md)

</td></tr><tr><td>

Korean

</td><td>

-   [Language identification](international-language-support-ais.md)
-   [Lemma and Unicode normalization](lemma-unicode-normalization-ais.md) \(including decompounding\)
-   [Result improvement rules](result-improvement-rules-ais.md)
-   [Stop words](stop-words-ais.md)
-   [Synonyms](synonyms-ais.md)

</td></tr><tr><td>

All other ServiceNow AI Platform languages activated in your instance

</td><td>

-   [Unicode normalization](lemma-unicode-normalization-ais.md)
-   [Result improvement rules](result-improvement-rules-ais.md)
-   [Stop words](stop-words-ais.md)
-   [Synonyms](synonyms-ais.md)

</td></tr></tbody>
</table>## Translated content search

By default, AI Search only returns results for records with translated content, such as knowledge articles, that are in the user's ServiceNow AI Platform session language. You can modify this default behavior in several ways:

-   **[Assign Knowledge article search languages by country](../task/assign-kb-srch-langs-country-ais.md)**

    Improve multilingual search recall by defining a set of Knowledge article search languages for each user country. User searches can match Knowledge articles in any of the search languages specified for their country as well as in the language associated with their ServiceNow AI Platform session.

-   **[Configure globally searchable knowledge articles](../task/configure-global-srch-kb-articles.md)**

    Define an encoded query to match knowledge articles that you want to make searchable regardless of the user's session language.

-   **[Configure a fallback language](interaction-fallback-language-ais.md)**

    [Set a fallback language](../../localization/task/set-fallback-language.md) for the user's session language. AI Search returns translated content results from the selected fallback language as well as the user's session language.

-   **[Enable a global fallback locale for translated content](../task/enable-global-fallback-lang-ais.md)**

    Configure a global fallback locale to use for all translated content searches. AI Search returns translated content results from the global fallback locale's language as well as the user's session language.

    **Note:** The global fallback locale works best if you want to make all English-language records globally searchable.


**Parent Topic:**[Exploring AI Search](explore-ais.md)

