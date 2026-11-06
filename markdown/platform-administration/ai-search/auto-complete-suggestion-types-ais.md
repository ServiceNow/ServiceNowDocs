---
title: List of auto-complete suggestion types for AI Search applications
description: AI Search provides multiple types of auto-complete suggestions that you can configure for display to users in the search field.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-administration/ai-search/auto-complete-suggestion-types-ais.html
release: australia
product: AI Search
classification: ai-search
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Auto-complete suggestions, Search application configurations, Configure, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# List of auto-complete suggestion types for AI Search applications

AI Search provides multiple types of auto-complete suggestions that you can configure for display to users in the search field.

The following auto-complete suggestion types are available for linking to search application configurations that specify AI Search as their search engine.

**Note:** Not all auto-complete suggestion types are available for the search application configurations included in the base system.

<table id="table_kts_rqn_4tb"><thead><tr><th>

Auto-complete suggestion type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Popular Search Reader Group for &lt;application name&gt;

</td><td>

Displays search query suggestions based on searches submitted by all users of the search application. When you create a search application configuration, this suggestion reader group isn't linked to it by default.

 Default section header: `Popular searches`

 Readers: Popular Query Reader

</td></tr><tr><td>

Recent Search Reader Group for &lt;application name&gt;

</td><td>

Displays search query suggestions based on the user's previous searches. Default section header: `Recent searches`

 Included readers: User History Reader

</td></tr><tr><td>

Search-based Suggested Results Reader Group for &lt;application name&gt;

</td><td>

Displays titles and tables for search result suggestions based on a search for the terms entered in the search field. This search applies search source filters, stop word and synonym dictionaries, and result improvement rules from the search application's linked search profile. AI Search treats the last term in the search field specially, as follows:

-   If the last term in the search field is followed by a space, AI Search treats it as a literal search term. As an example, `act` followed by a space matches results containing the term `act`.
-   If the last term in the search field isn't followed by a space, AI Search treats it as a wildcard search prefix. For example, `act` without following space matches results containing the terms `act`, `action`, `activated`, `actuated`, and so on.

 Selecting a suggested search result opens it as follows:

-   Catalog Item results open in Service Catalog.
-   Knowledge article results open in Knowledge.
-   Other results open in form view.

**Note:** If the suggested search result is an attachment, selecting it opens its parent record in form view.


 Default section header: `Suggested`

 Included readers: Search Based Suggestion Reader

</td></tr><tr><td>

Suggested Query Reader Group for &lt;application name&gt;

</td><td>

Displays a mix of search query suggestions \(based on the user's previous searches\) and search result suggestions \(based on results the user selected for previous searches\). Default section header: none

 Included readers: Popular Query Reader, User History Reader, User Search Term Reader

</td></tr><tr><td>

Suggested Result Reader Group for &lt;application name&gt;

</td><td>

Displays search result suggestions based on results the user selected for previous searches. When you create a search application configuration, this suggestion reader group isn't linked to it by default.

 Default section header: `Suggested results`

 Included readers: Personal Click Reader

</td></tr><tr><td>

User History Reader Group for &lt;application name&gt;

</td><td>

Displays the user's current search query, plus search query and result suggestions from the user's previous search activity that match the current input. When you create a search application configuration, this suggestion reader group isn't linked to it by default.

 Default section header: `Recently viewed`

 Included readers: User History and Click Reader, User Search Term Reader

</td></tr></tbody>
</table>**Note:** A search application configuration can't link to multiple search suggestion types that include the same reader and have the same click-in mode. If you try to link a second suggestion type with the same reader and click-in mode to a search application configuration, the system displays an error message.

**Parent Topic:**[Auto-complete suggestions in AI Search applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/ai-search/auto-complete-ais.md)

