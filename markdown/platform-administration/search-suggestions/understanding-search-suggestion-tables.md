---
title: Search Suggestions tables
description: Search Suggestions uses tables to generate and track relevant search suggestions. You can review data from these tables to gain insight into search suggestions offered in your system.
locale: en-US
release: zurich
product: Search Suggestions
classification: search-suggestions
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Installed with Search Suggestions, Search Suggestions reference, Search Suggestions, Search administration, Configure core features, Administer]
---

# Search Suggestions tables

Search Suggestions uses tables to generate and track relevant search suggestions. You can review data from these tables to gain insight into search suggestions offered in your system.

**Note:** Because the Search Suggestions tables are system tables, they are excluded from the Reporting module by default. To learn about enabling reporting on system tables, see [Reporting on system tables](https://www.servicenow.com/docs/access?context=c_ReportOnSystemTables&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US).

## Search Event table

The Search Event \[sys\_search\_event\] table stores search strings and their search results.

|Column|Description|
|------|-----------|
|Search query|Search string that the user entered.|
|Has results|Boolean value that specifies whether the search did \(true\) or didn't \(false\) return results. For all false values, consider adding information so that the same search would return suggestions in the future.|
|Click rank|Click rank shows which search result you selected. If you click the first result in the list of search results, the click rank value is 1. If you click the 6th result listed, the click rank value is 6. If you click multiple search results, the click rank is the highest listing value. For example, if you click the first result, return to the search page and click the 6th result, return to the search page and click the 4th result and find an answer, the click rank is 6 \(not 4\). A click rank of 0 means that you didn't select any search result, or that you selected a Genius Result answer card in AI Search. Lower positive click rank values indicate that the top search results are the most relevant, so the goal is to reduce the average value for this field.|
|User|User who performed the search.|
|Application ID|Application where the search feature was used, for example, you did a search in the Service Portal. See **UI source**.|
|Language|Language of the query. Search only returns results that are in the same language as the search query.|
|Refinements|Number of actions that you took to reduce the number of search results. Actions include sorting and filtering. The goal is to reduce this number.|
|UI source|Specific page \(mobile\) or page \(portal\) where the search query came from. See **Application ID**.|
|Session|ID of the session, which specifies when the search happened.|
|AI Search Profile|Name of the search profile used for the search. Only applicable for searches made with the AI Search engine.|
|GR Configurations Executed|Shows the list of Genius Result configurations that the system evaluated for the search. Genius Result configurations in this list may or may not have displayed answer cards for the search. Only applicable for searches made with the AI Search engine.|
|Genius Result Displayed|Shows whether or not any Genius Result answer cards were displayed for the search. Only applicable for searches made with the AI Search engine.|
|GR Configurations with Result Displayed|Shows the list of evaluated Genius Result configurations that displayed answer cards for the search. A Genius Result configuration can appear multiple times in this list if it displayed multiple answer cards for the search. Only applicable for searches made with the AI Search engine.|
|Last Clicked Genius Result Position|Shows which Genius Result answer card you selected an action from. If you select an action from the first displayed Genius Result answer card, the position value is 1. If you select an action from the third answer card, the value is 3. A value of 0 means that you didn't select actions from any Genius Result answer card. Only applicable for searches made with the AI Search engine.|
|Genius Result Events|JSON document showing details of actions you selected from Genius Result answer cards displayed for the search. Only applicable for searches made with the AI Search engine.|

## Search Event per source table

The Search Event per source \[sys\_search\_source\_event\] table stores records correlating search strings with results from a specific table, here called a data source. A search can query multiple tables. The sys\_search\_event table lists one record for the entire search, while the sys\_search\_source\_event table lists one record for each data source \(table\) queried.

|Column|Description|
|------|-----------|
|Search query|Search string that you entered.|
|Source|System ID of the data source. For example, the system ID of the Knowledge Base might be c45067sample3c82eef3e. Suggestions from one source are used as suggestions for that source only. For example, a suggestion derived from the Service Portal wouldn't be used as a suggestion in Now Mobile.|
|Has results|Boolean value that specifies whether the source did \(true\) or didn't \(false\) supply search results. For all false values, consider adding information so that the same search query would return suggestions in the future.|
|Created|Time stamp of the search query.|

## Search Suggestion table

The Search Suggestion \[sys\_search\_suggestion\] table stores auto-complete suggestions and search suggestions. A scheduled job uses the sys\_search\_event table to build the content of the suggestion table. This job segregates generated suggestions by source. Suggestions generated from searches on the Service Portal, for example, are only returned for other Service Portal searches. These suggestions aren't returned for Now Mobile queries.

|Column|Description|
|------|-----------|
|Application ID|Application where the search feature was used, for example, you did a search in the Service Portal.|
|User group|Specifies whether an internal or external user generated the search query. Suggestions for internal users aren't shared with external users and vice versa.|
|Language|Language of the query. Search only returns suggestions that are in the same language as the search query.|
|Score|Suggestion rank. The higher the score, the more relevant the suggestion. Once all suggestions are returned for a search query, the suggestions are sorted by **Score**, the highest listed first. Scores reflect how often you selected a suggestion. A popular suggestion implies that it answers the query.|
|Source|System ID of the data source. For example, the system ID of the Knowledge Base might be c45067sample3c82eef3e. Suggestions from one source are used as suggestions for that source only. For example, a suggestion derived from the Service Portal wouldn't be used as a suggestion in Now Mobile.|

