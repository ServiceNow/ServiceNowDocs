---
title: Dictionary Term form
description: The Dictionary Term form enables you to create a typo handling entry, a stop word, or a synonym in a dictionary linked to an AI Search search profile.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/ai-search/dictionary-term-form-ais.html
release: zurich
product: AI Search
classification: ai-search
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, AI Search, Search administration, Configure core features, Administer]
---

# Dictionary Term form

The Dictionary Term form enables you to create a typo handling entry, a stop word, or a synonym in a dictionary linked to an AI Search search profile.

For more details on creating or modifying dictionary terms, see [Exclude a term from a typo handling dictionary](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/exclude-typo-handling-terms-ais.md), [Create stop words](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/create-stop-word-ais.md), and [Create synonyms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/create-synonym-ais.md).

<table id="ais-dictionary-term-stop-word-table"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Dictionary

</td><td>

Name of the dictionary that includes the typo handling, stop word, or synonym term. This field is automatically set based on the dictionary that you selected.

</td></tr><tr><td>

Term

</td><td>

The term or phrase to include in the typo handling, stop word, or synonym dictionary.

</td></tr><tr><td>

Payload

</td><td>

List of equivalent terms or phrases in JSON array format. For example, `["wireless network", "WLANS"]`. This field only displays when editing a synonym term.

</td></tr><tr><td>

State

</td><td>

Current state for the dictionary term.-   **New**: The dictionary term has never been published.
-   **Draft**: The dictionary term is saved with unpublished changes.
-   **Published**: The dictionary term is saved with all changes published.

 This field only displays when editing a synonym term.

</td></tr><tr><td>

Active

</td><td>

Option to activate the term for use in the dictionary. To deactivate the term, clear the **Active** option.

</td></tr><tr><td>

Marked for Deletion

</td><td>

Option indicating that AI Search will delete the term the next time you publish the search profile linked to the selected dictionary. This field only displays when editing a typo handling or stop word term, and is automatically set.

</td></tr><tr><td>

Application

</td><td>

Application scope for the dictionary term. This field only displays when editing a typo handling or stop word term, and is automatically set.

</td></tr></tbody>
</table>**Parent Topic:**[AI Search reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/reference-ais.md)

