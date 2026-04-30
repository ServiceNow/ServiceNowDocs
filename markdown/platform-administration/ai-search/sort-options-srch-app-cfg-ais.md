---
title: Search result sort options in AI Search application configurations
description: A search result sort option enables users to display search results in an order determined by their field values. Applying a search result sort option overrides the default AI Search relevancy-based result order. You can define custom search result sort options for your AI Search applications.Define a sort option to enable users of an AI Search application to order their search results using field values.Remove a search result sort option from the sort menu in an AI Search application. The removal of the search result sort option prevents users of the application from selecting that option to reorder their search results with.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Search application configurations, Configure, AI Search, Search administration, Configure core features, Administer]
---

# Search result sort options in AI Search application configurations

A search result sort option enables users to display search results in an order determined by their field values. Applying a search result sort option overrides the default AI Search relevancy-based result order. You can define custom search result sort options for your AI Search applications.

When sorting search results on a string field, AI Search uses collation-based sort following the rules for the ServiceNow AI Platform® session language.

For details on how users apply search result sort options, see [Change the sort order for your search results](../task/sort-search-results-ais.md).

**Parent Topic:**[Search application configurations](defining-search-app-cfgs-ais.md)

## Create a search result sort option in an AI Search application configuration

Define a sort option to enable users of an AI Search application to order their search results using field values.

### Before you begin

Role required: search\_application\_admin

### About this task

A search result sort option enables users to sort their search results on a field, overriding the default AI Search relevancy-based result order. Each search result sort option specifies a field to sort results on, and a sort order \(ascending or descending\) order for the sort.

The sort menu in an AI Search application displays all active search result sort option defined for that application, plus the default **Most relevant** option.

**Note:** If no search result sort options are active for an AI Search application, the sort menu doesn't display for users of that application and results are automatically sorted by relevance.

### Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **Search Experience** &gt; **Search Applications**.

2.  Open the search application configuration that you want to create a search result sort option for.

3.  In the Sort Options related list, select **New**.

4.  On the Sort Option form, fill in the fields.

    For a description of the field values, see [Sort Option form](../reference/sort-option-form-ais.md).

5.  Select **Submit**.


### Result

The new search result sort option appears in the search application's Sort Options related list, and its title displays in the sort menu for users of the search application. Users can select the new option from the sort menu to apply the defined sort to their search results.

## Remove a search result sort option from an AI Search application configuration

Remove a search result sort option from the sort menu in an AI Search application. The removal of the search result sort option prevents users of the application from selecting that option to reorder their search results with.

### Before you begin

Role required: search\_application\_admin

### Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **Search Experience** &gt; **Search Applications**.

2.  Open the search application configuration that you want to disable a search result sort option for.

3.  In the Sort Options related list, open the search result sort option that you want to disable.

4.  On the Sort Option form, clear the **Active** option and select **Update**.

    For a description of the field values, see [Sort Option form](../reference/sort-option-form-ais.md).


### Result

The selected search result sort option no longer appears in the search application's sort menu.

**Note:** If no search result sort options are active for an AI Search application, the sort menu no longer displays for users of that application and results are automatically sorted by relevance.

