---
title: Synonyms
description: Synonyms expand search queries to include additional terms with equivalent meaning or usage. Improve search recall by configuring synonym dictionaries and defining synonyms.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Search profiles, Configuring AI Search, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Synonyms

Synonyms expand search queries to include additional terms with equivalent meaning or usage. Improve search recall by configuring synonym dictionaries and defining synonyms.

To define synonyms, modify the default synonym dictionary for a search profile or create a new synonym dictionary linked to one or more search profiles. Create and publish synonyms for each dictionary. Publish the dictionary to make your synonyms take effect for searches that use linked search profiles.

You can delete synonym dictionaries that aren't linked to any search profiles.

## Synonym usage in search

When a search query includes a term defined in a synonym, AI Search expands the search to include all equivalent terms defined in the synonym.

For example, a synonym might expand the search query term `vacation` to `vacation OR holiday OR pto`. The expanded query returns records that contain any of the three equivalent terms.

## Conditions for synonym eligibility

To be eligible for expanding a search query's terms, a synonym must satisfy the following conditions:

-   It must be active.
-   The synonym dictionary that includes it must be published.
-   Its length doesn't exceed the [dictionary term-length limit](synonyms-ais.md#dictionary-term-length-limit-synonyms).

The system locates eligible synonyms in synonym dictionaries as follows:

<table id="table_swg_bft_qtb"><thead><tr><th>

Condition

</th><th>

Result

</th></tr></thead><tbody><tr><td>

The search profile specified for the search query links to a published synonym dictionary for the search query's language.

</td><td>

The system only considers synonyms from the linked synonym dictionary. As an example, suppose a search application's search profile links to a French synonym dictionary. When a user searches in French in this application, only synonyms from the linked French synonym dictionary are eligible to expand search query terms.

</td></tr><tr><td>

The search profile specified for the search query doesn't link to a published synonym dictionary for the search query's language.

</td><td>

The system only considers synonyms from the default \(English\) synonym dictionary. As an example, suppose a search application's search profile has no linked Spanish synonym dictionary. When a user searches in Spanish in this application, only synonyms from the default \(English\) synonym dictionary are eligible to expand search query terms.

</td></tr></tbody>
</table>For more details on language support in synonym dictionaries, see [Language dependence](synonyms-ais.md#synonym-language-dependence-section).

## Synonym terms and payloads

Each synonym includes two or more equivalent terms, defined in two fields. The **Term** field contains one term designated as the synonym's label. The **Payload** field contains the remaining equivalent terms, formatted as a JSON array.

Synonym term expansion is bidirectional. AI Search treats all terms defined in the **Term** and **Payload** fields as equivalent, as illustrated in the following table.

|Use case|Synonym expansion behavior|
|--------|--------------------------|
|Search query term matches the term from a synonym's **Term** field|AI Search expands the search query term to match all equivalent terms from the **Payload** field.|
|Search query term matches a term from the **Payload** field|AI Search expands the search query term to match the term from the **Term** field and all remaining equivalent terms from the **Payload** field.|

## Dictionary term-length limit

By default, AI Search ignores synonym terms that exceed 256 characters in length. You can override this default limit by adding the **query.maxDictionaryTermLength** system property. The integer value of this system property indicates the maximum allowable character length for stop word and synonym dictionary terms.

For information on adding a system property, see [Add a system property](../../reference-pages/reference/r_AvailableSystemProperties.md#).

**Warning:** Exercise caution when increasing the dictionary term-length limit beyond its default value. Processing long dictionary terms increases AI Search's memory usage, and in some cases search queries may fail with out-of-memory errors.

## Multi-word phrases

A synonym term can include either a single word or a multi-word phrase. AI Search expands multi-word phrases when the search query terms exactly match the order and proximity of the phrased words in the synonym definition. If a user searches with these words in a different arrangement, no expansion occurs.

For example, the following table describes AI Search expansion behavior for a synonym that includes the single word `401k` and the multi-word phrase `retirement account`.

|Search query terms|Synonym expansion behavior|
|------------------|--------------------------|
|401k|AI Search expands the search query to match either `401k` or `retirement account`.|
|retirement account|AI Search expands the search query to match either `401k` or `retirement account`.|
|retirement account bank|AI Search expands the search query to match either `401k` or `retirement account` in addition to `bank`.|
|account retirement|AI Search doesn't expand the search query terms.|
|retirement bank account|AI Search doesn't expand the search query terms.|

When search query terms match a multi-term synonym, AI Search treats those terms as a quoted phrase. For example, if you define `401k` and `retirement account` as synonyms and a user searches for the unquoted terms `retirement account`, AI Search returns results that match the quoted phrase `"retirement account"`.

## Case sensitivity

By default, synonym expansion ignores letter case when comparing synonyms with search query terms. You can enable case sensitivity for a synonym dictionary. This option affects all synonyms defined in the dictionary.

When case sensitivity is enabled, synonyms in the dictionary only match search query terms or phrases that include the same combination of uppercase and lowercase letters.

For example, if you define a synonym including the word `CASE` and the phrase `Computer-Aided Software Engineering`, AI Search expands searches for `CASE` but not searches for `case`.

## Punctuation sensitivity

By default, synonym expansion ignores punctuation when comparing synonyms with search query terms. You can enable punctuation sensitivity for a synonym dictionary. This option affects all synonyms defined in the dictionary.

When punctuation sensitivity is enabled, synonyms in the dictionary only match search query terms or phrases that include the same punctuation.

For example, suppose you define a synonym equating `U-S-A` with `University of South Australia` and another synonym equating `U.S.A.` with `United States of America`. Without punctuation sensitivity enabled, a search for `U.S.A.` expands to match both `University of South Australia` and `United States of America`. When punctuation sensitivity is enabled, the same search only expands to match `United States of America`.

## Language dependence

Synonym expansion is language-dependent. You specify a language for each synonym dictionary, and this language applies to all synonyms defined in the dictionary. Synonyms from dictionaries with the same language as the search query are eligible for expansion.

**Note:** If the search profile specified for a search query has no linked synonym dictionary for the search query language, AI Search uses the default \(English\) synonym dictionary as a fallback.

AI Search supports synonym dictionaries for all languages activated in your instance. For the list of languages you can activate, see [Activate a language](../../localization/task/t_ActivateALanguage.md).

## Interaction with other search features

The following table describes interactions between synonyms and other search features.

<table id="table_vdr_yd5_fnb"><thead><tr><th>

Feature

</th><th>

Interaction with synonyms

</th></tr></thead><tbody><tr><td>

[Genius Results](genius-results-ais.md)

</td><td>

Synonym expansion terms can't trigger Genius Result configurations with Term trigger conditions. When computing Q&amp;A Genius Results for a search query, AI Search expands synonyms in the query.

</td></tr><tr><td>

[Lemma and Unicode normalization](lemma-unicode-normalization-ais.md)

</td><td>

If a search query term is defined as a synonym, AI Search doesn't normalize it.

</td></tr><tr><td>

[Result improvement rules](result-improvement-rules-ais.md)

</td><td>

By default, a synonym expansion term can activate a result improvement rule if it matches the rule's Query trigger. You can prevent synonym expansion terms from activating a rule with a Query trigger by clearing the **Expand Synonyms For Query Conditions** option that appears when you define the Query trigger.**Note:** Starting in the Xanadu release, AI Search uses synonyms to expand user context field values when applying boost actions from result improvement rules. As an example, if the user context location is `Paris` and you define a synonym that defines `Paris` and `France` as equivalent, your result improvement rule boosts documents containing `France` as well as those containing `Paris`. For more details on boost actions, see [Boost search results using a result improvement rule](../task/boost-results-ais.md#).

</td></tr><tr><td>

[Stop words](stop-words-ais.md)

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

If a misspelled search query term is defined as a synonym, AI Search expands that synonym without auto-correcting it.

</td></tr></tbody>
</table>## Publishing synonym dictionaries

Publishing a synonym dictionary makes its settings and active synonyms take effect in all linked search profiles.

Publishing a search profile updates the profile's synonym dictionary links but doesn't update the dictionary's settings or active synonyms in AI Search.

-   **[Create a synonym dictionary linked to a search profile](../task/create-synonym-dict-ais.md)**  
Define a new synonym dictionary and link it to a search profile.
-   **[Create synonyms](../task/create-synonym-ais.md)**  
Define terms to treat as equivalent in search queries.
-   **[Clone a synonym dictionary](../task/clone-synonym-dictionary-ais.md)**  
Create a copy of an existing synonym dictionary.
-   **[Link a synonym dictionary to a search profile](../task/link-synonym-dict-profile-ais.md)**  
Link an existing synonym dictionary to one or more search profiles.
-   **[Unlink a synonym dictionary from a search profile](../task/unlink-synonym-dict-ais.md)**  
Remove a synonym dictionary from a search profile.
-   **[Delete a synonym dictionary](../task/delete-synonym-dict-ais.md)**  
Remove a synonym dictionary that isn't linked from any search profile.

**Parent Topic:**[Search profiles in AI Search](defining-search-profiles-ais.md)

