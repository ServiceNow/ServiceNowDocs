---
title: Data sources for data visualizations
description: Each workspace data visualization references a specific data source.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/now-intelligence/data-sources-visualizations.html
release: zurich
topic_type: reference
last_updated: "2026-10-01"
reading_time_minutes: 5
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

When you select an indicator data source, you see a preview of the visualization, and a list of the indicator's properties. The list of properties includes its source type, indicator type, calculation, and available breakdowns, if configured.

**Note:** Many data visualizations support multiple data sources. However, you cannot mix Data snapshots indicators and regular indicators. If your first data source is a regular indicator \(automated, formula, or manual\), then only regular indicators are available for your additional data source. If your first data source is an automated or formula Data snapshots indicator, only Data snapshots are available for additional data sources.

For more information, see [Performance Analytics indicators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/c_Indicators.md).

</td></tr><tr><td>

Usage Insights

</td><td>

Activated by default. However, to include Usage Insights data sources in your visualizations, you need the Usage Insights in PAR Integration application from the ServiceNow® Store.

</td><td>

The ServiceNow® Usage Insights application provides dashboard views for monitoring usage analytics of your web applications, as well as Virtual Agent, ServiceNow mobile, and Service Portal applications. Visualize metrics and interactions to better understand the user experience, and create more intuitive journeys for your users.For more general information about Usage Insights, see [Usage Insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/usage-insights/user-exp-analytics-landing.md). For more information specific to data visualizations, see [User Experience Analytics data sources for data visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/uxa-data-sources.md).

</td></tr><tr><td>

MetricBase

</td><td>

Requires a separate subscription and must be activated by ServiceNow personnel.

</td><td>

The MetricBase application stores time-series data, which is data that is sampled at regular intervals. You can graph the stored data or use it with triggers to execute Flow Designer flows. MetricBase helps developers working with IoT-based applications that monitor or act on large amounts of machine-generated data. For more information, see [MetricBase](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/metricbase.md).

</td></tr><tr><td>

Workflow Data Fabric

</td><td>

Base system

</td><td>

Workflow Data Fabric Hub provides a view where you can browse data sources, establish connections, and create data fabric tables that provide access to data from external sources. Workflow Data Fabric tables are found in the same list as other tables when you create a visualization. Data from Workflow Data Fabric tables does not load automatically when you select it as a data source. Select **Run** to load the data in the preview. Select **Apply** to add the table as the data source.

For more information, see .

</td></tr><tr><td>

Health Log Analytics

</td><td>

Requires a separate subscription and must be activated by ServiceNow personnel.

</td><td>

The Health Log Analytics application helps prevent IT issues before your users are affected. It helps you identify the root cause of an issue by enabling you to triage related logs and analyze the raw data. For more information, see [Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/hla-landing-page.md).

 **Note:** You can create and edit data visualizations for Health Log Analytics only in the UI Builder, not in the Platform Analytics Visualization Designer or in dashboards.

</td></tr></tbody>
</table>-   **Table**

    Available in the base system. When you select a table, you can filter it by custom or preconfigured conditions. Custom conditions can include questions or Service Catalog variables.

    Configured report sources appear in the **Predefined conditions** list. For more information, see [Report sources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/reporting/c_ReportSources.md).

    To help you create a custom filter, there is a preview list of records that would be included in the visualization. You can change which fields are shown as columns and the width of columns in the list actions.

    \[Omitted image "dv-preview-edit-cols.png"\] Alt text: Preview record list for table source data visualization with list actions shown.

-   **Indicator**

    Available in the base system.You can filter the indicator scores by breakdowns and elements. Automated indicators can be configured with selected breakdowns. Formula indicators inherit their breakdowns from the parent indicators. Data snapshots indicator breakdowns are configured in the indicator. In both cases, only those breakdowns are available when you configure a visualization based on those indicators.

    **Note:** Benchmark indicators aren't supported.

    \[Omitted image "dv-ind-source-con-filter.png"\] Alt text: Conditional filter for indicator data source on data visualization.

    **Note:**

    You might have a multiple select \(is one of\) or dynamic \(is \(dynamic\)\) operator on the breakdown element filter. These operators require the indicator and breakdown to support them. For more information about the configurations that support these operators, see ["Is one of" and "Is \(Dynamic\)" operators on breakdown conditions in data visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/condition-operators-ind-bkdowns.md).

    Indicator types include Automated, Formula, and Manual indicators and Automated and Formula Data Snapshots. The Indicator Preview shows an example of the visualization and a list of the indicator's properties.

    \[Omitted image "image.dv-indicator-source-preview"\] Alt text: Indicator preview example with visualization example and list of properties including source type, indicator source, indicator type, additional conditions and available breakdowns.

-   **Usage Insights**

    Available with the User Experience PAR Integration application, to users with a required role. Choose one of up to three KPIs included with this application, depending on the visualization type. For more information, see [User Experience Analytics data sources for data visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/uxa-data-sources.md).


**Parent Topic:**[Data visualization reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/data-visualization-reference.md)

