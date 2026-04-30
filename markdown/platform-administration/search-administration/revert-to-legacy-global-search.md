---
title: Revert to the legacy global search UI
description: Disable the dynamic global search UI to preserve customizations you made to the legacy global search UI.The global text search results page allows users to set several user preferences for global text search.
locale: en-US
release: yokohama
product: Search Administration
classification: search-administration
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Set global text search properties, Global search finds records from multiple tables, Zing text indexing and search engine, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Revert to the legacy global search UI

Disable the dynamic global search UI to preserve customizations you made to the legacy global search UI.

## Before you begin

You must have Next Experience disabled on your instance. The legacy global search UI is only available in Core UI.

Role required: admin

## Procedure

1.  Navigate to the System Property \[sys\_properties\] table's list view.

    1.  Select **All**.

    2.  In the **Filter** field, enter `sys_properties.list`.

    3.  Press Enter.

2.  Select **New**.

3.  Enter these field values.

    |Field|Value|
    |-----|-----|
    |Name|glide.ui.use\_legacy\_global\_search|
    |Type|true \| false|
    |Value|true|

4.  Select **Submit**.


## Result

The system displays the global search UI and uses the legacy display logic.

**Parent Topic:**[Set global text search properties](set-global-text-search-properties.md)

**Related topics**  


[Configure parallel processing of search groups](t_ConfigureParallelProcessing.md)

## Legacy global search user preferences

The global text search results page allows users to set several user preferences for global text search.

The following search preferences are available from the **Search tips and preferences** link.

![Search preferences.](../image/SearchPreferences.png "Search preferences")

<table id="table_bsp_2xx_pp"><thead><tr><th>

User preference

</th><th>

Description

</th></tr></thead><tbody><tr><td>

-   **Label**

Use remembered expand / collapse preferences

-   **Preference**

ts.remember.expanded


</td><td>

Specifies whether you want the collapse state of any search groups/tables remembered for your next search. If selected and you collapse the search results for the People &amp; Places search group for example, that group will be collapsed on your next search. If cleared, all groups and tables are expanded for every search.

</td></tr><tr><td>

-   **Label**

Show list of tables with no search matches

-   **Preference**

ts.show\_negative\_result\_info


</td><td>

Specifies whether or not you want to see a summary of tables that had no search matches. For example: No matches for Requests, Catalog Tasks, Tickets.

</td></tr><tr><td>

-   **Label**

Show selectable search groups

-   **Preference**

ts.show\_search\_groups


</td><td>

Shows or hides the search group check box row.

</td></tr><tr><td>

-   **Label**

Show groups with no search matches

-   **Preference**

ts.show\_empty\_groups


</td><td>

Shows or hides a search group if it returns no matches. If selected, the search results display a placeholder row stating there were no matches for that group.

</td></tr><tr><td>

-   **Label**

Return task record if searching for exact number

-   **Preference**

ts.match


</td><td>

Shows or hides the full search results page if the search term matches a task record number. When selected, an exact match to a record number causes the system to hide the full search results and instead display the record with an exact match message. Exact search matches ignore most additional search conditions normally applied to the record such as the currently selected search groups or the knowledge article published state. For example, an exact search match for a knowledge article returns the article in any state as long as the current user has read access to it.

**Note:** The system filters exact search results to display only knowledge records that are in the same language as the preferred language setting.

 ![Sample search query for the knowledge article KB0000023.](../image/exact-search-filters.png "Sample exact match search query")

In this sample search, the **Knowledge &amp; Catalog** search filter is cleared, which would normally prevent returning any knowledge articles.

 ![Sample search results for the knowledge article record KB0000023.](../image/exact-search-match.png "Sample exact match search results")

In this sample exact match, the system displays the matching article and an information message in the form header reading `Exact search match. Click here to see full search results.`

</td></tr></tbody>
</table>**Related topics**  


[User preferences](https://www.servicenow.com/docs/access?context=c_UserPreferences&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US)

