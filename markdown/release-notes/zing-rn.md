---
title: Zing text indexing and search engine release notes
description: The ServiceNow Zing text indexing and search engine application is a legacy search engine that you can use to search ServiceNow AI Platform record data. See the following sections for release notes by version.The Brazil Early Availability release adds support for column-level query\_range read ACLs on table columns that are indexed for search.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/zing-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [Zing, text indexing, search engine, Zing, text indexing, search]
breadcrumb: [ServiceNow AI Platform administration release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Zing text indexing and search engine release notes

The ServiceNow® Zing text indexing and search engine application is a legacy search engine that you can use to search ServiceNow AI Platform® record data. See the following sections for release notes by version.

## About Zing text indexing and search engine

-   Index and search text and attachments from ServiceNow AI Platform tables.
-   Compute document relevancy scores based on the frequency, sequence, and weight of search terms in the document.
-   Search records from a table list view or search multiple tables using global search.
-   Filter search results to only display records the user can access.

See [Zing text indexing and search engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/c_ZingTextSearch.md) for more information.

## Activation and other requirements

-   **Activation information**

    Zing text indexing and search engine is a ServiceNow AI Platform feature that is active by default.

-   **Browser requirements**

    For optimal performance, use Zing text indexing and search engine in the latest release of Google Chrome or Mozilla Firefox. Zing text indexing and search engine doesn’t support Internet Explorer.


## Accessibility and localization

-   **Localization information**

    Zing text indexing and search engine supports all languages offered by the ServiceNow AI Platform. To improve Japanese-language search results, search administrators can configure the Kuromoji Japanese tokenizer on the text indexes for individual tables.


**Parent Topic:**[ServiceNow AI Platform administration release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/now-platform-admin-rn-landing.md)

## Brazil Early Availability

The Brazil Early Availability release adds support for column-level query\_range read ACLs on table columns that are indexed for search.

### What's new

-   **[Column-level query\_range read ACLs on table columns indexed for search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/verify-user-roles-access-searchable-tables.md)**

    Improve security for search with Zing's support for column-level query\_range read ACLs on table columns that are indexed for search. When searching tables with legacy v3 format text indexes, Zing only displays search results if the current user's role has access to all of the table's indexed columns. For tables with v4 format text indexes, Zing only displays search matches in indexed columns accessible by the user's role. Use the new Text Search Query Range ACL Checker tool to verify that user roles have access to all indexed columns for your searchable tables.


