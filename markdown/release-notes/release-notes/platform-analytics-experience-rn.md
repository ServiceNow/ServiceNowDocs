---
title: Platform Analytics experience release notes
description: The ServiceNow Platform Analytics experience provides a single center for consuming the data from all Platform Analytics products. Platform Analytics experience was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 6
---

# Platform Analytics experience release notes

The ServiceNow® Platform Analytics experience provides a single center for consuming the data from all Platform Analytics products. Platform Analytics experience was enhanced and updated in the Yokohama release.

## Platform Analytics experience highlights for the Yokohama release

-   Effortlessly create bold, meaningful data graphics by and refining the results in an AI-powered conversational interface.
-   Speed up the process of turning insights into actions with dynamic new features like suggested performance targets and more powerful data filtering.
-   Share data insights more broadly with enhanced Microsoft PowerPoint support.

See  for more information.

## Important information for upgrading the Platform Analytics experience to Yokohama

If you had previously migrated your analytics assets to Platform Analytics, assets that were in compatibility mode but are newly supported in Yokohama are migrated automatically.

## New in the Yokohama release

-   **Generate data visualizations conversationally**

    Generate Platform Analytics artifacts from conversational interactions using Analytics Generation. Analytics Generation is part of the ServiceNow Otto for Creator application.

-   **Implement filters in groups**

    Create filter groups with shared apply, clear, and reset buttons. Filters in a group appear in their own container. Grouping filters reduces the number of calls and improves performance compared to cascading filters for big data use cases.

-   **Apply multiple levels of breakdown to an indicator**

    Migrate indicators from traditional Performance Analytics architecture to change data capture \(CDC\)-based data snapshots. This new architecture allows for more than two levels of breakdown to apply to an indicator. RaptorDB Professional is required, and not all indicators qualify for migration.

-   **Show the distribution of data in box plot data visualizations**

    Show the median and lower and upper quartiles of numeric data along with outliers by using box plots. You can also compare the distribution of different groups of this data.

-   **Target suggestion cards**

    Be notified of missing target values and review dates for indicators. If you have target Insights active for your dashboard, Target suggestion cards alert you to the missing values and provide an easy way to fix them.


## UI changes

-   **Migration center flow UX improved**
    -   A confirmation modal is displayed when **Start moving** or **Activate** is selected.
    -   Bulk migration can be retriggered after source artifacts are changed.
    -   The creation of new analytics artifacts can be blocked when bulk migration starts.
-   **Percent information added to tooltips**

    Tooltips in geomap, vertical and horizontal bar, heatmap, and bubble visualizations now include percentages when applicable.


## Changed in this release

-   **Migrate more features to Platform Analytics from the Core UI**

    Migration scripts are improved to support more features. All migration script improvements are applied automatically on upgrade to content that was previously migrated in compatibility mode.

    -   Data table configurations are migrated from the Core UI to Platform Analytics data visualizations.
    -   Dashboard groups are migrated to dashboard categories.
    -   Pareto charts are migrated.
    -   List component border changes are migrated.
    -   Follow/unfollow filter settings are migrated for Lists.
-   **Use more Core UI features in Platform Analytics**

    Several data visualizations have been enhanced to match the capacities in Core UI reports and widgets. The migration script supports these enhancements. Each of these enhancements has an entry in the release notes with links to the product documentation.

    -   Use the new Box plot data visualization.
    -   Configure **Follow filters** per metric on bar or time series visualizations with multiple metrics.
    -   Sort values by name, report range, and element order on time series visualizations of table data.
    -   Choose an aggregate or separate view of breakdown elements on time series visualizations of indicator data.
    -   Select dates from business calendars on time series visualizations.
-   **Trend by Business calendars in time series data visualizations**

    Business calendars are a **Trend by** option for table data sources on time series visualizations. \(Core UI feature gap\)

-   **Use a Fiscal calendar in date filters**

    If your instance has Fiscal calendars installed, you can choose relative data ranges from that calendar.

-   **Export dashboards and data visualizations to PDF and PPT**

    Export dashboards and data visualizations to PDF or Microsoft PowerPoint files at will or in scheduled emails.

-   **Show breakdown elements separately on time series visualizations of indicators**

    Show multiple elements in the chart separately rather than as an aggregate value by turning on the **Show filter as separate series** option. \(Core UI feature gap\)

-   **Lock editing on dashboards**

    Ensure that only one person can have a dashboard open for editing at one time through the edit lock on dashboards. If you are locked out of editing a dashboard, you see who the current editor is.

-   ****

    Navigate either to the record of the indicator you are exploring or its scoresheet through KPI Details. Appropriate roles are required.

-   **Export records that underlie an indicator from KPI Details**

    With **Show records** activated in KPI Details, you can export the list of records in one of several formats, either as a local download or as an email attachment.

-   **Hide axes for bar visualizations**

    Control the display of axes on bar charts. On horizontal bar charts, you can hide the y-axis. On vertical bar charts, you can hide the x-axis.

-   **Cache indicator scorecard data**

    Indicator scorecards now support data caching.

-   **Group by elements more efficiently in data visualizations**

    Specify the maximum number of elements in a Group By you want to retrieve through the **Max number of groups** option. Previously, all elements from the database were retrieved and then sorted.

-   **Prefetch dashboard layout**

    If you have a dashboard component on a page in your own workspace, improve performance by using a preset to configure a data broker that pre-fetches static JavaScript, such as layout.

-   **Call multiple visualizations together**

    For a technical dashboard, if you have multiple data visualizations of the same type calling the same data source, configure a data resource to make a single call for all of them.

-   **Improvements to time-series visualizations**
    -   Simplify identifying specific values on line, spline, area, or step charts through the **Show markers** option, which displays a symbol at each data point.
    -   Sort by name, report range, group bucket, and element order. \(Core UI feature gap\)
-   **Improvements for visualizations that show multiple metrics**
    -   In time series visualizations, provide viewers an alternative group by, where the viewer chooses the group-by value at runtime, for up to 3 data sources. \(Core UI feature gap\)
    -   Set whether individual metrics follow filter components on the page or dashboard in both bar and time series visualizations. \(Core UI feature gap\)

## Activation information

The Platform Analytics experience is active by default. However, some additional steps might be required.

-   To use indicator data sources, you might need to activate Performance Analytics.
-   To use Process Mining with the Platform Analytics experience, you might need to activate Process Mining.

## Accessibility information

Dashboard overview and Filter components now support Reflow at 400% zoom.

## Related ServiceNow applications and features

-   ****

    Several Now Assist Generative AI tools are available for generating and working with Platform Analytics objects through iterative questions and answers.

-   **Performance Analytics \(Indicator data sources\)**

    Performance Analytics is an in-platform process optimization solution, providing the indicator data sources that the Platform Analytics experience exposes graphically. It enables  organizations to set, track, and analyze progress toward goals. Performance Analytics was enhanced  and updated in the Yokohama release.

-   ****

    This application provides dashboard views for monitoring usage analytics of your Next Experience web applications as well as Virtual Agent, ServiceNow mobile, and Service Portal applications. User Experience Analytics provides a data source which data visualizations can display.

-   ****

    Process Mining helps analysts and process owners quickly analyze and optimize their business processes. Use Process Mining with Platform Analytics insights to optimize your indicator data sources.


**Parent Topic:**[Platform Analytics release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/analytics-intel-report-rn-landing.md)

