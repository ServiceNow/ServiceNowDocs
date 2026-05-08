---
title: Data sources for data visualizations
description: Each workspace data visualization references a specific data source.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [What data can I base my visualization on]
breadcrumb: [Reference, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Data sources for data visualizations

Each workspace data visualization references a specific data source.

<table id="table_qb5_pks_s5b"><thead><tr><th>

Data source

</th><th>

Available in

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Base system

</td><td>

A Table data source is a collection of database records that together constitute the current state of your data. The rows of the table correspond to records and the columns correspond to fields. You often choose both table and field, or you group data by fields, when you configure a data visualization. Configured report sources appear in the **Predefined conditions** list when you choose to filter table data.

</td></tr><tr><td>

Indicator

</td><td>

Base system

</td><td>

An indicator, also called a key performance indicator \(KPI\), is a record of the changes to your table data over a period of time. You use indicators to determine trends and forecast the future. Indicators apply an aggregation and conditions to the data. For example, the indicator Number of open incidents applies the Count aggregation to the Incident table, resulting in a number of incidents. It also applies the conditions that the State of the incidents must not be Closed or Canceled, and the Active field must be True.Indicators often have breakdowns applied. A breakdown is a qualitative property for filtering the indicator scores. For example, for incident data, the priority, category, and assignment group for the incident are all commonly applied breakdowns.

When you select an indicator data source, you see a preview of the visualization, and a list of the indicator's properties including its source type, indicator type, calculation, and available breakdowns, if configured.

**Note:** Many data visualizations support multiple data sources. However, you cannot mix Data snapshots indicators and regular indicators. If your first data source is a regular indicator \(automated, formula, or manual\), then only regular indicators are available for your additional data source. If your first data source is an automated or formula Data snapshots indicator, only Data snapshots are available for additional data sources.

For more information, see [Performance Analytics indicators](../../performance-analytics/concept/c_Indicators.md).

</td></tr><tr><td>

Usage Insights

</td><td>

Activated by default. However, to include Usage Insights data sources in your visualizations, you need the Usage Insights in PAR Integration application from the ServiceNow® Store.

</td><td>

The ServiceNow® Usage Insights application provides dashboard views for monitoring usage analytics of your web applications as well as Virtual Agent, ServiceNow mobile, and Service Portal applications. Visualize metrics and interactions to better understand the user experience, and create more intuitive journeys for your users.For more general information about Usage Insights, see [Usage Insights](../../../administer/user-exp-analytics/content-framework/landing-page/user-exp-analytics-landing.md). For more information specific to data visualizations, see [Usage Insights data sources for data visualizations](../../performance-analytics/concept/uxa-data-sources.md).

</td></tr><tr><td>

MetricBase

</td><td>

Requires a separate subscription and must be activated by ServiceNow personnel.

</td><td>

The MetricBase application stores time-series data, which is data that is sampled at regular intervals. You can graph the stored data or use it with triggers to execute Flow Designer flows. MetricBase helps developers working with IoT-based applications that monitor or act on large amounts of machine-generated data. For more information, see MetricBase.

</td></tr><tr><td>

Workflow Data Fabric

</td><td>

Base system

</td><td>

Zero Copy Connector Hub provides a view where you can browse data sources, establish connections, and create data fabric tables that provide access to data from external sources. Workflow Data Fabric tables are found in the same list as other tables when you create a visualization. For more information, see Workflow Data Fabric Home.

</td></tr><tr><td>

Health Log Analytics

</td><td>

Requires a separate subscription and must be activated by ServiceNow personnel.

</td><td>

The Health Log Analytics application helps prevent IT issues before your users are affected. It helps you identify the root cause of an issue by enabling you to triage related logs and analyze the raw data. For more information, see Health Log Analytics.

 **Note:** You can create and edit data visualizations for Health Log Analytics only in the UI Builder, not in the Platform Analytics Visualization Designer or in dashboards.

</td></tr></tbody>
</table>**Parent Topic:**[Data visualization reference](data-visualization-reference.md)

