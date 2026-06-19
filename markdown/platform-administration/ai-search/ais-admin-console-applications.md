---
title: AI Search Admin Console Applications page
description: The AI Search admin console Applications page is where you monitor all the applications which use AI Search, as well as create and adjust AI Search configurations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/ai-search/ais-admin-console-applications.html
release: zurich
product: AI Search
classification: ai-search
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 16
keywords: [AI, Search, admin, console, applications, prebuilt]
breadcrumb: [AI Search Admin console reference, AI Search Admin console, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# AI Search Admin Console Applications page

The AI Search admin console Applications page is where you monitor all the applications which use AI Search, as well as create and adjust AI Search configurations.

\[Omitted image "ais-admin-02.png"\] Alt text: AI Search Admin Console Applications page with 5 callouts highlighted. For a text description, see the table that follows.

Each application is represented by a card on the Applications page. Each card shows the AI Search status of the application, its name, and the date when it was last modified or if its configuration isn’t started yet. Selecting a card takes you to the application's Configuration view.

\[Omitted image "ais-admin-02a.png"\] Alt text: Application cards showing AI Search in use, Ready to turn on, andConfiguration needed status messages.

<table id="table_lyh_wwg_rhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

1. Navigation bar

</td><td>

Tabs to navigate between Home, Applications, and Shared Configurations pages.

</td></tr><tr><td>

2. AI Search Applications tabs

</td><td>

Tabs to filter AI Search applications by type:-   All
-   Portals
-   Workspaces
-   Mobile
-   Virtual Agent
-   Other

</td></tr><tr><td>

3. AI Search Applications cards

</td><td>

List of cards for applications with AI Search prebuilt. Select a card to go to the application's AI Search configuration page.

</td></tr><tr><td>

4. Filters

</td><td>

Check boxes for filtering applications:-   Status
    -   AI Search is on
    -   Ready to turn on
    -   Configuration needed
-   Now Assist
    -   Now Assist in use
    -   Now Assist not in use
-   Persona
    -   Requester
    -   Agent

</td></tr><tr><td>

5. FAQ

</td><td>

Frequently asked questions related to AI Search.

</td></tr></tbody>
</table>## Application Configuration view

When you select an application's card in the Applications page, the application's configuration data appears. In the Configuration view, you can turn AI Search on and off for the application, choose and test search profiles and application configurations before publishing, and publish profiles. Select **Search Profile** or **Search Application Configuration** to view profile summaries. You can also select an individual option from the sidebar or its matching card on the main view to display it in detail.

\[Omitted image "ais-admin-02b.png"\] Alt text: AI Search Admin Console Employee Center application configuration summary view. The application's Current Status and Search Profile sections respectively show the AI Search and profile publication status.

**Note:** The Applications view varies if you select a Search Profile with Genius Results activated. For more information, see Genius Results in 

<table id="table_szg_w5q_1cc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Home

</td><td>

Navigation bar button to go to AI Search Admin Console Home page.

</td></tr><tr><td>

Applications

</td><td>

Navigation bar button to go to AI Search Admin Console Applications page.

</td></tr><tr><td>

Shared Configurations

</td><td>

Navigation bar button to go to AI Search Admin Console Shared Configurations page.

</td></tr><tr><td>

Application Configuration

</td><td>

Sidebar tab to view the application's configuration summary.

</td></tr><tr><td>

Search Profile

</td><td>

Sidebar tab to view Search Profile summary info:-   Search Sources
-   Dictionaries
-   Result Improvement Rules
-   Genius Results

</td></tr><tr><td>

Search Sources

</td><td>

Sidebar tab to view the list of Search Sources for this application. Alternatively, select the card with the same name on the summary view.

</td></tr><tr><td>

Dictionaries

</td><td>

Sidebar tab to view the list of Dictionaries for this application. Alternatively, select the card with the same name on the summary view.

</td></tr><tr><td>

Result Improvement Rules

</td><td>

Sidebar tab to view the list of result improvement rules for this application. Alternatively, select the card with the same name on the summary view.

</td></tr><tr><td>

Genius Results

</td><td>

Sidebar tab to view the list of Genius Results for this application. Alternatively, select the card with the same name on the summary view.

</td></tr><tr><td>

Search Application Configuration

</td><td>

Sidebar tab to view Search Application Configuration summary info:-   Auto-complete Suggestions
-   Navigation tabs
-   Sort Options
-   Facet Filters
-   Result-card Interface

</td></tr><tr><td>

Auto-complete Suggestions

</td><td>

Sidebar tab to view the list of Auto-complete Suggestions for this application. Alternatively, select the card with the same name on the summary view.

</td></tr><tr><td>

Navigation tabs

</td><td>

Sidebar tab to view the list of Navigation tabs for this application. Alternatively, select the card with the same name on the summary view.

</td></tr><tr><td>

Sort Options

</td><td>

Sidebar tab to view the list of Sort Options for this application. Alternatively, select the card with the same name on the summary view.

</td></tr><tr><td>

Facet Filters

</td><td>

Sidebar tab to view the list of Facet Filters for this application. Alternatively, select the card with the same name on the summary view.

</td></tr><tr><td>

Result-card Interface

</td><td>

Sidebar tab to view the list of Result-card Interfaces for this application. Alternatively, select the card with the same name on the summary view.

</td></tr><tr><td>

Test Search Profile

</td><td>

Option to test the currently selected Search Profile.

</td></tr><tr><td>

Try in application

</td><td>

Option to test the Search Profile in its application.

</td></tr><tr><td>

Turn off AI Search

</td><td>

Link to the application's Service Portal record. If you deactivate **Enable AI Search** in the application's record and select **Update**, **Turn off AI Search** disappears and **Try in application** deactivates. The AI Search status display also changes and a **Go to turn on** button appears. Select this button to return to the application record and reactivate **Enable AI Search**.

</td></tr><tr><td>

Use different profile

</td><td>

Option to select a different Search Profile.

</td></tr><tr><td>

Publish

</td><td>

Option to publish the current Search Profile being tested or used. If the Search Profile is already published, the **Publish** button deactivates.

</td></tr><tr><td>

Use different configuration

</td><td>

Option to select a different Search Application Configuration.

</td></tr></tbody>
</table>## Search Profile

The Search Profile view is where you review and publish your search profile. You get a summary view from the Search Profile tab, and you select each of the four subsections to review them before publishing. For more information on creating and publishing a search profile, see [Create a search profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/create-search-profile-ais.md) and [Publish an AI Search search profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/publish-search-profile-ais.md).

\[Omitted image "ais-admin-02c.png"\] Alt text: AI Search Admin Console Search Profile summary view.

|Field|Description|
|-----|-----------|
|Rename|Button to rename your search profile.|
|Use a different profile|Button to select a different search profile.|
|Test|Button to test your search profile.|
|Publish profile|Button to publish your search profile.|

You use Search Sources to make your searchable content available in search experiences. For more information, see [Search sources in AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/search-sources-ais.md) and [Create a search source for AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/create-search-source-ais.md).

\[Omitted image "ais-admin-02d.png"\] Alt text: AI Search Admin Console Search Sources view.

|Field|Description|
|-----|-----------|
|Refresh list \[Omitted image "refresh-list-icon.png"\] Alt text: Refresh list icon.|Button to refresh list of search sources.|
|List Actions \[Omitted image "list-actions-icon.png"\] Alt text: List actions icon.|Button to open list actions. Select **Edit columns** to add or remove columns from the table. Select **Reset widths** if you have adjusted any column widths.|
|Show/Hide Filter panel \[Omitted image "filter-panel-icon.png"\] Alt text: Filter panel icon.|Button to open filter conditions panel. Select the clear input icon \(\[Omitted image "icon-clear-input.png"\] Alt text: Clear input icon.\) next to any defined conditions to remove them. Select **Restore defaults** to reset default filters, or **Advanced view** to define filter conditions. For more information, see .|
|New|Button to create a Search Source.|
|Link|Button to select a Search Source to add to the list.|
|Unlink|Button to unlink a Search Source from the list. Select one or more Search Sources from the list before selecting **Unlink**.|

Dictionaries are an optional part of your search profile that guide your searches with synonyms, stop words, and spell checking options. For more information on synonyms, see [Synonyms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/synonyms-ais.md), [Create synonyms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/create-synonym-ais.md), and [Create a synonym dictionary linked to a search profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/create-synonym-dict-ais.md). For more information on stop words, see [Stop words](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/stop-words-ais.md), [Create stop words](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/create-stop-word-ais.md), and [Create a stop word dictionary linked to a search profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/create-stop-word-dict-ais.md).

\[Omitted image "ais-admin-02e.png"\] Alt text: AI Search Admin Console Dictionaries view.

|Field|Description|
|-----|-----------|
|Refresh list \[Omitted image "refresh-list-icon.png"\] Alt text: Refresh list icon.|Button to refresh list of Dictionaries.|
|List Actions \[Omitted image "list-actions-icon.png"\] Alt text: List actions icon.|Button to open list actions. Select **Edit columns** to add or remove columns from the table. Select **Reset widths** if you have adjusted any column widths.|
|Show/Hide Filter panel \[Omitted image "filter-panel-icon.png"\] Alt text: Filter panel icon.|Button to open filter conditions panel. Select the clear input icon \(\[Omitted image "icon-clear-input.png"\] Alt text: Clear input icon.\) next to any defined conditions to remove them. Select **Restore defaults** to reset default filters, or **Advanced view** to define filter conditions. For more information, see .|
|New|Button to create a Dictionary.|
|Link|Button to select a Dictionary to add to the list.|
|Unlink|Button to unlink a Dictionary from the list. Select one or more Dictionaries from the list before selecting **Unlink**.|

Result improvement rules are an optional part of the search profile that boost, block, or improve search results based on various trigger conditions. For more information, see [Result improvement rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/result-improvement-rules-ais.md) and [Create a result improvement rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/create-result-improve-rule-ais.md).

\[Omitted image "ais-admin-02f.png"\] Alt text: AI Search Admin Console Result Improvement rules view.

|Field|Description|
|-----|-----------|
|Refresh list \[Omitted image "refresh-list-icon.png"\] Alt text: Refresh list icon.|Button to refresh list of result improvement rules.|
|List Actions \[Omitted image "list-actions-icon.png"\] Alt text: List actions icon.|Button to open list actions. Select **Edit columns** to add or remove columns from the table. Select **Reset widths** if you have adjusted any column widths.|
|Show/Hide Filter panel \[Omitted image "filter-panel-icon.png"\] Alt text: Filter panel icon.|Button to open filter conditions panel. Select the clear input icon \(\[Omitted image "icon-clear-input.png"\] Alt text: Clear input icon.\) next to any defined conditions to remove them. Select **Restore defaults** to reset default filters, or **Advanced view** to define filter conditions. For more information, see .|
|New|Button to create a result improvement rule.|
|Link|Button to select a result improvement rule to add to the list.|
|Unlink|Button to unlink a Result improvement rule from the list. Select one or more result improvement rules from the list before selecting **Unlink**.|
|Mirrored Result Improvement rules \(advanced\)|List of result improvement rules mirrored from another Search Profile. Use the search window to find one or more Result Improvement rule, and select **Save**. For more information, see [Share result improvement rules between search profiles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/mirror-result-improvement-rules.md).|

Genius Results are an optional part of your Search Profile that displays the best results for search queries. You can view Genius Results configuration in basic and advanced configuration. For more information, see [Genius Results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/genius-results-ais.md) and [Create a Genius Result configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/create-genius-results-config-ais.md).

\[Omitted image "ais-admin-02g1.png"\] Alt text: AI Search Admin Console Genius Results view in basic configuration.

<table id="table_a5g_scn_bcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Use advanced configuration

</td><td>

Select to switch to advanced configuration.

</td></tr><tr><td>

Q&amp;A

</td><td>

Toggle to display top search results from the Knowledge table and related tables. Select from two options:-   Q&amp;A
-   Now Assist Q&amp;A

**Note:** If you activate Q&amp;A, the selected Genius Result is set with the default order. You can change the order by going to the advanced configuration. Now Assist Q&amp;A and Actions are only available to select if you have a Pro Plus license, otherwise they are greyed out.

</td></tr><tr><td>

Catalog Item

</td><td>

Toggle to display top search results from the Catalog Item table. Select from two options:-   Catalog Item
-   Now Assist Actions \(only available in portals\)

</td></tr><tr><td>

People

</td><td>

Toggle to display top search results from the User table.

</td></tr><tr><td>

NLQ

</td><td>

Toggle to use natural language processing to show information from tables, including non-indexed tables, that match a search query.

</td></tr></tbody>
</table>\[Omitted image "ais-admin-02g2.png"\] Alt text: AI Search Admin Console Genius Results view in advanced configuration.

|Field|Description|
|-----|-----------|
|Use basic configuration|Select to switch to basic configuration.|
|Refresh list \[Omitted image "refresh-list-icon.png"\] Alt text: Refresh list icon.|Button to refresh list of Genius Results.|
|List Actions \[Omitted image "list-actions-icon.png"\] Alt text: List actions icon.|Button to open list actions. Select **Edit columns** to add or remove columns from the table. Select **Reset widths** if you have adjusted any column widths.|
|Show/Hide Filter panel \[Omitted image "filter-panel-icon.png"\] Alt text: Filter panel icon.|Button to open filter conditions panel. Select the clear input icon \(\[Omitted image "icon-clear-input.png"\] Alt text: Clear input icon.\) next to any defined conditions to remove them. Select **Restore defaults** to reset default filters, or **Advanced view** to define filter conditions. For more information, see .|
|New|Button to create a Genius Result.|
|Link|Button to select a Genius Result to add to the list.|
|Unlink|Button to unlink a Genius Result from the list. Select one or more Genius Results from the list before selecting **Unlink**.|

## Search Application Configuration

The Search Application Configuration view is where you review how your Search Application is set up. You get a summary view from the Search Application Configuration tab, and you select each of the five subsections to review them in detail. For more information, see [Search application configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/defining-search-app-cfgs-ais.md) and [Create a search application configuration for AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/create-search-app-config-ais.md).

\[Omitted image "ais-admin-02h.png"\] Alt text: AI Search Admin Console Search Application summary view.

|Field|Description|
|-----|-----------|
|Rename|Button to rename your search profile.|
|Use different configuration|Button to select a different Search application configuration.|

Auto-complete Suggestions are an optional part of your search application configuration to display intelligent suggestions in your search application's input field. For more information, see [Auto-complete suggestions in AI Search applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/auto-complete-ais.md).

\[Omitted image "ais-admin-02i.png"\] Alt text: AI Search Admin Console Auto-complete suggestions view.

|Field|Description|
|-----|-----------|
|Refresh list \[Omitted image "refresh-list-icon.png"\] Alt text: Refresh list icon.|Button to refresh list of auto-complete suggestions.|
|List Actions \[Omitted image "list-actions-icon.png"\] Alt text: List actions icon.|Button to open list actions. Select **Edit columns** to add or remove columns from the table. Select **Reset widths** if you have adjusted any column widths.|
|Show/Hide Filter panel \[Omitted image "filter-panel-icon.png"\] Alt text: Filter panel icon.|Button to open filter conditions panel. Select the clear input icon \(\[Omitted image "icon-clear-input.png"\] Alt text: Clear input icon.\) next to any defined conditions to remove them. Select **Restore defaults** to reset default filters, or **Advanced view** to define filter conditions. For more information, see .|
|New|Button to create a auto-complete suggestion.|
|Link|Button to select an auto-complete suggestion to add to the list.|
|Unlink|Button to unlink a auto-complete suggestion from the list. Select one or more auto-complete suggestions from the list before selecting **Unlink**.|

Navigation tabs are an optional part of your search application configuration that refine your search query results by search source. For more information, see [Configure source facet buckets in an AI Search application configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/config-nav-tabs-ais.md).

\[Omitted image "ais-admin-02j.png"\] Alt text: AI Search Admin Console Navigation tabs view.

|Field|Description|
|-----|-----------|
|Refresh list \[Omitted image "refresh-list-icon.png"\] Alt text: Refresh list icon.|Button to refresh list of Navigation tabs.|
|List Actions \[Omitted image "list-actions-icon.png"\] Alt text: List actions icon.|Button to open list actions. Select **Edit columns** to add or remove columns from the table. Select **Reset widths** if you have adjusted any column widths.|
|Show/Hide Filter panel \[Omitted image "filter-panel-icon.png"\] Alt text: Filter panel icon.|Button to open filter conditions panel. Select the clear input icon \(\[Omitted image "icon-clear-input.png"\] Alt text: Clear input icon.\) next to any defined conditions to remove them. Select **Restore defaults** to reset default filters, or **Advanced view** to define filter conditions. For more information, see .|

Sort options are an optional part of your search application configuration that refine your search query results by search source. For more information, see [Configure source facet buckets in an AI Search application configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/config-nav-tabs-ais.md).

\[Omitted image "ais-admin-02k.png"\] Alt text: AI Search Admin Console Sort options view.

|Field|Description|
|-----|-----------|
|Refresh list \[Omitted image "refresh-list-icon.png"\] Alt text: Refresh list icon.|Button to refresh list of Sort options.|
|List Actions \[Omitted image "list-actions-icon.png"\] Alt text: List actions icon.|Button to open list actions. Select **Edit columns** to add or remove columns from the table. Select **Reset widths** if you have adjusted any column widths.|
|Show/Hide Filter panel \[Omitted image "filter-panel-icon.png"\] Alt text: Filter panel icon.|Button to open filter conditions panel. Select the clear input icon \(\[Omitted image "icon-clear-input.png"\] Alt text: Clear input icon.\) next to any defined conditions to remove them. Select **Restore defaults** to reset default filters, or **Advanced view** to define filter conditions. For more information, see .|
|New|Button to create a Sort option.|
|Delete|Button to delete Sort options. Select one or more Sort options before selecting **Delete**.|

Facet filters are an optional part of your search application configuration that refine searches by dynamically generating categories from your search results. For more information, see [Create a facet in an AI Search application configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/create-facet-ais.md).

\[Omitted image "ais-admin-02l.png"\] Alt text: AI Search Admin Console Facet Filters view.

|Field|Description|
|-----|-----------|
|Refresh list \[Omitted image "refresh-list-icon.png"\] Alt text: Refresh list icon.|Button to refresh list of Facet Filters.|
|List Actions \[Omitted image "list-actions-icon.png"\] Alt text: List actions icon.|Button to open list actions. Select **Edit columns** to add or remove columns from the table. Select **Reset widths** if you have adjusted any column widths.|
|Show/Hide Filter panel \[Omitted image "filter-panel-icon.png"\] Alt text: Filter panel icon.|Button to open filter conditions panel. Select the clear input icon \(\[Omitted image "icon-clear-input.png"\] Alt text: Clear input icon.\) next to any defined conditions to remove them. Select **Restore defaults** to reset default filters, or **Advanced view** to define filter conditions. For more information, see .|
|New|Button to create a Facet Filter.|
|Delete|Button to delete Facet Filters. Select one or more Facet Filters before selecting **Delete**.|

Result-card interfaces are an optional part of your search application configuration that provides a standardized display of search results in cards and lists. For more information, see  and .

\[Omitted image "ais-admin-02m.png"\] Alt text: AI Search Admin Console Result-card interface view.

|Field|Description|
|-----|-----------|
|Refresh list \[Omitted image "refresh-list-icon.png"\] Alt text: Refresh list icon.|Button to refresh list of result-card interfaces.|
|List Actions \[Omitted image "list-actions-icon.png"\] Alt text: List actions icon.|Button to open list actions. Select **Edit columns** to add or remove columns from the table. Select **Reset widths** if you have adjusted any column widths.|
|Show/Hide Filter panel \[Omitted image "filter-panel-icon.png"\] Alt text: Filter panel icon.|Button to open filter conditions panel. Select the clear input icon \(\[Omitted image "icon-clear-input.png"\] Alt text: Clear input icon.\) next to any defined conditions to remove them. Select **Restore defaults** to reset default filters, or **Advanced view** to define filter conditions. For more information, see .|
|New|Button to create a result-card interface.|
|Link|Button to select a result-card interface to add to the list.|
|Unlink|Button to unlink a result-card interface from the list. Select one or more Navigation tabs from the list before selecting **Unlink**.|

