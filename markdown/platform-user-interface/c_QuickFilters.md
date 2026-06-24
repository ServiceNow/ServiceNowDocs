---
title: Quick filters
description: To quickly filter a list using a value in a field, right-click in the field and select Show Matching or Filter Out. For date fields, choose from Show Before, Show After, and Filter Out.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-user-interface/c\_QuickFilters.html
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Filters and breadcrumbs, Lists in the classic environment, Working in the classic environment, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Quick filters

To quickly filter a list using a value in a field, right-click in the field and select **Show Matching** or **Filter Out**. For date fields, choose from **Show Before**, **Show After**, and **Filter Out**.

These functions add a condition to the right in the breadcrumb of the current filter.

\[Omitted image "QuickFilterListv3.png"\] Alt text: Quick filter

In this example, right-clicking **In Progress** and selecting **Show Matching** adds the condition **State = In Progress** as the most specific condition of the filter. By contrast, right-clicking **In Progress** and selecting **Filter Out** adds the condition **State != In Progress** as the most specific condition of the filter.

For date and date-time fields, you can also use **Show After** or **Show Before** to define a time-based filter.

Using the quick filter method to filter out a particular value builds the following conditions: \[field\] \[is not\] \[value\] or \[field\] \[is\] \[empty\]. Records that contain empty or null values still display in the filtered list. If you manually create a filter, it does not automatically include the OR condition \[field\] \[is\] \[empty\], so records that have an empty or null value do not display in the filtered list.

**Parent Topic:**[Filters and breadcrumbs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/c_UsingFiltersAndBreadcrumbs.md)

