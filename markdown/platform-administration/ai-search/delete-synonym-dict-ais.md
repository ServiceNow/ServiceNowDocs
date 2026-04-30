---
title: Delete a synonym dictionary
description: Remove a synonym dictionary that isn't linked from any search profile.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Synonyms, Search profiles, Configure, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Delete a synonym dictionary

Remove a synonym dictionary that isn't linked from any search profile.

## Before you begin

Role required: ais\_admin

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **Search Query Settings** &gt; **Dictionaries**.

    The AI Search Dictionaries list appears with a **\[Type\] \[!=\] \[Spell Check\]** filter condition applied and records grouped by dictionary type.

2.  Expand the Synonym record group if necessary and open the synonym dictionary that you want to delete.

3.  Select **Delete**.

    **Note:** If the synonym dictionary is still linked to any search profiles, deletion fails and an error message lists the linked profiles. Unlink the dictionary from these search profiles, then repeat the preceding steps. For details on unlinking a synonym dictionary from a search profile, see [Unlink a synonym dictionary from a search profile](unlink-synonym-dict-ais.md).


## Result

The selected synonym dictionary disappears from the AI Search Dictionaries list.

**Parent Topic:**[Synonyms](../concept/synonyms-ais.md)

