---
title: Typo handling
description: AI Search replaces misspelled search query terms with auto-correction terms derived from indexed content. Configure typo handling dictionary settings to control derivation of auto-correction terms.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Search profiles, Configuring AI Search, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Typo handling

AI Search replaces misspelled search query terms with auto-correction terms derived from indexed content. Configure typo handling dictionary settings to control derivation of auto-correction terms.

To define auto-correction terms for a search profile, modify settings in the profile's linked typo handling dictionary. The typo handling dictionary derives a list of auto-correction terms from indexed content found in search sources linked to its search profile. Update the typo handling dictionary to save its settings. Publish the linked search profile to make auto-correction terms available for searches that use the profile.

AI Search automatically creates a typo handling dictionary for a search profile when you link search sources to that profile. You can't delete a typo handling dictionary, unlink it from its search profile, or link it to any other search profile.

To disable typo handling auto-correction for a search application, deselect the **Enable Typo Handling** option in the search application configuration. For more details on search application configuration settings, see [Create a search application configuration for AI Search](../task/create-search-app-config-ais.md).

## Conditions for auto-correction term eligibility

When deriving its list of auto-correction terms, the typo handling dictionary only considers indexed terms that satisfy the following conditions:

-   The term includes at least 3 characters and no more than 255 characters.
-   The term appears at least once in indexed records from the search profile's linked search sources.

## Auto-correction of search query terms

When a search query includes a term not present in the typo handling dictionary, AI Search looks for terms in the dictionary with similar spelling. If it finds a good match, it automatically replaces the original search query term with the dictionary term.

For example, a search for `emial`, which isn't present on any indexed record, might auto-correct to the similarly spelled term `email` which exists on multiple indexed records and thus appears in the typo handling dictionary.

A notification message displays the auto-corrected term. Users can select the link in this message to repeat their search with the original query term.

![Sample auto-correction message showing replacement of search query term emial with email.](../image/auto-correction-message.png)

## Terms excluded from auto-correction

Auto-correction ignores search query terms that satisfy any of the following conditions:

<table id="table_hwv_325_vnb"><thead><tr><th>

Condition

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Search query term includes only 1 or 2 characters

</td><td>

Auto-correction ignores search query terms below 3 characters in length. For example, AI Search doesn't auto-correct the search query term `gi`.

</td></tr><tr><td>

Search query term includes only uppercase letters

</td><td>

To enable search for abbreviations, auto-correction ignores search query terms that contain only uppercase letters. For example, AI Search doesn't auto-correct the search query term `PINN`, even if it auto-corrects the lowercase form `pinn` to `pin`.

</td></tr><tr><td>

Search query term includes one or more numeric digits

</td><td>

To enable search for numbers and alphanumeric identifiers, auto-correction ignores search query terms that include numeric digits. For example, AI Search doesn't auto-correct the search query term `402K`.

</td></tr><tr><td>

Search query term excluded from typo handling dictionary

</td><td>

Auto-correction ignores search query terms excluded from the typo handling dictionary. For instructions on excluding terms from a typo handling dictionary, see [Exclude a term from a typo handling dictionary](../task/exclude-typo-handling-terms-ais.md).

</td></tr></tbody>
</table>## Automatic refresh of auto-correction term lists

Each typo handling dictionary automatically refreshes its list of auto-correction terms after a set interval. The refresh operation has the same effect as republishing the dictionary's linked search profile.

By default, typo handling dictionaries refresh every 24 hours. If you want the term list refreshed less frequently, you can increase this interval in the dictionary settings.

## Language dependence

Typo handling is language-dependent. AI Search derives a separate list of auto-correction terms for each supported language found in the search sources' indexed content.

AI Search supports derivation of auto-correction terms for Brazilian Portuguese, Dutch, English, Finnish, French - Canada, French, German, Italian, Norwegian \(Bokmål\), Polish, Portuguese, Spanish, and Swedish. Typo handling auto-correction term derivation isn't supported for Japanese, Korean, Simplified Chinese, or Traditional Chinese.

## Interaction with other search features

The following table describes interactions between typo handling and other search features.

<table id="table_vdr_yd5_fnb"><thead><tr><th>

Feature

</th><th>

Interaction with typo handling

</th></tr></thead><tbody><tr><td>

[Genius Results](genius-results-ais.md)

</td><td>

Auto-corrected search query terms can't trigger Genius Result configurations with Term trigger conditions. When computing Q&amp;A Genius Results for a search query, AI Search corrects terms in the query.

</td></tr><tr><td>

[Lemma and Unicode normalization](lemma-unicode-normalization-ais.md)

</td><td>

AI Search performs lemma and Unicode normalization on auto-corrected search query terms.

</td></tr><tr><td>

[Result improvement rules](result-improvement-rules-ais.md)

</td><td>

An auto-corrected search query term can trigger a result improvement rule if it matches the rule's Query trigger.

</td></tr><tr><td>

[Stop words](stop-words-ais.md)

</td><td>

If a misspelled search query term is defined as a stop word, AI Search auto-corrects that term normally instead of removing it.

 AI Search ignores terms defined as stop words when determining an auto-correction for a misspelled search query term. For example, if you define `email` as a stop word, AI Search doesn't offer `email` as an auto-correction when you search for `emial`.

</td></tr><tr><td>

[Synonyms](synonyms-ais.md)

</td><td>

If a misspelled search query term is defined as a synonym, AI Search expands that synonym without auto-correcting it.

</td></tr></tbody>
</table>-   **[Modify settings for a typo handling dictionary](../task/config-typo-handling-dict-ais.md)**  
Modify typo handling dictionary settings for a search profile.
-   **[Exclude a term from a typo handling dictionary](../task/exclude-typo-handling-terms-ais.md)**  
Prevent AI Search from auto-correcting a term in user search queries by excluding the term from a typo handling dictionary.

**Parent Topic:**[Search profiles in AI Search](defining-search-profiles-ais.md)

