---
title: Using search in Knowledge Management Service Portal
description: View a list of search results as well as options for sorting and filtering the items in the list. You can also use knowledge search in other Service Portals.
locale: en-US
release: yokohama
product: Knowledge Management
classification: knowledge-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Using Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Using search in Knowledge Management Service Portal

View a list of search results as well as options for sorting and filtering the items in the list. You can also use knowledge search in other Service Portals.

**Note:** When you perform a new search, the filters you selected earlier on the Knowledge Management search results page are not saved. You must reselect the filters that you want to apply for every search.

<table id="table_qtz_wzp_kbb"><thead><tr><th>

UI component

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Search bar

</td><td>

Use the search bar at the top of the page to search for additional information.

</td></tr><tr><td>

Sort

</td><td>

Sort the items in a knowledge base or search results list using the Sort by options at the top of the list. -   Views: sorts by number of article views.
-   Newest: sorts by the date created or updated.
-   Alphabetical: sorts alphabetically by the article Short description field.
-   Relevancy: sorts by relevance to the search term.

 The header displays the number of search results, which updates as the user selects and de-selects filters.

 When you navigate away from the search results page and then return, your last sort selection is retained.

</td></tr><tr><td>

Search results list

</td><td>

View knowledge articles and pinned articles. Knowledge article search results include articles in which the short description, text content, or attached file content includes the search term.

 View the knowledge article short description, the knowledge base in which the article is stored, author name, number of views, and rating information.

</td></tr><tr><td>

Language filter facet widget

</td><td>

Language: lists the languages that have been activated. Select one or more languages to display search results in. Your selection is maintained across logins. If multi-language search is enabled, you can search for multiple languages simultaneously.

</td></tr><tr><td>

Knowledge base filter facet widget

</td><td>

Knowledge Base: lists the available knowledge bases

</td></tr><tr><td>

Category filter facet widget

</td><td>

Category: lists the available knowledge categories.**Note:** Shows a hierarchy of categories if the administrator configured the Show category hierarchy \(valid for kb\_category only\) instance option for the facet widget.

</td></tr><tr><td>

Other filter facet widgets

</td><td>

Use filter facets to refine your search results. The selections you make filter the items displayed in the search results list. The search results list updates to display only those items that match your selections. Deleting a selection from the filter facet or breadcrumb reverses the filtering in the list.

 Clear selected filter options by:

 -   Deleting a single option from the search results list header.
-   Clicking Clear all in the search results list header.
-   Clicking Clear in the filter facet widget header.
-   Author: lists the names of the authors for the knowledge articles included in the search results list
-   Tags: lists the available knowledge tags
-   Resource: lists the types of items available, such as knowledge articles
-   Rating: lists article ratings from 0-5 stars \(clicking a rating displays articles that have the selected rating and higher\)
-   Last Modified: lists selections based on the timing of knowledge item modifications such as Past Month or Past Week
-   View Count: lists the knowledge item view counts such as More Than 50 or Less Than 10. Set the number of days to consider when calculating view count using the **glide.knowman.view\_age.days** property. For more information on this property, see [Knowledge portal properties](../reference/r_KnowledgeProperties.md#).

</td></tr><tr><td>

View additional search results

</td><td>

Depending on the system setup, view additional search results using one of these options:-   Standard Pagination: displays the search results in multiple pages.
-   Infinite Scroll: displays the search results while scrolling.

</td></tr></tbody>
</table>**Note:** If a custom widget on the knowledge search results page uses the **KnowledgeSearchService** angular service, you must add the **sn.knowledgeApplication** dependency to enable the functionality of the custom widget.

1.  Navigate to **Service Portal** &gt; **Dependencies**.
2.  In the **Name** field, search for the **sn.knowledgeApplication** dependency.
3.  If a message appears, click **here** to edit.

    You have to be in the **Knowledge Management - Service Portal** application to edit.

4.  Click **Update**.

The search functionality in Knowledge Management Service Portal pages uses the **Knowledge Base Search** search context to fetch results. As an administrator, you must not update the definition of this search context because it may impact the search behavior. For more information about contextual search, see [Contextual search concepts](https://www.servicenow.com/docs/access?context=contextual-search-concepts&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

