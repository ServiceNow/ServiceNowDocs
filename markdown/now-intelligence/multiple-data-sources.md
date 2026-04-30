---
title: Multiple data sources
description: Some visualization types support multiple data sources, while others do not. If your data visualization supports multiple data sources, the data sources must all be of the same type: all tables, all indicators, or all another type.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2025-03-19"
reading_time_minutes: 1
breadcrumb: [Data sources for data visualizations, Data visualizations in Platform Analytics, Platform Analytics]
---

# Multiple data sources

Some visualization types support multiple data sources, while others do not. If your data visualization supports multiple data sources, the data sources must all be of the same type: all tables, all indicators, or all another type.

|Visualization type|Multiple data source support|
|------------------|----------------------------|
|All time series \(line, column, spline, area, and others\)|Supported|
|All scores \(single score, dial, gauge\)|Not supported|
|All bars \(horizontal, vertical, Pareto\)|Supported|
|Heatmap|Not supported|
|Pies and donuts|Not supported|
|Pivot table|Supported|
|Bubble|Supported|
|Boxplot|Not supported|
|Calendar report|Not supported|
|Geomap|Not supported|
|Indicator scorecard|Not supported|
|List - simple|Not supported|

**Warning:** If you select multiple data sources for a visualization and then change the visualization type to one that does not support multiple data sources, you keep only the first data source. Switching back to a visualization type that supports multiple data sources does not restore the previously selected data sources.

**Parent Topic:**[Data sources for data visualizations](data-sources-visualizations.md)

**Related topics**  


[Indicator management and Performance Analytics](../concept/indicator-data-sources-pa.md)

[User Experience Analytics data sources for visualizations](../../performance-analytics/concept/uxa-data-sources.md)

