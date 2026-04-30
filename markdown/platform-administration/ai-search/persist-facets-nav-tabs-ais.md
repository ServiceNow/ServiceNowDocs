---
title: Clear facet filters when selecting a new navigation tab
description: Specify whether AI Search applications should preserve existing facet filters when you select a new navigation tab.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-07-16"
reading_time_minutes: 2
breadcrumb: [Search application configurations, Configure, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Clear facet filters when selecting a new navigation tab

Specify whether AI Search applications should preserve existing facet filters when you select a new navigation tab.

## Before you begin

Role required: admin

## About this task

By default, AI Search preserves your facet filters when you select a new navigation tab. As an example, suppose that you narrow your search results by selecting the Email field value from the **KB Category** facet displayed on the **All** navigation tab. If you then select the **Knowledge** navigation tab, the **KB Category** facet retains your Email selection and still filters your search results accordingly.

Administrators can override this default behavior by setting the value of the **glide.ais.facets.cross\_tab\_persistence** system property. When this system property value is set to false, selecting a new navigation tab removes all facet filters. In the preceding example, selecting the **Knowledge** navigation tab would remove your **KB Category** facet filter.

This option is global and applies to all AI Search applications on your instance.

**Note:** If an existing facet filter cannot be applied to search results from a selected navigation tab, AI Search ignores the facet filter. This behavior only occurs in search applications where you've disabled search result counts. For more details on search result counts, see [Display search result counts on the results page for a search application](display-result-counts-ais.md).

## Procedure

1.  Navigate to the System Property \[sys\_properties\] table's list view.

    1.  Select **All**.

    2.  In the **Filter** field, enter `sys_properties.list`.

    3.  Press Enter.

2.  Open the record for the **glide.ais.facets.cross\_tab\_persistence** system property.

3.  Enter the system property value according to the behavior that you want:

    -   To preserve existing facet filters when a new navigation tab is selected, set the system property value to true.
    -   To remove all facet filters when a new navigation tab is selected, set the system property value to false.
    The default property value is true.

4.  Select **Update**.


## Result

All AI Search applications preserve or discard existing facet filters when a new navigation tab is selected.

**Parent Topic:**[Search application configurations](../concept/defining-search-app-cfgs-ais.md)

