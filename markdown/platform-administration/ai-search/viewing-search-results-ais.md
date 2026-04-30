---
title: Viewing search results in AI Search
description: Learn about the components that AI Search uses to display results for search queries.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2025-08-25"
reading_time_minutes: 3
breadcrumb: [Search, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Viewing search results in AI Search

Learn about the components that AI Search uses to display results for search queries.

## Search result page elements

The layout and appearance of AI Search UI elements varies from application to application. This example shows the elements as they might appear on a Service Portal search results page.

![Sample search result page displaying email search query results.](../image/service-portal-search-results-ais.png "Sample search result page")

<table id="table_ljh_gxw_nnb"><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

1. Search input field

</td><td>

Displays the search query that produced the listed search results. You can modify this search query and search again to view different results.

</td></tr><tr><td>

2. Navigation tab filters

</td><td>

Displays static filter options for refining search results by search source. If you want to view only results from a single search source, select that search source's name. To remove the navigation tab filter, select **All**.

</td></tr><tr><td>

3. Search result sort order

</td><td>

Displays the currently selected sort order for search results. By default, AI Search displays the most relevant results first. To apply an alternative sort order, open this list and select one of the available search result sort options.

**Note:** If no search result sort options are available, the sort menu doesn't display and results are automatically sorted by relevance.

</td></tr><tr><td>

4. Facet filters

</td><td>

Displays dynamic filter options for refining search results by field value. To expand or collapse a facet, select the **+** \(plus\) or **-** \(minus\) symbol by its name.

 To view only search results that contain a specific field value, select the field value option in the facet. Clear the field value option to remove the facet filter.

**Note:** When faceting on a date field, the facet options are precomputed date ranges, such as `Past 3 months`, rather than exact date field values. Selecting an option displays only results that have date field values in the specified range. You can select and clear these date range options in the same way that you select and clear field value options for non-date facets.

 Some facets allow you to select multiple field values. Field values in multi select facets display as options instead of links, and include a label showing how multiple selections are applied when filtering your search results. Labels include:

-   **Contains all selected**: Displays only search results that include all of the selected field values. This label indicates the Multi Select And facet type.
-   **Contains any selected**: Displays search results that include any one of the selected field values. This label indicates the Multi Select Or facet type.

 If your facet filter cannot be applied to search results from the navigation tab you've selected, AI Search ignores the facet filter.

</td></tr><tr><td>

5. Genius Result answer cards

</td><td>

Display the best answers for your search query along with actions you can take directly from each card.**Note:** Genius Result answer cards may not appear for all search queries.

 You may see your regular search results appear before AI Search finishes computing Genius Result answers for your search. An animated message lets you know if Genius Result answer computation is still ongoing when your regular search results appear.

 When a search returns multiple Genius Result answers, the answer cards display in a carousel. You can scroll the carousel and select the answer card you want to take action from.

 To provide feedback relating to a Genius Result answer, select one of its **Was this suggestion helpful?** links. If the answer is relevant to your search, select **Yes**; otherwise, select **No**.

</td></tr><tr><td>

6. Search results

</td><td>

Displays the icon, summary field values, title, and text snippet for each search result, with search query terms highlighted in title and text snippets. Select a result to view its source record in full.

 When a search result displays the Open in New Tab icon ![](../image/icon-open-in-new-tab-ais.png), you can select it to view the source record in a new browser tab, preserving the state of your search in the current tab.

**Note:** If you select an attachment search result, the system may display the attachment or may prompt you to download the attachment.

</td></tr></tbody>
</table>## Auto-correction message

When AI Search auto-corrects a misspelled search query term, a `Showing results for <corrected_term>` message appears above the search results list.

![Sample auto-correction message showing replacement of search query term emial with email.](../image/service-portal-auto-correction-ais.png)

<table id="table_tgx_rgj_snb"><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

1. Typo handling auto-correction message and link to original search term

</td><td>

Displays the auto-corrected query term used for the search. To repeat the search using your original search query term, select the link in the **Search instead for &lt;original\_term&gt;** line of the message.

</td></tr></tbody>
</table>**Parent Topic:**[Searching in AI Search](use-ais.md)

