---
title: Search Application Configuration form
description: The Search Application Configuration form contains information about search application configurations defined for AI Search. Use this form when creating or modifying a search application configuration.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Reference, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Search Application Configuration form

The Search Application Configuration form contains information about search application configurations defined for AI Search. Use this form when creating or modifying a search application configuration.

For details on creating or modifying a search application configuration for use with AI Search, see [Create a search application configuration for AI Search](../task/create-search-app-config-ais.md).

<table id="search-app-config-table"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the search application configuration. Type: string

</td></tr><tr><td>

Search Engine

</td><td>

Search engine to use in the ServiceNow AI Platform® search application that links to the search application configuration. Type: choice list

 Default value: AI Search

 Supported values:

-   **AI Search**: Use AI Search as the search engine for the application. Select this search engine if your search application has the **Enable AI Search** option enabled.
-   **Zing**: Use the Zing text indexing and search engine as the search engine for the application. Select this engine if your search application has the **Enable AI Search** option disabled, or if it lacks this option.

 **Note:** If your search engine selection conflicts with your search application's **Enable AI Search** setting, the system displays an error message. Before changing search engines, first make sure that your search application has the proper **Enable AI Search** setting.

</td></tr><tr><td>

Search Profile

</td><td>

Search profile to use for searches in the application. This field appears only when you select **AI Search** as the application's search engine. Type: reference to a record from the Search Profile \[ais\_search\_profile\] table

</td></tr><tr><td>

Search Results Limit

</td><td>

Maximum number of search results the application should display on each search results page. This limit also specifies the minimum number of search results each query should return. When a search query returns less than this number of results, AI Search attempts to broaden the result set by automatically resubmitting the query with modified parameters. For more details on query resubmission, see [Automatic search query resubmission](../concept/auto-query-resubmission-ais.md).

 Type: integer

 Default value: 10

 Supported values: 0 or positive

</td></tr><tr><td>

Genius Results Limit

</td><td>

Maximum number of Genius Result answer cards the application should display on the search results page. This field appears only when you select **AI Search** as the application's search engine.Type: integer

Supported values: 0 or positive

When **Genius Results Limit** is set to 2 or greater and a search returns multiple Genius Result answers, the answer cards display in a carousel. You can scroll the carousel and select the answer card you want to take action from.

**Note:** Search applications display a maximum of 10 answer cards per search query. If you set this limit to 11 or more, the search application still displays a maximum of 10 answer cards.

Starting with version 6 of [Now Assist in AI Search](now-assist-ais.md), installing Now Assist in AI Search makes the value of this field default to 10 instead of 1 when you create a new search application configuration or edit an existing one.

</td></tr><tr><td>

Attachment Limit

</td><td>

Maximum number of grouped attachments to display by default on a parent search result when attachment grouping is specified in **Show parent for results that are attachments**. Attachments beyond this limit are hidden by default and only shown when you select **Show more** in the parent search result's attachments list.

 Type: integer

 Default value: 5

 Supported values: 0 or positive

</td></tr><tr><td>

Enable Typo Handling

</td><td>

Option to auto-correct search query terms to match terms found in the search profile's typo handling dictionary. This field appears only when you select **AI Search** as the application's search engine. For more details on typo handling auto-correction configuration and behavior, see [Typo handling](../concept/typo-handling-ais.md).

 Type: true \| false

 Supported values:

-   **true**: Auto-correct search query terms in the search application.
-   **false**: Don't auto-correct search query terms in the search application.

</td></tr><tr><td>

Enable Exact Match

</td><td>

Option to use exact matching in the search application. When this option is selected, if a search result's **Number** field exactly matches the search, the application displays the record or document associated with that search result, bypassing the search results page. Exact matching also bypasses any custom matchers defined for the search application.

**Important:** Exact match is not supported in portals. If you enable this option for a portal, users searching in that portal may experience navigation issues.

 Exact match behavior is controlled by the **com.snc.agent\_workspace.global\_search.typeahead.exact\_match\_request\_criterion\_regex** system property. This property's value is a Java regular expression pattern. Only search queries that match the regular expression pattern are evaluated as possible exact record matches. For details on Java regular expression pattern syntax, see [the Javadoc for the java.regex.util.Pattern class](https://docs.oracle.com/en/java/javase/21/docs/api/java.base/java/util/regex/Pattern.html).

 Type: true \| false

 Default value: true

 Supported values:

-   **true**: Use exact matching in the search application.
-   **false**: Don't use exact matching in the search application.

</td></tr><tr><td>

Show parent for results that are attachments

</td><td>

Option to display attachment search results inline with their parent results on the search application's results page. If cleared, attachment search results display separately from their parent results. For more details on the effects of attachment grouping, see [Grouping attachment search results with their parent search results](../concept/grouping-attachment-srch-results-ais.md).

 Type: true \| false

 Default value: true

 Supported values:

-   **true**: Group attachment search results inline with their parent results in the search application.
-   **false**: Display attachment search results separately from their parent results in the search application.

</td></tr><tr><td>

Filter Genius Results by tab

</td><td>

Option to filter Genius Result searches based on the selected source facet bucket.In a search application that has this option enabled, when you select a source from the application's source facet, Genius Result searches honor the source filter and so can only return results from the selected source. This means that only Genius Result configurations that include information from the selected source can generate Genius Result answers in the search application. Genius Result configurations that don't include information from the selected source don't return any search results and thus can't generate Genius Result answers.

As an example, suppose you select the Knowledge source facet bucket in a search application that has this option selected. With that Knowledge source selection applied, Q&amp;A Genius Results, which include information from the Knowledge source, can still find search results and generate Genius Result answers. But Catalog Item Genius Results, which include information from the Catalog Item source which isn't selected, can't find search results and so can't generate Genius Result answers.

**Note:** The Now Assist Multi-Content Response Genius Results configuration \(from the Now Assist in AI Search ServiceNow Store application\) includes information from multiple sources, so it can generate Genius Result answers no matter which source is selected. To learn more about Now Assist Multi-Content Response Genius Results, see [Now Assist Multi-Content Response Genius Results](../concept/now-assist-multi-content-qna-genius-results.md).

</td></tr><tr><td>

Show Search Results Count

</td><td>

Option to display search result counts for facets on the search application's results page. For more details on this option, see [Show search result counts for facets on the results page for a search application](../task/display-result-counts-ais.md).

 Type: true \| false

 Default value: true

 Supported values:

-   **true**: Display search result counts for facets on the search application's results page.
-   **false**: Don't display search result counts for facets on the search application's results page.

</td></tr></tbody>
</table>**Parent Topic:**[AI Search reference](../concept/reference-ais.md)

