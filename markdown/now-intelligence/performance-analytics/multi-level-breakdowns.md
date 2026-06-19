---
title: Data snapshots and multiple breakdowns
description: The Data snapshots feature in Platform Analytics allows for multiple breakdowns while analyzing your indicators \(KPIs\). This architecture uses a change data capture \(CDC\) process, which captures data changes from configurable tables that are optimized for generating scores and time series at run-time.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/performance-analytics/multi-level-breakdowns.html
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Data snapshots and multiple breakdowns

The Data snapshots feature in Platform Analytics allows for multiple breakdowns while analyzing your indicators \(KPIs\). This architecture uses a change data capture \(CDC\) process, which captures data changes from configurable tables that are optimized for generating scores and time series at run-time.

Classic Performance Analytics calculates multiple breakdowns applied to an indicator through a matrix. Mathematically, the number of calculations increases geometrically with the number of breakdowns. Practically, this approach limits you to a maximum of two breakdowns that can be applied to an indicator simultaneously.

The Data snapshots feature does not use breakdown matrixes. Thanks to the use of CDC instead, you can apply multiple breakdown levels. The ability to apply more than two levels of breakdown addresses one of the longstanding pain points of Performance Analytics. This feature deepens your ability to analyze data and broadens the insights you can gain through Performance Analytics.

**Important:**

-   Data snapshots requires that your instance uses the RaptorDB Professional database.
-   Domain-separated instances are not supported.
-   To get Data snapshots and enable multiple levels of breakdown, activate the Data Snapshots \(com.snc.pa.mlb\) plugin. A Performance Analytics subscription and the admin role are required. If you have Australia Patch 3 or later, the plugin is installed automatically on qualified instances.
-   Consider testing the Data snapshots feature in a development environment before activating it on a production instance.
-   To convert classic Performance Analytics indicators to Data snapshots, check whether the indicator supports Data snapshots. Then activate Data snapshots for the indicator if it does. For more information, see [Activate Data snapshots](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/activate-unlimited-breakdowns.md).
-   Only Platform Analytics experience components \(Data visualizations, KPI Details\) support Data snapshots. You cannot show more than two levels of breakdowns in Core UI components like PA widgets and the Analytics Hub.
-   Data snapshots collection jobs may result in increased storage use by Performance Analytics. The jobs copy subsets of the source tables and store every daily change for related records.

The following indicators support the Data snapshots feature:

-   Automated indicators that do not use scripted aggregations \(non-scripted indicators\).
-   Formula indicators with only non-scripted, automated [contributing indicators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/performance-analytics-glossary.md)
-   Formula indicators that contain other formula indicators, provided that ultimately the underlying indicators are non-scripted, automated indicators.

If an indicator does not support Data snapshots, the reasons appear in a warning on the indicator's record page.

**Important:** You cannot apply multiple breakdowns to data that was collected before the feature was activated. You can apply only two levels of breakdown to such data. If you try to apply more levels of breakdown, the result is an empty area for that date range on your data visualization or KPI Details chart.

## Supported and unsupported indicators

Filters apply differently to visualizations of indicators that support and that don’t support multiple breakdowns. In this example, you have a dashboard with two pivot table data visualizations. One pivot table shows the indicator Number of open incidents. This indicator isn’t scripted and thus supports multiple breakdowns. The other pivot table shows the indicator Summed age of open incidents. This indicator is scripted so doesn’t support multiple breakdowns. The dashboard has three filters, each of which filters on a breakdown that is on both indicators. All three filters are being applied. The filters were applied in the following chronological order: first Priority, then Category, then State. The visualization of Number of open incidents shows three filters applied, but the visualization of Summed age of open incidents shows only two.

\[Omitted image "mlb-dashboard.png"\] Alt text: Dashboard with visualizations of an indicator that supports multiple breakdowns and one that does not.

Examining the filters that are applied to the Number of open incidents indicator, you see that all three filters are being applied.

\[Omitted image "mlb-supported.png"\] Alt text: An indicator that supports multiple breakdown with three breakdowns applied.

For the Summed age of open incidents indicator, you see that only the first two filters that were applied to the dashboard apply to this indicator.

\[Omitted image "mlb-not-supported.png"\] Alt text: An indicator that does not support multiple breakdowns, showing that only the first two of three breakdowns applied to the dashboard are applied to the indicator.

## KPI Details for an indicator that uses Data snapshots

This example shows the KPI Details for the indicator Number of open incidents. The indicator supports Data snapshots and multiple breakdowns, as is shown by a badge in the header. Two breakdowns have been set, each with two elements.

\[Omitted image "mlb-kpi-details-2-filters.png"\] Alt text: KPI Details for an indicator that supports multiple breakdowns, with two breakdowns selected.

You can select a third breakdown. However, Data snapshots were only implemented on this instance a few days ago. Once you select a third breakdown, no data before this date is shown. You have a banner warning you to this effect.

\[Omitted image "mlb-kpi-details-3-filters.png"\] Alt text: KPI Details for an indicator that supports multiple breakdowns, with three breakdowns selected but no data from before the implementation of multiple breakdowns.

-   **[Activate Data snapshots](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/activate-unlimited-breakdowns.md)**  
Enable Data snapshots on an instance as a whole and on individual existing indicators \(KPIs\) on the instance. When Data snapshots are enabled, you can apply multiple breakdown levels to an indicator.
-   **[Limitations and requirements for Data snapshots](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/limitations-mlb.md)**  
Several features of indicators and breakdowns are not supported with Data snapshots and multiple breakdowns.
-   **[Data snapshots sources and collection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/tables-unlimited-breakdowns.md)**  
Data snapshots include data sources for indicator score collection and the mapping between indicators and these sources.
-   **[Create a Data snapshots automated indicator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/create-ds-automated-indicator.md)**  
To analyze the performance of a business process that is recorded in a ServiceNow table, use an automated indicator. If you have Data snapshots enabled on your instance, you can create a Data snapshots automated indicator.
-   **[Create a Data snapshots formula indicator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/create-ds-formula-ind.md)**  
Create a formula indicator to calculate a score from two or more Data snapshots indicators.
-   **[Deactivate Data snapshots](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/deactivate-mlb-for-indicator.md)**  
You can turn Data snapshots off or back on for an indicator, provided that indicator supports Data snapshots. An admin can turn the feature off for an instance.
-   **[Data snapshots jobs and tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/ds-jobs-tables.md)**  
Several types of components are installed with activation of the Data snapshots plugin, including tables and scheduled jobs.

**Parent Topic:**[Configure Performance Analytics fundamentals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/c_PAWidgetsAndDashboards.md)

