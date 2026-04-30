---
title: Configure "Did you mean?" suggestions
description: The Knowledge Base and global text searches can provide "Did you mean?" suggestions. Suggestions appear if a search doesn't return any results and an alternate spelling or similar recent search does. This feature is disabled by default.
locale: en-US
release: xanadu
product: Search Administration
classification: search-administration
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Global text search suggestions, Global search finds records from multiple tables, Zing text indexing and search engine, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure "Did you mean?" suggestions

The Knowledge Base and global text searches can provide "Did you mean?" suggestions. Suggestions appear if a search doesn't return any results and an alternate spelling or similar recent search does. This feature is disabled by default.

## Before you begin

Role required: admin

## About this task

Set system properties to enable "Did you mean?" suggestions in the Knowledge Base and legacy global search tools.

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **Text Search**.

2.  Select any of the following check boxes:

    -   **Suggest alternate search spellings for knowledge or global search** \(the **glide.ts.dym.enable\_spell\_correct** property\).
    -   **Suggest related searches for knowledge or global search** \(the **glide.ts.dym.enable\_chain\_suggest** property\); uses search chains, which generate suggestions by tracking occurrences of similar searches, in order, over time.
    **Note:** The global search references in these check boxes only apply to the legacy global search functionality. They don't apply to the global search functionality introduced in the New York release, because the "Did you mean?" functionality isn't available.

3.  Select **Save**.


**Parent Topic:**[Global text search suggestions](../reference/r_GlobalTextSearchSuggestions.md)

**Related topics**  


[Update a type-ahead suggestion](t_UpdateATypeAheadSuggestion.md)

