---
title: Selecting data sources for data visualizations
description: The key purpose of a data visualization is to show data. Thus, one of the most important steps in creating a data visualization is to select the source of the data to show.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Selecting data sources for data visualizations

The key purpose of a data visualization is to show data. Thus, one of the most important steps in creating a data visualization is to select the source of the data to show.

**Note:** This documentation focuses on data visualizations in the Visualization Designer or the inline dashboard editor. The information also applies in the UI Builder, but in the latter environment you have more options, such as custom and JSON data sources.

The data source is one of the first two things you select for a data visualization, either just before or just after the visualization type.

**Warning:** If you select data sources and then change the visualization type to one that does not support those data sources, the unsupported sources are cleared. If you later switch back to a visualization type that supports the original selection, you do not restore your original selection. You then have to reselect sources manually.

-   **[Select a table data source for a data visualization](../task/select-table-data-source.md)**  
Select a table whose records you wish to display. Filter by predefined or custom conditions. Preview a list of records.
-   **[Select an indicator data source for a data visualization](../task/select-indicator-data-source.md)**  
Select a Performance Analytics indicator \(KPI\) to display in your data visualization. You can filter the indicator scores by breakdowns.
-   **[User Experience Analytics data sources for data visualizations](uxa-data-sources.md)**  
You can show metrics related to User Experience Analytics in a data visualization component. The available metrics depend on the visualization type.
-   **[Multiple data sources](../../par-for-workspace/reference/multiple-data-sources.md#)**  
Some visualization types support multiple data sources, while others do not. If your data visualization supports multiple data sources, the data sources must all be of the same type: all tables, all indicators, or all another type.

**Parent Topic:**[Configure data visualizations](configure-data-visualizations.md)

