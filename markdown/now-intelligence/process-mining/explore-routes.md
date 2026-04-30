---
title: Exploring and comparing workflow routes
description: Compare key indicators and analyze differences between the optimal route and exception or alternate routes.
locale: en-US
release: xanadu
product: Process Mining
classification: process-mining
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Analyzing and getting process insights, Using Process Mining, Process Mining, Platform Analytics]
---

# Exploring and comparing workflow routes

Compare key indicators and analyze differences between the optimal route and exception or alternate routes.

The process map visually shows how routes are distributed over the records. Routes consist of start-to-end paths through the steps or activities in your process. The various routes in a process can have different combinations of steps for process cycles \(records\). Process Mining automatically extracts process routes from data, giving you a view into what's going right and wrong within your process.

For example, explore routes to investigate or identify the following issues:

-   How many records are covered by the most common route, or how much route variation exists.
-   How long most routes take to complete a process.
-   Whether there are long wait times occurring in a particular activity or the number of process steps has evolved over time.
-   Unexpected or uncommon record state or route transitions, such as when a record is closed then re-opened, or recategorized far into its duration.
-   Benchmarks by comparing insights from a successful process to a less efficient one.
-   Clustered similarity groupings within a route.

## Variation Analysis panel

The Variation Analysis panel shows the cumulative number of records represented in a route, the number of steps in each route, and the duration in days that it took to complete a route. When you hover over a variation, a pop-up appears that shows the variation of the route.

![Variation Analysis panel](../image/routes-panel2.png)

You can use **Sort by** to sort the order of routes displayed in the list.

The example panel shows 130 different routes that were taken. From the routes visible on the example list, we see that each route was taken from 18 through 244 times. For each route, the average duration or standard deviation is calculated, for example, resulting in 130 averages or standard deviations. The list sorts by these averages from highest/longest to lowest/shortest.

<table id="table_rwr_xjc_lpb"><tbody><tr><td>

Highlights

</td><td>

Sorts routes in order of most heavily deviated toward the longer end of duration.

</td></tr><tr><td>

Most Records

</td><td>

Sorts routes in order of those with the greatest to least number of records that have run through the route.

</td></tr><tr><td>

Least Records

</td><td>

Sorts routes in order of those with the least to greatest number of records that have run through the route.

</td></tr><tr><td>

Longest Avg Duration

</td><td>

Based on calculation of duration averages for each route, sorts routes in order of longest to shortest average values \(average time from process start to finish\).

</td></tr><tr><td>

Shortest Avg Duration

</td><td>

Based on calculation of duration averages for each route, sorts routes in order of shortest to longest average values \(average time from process start to finish\).

</td></tr><tr><td>

Longest Med Duration

</td><td>

Based on calculation of duration middle \(or average of two middle\) values for each route, sorts routes in order of longest to shortest median values.

</td></tr><tr><td>

Shortest Med Duration

</td><td>

Based on calculation of duration middle \(or average of two middle\) values for each route, sorts routes in order of shortest to longest median values.

</td></tr><tr><td>

Most steps

</td><td>

Sorts routes in order of those with the greatest to least number of steps.

</td></tr><tr><td>

Least steps

</td><td>

Sorts routes in order of those with the least to greatest number of steps.

</td></tr><tr><td>

Highest Std Deviation

</td><td>

Based on calculation of standard deviation of duration for each route, sorts routes in order of highest to lowest variation from route average values.

</td></tr><tr><td>

Lowest Std Deviation

</td><td>

Based on calculation of standard deviation of duration for each route, sorts routes in order of lowest to highest variation from route average values.

</td></tr></tbody>
</table>You can also perform these actions from the Variation Analysis panel.

-   View the routes list as a graph or table.
-   Highlight routes:
    -   Select a route from the list to highlight it on the process map.
    -   Point to a second route in the list to simultaneously highlight it.
    -   Selected route appears as a pop-up at the bottom of the page.
-   Perform a [Cluster analysis](cluster-analysis.md).

-   **[Show a route](../task/show-variant-route.md)**  
Show one or more routes that followed different sequences of steps in your process.
-   **[View records for a route](view-records.md)**  
From the Variation Analysis panel, view the list of records which followed one or more selected routes.

**Parent Topic:**[Analyzing and getting process insights](analyze-get-process-insights.md)

