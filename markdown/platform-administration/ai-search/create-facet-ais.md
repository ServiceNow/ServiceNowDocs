---
title: Create a facet in an AI Search application configuration
description: Define facets to refine your searches using categories dynamically generated from the current search results.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-07-16"
reading_time_minutes: 3
breadcrumb: [Search application configurations, Configure, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a facet in an AI Search application configuration

Define facets to refine your searches using categories dynamically generated from the current search results.

## Before you begin

Role required: search\_application\_admin

## About this task

Create a facet to populate a refinement filter for search results based on indexed source field values. The facet initially displays filter options for all field values found in the current search result set. Selecting a field value refines the search result set, displaying only those results that satisfy the filter logic for the facet.

**Note:** If AI Search applies late binding security to any results from an indexed source used by a facet, the list of available filter selections for the facet changes. When this happens, the facet only displays field values found in the current page of search results. For more information on late binding security, see [Content security in AI Search](../concept/content-security-ais.md).

Facets can have any one of the following types. Each facet type has its own filter logic.

-   **Single Select**

    In a Single Select facet, you can only select a single field value as a facet refinement filter.

    When you select a field value from a Single Select, AI Search filters the search results list, displaying only results that contain your chosen field value.

    A Single Select facet only allows you to select field values that are found in the current result set.

-   **Multi Select And**

    In a Multi Select And facet, you can select multiple field values as facet refinement filters.

    When you select a field value from a Multi Select And facet, AI Search filters the search results list, displaying only results that contain all of the field values you've selected from the facet.

    A Multi Select And facet only allows you to select field values that are found in the current result set.

-   **Multi Select Or**

    In a Multi Select Or facet, you can select multiple field values as facet refinement filters.

    When you select a field value from a Multi Select Or facet, AI Search filters the search results list, displaying only results that contain any of the field values you've selected from the facet.

    A Multi Select Or facet initially only allows you to select field values that are found in the current result set. All field values that are available when you make your first selection remain available for selection.

    As an example, suppose you have a Multi Select Or facet for a custom **Color** field with blue, green, and red field values. If your search returns only green and red results, the **Color** facet only displays **green** and **red** field values. When you select the **red** field value, AI Search keeps the **green** field value available for selection because it was available before you made any **Color** selection.


**Warning:** Applying multiple filters from a Multi Select And or Multi Select Or facet makes your search query URL longer. Test your multi-select facet configurations to ensure that search query URLs with facet filters don't exceed the maximum URL length limit for your web browser. \(Different web browsers have different URL length limits.\)

Facets work best when created from fields of the following types with relatively few unique values:

-   Choice
-   Reference
-   String
-   String \(Full UTF-8\)
-   True/False

When sorting facet refinement filters by name, AI Search uses collation-based sort following the rules for the ServiceNow AI Platform® session language.

For tables other than Knowledge \[kb\_knowledge\], facets display appropriate field translations for the current user session. Facets don't display translated versions of kb\_knowledge translated fields.

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **Search Experience** &gt; **Search Applications**.

2.  Open the search application configuration that you want to configure a facet for.

3.  In the Facets related list, select **New**.

4.  On the Facet form, fill in the fields.

    For a description of the field values, see [Facet form](../reference/facet-form-ais.md).

5.  Select **Submit**.


## Result

The new facet appears in the Facets related list.

**Parent Topic:**[Search application configurations](../concept/defining-search-app-cfgs-ais.md)

