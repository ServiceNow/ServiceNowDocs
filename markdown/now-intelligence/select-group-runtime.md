---
title: Select a group-by value in a data visualization as a viewer
description: A viewer of a data visualization can select the value for grouping the data in the visualization.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Platform Analytics]
---

# Select a group-by value in a data visualization as a viewer

A viewer of a data visualization can select the value for grouping the data in the visualization.

If a data visualization is configured with alternative group-by values, a viewer can pick which value to apply. No editing rights are required. On a visualization that shows Service Catalog data, the options can include Service Catalog variables, as described in [Service catalog variables in data visualizations](../../reporting/concept/dv-rep-sc-variables.md#).

**Note:** Instructions for configuring alternative group by are included in the data options topics for the relevant data visualizations.

Toggle the visibility of the selector for group-by values by selecting **Change group by** in the data visualization's More actions menu. An editor of the visualization can set whether the selector is visible or hidden by default.

![The toggle for showing or hiding the group-by value selector in the data visualization More options menu.](../image/change-group-by.png)

All data visualizations that support group by also let viewers select the group-by value, except for pivot tables. For all such data visualizations except bar visualizations, you have only a single group-by value to select.

![Group-by selector for time series visualizations](../image/group-by-ts.png)

Bar visualizations also let you choose a stack-by value.

![Bar visualization group by selector for both group by and stack by.](../image/group-by-bar.png)

**Parent Topic:**[Platform Analytics](c_performanceAnalyticsAndReporting.md)

