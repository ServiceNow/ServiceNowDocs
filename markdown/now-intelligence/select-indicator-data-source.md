---
title: Select an indicator data source for a data visualization
description: Select a Performance Analytics indicator \(KPI\) to display in your data visualization. You can filter the indicator scores by breakdowns.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/select-indicator-data-source.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Selecting data sources, Configure, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Select an indicator data source for a data visualization

Select a Performance Analytics indicator \(KPI\) to display in your data visualization. You can filter the indicator scores by breakdowns.

## Before you begin

Role required: Anyone with access to data can create a visualization of that data on any dashboard that they can edit. Users with the itil, report\_user, admin, or viz\_creator role can create a visualization in the Visualization Designer. When you create a visualization in the Visualization Designer, it is saved to the Library. For more information on access, see [Report\_view access control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/reporting/report-view-access-control.md) and [Platform Analytics roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/platform-analytics-roles.md).

## About this task

This procedure assumes you're in the process of creating or editing a data visualization and need more information about selecting the data source. It also assumes you're working in either the Visualization Designer or the inline dashboard editor. More options are available in the UI Builder.

\[Omitted image "dv-select-indicator.png"\] Alt text: An Add data source form for an indicator data source, in the process of selecting a breakdown.

## Procedure

1.  Start to create a data visualization, or open an existing visualization for editing.

    For more information, see [Creating data visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/creating-data-visualizations.md).

2.  Choose one of the following:

    -   If you have not yet selected the visualization type, select **Add data source** from the main panel.
    -   If you have selected the visualization type, select **Add data source** from the Data sources section of the configuration panel.
3.  To select an indicator data source, choose one of the following:

    -   Enter the indicator name or the first few letters of the name in the **Search sources** field.
    -   Locate the indicator in the **Suggested** list. Indicators are marked by an indicator icon. \[Omitted image "icon-indicator.png"\] Alt text: Indicator icon
    -   Expand the **Indicators** list and navigate down to the desired indicator.
    When you select an indicator, the breakdown selector and the preview list become available.

4.  Select one or more breakdowns, each with an operator and one or more elements.

    The number of breakdowns and elements may be limited. For more information, see [Indicator breakdowns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/c_CreatingBreakdowns.md).

5.  Review the indicator properties and the score.

6.  Select **Cancel** or **Add this source**.

    You return to the data visualization editor. In the configuration panel, you can add Group by fields and set other data properties, depending on the visualization type.


**Parent Topic:**[Selecting data sources for data visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/selecting-data-sources.md)

**Related topics**  


[Select a table data source for a data visualization]()

[Select a Workflow Data Fabric data source for a data visualization]()

[Usage Insights data sources for data visualizations]()

[Multiple data sources]()

[Creating data visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/creating-data-visualizations.md)

[Indicator management and Performance Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/indicator-data-sources-pa.md)

