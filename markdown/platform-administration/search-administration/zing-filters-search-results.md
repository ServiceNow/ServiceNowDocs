---
title: Zing filters search results with access controls
description: Zing filters search results to only display records the user can access.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/search-administration/zing-filters-search-results.html
release: australia
product: Search Administration
classification: search-administration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Zing text indexing and search engine, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Zing filters search results with access controls

Zing filters search results to only display records the user can access.

For example, suppose you index the System Property \[sys\_properties\] table. When the ITIL user searches for a term in the System Property table, Zing returns no search results because the ITIL user doesn't meet the ACL rule requirements.

\[Omitted image "ITILUserSearch.png"\] Alt text: Empty search results page for ITIL user search in System Property table.

When a system administrator searches for the same property, Zing returns search results from the System Property table because the administrator meets the ACL rule requirements.

\[Omitted image "SystemAdministratorSearch.png"\] Alt text: Search results for system administrator search in System Property table.

**Parent Topic:**[Zing text indexing and search engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/c_ZingTextSearch.md)

**Related topics**  


[Features of Zing text indexing and search engine]()

[Available search options]()

[Global search finds records from multiple tables]()

[Zing generates search results in four phases]()

[Zing computes document scores using three components]()

[Zing indexes words]()

[Zing can include attachments in search results]()

[Zing removes stop words from queries]()

[Zing matches derived words with stemming]()

[Zing can expand search results with synonyms]()

[Zing displays search suggestions as users enter search terms]()

[Installed with Zing]()

