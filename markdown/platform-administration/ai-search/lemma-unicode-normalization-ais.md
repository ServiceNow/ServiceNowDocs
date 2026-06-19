---
title: Lemma and Unicode normalization
description: AI Search normalizes inflected words and Unicode glyphs during indexing and at search query time. Normalization improves search recall and enables users to find content with variant forms of their search query terms.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/ai-search/lemma-unicode-normalization-ais.html
release: zurich
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Administer, AI Search, Search administration, Configure core features, Administer]
---

# Lemma and Unicode normalization

AI Search normalizes inflected words and Unicode glyphs during indexing and at search query time. Normalization improves search recall and enables users to find content with variant forms of their search query terms.

Normalization features are automatically enabled and aren't configurable.

## Lemma normalization

Many languages include inflected forms of terms, such as plural nouns or verb tenses. AI Search normalizes inflected terms found in indexed content and search queries. Normalization enables matching based on a root form, such as the singular for a plural noun or the base form for a conjugated verb. This root form is called a lemma, and this process is referred to as lemma normalization.

For example, when a source record includes the conjugated verb `selling`, AI Search expands the indexed term to include the lemma form `sell` in addition to `selling`. When a user searches for the past-tense conjugated form `sold`, AI Search expands the search query term to include the lemma form `sell` as well as `sold`. Because the indexed term and the search query term include matching forms, the user's search returns the `selling` record as a result.

AI Search supports language-specific lemma normalization for Arabic, Brazilian Portuguese, Czech, Danish, Dutch, English, Finnish, French, French - Canada, German, Hebrew, Hungarian, Italian, Japanese, Korean, Norwegian \(Bokmål\), Polish, Portuguese, Russian, Simplified Chinese, Spanish, Swedish, Traditional Chinese, and Turkish.

**Note:** When parsing Finnish source record text and search terms, AI Search uses algorithmic stemming to identify lemmas.

## Decompounding

In addition to normalizing lemmas for German, Danish, Hungarian, Korean, Norwegian \(Bokmål\), and Swedish, AI Search indexes compound words and their individual component words. For example, when indexing a German record that contains the compound word `Humanressourcen`, AI Search indexes the component terms `Human` and `ressourcen` in addition to the compound term.

## Unicode normalization

AI Search performs Unicode normalization on indexed terms and search query terms. This normalization makes alphabetical Unicode glyphs searchable using their nearest equivalent characters.

For example, when indexing a record containing the term `resumé`, AI Search expands the term to also include the non-accented form `resume`. This record appears as a search result when users search for either `resume` or `resumé`.

Unicode normalization includes NFKD \(compatibility decomposition\) and NFKC \(compatibility composition\) stages. For more information on these normalization forms, see the Unicode Standard Annex \#15, [https://www.unicode.org/reports/tr15/](https://www.unicode.org/reports/tr15/).

## Interaction with other search features

The following table describes interactions between normalization and other search features.

|Feature|Interaction with lemma and Unicode normalization|
|-------|------------------------------------------------|
|[Genius Results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/genius-results-ais.md)|Search query terms added by lemma or Unicode normalization can't trigger Genius Result configurations with Term trigger conditions.|
|[Result improvement rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/result-improvement-rules-ais.md)|A search query term added by lemma or Unicode normalization can trigger a result improvement rule if it matches the rule's Query trigger.|
|[Stop words](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/stop-words-ais.md)|If a search query term is defined as a stop word, AI Search removes that term without normalizing it.|
|[Synonyms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/synonyms-ais.md)|If a search query term is defined as a synonym, AI Search doesn't normalize it.|
|[Typo handling](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/typo-handling-ais.md)|AI Search performs lemma and Unicode normalization on auto-corrected search query terms.|

**Parent Topic:**[Administering AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/administer-ais.md)

