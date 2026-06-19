---
title: Select a group-by value in a data visualization as a viewer
description: A viewer of a data visualization can select the value for grouping the data in the visualization.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/now-intelligence/select-group-runtime.html
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [View, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Select a group-by value in a data visualization as a viewer

A viewer of a data visualization can select the value for grouping the data in the visualization.

If a data visualization is configured with alternative group-by values, a viewer can pick which value to apply. No editing rights are required. On a visualization that shows Service Catalog data, the options can include Service Catalog variables, as described in [Service catalog variables in data visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/dv-rep-sc-variables.md).

**Note:** Instructions for configuring alternative group by are included in the data options topics for the relevant data visualizations.

Toggle the visibility of the selector for group-by values by selecting **Change group by** in the data visualization's More actions menu. An editor of the visualization can set whether the selector is visible or hidden by default.

\[Omitted image "change-group-by.png"\] Alt text: The toggle for showing or hiding the group-by value selector in the data visualization More options menu.

All data visualizations that support group by also let viewers select the group-by value, except for pivot tables. For all such data visualizations except bar visualizations, you have only a single group-by value to select.

\[Omitted image "group-by-ts.png"\] Alt text: Group-by selector for time series visualizations

If you are viewing a bar visualization, you can choose a stack-by value as well as a group-by value.

\[Omitted image "group-by-bar.png"\] Alt text: Bar visualization group by selector for both group by and stack by.

In a time series visualization that shows more than one metric, you might have the option of selecting a group-by for each metric. You are given only valid choices.

\[Omitted image "dv-select-group-by-1.png"\] Alt text: Selecting a group-by for the first of 2 metrics in a time series visualization. \[Omitted image "dv-select-group-by-2.png"\] Alt text: Selecting the second of 2 metrics in a time series visualization.

**Parent Topic:**[View data visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/view-data-visualizations.md)

