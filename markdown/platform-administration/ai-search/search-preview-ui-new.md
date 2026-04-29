---
title: Search Preview UI for AI Search
description: The Search Preview UI enables you to test AI Search queries using settings from a selected search application configuration or search profile. Administrator tools help you review search query performance data and feedback, debug queries, and override default query settings for testing purposes.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Administer, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Search Preview UI for AI Search

The Search Preview UI enables you to test AI Search queries using settings from a selected search application configurationor search profile. Administrator tools help you review search query performance data and feedback, debug queries, and override default query settings for testing purposes.

**Note:** The new Search Preview UI feature is included with AI Search. It replaces the legacy Search Preview UI that's included with Advanced AI Search Management Tools. The new version provides additional functionality when compared with the legacy version, and offers a revised and cleaner interface.

Access the new Search Preview UI by navigating to **AI Search** &gt; **Preview** &gt; **Search Preview \(New\)**.

## Required ServiceNow AI Platform® roles

-   The ais\_admin role is required to view and use the Search Preview UI.
-   The impersonator role is required for some AI Search administrator tools.
-   The ais\_high\_security\_admin role is required to bypass search source and content security filtering. For details on this procedure, see [Diagnose search result access issues using the Search Preview UI](../task/diagnose-srch-result-access-ais.md).

## Search Preview UI components

![Sample Search Preview UI screen displaying service issue search query results.](../image/search-preview-new-example-q4-2025.png "Search Preview UI")

<table id="table_b4r_ql2_hhc"><thead><tr><th>

Component

</th><th>

Description

</th></tr></thead><tbody><tr><td>

1. Preview types list

</td><td>

Select the type of preview you want to view.-   **Full visual view**: preview search query results using the search profile and display settings defined for the search application configuration record selected in the **Search Application** list.
-   **Text view**: preview search query results using a search profile selected in the **Search Profile** list. When previewing in text view, features from search application configurations, such as auto-complete suggestions, are not available.

</td></tr><tr><td>

2. Search mode list

</td><td>

Select the search mode you want to use for your search query.-   **Keyword search**: Use the legacy keyword search mode to find the best matches for your search query terms.
-   **Hybrid search**: Use the hybrid search mode, blending keyword search and semantic vector search to find the best combination of search precision and contextual relevance for your search query.

**Note:** Hybrid search only affects knowledge article, Catalog Item, external content, and topic retrieval searches. AI Search continues to use keyword search when searching indexed content from other sources.


</td></tr><tr><td>

3. Search Application / Search Profile list

</td><td>

Select the search application configuration or search profile that you want to apply when previewing search queries.When you select full visual view as the preview type, the name of this list is **Search Application** and it includes all available search application configurations that have published search profiles with one or more linked search sources.

When you select text view as the preview type, the name of this list is **Search Profile** and it includes all published search profiles with one or more linked search sources.

**Note:** If a search profile has unpublished changes, its entry in the list displays a warning icon ![](../../../use/dashboards/image/icon-warning-circle.png) and shows `[DRAFT]` after the profile's name. Publish the search profile to see the changes reflected in the Search Preview UI results.

</td></tr><tr><td>

4. Card view list

</td><td>

Select how you want to display the results from your search query:-   **Result cards with details**: Display search results using EVAM result cards, with a text box for each result showing key details like its relevancy score, language, source table, and source record system\_id.
-   **Result cards**: Display search results using EVAM result cards, as they appear in search portals and applications.
-   **Raw output**: Display the search query response object in JSON format. Individual search results appear in this document as objects in the response object's `searchResults` array.

</td></tr><tr><td>

5. Search input field

</td><td>

Enter search query terms and operators in this field. To preview the query's results using settings from the selected search application configuration or search profile, press Enter or select the Submit search icon ![](../image/search-preview-new-icon-submit-search.png). To clear the search input field, select the Clear search term icon ![](../image/search-preview-new-icon-clear-search-term.png). For details on search query syntax and operators, see [AI Search query language](query-language-ais.md).

When you select full visual view as the preview type, this field displays auto-complete suggestions from your selected search application configuration. When you select text view as the preview type, this field does not display auto-complete suggestions.

</td></tr><tr><td>

6. Open Debugger button

</td><td>

Select this icon to enable session debugging for AI Search and launch the Script Debugger in a new browser tab. To learn about session debugging and using the Script Debugger, see [Enable session debugging for AI Search](../task/session-debugging-ais.md) and [Script Debugger and Session Log](https://www.servicenow.com/docs/access?context=script-debugger&version=australia&pubname=australia-api-reference&ft:locale=en-US).

</td></tr><tr><td>

7. Genius Result answers

</td><td>

Review the Genius Result answers the search query produces when executed with the selected search application configuration or search profile.**Note:** Genius Result answers may not appear for all search queries. If multiple Genius Result answers are produced for the search query, they appear in a carousel, with the currently selected answer displayed.

</td></tr><tr><td>

8. AI Search administrator tools

</td><td>

Select the icon for the administrator tool that you want to use:-   **Summary ![](../image/search-preview-new-icon-summary.png)**

View links to the search query's search profile \(and search application configuration, in full visual view\). Review overview data on the processing of the search query.

-   **Genius Results ![](../image/search-preview-new-icon-genius-results.png)**

View the Genius Result configurations activated for the search query, with those that generated Genius Result answers indicated. Review the set of search results that were sent to the LLM for Genius Result answer generation.

-   **Details ![](../image/search-preview-new-icon-details.png)**

View summaries of how stop word, typo handling, and synonym dictionaries affected processing of the search query. Review the list of fields and values from the search query object, filtering to focus on areas of interest.

-   **Profile ![](../image/search-preview-new-icon-summary.png)**

Set a user or locale for the search query to test user access to results or view translated documents. Specify user context field values for the search query to test result improvement rule triggers.


 For more details on each administrator tool's output, controls, and fields, see [Search Preview admin tools](../reference/search-preview-ui-new-admin-tools.md).

</td></tr><tr><td>

9. Filters

</td><td>

View facet filters applicable to your current search results. To filter the query results, select a facet bucket. To remove the filter, clear the facet bucket selection, select **Clear** at the facet level, or select **Clear all**. You can hide the filter list by selecting **Hide filters** and display it again by selecting **Show filters**.

The filter list contents depend on whether you're previewing results for a search application configuration or a search profile.

-   **Search application configuration**: The filter list displays facet filters for the facets defined in the search application configuration.
-   **Search profile**: The filter list displays a facet filter for the source table field.

To learn more about facet filters, see [Create a facet in an AI Search application configuration](../task/create-facet-ais.md).

</td></tr><tr><td>

10. Search query results

</td><td>

View the results the search query produces when executed with the selected search application configuration or search profile.When viewing result cards, you can page through results by selecting **Next** or **Previous**, and use the Sort search results list to choose a sort order for the displayed search results.

When viewing raw output, this section displays the search query response object in JSON format. Select the Search icon ![](../image/search-preview-new-icon-submit-search.png) to search for a term in the response. Open the More options menu to activate or deactivate syntax highlighting, show or hide the navigation minimap of the full JSON response, or enable or disable word wrap.

</td></tr></tbody>
</table>-   **[Search Preview admin tools](../reference/search-preview-ui-new-admin-tools.md)**  
Learn about the output, controls, and fields provided by admin tools in the new Search Preview UI.

**Parent Topic:**[Administering AI Search](administer-ais.md)

