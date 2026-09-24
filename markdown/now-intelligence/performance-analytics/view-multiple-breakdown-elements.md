---
title: Viewing multiple breakdown elements
description: You can view multiple elements of a breakdown either separately or as an aggregate. It depends on the indicator configuration and how the indicator is visualized.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/performance-analytics/view-multiple-breakdown-elements.html
release: brazil
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2026-09-09"
reading_time_minutes: 3
keywords: [indicator, breakdown, aggregate view, separated view]
breadcrumb: [Indicator breakdowns, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Viewing multiple breakdown elements

You can view multiple elements of a breakdown either separately or as an aggregate. It depends on the indicator configuration and how the indicator is visualized.

## Indicators that support aggregate views of multiple breakdown elements

All indicators support a separated view of multiple breakdown elements. The following indicators support an aggregate view of multiple elements:

-   Automated indicators that aggregate data as a Count, Sum, Minimum, or Maximum value

    **Note:** The word "aggregate" is used for two different things here: the aggregate view of multiple indicator scores, and the data aggregation that is set on an indicator.

-   Manual indicators
-   External indicators that do not use `SQL AVG()` or `SQL COUNT(DISTINCT...)` in their SQL statement
-   Formula indicators that have aggregate element views enabled on their indicator records. For more information, see the entry on the **Allow aggregation of multiple breakdown element scores** field on the Other tab in [Create a formula indicator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/t_CreateAFormulaIndicator.md).

## Aggregate and separate view of multiple breakdown elements on Platform Analytics dashboards

In Platform Analytics, three different routes to showing multiple element values lead to an aggregate or a separate view.

-   **Show each breakdown element separately**

    Select a breakdown in the **Group by** section of a data visualization configuration panel. Each element is shown separately. You can restrict the elements shown to a number of the largest values.

    \[Omitted image "separate-elements.png"\] Alt text: Time series of an indicator grouped by Priority, no filter on dashboard.

-   **Show the aggregate value of selected breakdown elements**

    On a dashboard with a data visualization of the indicator, add a multi-select filter with the desired breakdown as the filter source. Do not select a breakdown in the data visualization's configuration panel. Also, the indicator in the visualization must support an aggregate view of multiple elements. If these conditions are met, the data visualization shows the aggregate score of the elements selected in the filter.

    \[Omitted image "aggregated-elements.png"\] Alt text: Time series of an indicator filtered on the Critical and Planning elements of the Priority breakdown, showing an aggregated value.

-   **Show a separated view of dynamically selected breakdown elements**

    On a dashboard with a data visualization of the indicator, add a multi-select filter with the desired breakdown as the filter source. In the data visualization configuration panel, select that breakdown. The visualization shows a separated view of the elements selected on the filter. The visualization and filter combination also works like this when the indicator does not support an aggregate view of multiple elements. In the latter case, it doesn't matter if the breakdown is specified on the data visualization configuration panel.

    \[Omitted image "filtered-separate-elements.png"\] Alt text: Time series of an indicator with a breakdown specified in the configuration and only two of those breakdown elements selected in a dashboard filter.


## Aggregate and separate view of multiple breakdown elements on Core UI dashboards

The use case in Core UI is more complex than in Platform Analytics. For more information, see [Showing multiple elements separately or aggregated in Core UI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/multi-element-select-indicator-views.md).

**Parent Topic:**[Indicator breakdowns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/c_CreatingBreakdowns.md)

**Related topics**  


[Indicator data options for time series data visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/config-dv-time-series-ind-data.md)

[Configure a Single/Multiple select or cascading filter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/create-select-filter-workspace.md)

