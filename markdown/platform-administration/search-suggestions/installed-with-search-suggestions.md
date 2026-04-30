---
title: Installed with Search Suggestions
description: Several types of components are installed with activation of the Search Suggestions plugin, including tables, user roles, and scheduled jobs.
locale: en-US
release: xanadu
product: Search Suggestions
classification: search-suggestions
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Search Suggestions reference, Search Suggestions, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Installed with Search Suggestions

Several types of components are installed with activation of the Search Suggestions plugin, including tables, user roles, and scheduled jobs.

## Roles installed

<table id="table_rr5_zj2_dzb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Search Suggestions blocked searcher \[cannot\_read\_suggestions\]

</td><td>

Doesn't see search or auto-complete suggestions displayed when searching.

</td><td>

None

</td></tr><tr><td>

Search Suggestions exempt searcher \[suggestion\_exempt\]

</td><td>

Submits searches that the system ignores when generating search or auto-complete suggestions.

</td><td>

None

</td></tr></tbody>
</table>For more details on restricting generation of search suggestions, see [Prevent the creation of suggestions in special cases](../task/preventing-suggestions.md).

## Scheduled jobs installed

|Scheduled job|Description|
|-------------|-----------|
|Build Search Suggestions|Converts searches stored in the Search Event \[sys\_search\_event\] table into auto-complete suggestions and search suggestions stored in the Search Suggestion \[sys\_search\_suggestion\] table.|
|Prune Search Suggestions|Removes the lowest-rated auto-complete suggestions and search suggestions from the Search Suggestion \[sys\_search\_suggestion\] table to keep the maximum number of suggestions at 500,000.|

## Tables installed

<table id="table_vr5_zj2_dzb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Search Event \[sys\_search\_event\]

</td><td>

Search strings and details about their associated results, including the search user, application, UI source, session, and language, and any user-specified click rank and refinements.

</td></tr><tr><td>

Search Event per source table \[sys\_search\_source\_event\]

</td><td>

Correlations between search strings with search results from a specific table \(data source\). A search that queries multiple tables produces multiple Search Event per source records.

</td></tr><tr><td>

Search Suggestion \[sys\_search\_suggestion\]

</td><td>

auto-complete suggestions and search suggestions generated from user searches by the Build Search Suggestions scheduled job. The Prune Search Suggestions scheduled job removes the lowest-rated auto-complete suggestions and search suggestions from this table to keep its maximum size at 500,000 suggestion records.

</td></tr></tbody>
</table>To learn about individual columns on these tables, see [Search Suggestions tables](understanding-search-suggestion-tables.md).

