---
title: Internationalization support for AI Search
description: AI Search supports indexing and search in all languages offered by the ServiceNow AI Platform. Search linguistic features are supported in Brazilian Portuguese, Dutch, English, Finnish, French, French - Canada, German, Italian, Japanese, Korean, Norwegian \(Bokmål\), Polish, Portuguese, Simplified Chinese, Spanish, Swedish, and Traditional Chinese.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2025-09-10"
reading_time_minutes: 8
breadcrumb: [Administer, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Internationalization support for AI Search

AI Search supports indexing and search in all languages offered by the ServiceNow AI Platform®. Search linguistic features are supported in Brazilian Portuguese, Dutch, English, Finnish, French, French - Canada, German, Italian, Japanese, Korean, Norwegian \(Bokmål\), Polish, Portuguese, Simplified Chinese, Spanish, Swedish, and Traditional Chinese.

Internationalization support is automatically enabled and isn't configurable.

To view the full list of languages offered as ServiceNow AI Platform plugins and supported in AI Search, see [Activate a language](../../localization/task/t_ActivateALanguage.md).

**Note:** After you activate a new language plugin, you must reindex all indexed source content that you want to make searchable in the new language. For details on reindexing, see [Perform a full table index or reindex for a single AI Search indexed source](../task/index-single-source-ais.md).

Language settings determine how AI Search separates the text of indexed content and search queries into individual terms. This process, called tokenization, is handled differently for each supported language, using language-specific settings. For example, most languages use spaces and punctuation to separate words and sentences, but when tokenizing Chinese or Japanese text, AI Search instead uses contextual interpretation to correctly identify word and sentence breaks. When tokenizing Japanese text, AI Search additionally recognizes the nakaguro \(middle dot\) as a word separator.

**Note:** If you indexed content in any of the following languages prior to the specified date, you should reindex it to benefit from improved tokenization and feature support added in the AI Search back end.

|Date|Languages to reindex|
|----|--------------------|
|August 2024|Brazilian Portuguese, Dutch, Italian, Japanese, Korean, Portuguese, Swedish|
|August 2025|Finnish|
|December 2025|Norwegian \(Bokmål\), Polish|

## Indexing behavior in supported languages

When indexing content and metadata from a ServiceNow AI Platform source record or an external document, AI Search uses tokenization settings for the language of the record or document, as shown in the following table.

<table id="table_kkt_zpc_pvb"><thead><tr><th>

Record or Document

</th><th>

Tokenization Settings

</th></tr></thead><tbody><tr><td>

Source record from the Task \[task\] table or one of its child tables

</td><td>

AI Search performs language identification and uses tokenization settings for the detected language to index the record's content and metadata.**Note:** Language identification only identifies Brazilian Portuguese, Dutch, English, Finnish, French, French - Canada, German, Italian, Japanese, Korean, Norwegian \(Bokmål\), Polish, Portuguese, Simplified Chinese, Spanish, Swedish, and Traditional Chinese. Content in other languages is identified and treated as English.

</td></tr><tr><td>

Source record from a non-Task table

</td><td>

AI Search uses tokenization settings for the record's language to index its content and metadata. If the record has no language specified, the ServiceNow AI Platform treats it as being in the instance's default language. In an English instance, for example, AI Search indexes records without specified languages using tokenization settings for English.

</td></tr><tr><td>

External document

</td><td>

AI Search performs language identification and uses tokenization settings for the detected language to index the document's content and metadata.**Note:** Language identification only identifies Brazilian Portuguese, Dutch, English, Finnish, French, French - Canada, German, Italian, Japanese, Korean, Norwegian \(Bokmål\), Polish, Portuguese, Simplified Chinese, Spanish, Swedish, and Traditional Chinese. Content in other languages is identified and treated as English.

</td></tr></tbody>
</table>**Note:** When indexing content and metadata, AI Search recognizes regions of Japanese, Simplified Chinese, and Traditional Chinese text embedded within text in other languages. These text regions are indexed with the appropriate language tokenization settings regardless of the surrounding text's language. As an example, suppose you index an English-language knowledge article that includes a paragraph of Simplified Chinese. AI Search indexes this paragraph's content as Simplified Chinese and the rest of the record's content as English.

## Search query behavior in supported languages

When processing search query text, AI Search uses tokenization settings for the language of the current user's ServiceNow AI Platform session.

**Note:** AI Search recognizes Japanese, Simplified Chinese, and Traditional Chinese terms in search queries. These terms are processed with the appropriate language tokenization settings regardless of the user session's language. As an example, if a user in a French user session searches for `remplacement ordinateur 笔记本电脑`, AI Search applies Simplified Chinese settings for the `笔记本电脑` term and French settings for the other search terms.

AI Search compares your search query terms with terms from indexed content and metadata, returning search results for indexed records or documents that contain matches. When your search terms are in the same language as the indexed terms, AI Search processes both sets of terms with the same tokenization settings, producing predictable matches and search results. If your search terms aren't in the same language as the indexed terms, AI Search processes the two sets of terms with different tokenization settings and matching may be unpredictable.

## Language dependence for search features

The following search features are language-dependent and supported only for the listed languages.

<table id="table_sp5_rt5_fnb"><thead><tr><th>

Feature

</th><th>

Language dependence and supported languages

</th></tr></thead><tbody><tr><td>

[Genius Results](genius-results-ais.md)

</td><td>

AI Search only evaluates Genius Result configurations with NLU triggers if the linked NLU model has the same language as the search query. Supported languages: English.

</td></tr><tr><td>

Language identification and tokenization

</td><td>

During indexing, AI Search identifies supported languages in Task table records and external documents. Text processing for the indexed content uses tokenization settings for the identified language. Supported languages: Brazilian Portuguese, Dutch, English, Finnish, French, French - Canada, German, Italian, Japanese, Korean, Norwegian \(Bokmål\), Polish, Portuguese, Simplified Chinese, Spanish, Swedish, and Traditional Chinese.

</td></tr><tr><td>

[Lemma and Unicode normalization](lemma-unicode-normalization-ais.md)

</td><td>

AI Search performs language-specific lemma normalization for terms in indexed content and search queries. Supported languages: Brazilian Portuguese, Dutch, English, Finnish, French, French - Canada, German, Italian, Japanese, Korean, Norwegian \(Bokmål\), Polish, Portuguese, Simplified Chinese, Spanish, Swedish, and Traditional Chinese.

**Note:** For German, Korean, Norwegian \(Bokmål\), and Swedish, AI Search performs term decompounding in addition to lemma normalization. For Finnish, AI Search uses algorithmic stemming to identify lemmas.

 AI Search performs Unicode normalization for all terms in indexed content and search queries.

 For more information on normalization of lemmas and Unicode forms in indexed content and search queries, see [Lemma and Unicode normalization](lemma-unicode-normalization-ais.md).

</td></tr><tr><td>

[Result improvement rules](result-improvement-rules-ais.md)

</td><td>

AI Search only evaluates activation for result improvement rules that have the same language as the search query or that have **All Languages** specified. Supported languages: All languages activated in your instance. For the list of languages you can activate, see [Activate a language](../../localization/task/t_ActivateALanguage.md).

</td></tr><tr><td>

[Stop words](stop-words-ais.md)

</td><td>

AI Search only considers stop words from dictionaries that have the same language as the search query. Supported languages: All languages activated in your instance. For the list of languages you can activate, see [Activate a language](../../localization/task/t_ActivateALanguage.md).

</td></tr><tr><td>

[Synonyms](synonyms-ais.md)

</td><td>

AI Search only considers synonyms from dictionaries that have the same language as the search query. Supported languages: All languages activated in your instance. For the list of languages you can activate, see [Activate a language](../../localization/task/t_ActivateALanguage.md).

</td></tr><tr><td>

[Typo handling](typo-handling-ais.md)

</td><td>

AI Search derives a separate list of auto-correction terms for each supported language found in search source indexed content. Auto-correction only replaces search query terms with terms from the list that has the same language as the search query. Supported languages: Brazilian Portuguese, Dutch, English, Finnish, French - Canada, French, German, Italian, Norwegian \(Bokmål\), Polish, Portuguese, Spanish, and Swedish. Typo handling isn't supported for Japanese, Korean, Simplified Chinese, or Traditional Chinese.

</td></tr></tbody>
</table>-   **[Searching translated content](searching-translated-content-ais.md)**  
Understand how AI Search searches translated fields and documents.
-   **[Assign Knowledge article search languages by country](../task/assign-kb-srch-langs-country-ais.md)**  
Improve multilingual search recall by defining a set of Knowledge article search languages for each user country. User searches can match Knowledge articles in any of the search languages specified for their country as well as in the language associated with their ServiceNow AI Platform® session.
-   **[Configure globally searchable knowledge articles](../task/configure-global-srch-kb-articles.md)**  
Define an encoded query for knowledge articles that you want to make searchable in any language.
-   **[Configure translation for knowledge article reference field values in facets](../task/translate-facet-field-values-kb.md)**  
Specify whether facets should display knowledge article reference field values in the search user's session language. If you disable translation, facets display knowledge article reference field values in your instance's default language.
-   **[AI Search interaction with fallback languages](interaction-fallback-language-ais.md)**  
When a fallback language is configured for the user's session language, AI Search searches translated documents in both languages. Search uses the appropriate stop word, synonym, and typo handling dictionaries for the fallback language.
-   **[Enable a global fallback locale for translated content](../task/enable-global-fallback-lang-ais.md)**  
Configure AI Search to match translated documents in a global fallback locale's language as well as the user's session language.

**Parent Topic:**[Administering AI Search](administer-ais.md)

