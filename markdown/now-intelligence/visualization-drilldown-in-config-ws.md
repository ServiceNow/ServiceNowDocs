---
title: Data views for different data sources
description: When the chart interaction for a data visualization is set to Go to data, interacting with a data value on the chart opens different pages depending on the data source.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Chart interactions in a data visualization, Platform Analytics]
---

# Data views for different data sources

When the chart interaction for a data visualization is set to Go to data, interacting with a data value on the chart opens different pages depending on the data source.

**Note:** For an overview of the data sources that are available for data visualizations, see [Data sources for data visualizations](../../par-for-workspace/reference/data-sources-visualizations.md).

## Table data visualizations

**Go to data** chart interactions from table data visualizations open the associated Core UI list of table records.

**Note:** This chart interaction can only open the default ServiceNow AI Platform list view of table records, which is currently in the Core UI. For technical reasons, it cannot open a Simple List or other Platform Analytics component. This restriction does not apply to dashboards in configurable workspaces and experiences, which use manually configured event handlers instead of chart interactions.

![Drilling down from a single score visualization of table data to a list of table records.](../../par-for-workspace/image/dv-drilldown-table.gif)

## Indicator visualizations

**Go to data** chart interactions from indicator visualizations open the associated KPI Details page. For more information, see [KPI Details](../../par-for-workspace/concept/kpi-details.md).

![Drilling down from the bar visualization of an indicator to the KPI Details page for that indicator on that date.](../../par-for-workspace/image/dv-drilldown-kpi.gif)

## Health Log Analytics

**Go to data** chart interactions from Health Log Analytics data visualizations open the log viewer. For more information, see [Health Log Analytics](https://www.servicenow.com/docs/access?context=hla-landing-page&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US).

**Note:** You cannot create or edit data visualizations for Health Log Analytics from the Platform Analytics experience, but only from the UI Builder.

## MetricBase

**Go to data** chart interactions from MetricBase visualizations open the Metrics Explorer. For more information, see [MetricBase](https://www.servicenow.com/docs/access?context=metricbase&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

**Important:** **Go to data** chart interactions for MetricBase require the Metric Explorer for Service Operations \(sn\_sow\_metric\_exp\) plugin.

## User Experience Analytics

User Experience Analytics does not support **Go to data** chart interactions.

**Parent Topic:**[Chart interactions in a data visualization](../../par-for-workspace/concept/dv-chart-interactions.md)

