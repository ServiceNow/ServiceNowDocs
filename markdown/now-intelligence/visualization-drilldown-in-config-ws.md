---
title: Data views for different data sources
description: When the chart interaction for a data visualization is set to Go to data, interacting with a data value on the visualization opens different pages depending on the data source.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Chart interactions in a data visualization, Configure, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Data views for different data sources

When the chart interaction for a data visualization is set to Go to data, interacting with a data value on the visualization opens different pages depending on the data source.

**Note:** For an overview of the data sources that are available for data visualizations, see [Data sources for data visualizations](../../par-for-workspace/reference/data-sources-visualizations.md).

## Table data visualizations

**Go to data** chart interactions from table data visualizations open an associated list of table records. When the system property **com.glide.par.pae.drilldown\_to\_core\_ui** is true, the list is a Core UI list. When it is false, the list is a Platform Analytics list. If you are drilling down from a List, you open a table record either in Core UI or in Platform Analytics, again depending on **com.glide.par.pae.drilldown\_to\_core\_ui**. For more information, see [Data Visualization properties](../../par-for-workspace/reference/data-visualization-properties.md).

**Note:** This system property does not apply to data visualizations in technical dashboards or other UIB pages, which use manually configured event handlers instead of chart interactions.

![Drilling down from a single score visualization of table data to a list of table records.](../../par-for-workspace/image/dv-drilldown-table.gif)

## Indicator visualizations

**Go to data** chart interactions from indicator visualizations open the associated KPI Details page. For more information, see [KPI Details](../../par-for-workspace/concept/kpi-details.md).

![Drilling down from the bar visualization of an indicator to the KPI Details page for that indicator on that date.](../../par-for-workspace/image/dv-drilldown-kpi.gif)

## Usage Insights visualizations

**Go to data** chart interactions from Usage Insights visualizations opens an overview page for the individual application in the visualization. The overview opens on the Data Foundations view that matches the data visualization: event, session, user, or page data. For more information, see [Navigating the Usage Insights application](../../../administer/user-exp-analytics/concept/user-exp-analytics-dashboard.md).

## Health Log Analytics visualizations

**Go to data** chart interactions from Health Log Analytics data visualizations open the log viewer. For more information, see [Health Log Analytics](https://www.servicenow.com/docs/access?context=hla-landing-page&version=australia&pubname=australia-it-operations-management&ft:locale=en-US).

**Note:** You cannot create or edit data visualizations for Health Log Analytics from the Platform Analytics experience, but only from the UI Builder.

## MetricBase visualizations

**Go to data** chart interactions from MetricBase visualizations open the Metrics Explorer. For more information, see [MetricBase](https://www.servicenow.com/docs/access?context=metricbase&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

**Important:** **Go to data** chart interactions for MetricBase require the Metric Explorer for Service Operations \(sn\_sow\_metric\_exp\) plugin.

**Parent Topic:**[Chart interactions in a data visualization](../../par-for-workspace/concept/dv-chart-interactions.md)

