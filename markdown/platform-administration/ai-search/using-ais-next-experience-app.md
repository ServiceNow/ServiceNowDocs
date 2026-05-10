---
title: Using global search with AI Search for Next Experience
description: Global search enables you to search multiple record types at once from the Next Experience Unified Navigation search field. You can switch between global search results and results from workspace applications that you have access to.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 11
breadcrumb: [AI Search for Next Experience, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Using global search with AI Search for Next Experience

Global search enables you to search multiple record types at once from the Next Experience Unified Navigation search field. You can switch between global search results and results from workspace applications that you have access to.

## Search in the Unified Navigation search field

To use global search, enter your search query in the Unified Navigation search field, then select **View all results for "&lt;search-query&gt;"** or press Enter.

![Unified Navigation search field.](../../../get-started/servicenow-overview/image/pol-nav-global-search.png)

![Unified Navigation search field with search terms entered, showing the View results link.](../image/unified-nav-ai-search-terms.png)

The search results page displays a list of previews for records that match your search query. You can open any search result record in a new browser tab by selecting its preview in the list. Your search remains open in your original browser tab, so you can return to it and refine it.

**Note:** AI Search administrators can configure search results to open in the same browser tab as the search. To make this change, edit the EVAM configuration bundle from the EVAM definition for the **\[AIS\] Next Experience Search Configuration** search application, setting the **forceNewTab** property to false in the relevant Search Result card EVAM view configurations. For more details on editing EVAM display settings for search results, see [Configure EVAM display settings for search results in AI Search applications](../task/configure-search-result-card-opts.md) and [List of Search Result EVAM card properties](../reference/search-result-evam-card-opts.md).

![Global search results page showing search results for a service desk search query.](../image/unified-nav-ai-search-results.png)

**Note:** When you search with a search query, the system only displays results for records included in the AI Search index. Search queries won't match records that have never been indexed or records that have been purged from the index by a retention policy. AI Search administrators can configure indexing and retention policy settings. For details on these settings, see [Indexing content from AI Search indexed sources](indexing-content-ais.md) and [Indexed source retention policies and filter conditions](retention-policies-conditions-ais.md).

AI Search administrators can customize the index fields displayed on search result previews. For details, see the customization section found in this topic.

## Narrow your search by source on the search results page

You can narrow your search to display only results from a particular search source. When you select one or more of the search results page's source facet bucket options, the page shows only those matching records that come from the selected sources. To return to viewing matching records from all sources, clear the selected source facet bucket options or select **Clear** in the Sources list.

![Detail of global search results page with Incident source facet bucket option selected, showing only incident search results.](../image/unified-nav-ai-search-source-facet-buckets.png)

AI Search administrators can configure display settings for source facet buckets. For details, see [Configure source facet buckets in an AI Search application configuration](../task/config-nav-tabs-ais.md).

## Narrow your search by field value on the search results page

After you select one or more source facet buckets, you may see a Filters list. Each facet filter in this list indicates a field from your selected search source\(s\). The filter displays the field's values that are found on one or more of your currently displayed search result records. When you select a facet filter value, your search narrows to show only those matching records that include the specified field value.

For example, suppose you select the **Incident** source facet bucket to view only Incident records that match your search query. The Filters list appears, displaying facet filters for Incident fields such as **Priority**, **State**, **Category**, and **Assignment Group**. Selecting the **In Progress** value from the **State** facet filter narrows your search to show only matching records for Incidents that are in progress.

![Detail of global search results page with Incidents source facet bucket and State: In Progress facet bucket selected and filters list showing additional facet filter options.](../image/unified-nav-ai-search-facets.png)

To remove an applied facet filter, select **Clear** by the facet field name, or **Clear all** to remove all applied filters at once. You can hide the Filters list by selecting **Hide filters**.

AI Search administrators can define facets in search application configurations. For details, see [Create a facet in an AI Search application configuration](../task/create-facet-ais.md).

In the base system, facets don't appear in the Filters list until you've selected a source facet bucket. Administrators can override this behavior and show all available facets in the Filters list by creating a **glide.ui.ais.show\_all\_facets** system property record and setting its value to **true**. For more details on this system property, see [AI Search for Next Experience properties](../reference/ai-search-next-experience-properties.md).

The Filters list defaults to displaying a count of matching search results for each facet bucket. Search administrators can configure this behavior in search application configurations. To learn more about result counts for facets, see [Show search result counts for facets on the results page for a search application](../task/display-result-counts-ais.md).

## Sort your search results

By default, AI Search displays the most relevant search results first. To change the display order for records on the search results page, select a sort option from the sort menu.

![Detail of global search results page with search results sort order menu highlighted.](../image/unified-nav-ai-search-sort-results.png)

AI Search administrators can configure search result sort options. For details, see [Search result sort options in AI Search application configurations](sort-options-srch-app-cfg-ais.md#).

## Return to your starting point from the search results page

To return to the page where you initiated your search, select the link with a left arrow that appears above the source facet buckets on the search results page. The title of this link indicates the page it returns you to. For example, if you searched from the Home page, the link text would be **Home**, but if you searched from the Dashboards page, the link text would be **Dashboards Overview**.

![Detail of global search results page with Dashboards Overview return link highlighted.](../image/unified-nav-ai-search-return-link.png)

## Search suggestions in the Unified Navigation search field

AI Search displays auto-complete suggestions to help you get directly to the results you need. Suggestions may include recent search queries, recently viewed search results, or search queries or results that match the terms you're typing into the search field.

Some suggestion types appear when you initially select the search field.

![Unified Navigation search field showing Recent Searches auto-complete suggestions.](../image/unified-nav-ai-search-suggs-click.png)

Other suggestion types appear when you begin typing your search query into the search field.

![Unified Navigation search field showing Suggested Queries and Suggested Results auto-complete suggestions.](../image/unified-nav-ai-search-suggs-type.png)

AI Search administrators can configure auto-complete suggestions. For details, see [Auto-complete suggestions in AI Search applications](auto-complete-ais.md#).

## Search for a specific record using Exact Match

Enter a record number into the Unified Navigation search field but don't press Enter or select **View results**. The search field displays a preview of the record with an **Exact Match** tag. Select the preview to go directly to the matching record, bypassing the search results page.

![Global search field displaying exact match record preview.](../image/unified-nav-ai-search-exact-match.png)

**Note:** When you search for a record by number, the system displays the matching record regardless of whether it's included in the AI Search index or not.

Exact matching returns results from tables with a prefix defined in the Number \[sys\_number\] table. If the search includes a single term that starts with the table's prefix, AI Search returns an exact match result from the table if one exists. As an example, searching for the single term `INC3263827` returns an exact match from the Incident \[incident\] table because the search term starts with the INC prefix defined for that table.

If more than one record has a **Number** field value that exactly matches your search, AI Search displays the first exact match. An informational message reports the total number of exact matches and provides links to the other exact matches.

Search administrators can override the default exact match behavior by configuring custom search matchers. For details on this procedure, see [Create a custom search matcher for global search](../task/create-search-matcher-ais.md).

## View results for your search in an available workspace application

If you have access to search in workspace applications, an arrow appears at the right of the Unified Navigation search field after you search that enables you to switch between the results in global search and in your workspace applications.

![Global search field displaying search context menu.](../../../get-started/servicenow-overview/image/pol-search-context.png)

For example, if the context menu in the illustration was available after you performed a global search, you could select **CSM/FSM Configurable Workspace** from the context menu to view results for the search in CSM/FSM Configurable Workspace.

Exact matches open in the selected workspace application. For example, if you selected **CSM/FSM Configurable Workspace**, entered a record number, and selected the record preview in the search results, the record would open in CSM/FSM Configurable Workspace.

## Customize display fields for your search result previews

Search result previews display a default set of AI Search index fields. If you have the ais\_admin role, you can customize the set of index fields a search result preview displays by modifying its EVAM view configuration. For information on EVAM view configurations, see [Entity View Action Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/entity-view-action-mapper-evam/exploring-entity-view-action-mapper.md).

When customizing a search result preview's EVAM view configuration, you can reference the AI Search index fields that exist on the previewed search result. To add a new AI Search index field to search results from an indexed source, define a **map\_to** field setting. This field setting populates the index field on each affected search result with the value of a field you specify from the search result's source record or document. For an overview of mapping source fields to AI Search index fields, see [Field settings for AI Search](field-settings-ais.md). To create a new **map\_to** field setting for one of your indexed sources, see [Create a field setting for an AI Search indexed source](../task/create-field-setting-ais.md).

## Now Assist in Virtual Agent enhanced chat entry point

If Now Assist in Virtual Agent enhanced chat is activated in the Now Assist panel, the search field in global and workspace search displays a search icon and `Search or ask Now Assist` placeholder text. When you enter search terms, the search field displays Now Assist suggestions. Selecting a Now Assist suggestion takes you to enhanced chat in the dynamic window.

**Note:**

To see this enhanced chat entry point behavior, your instance must satisfy all of the following conditions:

-   [Now Assist in AI Search](../reference/now-assist-ais.md) is installed.
-   [Now Assist in Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/now-assist-in-virtual-agent/now-assist-in-va-landing.md) is installed.
-   Enhanced chat is activated via the Now Assist panel. For details on activating enhanced chat, see [Activate Now Assist panel enhanced chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-panel-enhanced-activate.md).

If these conditions aren't satisfied, the search field in global and workspace search doesn't display the icon and placeholder text or show Now Assist suggestions.

To learn about Now Assist in Virtual Agent enhanced chat, see [Enhanced chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/now-assist-in-virtual-agent/nava-enhanced-chat.md).

**Parent Topic:**[AI Search for Next Experience](ais-next-experience-app.md)

