---
title: Dictionary and AI Search Dictionary forms
description: The Dictionary and AI Search Dictionary forms contain information about your AI Search typo handling, stop word, and synonym dictionaries. Use these forms when creating or modifying a typo handling, stop word, or synonym dictionary for use with AI Search.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Reference, AI Search, Search administration, Configure core features, Administer]
---

# Dictionary and AI Search Dictionary forms

The Dictionary and AI Search Dictionary forms contain information about your AI Search typo handling, stop word, and synonym dictionaries. Use these forms when creating or modifying a typo handling, stop word, or synonym dictionary for use with AI Search.

For details on creating and modifying dictionaries, see [Modify settings for a typo handling dictionary](../task/config-typo-handling-dict-ais.md), [Create a stop word dictionary linked to a search profile](../task/create-stop-word-dict-ais.md), and [Create a synonym dictionary linked to a search profile](../task/create-synonym-dict-ais.md).

<table id="table_nss_bh5_kmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

Unique label for the dictionary.

</td></tr><tr><td>

Dictionary name

</td><td>

Name for the dictionary. This field is automatically set based on the **Label** field value.

</td></tr><tr><td>

Language

</td><td>

Language for all terms defined in the dictionary. This field only displays when editing a stop word or synonym dictionary. AI Search automatically sets the language for typo handling dictionaries.**Note:** You can only link one stop word dictionary with a given language to a search profile.

</td></tr><tr><td>

Type

</td><td>

Dictionary type. This field is automatically set to **Spell Check**, **Stop Word**, or **Synonym**.

</td></tr><tr><td>

State

</td><td>

Current state of the dictionary.-   **New**: The dictionary has never been published.
-   **Draft**: The dictionary is saved with unpublished changes.
-   **Published**: The dictionary is saved with all changes published.

</td></tr><tr><td>

Case sensitive

</td><td>

Option to enable case sensitivity for all terms in the dictionary. For more details on case sensitivity, see [Typo handling](../concept/typo-handling-ais.md), [Stop words](../concept/stop-words-ais.md), or [Synonyms](../concept/synonyms-ais.md).

</td></tr><tr><td>

Punctuation sensitive

</td><td>

Option to enable punctuation sensitivity for all terms in the dictionary. For more details on punctuation sensitivity, see [Typo handling](../concept/typo-handling-ais.md), [Stop words](../concept/stop-words-ais.md), or [Synonyms](../concept/synonyms-ais.md).

</td></tr><tr><td>

Derived

</td><td>

Option to derive dictionary entries from indexed content. This field and the **Derive Settings** section only display when editing a typo handling dictionary.

</td></tr><tr><td class="sub-head" colspan="2">

Derive Settings

</td></tr><tr><td>

Indexed sources

</td><td>

List of indexed sources. The dictionary derives auto-correction terms from content indexed for these sources. This field only displays when editing a typo handling dictionary. For more information on indexed sources, see [Indexed sources in AI Search](../concept/indexed-sources-ais.md).

</td></tr><tr><td>

Auto refresh

</td><td>

Interval, in hours, after which derived typo handling entries automatically refresh. The minimum value is 24 hours. This field only displays when editing a typo handling dictionary.

</td></tr><tr><td>

Blocked Fields

</td><td>

Comma-separated list of fields. The dictionary excludes terms found in these fields when deriving typo handling auto-correction terms from indexed source records. This field only displays when editing a typo handling dictionary. You can specify fields using the following formats:

-   **\*** \(asterisk\): Exclude terms found in all fields. This value disables derivation of typo-handling auto-corrections for the dictionary.
-   **fieldname**: Exclude terms found in the specified AI Search index field, such as **title** or **text**. For details on AI Search index fields, see [AI Search index fields](index-fields-list-ais.md).
-   **tablename.fieldname**: Exclude terms found in the specified field on the specified ServiceNow AI Platform® table.
-   **tablename.\***: Exclude terms found in all fields in the specified ServiceNow AI Platform table.

</td></tr></tbody>
</table>**Parent Topic:**[AI Search reference](../concept/reference-ais.md)

