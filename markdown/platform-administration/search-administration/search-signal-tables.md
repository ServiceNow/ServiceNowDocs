---
title: Search signal tables
description: Search uses tables to store details from user searches, search refinements, and interactions with search results. These details are called search signals. Data from the search signal tables helps improve the relevancy of search results in your system.
locale: en-US
release: australia
product: Search Administration
classification: search-administration
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Search signals, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Search signal tables

Search uses tables to store details from user searches, search refinements, and interactions with search results. These details are called search signals. Data from the search signal tables helps improve the relevancy of search results in your system.

Search signals refer to user, query, and similar data stored in columns on search suggestion tables. For a guide to search suggestion tables and their columns, see [Search Suggestions tables](understanding-search-suggestion-tables.md).

**Note:** Because the search signal tables are system tables, they are excluded from the Reporting module by default. To learn about enabling reporting on system tables, see [Reporting on system tables](https://www.servicenow.com/docs/access?context=c_ReportOnSystemTables&version=australia&pubname=australia-now-intelligence&ft:locale=en-US).

## Search Signal Event table

The Search Signal Event \[sys\_search\_signal\_event\] table stores signal data produced when users submit a search.

<table id="table_yn5_lnw_3nb"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Search event

</td><td>

Reference to the record for the search event on the Search Event \[sys\_search\_event\] table.

</td></tr><tr><td>

Browser

</td><td>

User browser agent string.

</td></tr><tr><td>

Latitude

</td><td>

Latitude coordinate of the user location in decimal degrees.

</td></tr><tr><td>

Longitude

</td><td>

Longitude coordinate of the user location in decimal degrees.

</td></tr><tr><td>

Matched Query Intents

</td><td>

List of query intents matched in the user search query.

</td></tr><tr><td>

First page results

</td><td>

JSON array of objects in which each node represents a single result returned in the first page of results for the search. The result order is preserved. Each object includes the unique record identifier \(sys\_id\) of a result and the table where the result is located.**Note:** The first page results aren't updated when you refine a search.

</td></tr><tr><td>

Search Response Time\(ms\)

</td><td>

Time taken by the search, in milliseconds.

</td></tr><tr><td>

User Query Language

</td><td>

Language of the user search query.

</td></tr></tbody>
</table>## Search Signal Result Event table

The Search Signal Result Event \[sys\_search\_signal\_result\_event\] table stores signal data for search results that users select.

|Column|Description|
|------|-----------|
|Search query|Search query that led to the search result selection.|
|User|User that selected the search result.|
|Result DocID|Source table and record names for the selected search result.|
|Description|Short description for the selected search result.|
|Source Table|Source table for the selected search result.|
|AIS DocID|Source table name and record sys\_id for the selected search result.|
|Result Type|Type of search result selected. For example, **REGULAR** for a regular search result or **GENIUS** for a Genius Result answer card.|
|Search Signal Event|Reference to the record for the search on the Search Signal Event \[sys\_search\_signal\_event\] table.|
|Number|Record number for the selected search result.|
|Domain|Domain to which the selected search result belongs.|
|Use for Suggestions|Option indicating whether AI Search uses this result selection when computing auto-complete suggestions. For more details, see [Auto-complete suggestions in AI Search applications](../../ai-search/concept/auto-complete-ais.md#)|
|Source URL|URL for the selected search result.|
|Action Data|JSON array of objects representing the search result selection action.|

## Search Signal Result Event Action table

The Search Signal Result Event Action \[sys\_search\_signal\_result\_event\_action\] table stores signal data for user interactions with search results.

|Column|Description|
|------|-----------|
|Signal Type|The type of user interaction signal recorded for the search result. For example, **CLICK** indicates that the user selected a search result.|
|Signal Value|The value for the user interaction signal. For example, when the signal type is **CLICK**, the signal value is the numeric index for the search result that the user selected.|
|Search Signal Result Event|Reference to the record for the search result on the Search Signal Result Event \[sys\_search\_signal\_result\_event\] table.|

## Search Autocomplete Query Event table

The Search Autocomplete Query Event \[sys\_search\_autocomplete\_query\_event\] table stores signal data for auto-complete suggestions that users select from the search input field.

|Column|Description|
|------|-----------|
|Selected Query|The auto-complete suggested query that the user selected in the search input field.|
|Click Index|The numeric index of the auto-complete suggestion that the user selected in the search input field.|
|Latitude|Latitude coordinate of the user location in decimal degrees.|
|Longitude|Longitude coordinate of the user location in decimal degrees.|
|Search Profile|Reference to the search profile used for the search query.|

## Genius Result Event Action table

The Genius Result Event Action \[sys\_search\_genius\_result\_event\_action\] table stores signal data for user interactions with Genius Result answer cards.

<table id="table_sxq_nvc_qnb"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Action Id

</td><td>

The identifier for this Genius Result event action signal.

</td></tr><tr><td>

Action Type

</td><td>

The type of action taken from the Genius Result answer card.

</td></tr><tr><td>

Action Value

</td><td>

The value, if any, for the action taken from the Genius Result answer card.

</td></tr><tr><td>

Matched Genius Result Intents

</td><td>

List of NLU model intents matched by the action taken from the Genius Result answer card.**Note:** This field is only populated for Genius Result configurations with NLU triggers.

</td></tr><tr><td>

Card Type

</td><td>

The type of Genius Result answer card that the user interacted with.

</td></tr><tr><td>

Search Signal Result Event

</td><td>

Reference to the record for the Genius Result answer card on the Search Signal Result Event \[sys\_search\_signal\_result\_event\] table.

</td></tr></tbody>
</table>