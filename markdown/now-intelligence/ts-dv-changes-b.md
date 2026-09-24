---
title: Time series visualization changes
description: In the Brazil release, several time series visualizations have minor changes in their presentations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/ts-dv-changes-b.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Time series visualizations, Create, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Time series visualization changes

In the Brazil release, several time series visualizations have minor changes in their presentations.

The Data Visualizations bundle now renders charts using an updated charting engine. This change is behind the scenes — your existing charts, configurations, and data sources continue to work as before, with no action needed.

## Period over period

Time Series charts now support Period over Period comparison. This overlays a prior period against the current one so you can spot trends and shifts at a glance. See the **Compare Period over Period** setting under Date ranges in the configuration panel.

## Legend pagination

When a legend runs longer than two rows, it now paginates so the chart area stays clean and readable instead of being crowded out by legend entries. Under the previous charting engine, legends longer than two rolls scrolled.

## Series highlighting

When you hover over an item in the legend of a time series visualization, the corresponding segments of the visualization are highlighted. The rest of the segments dimmed.

## Normalized column variation

Time Series column charts now offer a Normalized display option, joining the existing Stacked and Side-by-side variations. Normalized scales each column to 100%, so you can compare the proportional contribution of each series across time periods.

## Axis labels

Axis labels are angled in HC and may take up more space, so the size of the visualized data itself might be different.

## Line visualizations

When you have multiple data sources in a single visualization, changes in number formatting for one, change the format for the others and for the Y axis.

## Scatter visualizations

The symbols associated with each element are slightly different in the new charting engine.

\[Omitted image "dv-scatter-hc.png"\] Alt text: List of scatter visualization elements with their symbols in the Brazil instance

\[Omitted image "dv-scatter-xen.png"\] Alt text: List of scatter visualization elements with their symbols in pre-Brazil instances

**Parent Topic:**[Create time series data visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/create-dv-time-series-ac.md)

