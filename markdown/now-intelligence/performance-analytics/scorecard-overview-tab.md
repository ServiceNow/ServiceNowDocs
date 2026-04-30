---
title: View scores and statistics
description: The Analytics Hub Overview tab shows the score for a time period, statistics, and a time series. You can set the time period for the statistics and time series. You can also filter scores by breakdown and element.The top of the View tab summarizes information about the indicator being viewed.You can select real-time scores to view instead of the last score.On the Analytics Hub, you can aggregate changes in indicators into discrete time intervals.You can set the time period of scores that the Analytics Hub describes.In the View tab of the Analytics Hub, you can set various statistics to apply to the indicator score.On the Analytics Hub, you have several options for viewing breakdowns and breakdown elements.If you click a value on a chart in a widget on a dashboard, you open the Analytics Hub on that indicator. If you are on a breakdown dashboard and have multiple elements selected, and the widget shows the aggregate of those elements, the Analytics Hub also shows the aggregate of those elements.You can toggle between showing a time series of indicator scores and a list of the records used to calculate those scores.You can change what the chart displays in the View tab of the Analytics Hub.To change the visualization used for the graph, select a visualization from the list menu. Area, column, line, and spline visualizations are available.You can set display preferences per indicator and have them persist for each time you view that indicator.The Analytics Hub follows whichever domain you have selected in the System Settings. You see only the scores that are collected in that domain.
locale: en-US
release: yokohama
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 13
breadcrumb: [Analytics Hub for a specific indicator, Analytics Hub, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# View scores and statistics

The Analytics Hub Overview tab shows the score for a time period, statistics, and a time series. You can set the time period for the statistics and time series. You can also filter scores by breakdown and element.

![The overview tab of the Analytics Hub](../image/detailed-scorecard-overview.png "Overview tab")

**Note:** The ability to view formula indicator calculations, which had been available in Detailed Scorecard before Madrid, is not supported on the Analytics Hub. For more information, see the [Performance Analytics: Formula calculation is not shown for scores on Analytics Hub \[KB0783438\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0783438) article in the Now Support Knowledge Base.

## Indicator summary

The top of the View tab summarizes information about the indicator being viewed.

At the top of the tab, you see the following information:

-   The score for a chosen time period
-   The change, both absolute and percentage, between that score and the score for the previous time period
-   If a target is set, the difference between the score and that target
-   Controls for switching to the previous, next, or last time period
-   A calendar for selecting a time period or the real-time score

![Score section of Analytics Hub](../image/detailed-scorecard-score.png "Score section showing compliance with a target")

Results are color-coded to show favorability. If the direction of an indicator is Maximize, increases in scores are shown in green and decreases in red. If the direction of an indicator is Minimize, increases in scores are shown in red and decreases in green. Similarly, a color bar indicates whether the target has been met or missed. The colors depend on the color scheme that has been set for the target. For more information, see [Create a target color scheme](pa-targets.md#).

The time period that is associated with a score is shown above the score. Controls let you move to the next time period, the previous time period, or the last time period. The date you select here is reflected in the statistics and the time series graph. The selected time period is carried over when you change to another tab. The length of a time period \(day, month, quarter...\) is the same as the frequency of the indicator.

You can also select the date by clicking along the time series chart. Furthermore, if you navigate to this Analytics Hub from a widget, the date that you select in the widget persists when you open the Analytics Hub.

## Viewing real-time scores on the Analytics Hub

You can select real-time scores to view instead of the last score.

You can view real-time scores in the following circumstances:

-   The indicator is an [automated indicator](https://www.servicenow.com/docs/access?context=now-platform-glossary&version=yokohama&pubname=yokohama-glossary&section=gloss-automated-indicator&ft:locale=en-US).
-   It is configured to show real-time scores.
-   The aggregate function for the indicator does not use a script.
-   The indicator source does not use a [database view](https://www.servicenow.com/docs/access?context=now-platform-glossary&version=yokohama&pubname=yokohama-glossary&section=gloss-database-view&ft:locale=en-US).
-   None of the breakdowns that are applied to the indicator use a scripted breakdown source.

**Warning:**

-   Real-time scores can differ per viewer and differ from collected scores. Real-time scores are taken directly from the relevant facts tables. Therefore, the Access Control Lists \(ACL\) of those facts tables determine the real-time scores that each logged-in user sees.
-   The Analytics Hub does not refresh real-time scores automatically. To get the most up-to-date score, refresh the browser page.

If you can select real-time scores, select them in the date selector or by selecting the current time period in the **Records** view. However, when viewing real-time scores, you cannot see records that do not match a breakdown element in the **Records** view.

![Score time period navigation buttons showing real-time option](../image/ds-overview-period-nav.png "Selecting to show real-time score") ![The Score section of the Analytics Hub with the calendar expanded to show that real-time scores are selected.](../image/detailed-scorecard-overview-real-time.png "Selecting to show real-time score")

**Note:** You can show real-time scores to dashboard users in some widgets. For more information, see [Real-time scores](real-time-scores.md).

## Time-series aggregations in the Analytics Hub

On the Analytics Hub, you can aggregate changes in indicators into discrete time intervals.

In the top-right corner, you can set the time series aggregation for the Analytics Hub.

![Possible time series aggregations for a daily indicator](../image/detailed-scorecard-monthly-agg.png "Menus of daily time series aggregations")

The time series aggregation is reflected in the score, the statistics, the time series graph, and the charts in other tabs. The available time series depend on the frequency of the indicator. For more information, see [Applying time series aggregations](applying-time-series-aggregations.md#). For examples and a deeper exploration of using time series aggregations with indicators, see this Performance Analytics Academy video, [Leveraging Time Series with Performance Analytics](https://youtu.be/aM6JtUndRYk).

**Note:**

-   Business and fiscal calendars do not support time series aggregations. You cannot set a time series aggregation for an indicator that uses such a calendar.
-   Selecting a time series aggregation overrides the **Render continuous lines** option that is set on the indicator. This option causes the Analytics Hub to show unbroken data lines for this indicator, even when there is no data for a specific date.
-   You cannot compare records in the Compare tab if you set a time series aggregation. You can compare aggregated scores.

## Date ranges of scores in the Analytics Hub

You can set the time period of scores that the Analytics Hub describes.

The controls for selecting a date range are above the statistics and to the left of the time series aggregation. The time period you choose is reflected in the statistics and the time series graph. You have two control options to set the time period:

-   ![Calendar for setting time period](../image/detailed-scorecard-calendar.png "Date range calendar")

-   The sliders with the navigation bar: ![Navigation bar consisting of sliders and graph for setting the time period](../image/detailed-scorecard-slider.png)

**Note:** If you specify a date range such as 3 MONTHS with a time series aggregation such as By month SUM, you may see one more time period than you expect. The instance interprets a period such as three months as 0-3 months and may show four months of scores.

## Statistics on the Analytics Hub

In the View tab of the Analytics Hub, you can set various statistics to apply to the indicator score.

You cannot customize the statistics display on the Analytics Hub. However, because not all statistics are relevant to all indicators, you can exclude statistics on the indicator record. For example, you can exclude Change % for an indicator with a score expressed as a percentage. For more information, see [Create an automated indicator](../task/t_CreateAnAutomatedIndicator.md#).

## Breakdowns, elements, and element filters

On the Analytics Hub, you have several options for viewing breakdowns and breakdown elements.

You can show a separate line or column on the chart for every element of a breakdown. You can also filter the scores by selecting a breakdown and an element. You can search for breakdowns and elements by name or you can open a breakdown and element selection dialog.

![Breakdown and element search field and icon for opening breakdown and element selector](../image/detailed-scorecard-breakdown.png "Breakdown menu and search field")

If you select a breakdown but not an element, the chart shows each element of the breakdown.

![With the Priority breakdown selected but no elements selected, the chart shows a line for each element of Priority.](../image/detailed-scorecard-breakdown-elements.png "Chart with all elements of a breakdown")

**Note:**

-   The scores are not shown when no element from the breakdown applies. This rule also applies to Choice \[sys\_choice\] table breakdowns when a label defined in NULL\_OVERRIDE replaces the value of `none`.
-   If you try to apply a breakdown to a formula indicator but not all contributing indicators support the breakdown, the breakdown is not applied. Instead, you see the score for the formula indicator without the breakdown. A message appears to let you know this has happened.

If you select a breakdown and an element, you filter the entire Analytics Hub to show only the values for that breakdown and element.

![With Priority of Low selected, the score, the statistics, and the chart show only the incidents that match Priority=Low.](../image/detailed-scorecard-one-element.png "Analytics Hub filtered to show only low-priority incidents")

If the breakdown has an elements filter defined for its breakdown source, you can choose one of those elements filters. For more information, see [Element filters](c_BreakdownElementFilters.md#).

![Breakdown and element selector on Analytics Hub showing elements filters](../image/ah-elements-filter.png "Element filter")

If breakdown relations are defined for the indicator, after you select a first-level breakdown and element, you can navigate to a related element. The element can be in a parent-child relationship in the same breakdown, or it can be in another breakdown. For more information about breakdown relations including procedures for creating them, see [Navigating breakdown elements with breakdown relations](breakdown-relations.md).

![Analytics Hub showing breakdown relations between parent and child elements in the same breakdown](../image/child-locations.png "Breakdown relations")

After you select a first-level breakdown and element, you can select a second-level breakdown and element. You cannot select more than two levels of breakdown in total.

![With Category: Software the first breakdown and element selected, the user is selecting from the elements of the Priority breakdown.](../image/detailed-scorecard-bkdown-element-filtr.png "Selecting breakdowns and elements")

The following animation shows the selection and clearing of a first- and second-level breakdown and element:

![Setting and clearing breakdown and element](../image/detailed-scorecard-bkdown.gif)

You can clear either the first- or second-level breakdown and element combination by clicking the X in the tile for that breakdown/element pair. If you clear the first-level breakdown/element, the second-level breakdown/element becomes the first-level breakdown/element. You can also clear the selection by following the breadcrumbs above the score.

## Viewing aggregate scores for multiple elements

If you click a value on a chart in a widget on a dashboard, you open the Analytics Hub on that indicator. If you are on a breakdown dashboard and have multiple elements selected, and the widget shows the aggregate of those elements, the Analytics Hub also shows the aggregate of those elements.

For more information about the aggregate view of multiple elements selected on a dashboard, see [Showing multiple elements separately or aggregated](../../dashboards/concept/multi-element-select-indicator-views.md).

![Clicking on a score that is the aggregate of all the selected elements in a widget on a breakdown dashboard](../image/ah-from-multi-element-aggregate.png "Analytics hub with aggregate score of three elements")

The Analytics Hub opens on whichever date was selected in the widget. The multiple elements are shown in the format **\{Breakdown\} in \(element\_1, element\_2, element\_3, +x more\)**.

![Analytics Hub showing the Software, Hardware, and Database elements of the Category breakdown selected from a breakdown dashboard](../image/ah-multi-element.png "Analytics Hub with multiple elements")

**Note:** Targets, thresholds, and comments are not available when you navigate to the Analytics Hub from a widget with multiple breakdown elements selected in an aggregate view. The breakdown selector and search functionality are also unavailable. If you then select **Show Records** on the Analytics Hub, you see the records that match any of the elements you selected on the dashboard.

## Showing records in the Analytics Hub

You can toggle between showing a time series of indicator scores and a list of the records used to calculate those scores.

Click **Show Records** or **Hide Records** in the upper right corner to toggle. In either case, the scores or records are shown for the time period that is chosen at the top of the tab. The scores or records are also filtered by any breakdown/element pairs that you selected.

If you opened the Analytics Hub from a breakdown dashboard with multiple elements selected, what you see depends on the dashboard widget. If the widget displays each element value separately, you see the records that match the element you selected. If the widget displays an aggregate score of the elements, you see the records that match any of those elements.

**Note:**

-   Records are shown only for automated indicators.
-   The Show Records function is not supported for real-time scores of unmatched breakdown elements. If you are viewing scores in real time, records that are not assigned to any breakdown element are not displayed.
-   You can change the view of the list of records in the context menu of the Records list, depending on the views available to the facts table. The default view is set on the indicator source.
-   In some cases, when you collect second-level breakdowns, the score and the number of records do not agree. When these values do not agree, the score is correct. For more details and an example, see [KB0748969](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0748969).

## Chart options on the Analytics Hub

You can change what the chart displays in the View tab of the Analytics Hub.

Click the **Show more** icon, and a toolbar of additional icons appears.

![Icons that change the chart display.](../image/detailed-scorecard-timeseries-icons.png "Chart option icons")

A tooltip for each icon identifies which chart option the icon turns on and off. The chart options include:

-   The type of measurement that is displayed.
-   Displaying labels
-   Displaying a forecast of future scores, depending on how forecasting is set up on the indicator.
-   Displaying confidence bands
-   Displaying the trend line
-   Displaying comments
-   Displaying thresholds
-   Displaying targets
-   Selecting the chart visualization

![Chart showing score, trend, confidence band, forecast, target, and threshold](../image/ah-busy-chart.png "Chart showing multiple options selected")

If you have the Continual Management Improvement application installed, you also have an icon to show or hide Improvement Initiatives \(![](../image/scorecard-cim-icon.png)\). If you also have the sn\_cim.improvement\_requester role, you can create an improvement initiative by clicking the identical icon in the toolbar, as described in [Analytics Hub for a specific indicator](view-scorecard.md).

The available measurements are:

-   Year-over-year
-   Change
-   Change percent
-   Score

Score is the default measurement. All measurement types except Year-over-year can be shown together. Year-over-year can apply to only one other measurement at a time, such as Score or Change, but not both. A full year of data is necessary to make Year-over-year meaningful.

## Visualizations on the Analytics Hub

To change the visualization used for the graph, select a visualization from the list menu. Area, column, line, and spline visualizations are available.

![Expanded drop-down list showing the available chart visualizations](../image/detailed-scorecard-visualizations.png "Available chart visualizations")

## User preferences on the Analytics Hub

You can set display preferences per indicator and have them persist for each time you view that indicator.

The Analytics Hub tracks the following user preferences:​

-   All display settings
-   Chart visualizations
-   Time period

All preferences are stored per indicator and user,​ so each user can configure each Analytics Hub to display as preferred.

**Note:** If you are upgrading from a version with scorecards instead of the Analytics Hub, the table with old user preferences is preserved. The first time a user opens the Analytics Hub for an indicator, the preferences are imported from the old table. This import is overridden if the preferences for that user and indicator are set manually in the PA Analytics Hub Preferences \[pa\_ds\_preference\] table before the user opens the Analytics Hub.

## Domain separation on the Analytics Hub

The Analytics Hub follows whichever domain you have selected in the System Settings. You see only the scores that are collected in that domain.

Any target, threshold, or comment you add is automatically associated with the current domain. The **Edit scores** option is not available.

Besides system settings, some dashboards are configured so that you can select the domain on the dashboard. If you navigate to the Analytics Hub from a widget on such a dashboard, you see only the scores that are collected for that domain. For more information, see [Associate a domain configuration with a dashboard](../task/associate-domain-config-dashboard.md).

