---
title: Zing filters search results with access controls
description: Zing filters search results to only display records the user can access.
locale: en-US
release: xanadu
product: Search Administration
classification: search-administration
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Zing text indexing and search engine, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Zing filters search results with access controls

Zing filters search results to only display records the user can access.

For example, suppose you index the System Property \[sys\_properties\] table. When the ITIL user searches for a term in the System Property table, Zing returns no search results because the ITIL user doesn't meet the ACL rule requirements.

![Empty search results page for ITIL user search in System Property table.](../image/ITILUserSearch.png "ITIL User Search")

When a system administrator searches for the same property, Zing returns search results from the System Property table because the administrator meets the ACL rule requirements.

![Search results for system administrator search in System Property table.](../image/SystemAdministratorSearch.png "System Administrator Search")

**Parent Topic:**[Zing text indexing and search engine](c_ZingTextSearch.md)

**Related topics**  


[Features of Zing text indexing and search engine](../reference/features-zing.md)

[Available search options](c_IntroductionToSearching.md)

[Global search finds records from multiple tables](c_GlobalTextSearch.md)

[Zing generates search results in four phases](c_SearchProcess.md)

[Zing computes document scores using three components](c_DocumentScoring.md)

[Zing indexes words](zing-indexes-words.md)

[Zing can include attachments in search results](c_SearchingForAttachments.md)

[Zing removes stop words from queries](stop-words-removed-from-queries.md)

[Zing matches derived words with stemming](stemming-matches-derived-words.md)

[Zing can expand search results with synonyms](search-synonyms-expand-results.md)

[Zing displays search suggestions as users enter search terms](search-suggestions-zing.md)

[Installed with Zing](../reference/installed-with-zing.md)

