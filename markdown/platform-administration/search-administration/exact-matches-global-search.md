---
title: Global search displays exact matching records
description: When your search exactly matches the Number field value for a record, global search takes you directly to that record, bypassing the search results page.When your search in Next Experience UI exactly matches a searchable record, the Unified Navigation search field displays a preview of that record. Selecting the preview takes you directly to that record and bypasses the search results page.When your search in Core UI exactly matches a searchable record, global search takes you directly to that record, bypassing the search results page.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/search-administration/exact-matches-global-search.html
release: australia
product: Search Administration
classification: search-administration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Global search finds records from multiple tables, Zing text indexing and search engine, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Global search displays exact matching records

When your search exactly matches the **Number** field value for a record, global search takes you directly to that record, bypassing the search results page.

As an example, if you search for `INC0038278`, global search shows Incident record INC0038278 in form view instead of showing the search results page.

**Note:** Exact match respects security settings. If you don't have permission to view the record that matches your search, global search won't show you that record.

If more than one record has a **Number** field value that exactly matches your search, global search displays the first exact match. An informational message reports the total number of exact matches and provides links to the other exact matches.

## Exact match configuration settings

Exact match only returns matches for Number values that contain prefixes defined in the Numbers \[sys\_number\] table. To view prefixes and their matching tables, navigate to **All** &gt; **System Definition** &gt; **Number Maintenance**.

Search behavior for exact match is controlled by the **com.snc.agent\_workspace.global\_search.typeahead.exact\_match\_request\_criterion\_regex** system property. This property's value is a Java regular expression pattern. Only search queries that match the regular expression pattern are evaluated as possible exact record matches. For details on Java regular expression pattern syntax, see [the Javadoc for the java.regex.util.Pattern class](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html).

**Parent Topic:**[Global search finds records from multiple tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/c_GlobalTextSearch.md)

**Related topics**  


[Global search displays a page of matching results]()

[Text search views control format of global search results for tables]()

[Search settings filter and group global search results by table]()

[Global search displays your most recent search queries and results in Next Experience UI]()

[Set global text search properties]()

[Set the preview limit for global or workspace search in Next Experience UI]()

[Hide per-table search result counts in Next Experience UI]()

[Add a workspace application to the Unified Navigation search context menu]()

[Global text search suggestions]()

## Exact search matches in Next Experience UI

When your search in Next Experience UI exactly matches a searchable record, the Unified Navigation search field displays a preview of that record. Selecting the preview takes you directly to that record and bypasses the search results page.

\[Omitted image "exact-match-result-polaris-ui.png"\] Alt text: Unified Navigation showing exact match preview for Incident record.

The preview of the matching record appears below the Unified Navigation search field with an **Exact Match** tag. Select this tag or press Enter to navigate directly to the record.

To see the full search results page for your search, select **View results**. For details on the elements that make up the search results page, see [Search results page in Next Experience UI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/global-search-polaris-ui.md).

**Note:** You may need to wait a few seconds after entering your record number into the search field for the system to process your search request and display the preview. Once the preview appears, you can press Enter to go directly to the matched record. If you press Enter before the preview appears, the system shows you the full search results page for your search instead.

## Exact search matches in Core UI

When your search in Core UI exactly matches a searchable record, global search takes you directly to that record, bypassing the search results page.

\[Omitted image "exact-match-result-ui16.png"\] Alt text: Incident record with exact search match informational message.

The system displays the matching record with an informational message indicating that your search produced an exact search match.

To see the full search results page for your search, select the link in the informational message. For details on the elements that make up the search results page, see [Search results page in Core UI and UI15](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/global-search-polaris-ui.md).

