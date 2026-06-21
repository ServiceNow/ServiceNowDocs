---
title: Search Preview UI for AI Search
description: The Search Preview UI enables you to test AI Search queries using settings from a selected search application configuration. Administrator tools help you review search query performance data and feedback, debug queries, and override default query settings for testing purposes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/platform-administration/ai-search/search-preview-ui-new.html
release: xanadu
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2025-09-19"
reading_time_minutes: 4
breadcrumb: [Administer, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Search Preview UI for AI Search

The Search Preview UI enables you to test AI Search queries using settings from a selected search application configuration. Administrator tools help you review search query performance data and feedback, debug queries, and override default query settings for testing purposes.

**Note:** The new Search Preview UI feature is included with AI Search. It replaces the legacy Search Preview UI that's included with Advanced AI Search Management Tools. The new version includes all of the same functionality as the legacy version, with a revised and cleaner interface.

Access the new Search Preview UI by navigating to **AI Search** &gt; **Preview** &gt; **Search Preview \(New\)**.

## Required ServiceNow AI Platform® roles

-   The ais\_admin role is required to view and use the Search Preview UI.
-   The impersonator role is required for some AI Search administrator tools.
-   The ais\_high\_security\_admin role is required to bypass search source and content security filtering. For details on this procedure, see [Diagnose search result access issues using the Search Preview UI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-administration/ai-search/diagnose-srch-result-access-ais.md).

## Search Preview UI components

\[Omitted image "search-preview-new-example.png"\] Alt text: Sample Search Preview UI screen displaying sales laptop search query results.

<table id="table_f15_qb3_b4b"><thead><tr><th>

Component

</th><th>

Description

</th></tr></thead><tbody><tr><td>

1. Search application configuration list

</td><td>

Select the search application configuration that you want to apply when previewing search queries.

 The list includes all available search application configurations.

</td></tr><tr><td>

2. Search input field

</td><td>

Enter search query terms and operators in this field. To preview the query's results using settings from the selected search application configuration, press Enter or select the Submit search icon \[Omitted image "search-preview-new-icon-submit-search.png"\] Alt text:. To clear the search input field, select the Clear search term icon \[Omitted image "search-preview-new-icon-clear-search-term.png"\] Alt text:.

 For details on search query syntax and operators, see [AI Search query language](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-administration/ai-search/query-language-ais.md).

 This field displays auto-complete suggestions from your selected search application configuration.

</td></tr><tr><td>

3. Debug AI Search icon

</td><td>

Select this icon to enable session debugging for AI Search and launch the Script Debugger in a new browser tab.

 To learn about session debugging and using the Script Debugger, see [Enable session debugging for AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-administration/ai-search/session-debugging-ais.md) and .

</td></tr><tr><td>

4. Genius Result answers

</td><td>

Review the Genius Result answers the search query produces when executed with the selected search application configuration.**Note:** Genius Result answers may not appear for all search queries. If multiple Genius Result answers are produced for the search query, they appear in a carousel, with the currently selected answer displayed.

</td></tr><tr><td>

5. AI Search administrator tools

</td><td>

Select the icon for the administrator tool that you want to use:

-   **Data \[Omitted image "search-preview-new-icon-process-data.png"\] Alt text:**

View summary information on the search query's triggered result improvement rules, matched NLU model intents, and processing time.

-   **Alert \[Omitted image "search-preview-new-icon-alerts.png"\] Alt text:**

Review alert feedback messages produced during processing of the search query.

-   **Feedback \[Omitted image "search-preview-new-icon-feedback.png"\] Alt text:**

Review dictionary and query feedback messages and NLU model intent data for the search query.

-   **Context \[Omitted image "search-preview-new-icon-context.png"\] Alt text:**

Specify user context values for the search query to trigger result improvement rules.

-   **User \[Omitted image "search-preview-new-icon-user.png"\] Alt text:**

Set the search query's user or locale to test user access to results or view translated documents.


 For more details on each administrator tool's output, controls, and fields, see [Search Preview admin tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-administration/ai-search/search-preview-ui-new-admin-tools.md).

</td></tr><tr><td>

6. Filters

</td><td>

View facet filters applicable to your current search results. To filter the query results, select a facet bucket. To remove the filter, clear the facet bucket selection, select **Clear** at the facet level, or select **Clear all**.

 You can hide the filter list by selecting **Hide filters** and display it again by selecting **Show filters**.

 The filter list displays facet filters for the facets defined in your selected search application configuration.

 To learn more about facet filters, see [Create a facet in an AI Search application configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-administration/ai-search/create-facet-ais.md).

</td></tr><tr><td>

7. Search query results

</td><td>

View the results the search query produces when executed with the selected search application configuration. To page through results, select **Next** or **Previous**. Use the Sort search results list to choose a sort order for the displayed search results.

 Select an option from the View list to control how search results are displayed:

-   **Result cards**: Display search results using EVAM result cards, as they appear in search portals and applications.
-   **Raw output**: Display the search response as a JSON document. Individual search results appear in this document as objects in the `searchResults` array.
-   **Result cards with details**: Display search results using EVAM cards, with a text box for each result showing key details like its relevancy score, language, source table, and source record system\_id.

</td></tr></tbody>
</table>-   **[Search Preview admin tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-administration/ai-search/search-preview-ui-new-admin-tools.md)**  
Understand the output, controls, and fields provided by admin tools in the new Search Preview UI.

**Parent Topic:**[Administering AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-administration/ai-search/administer-ais.md)

