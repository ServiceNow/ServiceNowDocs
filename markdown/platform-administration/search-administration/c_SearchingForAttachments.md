---
title: Zing can include attachments in search results
description: Search content from attachments on indexed tables. Display attachments for search results from the Knowledge \[kb\_knowledge\] table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/search-administration/c\_SearchingForAttachments.html
release: australia
product: Search Administration
classification: search-administration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Zing text indexing and search engine, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Zing can include attachments in search results

Search content from attachments on indexed tables. Display attachments for search results from the Knowledge \[kb\_knowledge\] table.

\[Omitted image "Km\_search\_filter\_H.png"\] Alt text: Sample Knowledge search including attachments.

By default, search only matches content from attachments on Knowledge \[kb\_knowledge\] records. Administrators can [enable search for attachments on other tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_DisablingAttachmentsOnATable.md), but doing so causes the system to re-index the selected table, its parent table, and any children of the parent table.

**Warning:** For large tables, such as the Task table, re-indexing can take several hours and slows down the system until complete. Re-indexing is best performed during non-peak times.

The search results page only displays attachments for search results from the Knowledge \[kb\_knowledge\] table, even if other tables have attachment search enabled.

\[Omitted image "global-search-result-attachments.png"\] Alt text: Global search results page displaying attachments for Knowledge search results but not for search results from other tables.

Zing supports indexing and searching these attachment file types.

-   .doc
-   .docx
-   .dot
-   .dotx
-   .htm
-   .html
-   .ini
-   .pdf
-   .pot
-   .potx
-   .ppt
-   .pptx
-   .reg
-   .txt
-   .xls
-   .xlsx
-   .xlt
-   .xltx

-   **[Index attachments on a table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_DisablingAttachmentsOnATable.md)**  
You can enable attachment indexing for a table so text searches can return matches from the record and its file attachments.

**Parent Topic:**[Zing text indexing and search engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/c_ZingTextSearch.md)

**Related topics**  


[Features of Zing text indexing and search engine]()

[Available search options]()

[Global search finds records from multiple tables]()

[Zing generates search results in four phases]()

[Zing filters search results with access controls]()

[Zing computes document scores using three components]()

[Zing indexes words]()

[Zing removes stop words from queries]()

[Zing matches derived words with stemming]()

[Zing can expand search results with synonyms]()

[Zing displays search suggestions as users enter search terms]()

[Installed with Zing]()

[Index attachments on a table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_DisablingAttachmentsOnATable.md)

