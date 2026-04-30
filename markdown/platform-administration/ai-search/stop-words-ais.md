---
title: Stop words
description: Stop words remove search query terms that don't produce meaningful results. Improve search precision and relevancy by configuring stop word dictionaries and defining stop words.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2025-07-16"
reading_time_minutes: 8
breadcrumb: [Search profiles, Configure, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Stop words

Stop words remove search query terms that don't produce meaningful results. Improve search precision and relevancy by configuring stop word dictionaries and defining stop words.

Stop words are common terms that appear on a large proportion of indexed records. Examples of such terms can include articles, conjunctions, personal pronouns, and prepositions. By defining these terms as stop words, you can improve search precision and result relevancy for users.

You can define stop words in the default stop word dictionary for a search profile, or create your own stop word dictionaries linked to search profiles. Create and publish stop words for each dictionary. Publish the dictionary to make your stop words take effect for searches that use linked search profiles.

You can delete stop word dictionaries that aren't linked to any search profiles.

## Stop word usage in search

When a search query includes a term defined as a stop word, AI Search removes the term from the search query.

For example, a stop word might remove the term `my` from a search query for `upgrade my laptop`. This modified search query only matches records containing the more relevant terms `upgrade` and `laptop`.

## Conditions for stop word eligibility

To be eligible for removal from a search query's terms, a stop word must satisfy the following conditions:

-   It must be active.
-   The stop word dictionary that includes it must be published.
-   Its length doesn't exceed the [dictionary term-length limit](stop-words-ais.md#dictionary-term-length-limit-stop-words).

The system locates eligible stop words in stop word dictionaries as follows:

<table id="table_swg_bft_qtb"><thead><tr><th>

Condition

</th><th>

Result

</th></tr></thead><tbody><tr><td>

The search profile specified for the search query links to a published stop word dictionary for the search query's language.

</td><td>

The system only considers stop words from the linked stop word dictionary. As an example, suppose a search application's search profile links to a French stop word dictionary. When a user searches in French in this application, only stop words from the linked French stop word dictionary are eligible for removal from the search query terms.

</td></tr><tr><td>

The search profile specified for the search query doesn't link to a published stop word dictionary for the search query's language.

</td><td>

The system only considers stop words from the default \(English\) stop word dictionary. As an example, suppose a search application's search profile has no linked Spanish stop word dictionary. When a user searches in Spanish in this application, only stop words from the default \(English\) stop word dictionary are eligible for removal from the search query terms.

</td></tr></tbody>
</table>For more details on language support in stop word dictionaries, see [Language dependence](stop-words-ais.md#stop-word-language-dependence-section).

## Dictionary term-length limit

By default, AI Search ignores stop word terms that exceed 256 characters in length. You can override this default limit by adding the **query.maxDictionaryTermLength** system property. The integer value of this system property indicates the maximum allowable character length for stop word and synonym dictionary terms.

For information on adding a system property, see [Add a system property](../../reference-pages/reference/r_AvailableSystemProperties.md#).

**Warning:** Exercise caution when increasing the dictionary term-length limit beyond its default value. Processing long dictionary terms increases AI Search's memory usage, and in some cases search queries may fail with out-of-memory errors.

## Multi-word phrases

A stop word can include either a single word or a multi-word phrase. AI Search removes multi-word phrases from the search query when the query terms exactly match the order and proximity of the phrased words in the stop word definition. If a user searches with these words in a different arrangement, no term removal occurs.

For example, the following table describes AI Search stop word removal behavior for a stop word that includes the multi-word phrase `retirement account`.

|Search query terms|Stop word removal behavior|
|------------------|--------------------------|
|my retirement account|AI Search removes the terms `retirement account` from the search query.|
|my bank retirement account|AI Search removes the terms `retirement account` from the search query.|
|my account retirement|AI Search doesn't remove any terms from the search query.|
|my retirement bank account|AI Search doesn't remove any terms from the search query.|

## Case sensitivity

By default, AI Search ignores letter case when comparing stop words with search query terms. You can enable case sensitivity for a stop word dictionary. This option affects all stop words defined in the dictionary.

When case sensitivity is enabled, stop words in the dictionary only match search query terms or phrases that include the same combination of uppercase and lowercase letters.

For example, if you define a `RAID` stop word in a dictionary with case sensitivity enabled, AI Search ignores the search query term `RAID` but treats the search query term `raid` normally.

## Punctuation sensitivity

By default, AI Search ignores punctuation when comparing stop words with search query terms. You can enable punctuation sensitivity for a stop word dictionary. This option affects all stop words defined in the dictionary.

When punctuation sensitivity is enabled, stop words in the dictionary only match search query terms or phrases that include the same punctuation.

For example, if you define a `one-half` stop word in a dictionary with punctuation sensitivity enabled, AI Search removes the search query term `one-half` but doesn't remove the search query term `one half`.

## Language dependence

Stop word removal is language-dependent. You specify a language for each stop word dictionary, and this language applies to all stop words defined in the dictionary. Stop words from dictionaries with the same language as the search query are eligible for removal.

**Note:** If the search profile specified for a search query has no linked stop word dictionary for the search query language, AI Search uses the default \(English\) stop word dictionary as a fallback.

AI Search supports stop word dictionaries for all languages activated in your instance. For the list of languages you can activate, see [Activate a language](../../localization/task/t_ActivateALanguage.md).

You can only link one stop word dictionary per language to a given search profile.

## Interaction with other search features

The following table describes interactions between stop words and other search features.

<table id="table_vdr_yd5_fnb"><thead><tr><th>

Feature

</th><th>

Interaction with stop words

</th></tr></thead><tbody><tr><td>

[Genius Results](genius-results-ais.md)

</td><td>

If a search query term that matches a Genius Result configuration's Term trigger is defined as a stop word, AI Search evaluates the trigger before removing that stop word from the search query. When computing Q&amp;A Genius Results for a search query, AI Search ignores stop words in the query.

</td></tr><tr><td>

[Lemma and Unicode normalization](lemma-unicode-normalization-ais.md)

</td><td>

If a search query term is defined as a stop word, AI Search removes that term without normalizing it.

</td></tr><tr><td>

[Result improvement rules](result-improvement-rules-ais.md)

</td><td>

If a search query term that matches a result improvement rule's Query trigger is defined as a stop word, AI Search evaluates the rule trigger before removing the stop word from the search query.

</td></tr><tr><td>

[Synonyms](synonyms-ais.md)

</td><td>

If a synonym definition includes a term defined as a stop word, AI Search retains that term when checking whether the synonym expands a search query.

 For example, suppose you define `as` and `a` as stop words and `SAAS`↔`︎software as a service` as a synonym.

-   If you search for `saas`, AI Search retains the `as` and `a` terms in the synonym expansion. As a result, the search query matches the following records:
    -   records that contain the original search query term `saas`
    -   records that contain the synonym expansion phrase `software as a service`
-   If you search for `software as a service`, AI Search retains the `as` and `a` query terms when checking for synonym expansions. As a result, the search query matches the following records:
    -   records that contain the phrase `software as a service`
    -   records that contain the synonym expansion term `saas`

</td></tr><tr><td>

[Typo handling](typo-handling-ais.md)

</td><td>

If a misspelled search query term is defined as a stop word, AI Search auto-corrects that term normally instead of removing it.

 AI Search ignores terms defined as stop words when determining an auto-correction for a misspelled search query term. For example, if you define `email` as a stop word, AI Search doesn't offer `email` as an auto-correction when you search for `emial`.

</td></tr><tr><td>

[Wildcard operators](use-ais.md)

</td><td>

When expanding search terms that contain `%` or `*` wildcard operators, AI Search ignores terms defined as stop words. For example, suppose you define `the` and `their` as stop words. A search for `the*` won't expand to match `the` or `their`, but will still match non-stop word terms such as `there` and `these`.

</td></tr></tbody>
</table>## Publishing stop word dictionaries

Publishing a stop word dictionary makes its settings and active stop words take effect in all linked search profiles.

Publishing a search profile updates the profile's stop word dictionary links but doesn't update the dictionary's settings or active stop words in AI Search.

-   **[Create a stop word dictionary linked to a search profile](../task/create-stop-word-dict-ais.md)**  
Define a new stop word dictionary and link it to a search profile.
-   **[Create stop words](../task/create-stop-word-ais.md)**  
Define terms to remove from search queries.
-   **[Clone a stop word dictionary](../task/clone-stop-word-dictionary-ais.md)**  
Create a copy of an existing stop word dictionary.
-   **[Link a stop word dictionary to a search profile](../task/link-stop-word-dict-profile-ais.md)**  
Link an existing stop word dictionary to one or more search profiles.
-   **[Unlink a stop word dictionary from a search profile](../task/unlink-stop-word-dict-ais.md)**  
Remove a stop word dictionary that isn't linked from any search profile.
-   **[Delete a stop word dictionary](../task/delete-stop-word-dict-ais.md)**  
Remove a stop word dictionary that isn't linked from any search profile.

**Parent Topic:**[Search profiles in AI Search](defining-search-profiles-ais.md)

