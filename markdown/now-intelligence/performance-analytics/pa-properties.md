---
title: Performance Analytics properties
description: These system properties control the behavior of Performance Analytics.
locale: en-US
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Performance Analytics reference, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Performance Analytics properties

These system properties control the behavior of Performance Analytics.

To configure properties, navigate to **Performance Analytics** &gt; **System** &gt; **Properties** or to `sys_properties_list.do`.

**Note:** Only the properties on the Performance Analytics Properties page are described here. The `sys_properties.list` page contains other properties that affect Performance Analytics. For more information, see [Available system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

-   **[Collection cleanup Performance Analytics properties](pa-collection-cleanup-props.md)**  
Several properties determine how long Performance Analytics scores and snapshots are maintained before the scheduled cleanup job deletes them.
-   **[Fiscal year Performance Analytics properties](pa-fiscal-year-props.md)**  
These properties set the year in Performance Analytics to match your company fiscal year.
-   **[Default color scheme Performance Analytics properties](pa-default-color-scheme-props.md)**  
These properties set the default colors for the chart overall and for indicator targets.
-   **[Breakdown and indicator Performance Analytics properties](pa-limit-setting-props.md)**  
These properties set limits on breakdown elements and indicators, mostly in the context of visualizations.
-   **[Chart properties for Performance Analytics](pa-chart-props.md)**  
A chart refers here to a graphical component of a Performance Analytics widget or the Analytics Hub. These properties apply only to the Core UI, not visualizations in configurable workspaces.
-   **[Data collector Performance Analytics properties](pa-dc-props.md)**  
Data collector properties enable you to configure various limits for Performance Analytics data collection. The properties are configured to safeguard the data collection process. The default values are appropriate for most environments.
-   **[Collected scores and com.snc.pa.breakdown\_element\_cutoff](../concept/collected-element-display-cutoff.md)**  
The elements of a breakdown that the Analytics Hub and KPI Details display for a selected date depend on the number of elements and the value of **com.snc.pa.breakdown\_element\_cutoff**.

**Parent Topic:**[Performance Analytics reference](../concept/performance-analytics-reference.md)

