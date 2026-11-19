---
title: Data Visualization component setup
description: The Data visualization component contains various charts that let users visualize and compare system data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/data-visualization-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Data Visualization component setup

The Data visualization component contains various charts that let users visualize and compare system data.

## Before you begin

This task assumes you have placed the Data visualization component on the stage and are ready to configure the component properties and events. For instructions on accessing and using the UI Builder toolbox, see [Customize UI pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md). For instructions on overriding styles using the Styles pane, see [Change the default appearance of components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-styling-to-component.md).

Role required: For UI Builder: admin or ui\_builder\_admin. For Visualization Designer in runtime: any internal role

## Procedure

1.  Define a label for your Data visualization component that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "data-vis-content-tree.png"\] Alt text: Data Visualization component with label displayed in the content tree

2.  Select the Data visualization component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the data visualization label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.

3.  Select the **Data Visualization Type**.

    The available data sources and properties change depending on the selected chart type. To see information on the properties and events for specific visualization types, see these components:

    -   [Single score](https://developer.servicenow.com/dev.do#!/reference/now-experience/washingtondc/shared-components/now-vis-score-wrapper/overview)
    -   [Bubble chart](https://developer.servicenow.com/dev.do#!/reference/next-experience/washingtondc/now-components/now-vis-bubble-wrapper/overview)
    -   [Dial](https://developer.servicenow.com/dev.do#!/reference/now-experience/washingtondc/shared-components/now-vis-dial-wrapper/overview)
    -   [Gauge](https://developer.servicenow.com/dev.do#!/reference/next-experience/washingtondc/now-components/now-vis-gauge-wrapper/overview)
    -   [Geomap](https://developer.servicenow.com/dev.do#!/reference/next-experience/washingtondc/now-components/now-vis-geomap-wrapper/overview)
    -   [Heatmap](https://developer.servicenow.com/dev.do#!/reference/next-experience/washingtondc/now-components/now-vis-heatmap-wrapper/overview)
    -   [Horizontal or Vertical Bar or Pareto](https://developer.servicenow.com/dev.do#!/reference/now-experience/washingtondc/shared-components/now-vis-bar-wrapper/overview)
    -   [Pie, Donut, or Semi donut](https://developer.servicenow.com/dev.do#!/reference/now-experience/washingtondc/shared-components/now-vis-pie-wrapper/overview)
    -   [Pivot Table](https://developer.servicenow.com/dev.do#!/reference/now-experience/washingtondc/now-components/sn-multipivot/overview)
    -   [Time series \(Area, Column, Line, Scatter, Spline, Step\)](https://developer.servicenow.com/dev.do#!/reference/now-experience/washingtondc/shared-components/now-vis-timeseries-wrapper/overview)
4.  Click **Add data source** to select a table, indicator, MetricBase, Health Log Analytics, or Usage Insights data source to base a visualization on.

    MetricBase is only available with time series visualizations. See the sections on each visualization type for instructions about how to add data sources manually or through data binding.

5.  Add filters to the data as needed.

    When you select a Health Log Analytics data source, you must select a component \(such as a host-application pair\) and run the analysis.

6.  Click **Add this source** to add your selected data source.

7.  Enter static input in the input fields by typing in the content or selecting it from a drop-down list.

    See the sections on each visualization type to see configurations options available based on the selected data source.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

