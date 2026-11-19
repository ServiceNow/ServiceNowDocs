---
title: Viewing business insights
description: View key information about your business process from the Summary and Insights page. See goals and performance indicators, and get insights on the improvement opportunities.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/now-intelligence/process-mining/view-business-findings.html
release: yokohama
product: Process Mining
classification: process-mining
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Analyzing and getting process insights, Using Process Mining, Process Mining, Platform Analytics]
---

# Viewing business insights

View key information about your business process from the Summary and Insights page. See goals and performance indicators, and get insights on the improvement opportunities.

The Summary and Insights page shows opportunities for optimizing your process. You can see the following snapshots.

-   Met or unmet goals and KPIs
-   Improvement opportunities overview
-   New improvement opportunities

**Note:** The Goals and KPIs section is available with the integration of Performance Analytics.

The Goals and KPIs section is configured from the UI Builder.

From the Goals and KPIs section, choose a visualization to analyze indicator details more closely from the [KPI Details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/now-intelligence/kpi-details.md) view. KPI Details shows you trends, predictions, breakdowns, and associated records for a specific indicator. The KPI Details page leads you to deeper information behind your key performance indicators.

\[Omitted image "summary-insights-goals-kpis.png"\] Alt text: Summary and Insights - Goals and KPIs example

From the Improvement opportunities overview section, you can see opportunities sorted by category, type, and KPIs in three different cards.

\[Omitted image "summary-insights2.png"\] Alt text: Summary and Insights - Improvement Opportunities overview examples

The rules that you configure discover business findings. For example, you might configure rules which show:

-   records that went directly into a Closed or Resolved state
-   reworked records with solutions that customers didn't accept, or whose states changed from 'Resolved' to 'Work in progress' status.
-   wrong or many group assignments

Select a combination of these insight categories to show on the dashboard.

-   Quality
-   Performance
-   Conformance

From each insight, you can request or view a completed cluster or process analysis, then view from the workbench the completed cluster or model.

To generate a project for a selected insight, select on the card to get to the Analyst Workbench for the card data. When the project becomes available to view, select **View Process analysis**.

From the Bottleneck Analysis section, you can see identified bottleneck sources discovered in your process records.

\[Omitted image "summary-insights-bottleneck-analysis.png"\] Alt text: Summary and insights - Bottleneck analysis showing transitions

Select a breakdown to refine the routes list, then sort the list by:

-   Unique Occurrences
-   Total Duration
-   Avg Duration
-   Max Repeat Occurrences
-   Total Occurrences

\[Omitted image "bottleneck-analysis-breakdowns.png"\] Alt text: Bottleneck Analysis by breakdown

Select **View in Workbench** to view the project for the selected transition.

All routes for a process show in the Variation Analysis section. You can sort the order for routes by highlights, number of records, average duration, or steps.

\[Omitted image "summary-insights-variation-analysis.png"\] Alt text: Variation analysis showing variation of routes

Select **View in Workbench** to view the project for an individual route.

**Parent Topic:**[Analyzing and getting process insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/now-intelligence/process-mining/analyze-get-process-insights.md)

**Related topics**  


[KPI Details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/now-intelligence/kpi-details.md)

