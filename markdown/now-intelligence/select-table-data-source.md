---
title: Select a table data source for a data visualization
description: Select a table whose records you want to display. Filter by predefined or custom conditions. Preview a list of records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/select-table-data-source.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Selecting data sources, Configure, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Select a table data source for a data visualization

Select a table whose records you want to display. Filter by predefined or custom conditions. Preview a list of records.

## Before you begin

Role required: Anyone with access to data can create a visualization of that data on any dashboard that they can edit. Users with the itil, report\_user, admin, or viz\_creator role can create a visualization in the Visualization Designer. When you create a visualization in the Visualization Designer, it is saved to the Library. For more information on access, see [Report\_view access control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/reporting/report-view-access-control.md) and [Platform Analytics roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/platform-analytics-roles.md).

## About this task

This procedure assumes you're in the process of creating or editing a data visualization and need more information about selecting the data source. It also assumes you're working in either the Visualization Designer or the inline dashboard editor. More options are available in the UI Builder.

\[Omitted image "dv-table-data-source-ex.png"\] Alt text: A completed Add data source form for a table data source, with a predefined filter selected.

## Procedure

1.  Start to create a data visualization, or open an existing visualization for editing.

    For more information, see [Creating data visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/creating-data-visualizations.md).

2.  Choose one of the following:

    -   If you have not yet selected the visualization type, select **Add data source** from the main panel.
    -   If you have selected the visualization type, select **Add data source** from the Data sources section of the configuration panel.
3.  To select a table data source, choose one of the following:

    -   Enter the table name or the first few letters of the name in the **Search sources** field.
    -   Locate the table in the **Suggested** list. Tables are indicated by a table icon. \[Omitted image "icon-tables.png"\] Alt text: Tables icon
    -   Expand the **Tables** list and navigate down to the desired table.
    When you select a table, the filters and preview list become available.

4.  Select a predefined filter.

    Predefined filters are defined on the Report Sources \[sys\_report\_source\] table. For more information, see [Report sources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/reporting/c_ReportSources.md).

5.  Select **+Add custom conditions** and build a filter in the ServiceNow AI Platform Condition builder.

    For more information, see .

6.  With **+Add custom conditions** open, add a relationship with a field in another table by expanding **Related list condition**.

    For information about building a related list condition, see .

7.  Run your filter query or save it as a predefined condition on the Report Sources table.

8.  Examine the filtered list of records in the Preview records list.

    You can reorder, sort, or resize the list in the column header row. You can choose which columns to show or restore the original widths in the list actions \[Omitted image "icon-cogwheel-ac.png"\] Alt text: Cogwheel icon.

9.  Select **Cancel** or **Add this source**.

    You return to the data visualization editor. In the configuration panel, you can add Group by fields and set other data properties, depending on the visualization type.


**Parent Topic:**[Selecting data sources for data visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/selecting-data-sources.md)

**Related topics**  


[Select an indicator data source for a data visualization]()

[Select a Workflow Data Fabric data source for a data visualization]()

[Usage Insights data sources for data visualizations]()

[Multiple data sources]()

