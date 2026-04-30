---
title: Summary and Insights page
description: The Summary and Insights page enables you to view opportunities for optimizing your process. Access the dashboard from a Process Mining project.
locale: en-US
release: yokohama
product: Process Mining
classification: process-mining
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Process details page, Process Mining workspace, Exploring Process Mining, Process Mining, Platform Analytics]
---

# Summary and Insights page

The Summary and Insights page enables you to view opportunities for optimizing your process. Access the dashboard from a Process Mining project.

You can view the Process overview dashboard where you see some initial information about your mined data. This is showcased in two graphs:

-   Time series graph: Trendline to show the average time taken for completion of records over time.
-   Histogram: Distribution of records by the time taken to reach the process end.

![Process overview](../image/proj-metrics.png)

## Improvement opportunities overview

On the Summary and Insights page, see the Improvement opportunities overview. Here you find an overview of project-related statistics that are generated on the project.

![Improvement opportunities](../image/improve-opp.png)

## Variation Analysis

On the Summary and Insights page, you can also see the variation analysis of your data.

Variation analysis enables you to compare different variants of a mined project and view the analysis of a selected variant.

![Variation Analysis from Summary and Insights page](../image/variation-analysis-sum.png)

-   Filter the routes using the filter icon.
-   Sort the results using the **Sort by** list.
-   Select **View process analysis** to view the graph for the selected variant in the Analyst Workbench.

## Opportunities

In the Opportunities section, you can view a list of rule-based and automated improvement opportunities associated with the project.

![Improvement Opportunities](../image/action-find.png)

You can view the following details:

-   Improvement opportunities that are new, under review, and archived.
-   List of improvement opportunities associated with the project with all the details.
-   Select ![finding details](../image/details-finding.png) beside the title to see the details about the Improvement opportunities.
-   Select the list beside **View in Workbench** to get more options.

    -   The states, New, Under review, and Archived, are available to track your progress taken on the improvement opportunities listed there. Any new improvement opportunity on which no work is done is in the New state. If an action is taken, then the improvement opportunity is moved to Under review. If some action has been taken in the background, you can manually set the improvement opportunity to Under review. If something is not relevant anymore, you can archive it. However, if an improvement opportunity is in the Archived state, you can only move it to New. Also, when you add a note, CIM, or Automation request to an improvement opportunity that is in the New state, then the improvement opportunity automatically moves to Under review.
    -   You can start any investigative actions, such as running a root cause analysis.
    -   You can also add a note, create a CIM, or create an automation request.
-   Select ![Show/hide icon](../image/show-hide-find.png) to hide or show columns.
-   Select ![Sort](../image/order-by-find.png) to sort the columns.
-   Select ![Filter](../image/filter-finding.png) to filter the list of improvement opportunities.
-   Select the **Card view** toggle to view the improvement opportunities in card view.

## Integration with Performance Analytics dashboards

Integrate Performance Analytics dashboards to include the KPIs and visualizations you want to see. Using the dashboard builder, you can create your own dashboards with custom widgets/KPIs specifically for your project. These dashboards can be linked at the project or process configuration level.

**Parent Topic:**[Process details page](project-view-screen.md)

