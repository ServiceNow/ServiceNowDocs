---
title: Benchmarks KPI performance trend and recommendations \(deprecated\)
description: The Benchmarks KPI performance chart trend view shows your KPI performance comparison with global data, and provides recommendations to implement for improved performance of your KPI.
locale: en-US
release: xanadu
product: Benchmarks
classification: benchmarks
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Deprecated Benchmarks dashboard, Benchmarks, IT Service Management]
---

# Benchmarks KPI performance trend and recommendations \(deprecated\)

The Benchmarks KPI performance chart trend view shows your KPI performance comparison with global data, and provides recommendations to implement for improved performance of your KPI.

The KPI Performance Trends chart section is shown only for users with the Benchmarks viewer role \(sn\_bm\_client.benchmark\_data\_viewer\).

## KPI Performance Trends chart

![KPI Performance Trends](../image/BenchTrend.png "6-month monthly data mapped against global data")

Your 6-month monthly data is mapped against global data, and your percentile rank indicating your standing within the participating peer group is shown.

Functionality of the performance trend chart view includes:

-   Switching between KPIs in the same category using the KPI list.
-   Viewing your instance and global data for a certain month by hovering over a point on the graph.
-   Accessing the Performance Analytics scorecard for a data point in your instance.
-   Downloading KPI chart reports.
-   Filtering data by type of industry, number of users, or geographic region.

## Recommendations

The Recommendations section is shown only for users with the Benchmarks recommendation role \(sn\_bm\_client.benchmark\_recommendation\_viewer\).

Recommendation candidates are provided in the performance trend view to help improve the performance of your KPIs. All recommendations are dynamic and are updated monthly, based on data analyzed from the previous month. Recommendation candidates are listed by rank.

**Note:** Some KPI recommendations that use guided setup require system admin permission. Work with your system administrator to implement these recommendations.

![Recommendations filtered into Implemented or Saved tabs](../image/bench-recommend.png "Recommendations filtered into Implemented or Saved tabs")

Actions are available for each recommendation candidate. Based on the action, recommendations get filtered into the appropriate group tab \(Implemented or Saved\). Closing out the recommendation removes the recommendation candidate from the list.

-   **Get Started**: Executes Guided Setup, if available, otherwise opens documentation containing information regarding the improvement.
-   **Mark as Implemented**: Moves the recommendation candidate to the Implemented tab. This action is no longer available when a CIM improvement initiative is associated with the recommendation candidate.
-   **Save for Later**: Moves the recommendation candidate to the Saved tab to be implemented at a later time.
-   **Improvement Initiative** section:
    -   **Create Improvement Initiative**: Creates a CIM improvement initiative, which contains phases and tasks to improve the KPI. Once the CIM improvement initiative is created, the recommendation candidate is moved to Saved tab.

        CIM fields automatically populated:

        -   Short description: Recommendation candidate name.
        -   Description: Recommendation candidate content and action URL.
    -   **Select Improvement Initiative**: Associates an existing CIM improvement initiative. The state of the recommendation candidate is set to the state of the associated CIM improvement initiative.

        **Note:** CIM **Short description** and **Description** fields are populated automatically from the recommendation candidate content only when the CIM improvement initiative is initially created from a recommendation candidate, not when associating afterward.

    -   **Improvement Initiative** related link: Links to the associated CIM improvement initiative. Click the related link to view the CIM improvement initiative in Continual Improvement Management.
    -   **Remove Improvement Initiative**: Removes the associated CIM improvement initiative from the item in the Recommendations list.

        When the CIM improvement initiative is closed, the recommendation candidate is moved to the Implemented tab. If the CIM improvement initiative is canceled, the recommendation candidate remains in the Saved tab. The associated CIM improvement initiative can always be removed, and another can be selected.


Tabs for recommendation candidates:

-   **Recommendations**

    Lists all recommendation candidates based on the analysis of the monthly data. This list gets refreshed monthly.

-   **Implemented**

    Lists all recommendation candidates that you have implemented. Recommendation candidates that were implemented the previous month include tracking information on the trend chart so you can determine the impact of the change. Hovering over the implementation point shows the recommendation implemented.

    **Note:** Recommendation candidates implemented in the current month do not have tracking data points on the chart until the following month.

-   **Saved**

    Lists all recommendation candidates that have been saved to implement later.


**Parent Topic:**[Deprecated Benchmarks dashboard](c_BenchDashboard.md)

