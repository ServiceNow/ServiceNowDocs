---
title: Using page properties
description: Filter a page detail page by one or more page properties to see how usage differs across page attributes such as owner, category, or load time.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/usage-insights/using-page-properties.html
release: australia
product: Usage Insights
classification: usage-insights
topic_type: task
last_updated: "2026-08-25"
reading_time_minutes: 1
keywords: [Using page properties]
breadcrumb: [Page properties analytics, Viewing session analytics, Using Usage Insights, Usage Insights, Platform Analytics]
---

# Using page properties

Filter a page detail page by one or more page properties to see how usage differs across page attributes such as owner, category, or load time.

## Before you begin

Role required: none

The properties available for a page depend on the URL parameters and record metadata captured for that page. If a property that you expect is missing, it is not being captured.

## About this task

Filters apply to the entire page detail page. When you apply a page property filter, the metric tiles and every chart in the **Page properties** section are recalculated for the matching subset. For example, filtering by a page owner changes the page view count to reflect only the pages owned by that team.

## Procedure

1.  Navigate to **Usage Insights** &gt; **Data Foundation** &gt; **Sessions**.

    1.  In the application list, select the application that contains the page.

        \[Omitted image "uxa-sessions-page-properties.png"\] Alt text: Page properties

    2.  Set **Date range** to the period that you want to analyze.

    3.  Select **Add Filter**, and then under **Page Properties**, select a property.

    4.  Select **Advanced filters** and create additional conditions.

        \[Omitted image "uxa-sessions-pageprop-adv-filter.png"\] Alt text: Advanced filters within page properties

    5.  Select **Apply** to save.

2.  Select **Data Foundation** &gt; **Pages**.

    1.  In the application list, select the application that contains the page.

    2.  Select the page that you want to analyze.

        The page detail view opens and shows the metric tiles and the **Page properties** section.

    3.  Set **Date range** to the period that you want to analyze.

    4.  Select **Add Filter**, and then under **Page Properties**, select a property.

    5.  Select one or more of the values recorded for that property, and then apply the filter.

        The metric tiles and all property distributions refresh to show only the occurrences that match the selected values.

3.  Repeat the previous two steps to filter by additional properties.

4.  To export the data behind a distribution, select the download icon on that chart.


## Result

The page detail view reports usage for the filtered subset of page occurrences only.

**Parent Topic:**[Page properties analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/usage-insights/page-properties-analytics.md)

